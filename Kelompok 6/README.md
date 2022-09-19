# Pengembangan Beroritentasi Penggunaan Ulang

### Dosen Pengampu: Andri Santoso, S.kom., M.Sc.,

| Nama | NIM |
| --- | --- |
| Prasetya Naufal Rahmandita | 195150401111035 |
| Aditya Akhmad Jatnika | 195150401111025 |
| Mohammad Aditya Putra | 195150400111054 |
| Ronaldo Simatupang | 195150400111015 |
| Hendika Fashobiqul Galang F. | 195150400111024 |

### Kasus :
Buatlah sebuah UML Diagram mengenai alur kerja dari sistem antara e-commerce yang terintegrasi dengan ekspedisi dimana nantinya e-commerce dapat melihat tarif dan mengirim request untuk berbagai ekspedisi yang tersedia.

## Deklarasi Kelas

### eCommerece Class
Terdapat Beberapa atribut dari kelas ini yakni :

| Nama Field | Type | Visibility |
| --- | --- | -- |
| userName | String | private |
| address | String | private |
| packages | barang | private |

Terdapat juga method yang dipakai pada kelas ini, yakni :

| Nama Method | Parameter | Visibility |
| --- | --- | -- |
| delivery | barang : pemilihanKurir | public |

### jne Class
Terdapat Beberapa atribut dari kelas ini yakni :

| Nama Field | Type | Visibility |
| --- | --- | -- |
| name | String | private |

Terdapat juga method yang dipakai pada kelas ini, yakni :

| Nama Method | Parameter | Visibility |
| --- | --- | -- |
| pengirimanYES | tarifPengiriman, reuquestPengiriman | public |
| pengirimanREG | tarifPengiriman, reuquestPengiriman | public |
| pengirimanOKE | tarifPengiriman, reuquestPengiriman | public |

## Penjelasan 
Diagram UML yang telah dibuat mencerminkan alur kerja sistem E-Commerce yang terintegrasi dengan ekspedisi. Dalam kasus ini, Kelas E-Commerce memiliki ketergantungan terhadap kelas interface pemilihanKurir. Hal ini terjadi karena Kelas E-Commerce dibatasi hanya akan berinteraksi dengan objek kurir yang mengimplementasikan interface pemilihanKurir. Artinya, setiap packages atau barang pada kelas E-Commerce harus bisa dikirimkan oleh objek Kurir dengan mengimplementasikan method tarifPengiriman() dan juga requestPengiriman().

