<?php

$koneksi = mysqli_connect("localhost", "root", "", "pendaftar");
if (!$koneksi) {
    die("Koneksi gagal: " . mysqli_connect_error());
}


if ($_SERVER["REQUEST_METHOD"] === "POST") {

   
    $nama     = $_POST['nama'] ?? '';
    $email    = $_POST['email'] ?? '';
    $hp       = $_POST['hp'] ?? '';
    $tanggal  = $_POST['tanggal'] ?? '';
    $alamat   = $_POST['alamat'] ?? '';
    $jurusan  = $_POST['jurusan'] ?? '';

  
    $foto_nama = "";
    if (!empty($_FILES['foto']['name'])) {
        $folder = "uploads/";
        if (!is_dir($folder)) {
            mkdir($folder, 0777, true); 
        }

        $foto_nama = time() . "_" . basename($_FILES["foto"]["name"]);
        $target_file = $folder . $foto_nama;

        move_uploaded_file($_FILES["foto"]["tmp_name"], $target_file);
    }


    $stmt = $koneksi->prepare("INSERT INTO pendaftar (nama, email, hp, tanggal, alamat, jurusan, foto) VALUES (?, ?, ?, ?, ?, ?, ?)");
    $stmt->bind_param("sssssss", $nama, $email, $hp, $tanggal, $alamat, $jurusan, $foto_nama);
    $stmt->execute();

    
    header("Location: success.php?" . http_build_query([
        'nama'     => $nama,
        'email'    => $email,
        'hp'       => $hp,
        'tanggal'  => $tanggal,
        'alamat'   => $alamat,
        'jurusan'  => $jurusan,
        'foto'     => $foto_nama
    ]));
    exit;

} else {
   
    echo "<h3>Akses ditolak! Silakan isi form pendaftaran terlebih dahulu.</h3>";
    echo "<a href='index.php'>Kembali ke Form Pendaftaran</a>";
}


mysqli_close($koneksi);
?>
