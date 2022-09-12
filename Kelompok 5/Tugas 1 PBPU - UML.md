## TUGAS 1 - PERANCANGAN UML MENGENAI SISTEM ANTARA ECOMMERCE SERTA EKSPEDISI PENGIRIMAN
### Dosen Pengampu: Andri Santoso, S.kom., M.Sc.,

**Disusun oleh : Kelompok 5** 
Faidatul Syafiqah - 205150401111039 
Erlinda Argyanti - 205150401111041 
Maria Nicole Natasha Putri Iriandi -205150401111042 
Ivanna Ruth Theophilia Putri - 205150401111043 
Rahajeng Yusita Sari - 205150401111045

**Kasus :** 
Buatlah sebuah UML Diagram mengenai alur kerja dari sistem antara e-commerce yang terintegrasi dengan ekspedisi dimana nantinya e-commerce dapat melihat tarif dan mengirim request kepada ekspedisi delivery.

**Gambar UML:**
![Gambar UML](https://drive.google.com/file/d/1ZJ_U28zUnA1_b9Q5ZjCs2KedBa_IAnIW/view?usp=sharing)

**Code UML :** 
@startuml 
class Ecommerce { 
    +name +product
    +checkRate(expedition:expeditionDelivery)
    +sendRequest(expedition:expeditionDelivery) 
}

interface expeditionDelivery { 
    +product
    +checkRate(expedition:expeditionDelivery)
    +sendRequest(expedition:expeditionDelivery) 
}

class JNT { 
    -standartRateJNT 
    +checkRate(expedition:expeditionDelivery)
    +sendRequest(expedition:expeditionDelivery) 
}

class JNE { 
    -standartRateJNE 
    +checkRate(expedition:expeditionDelivery)
    +sendRequest(expedition:expeditionDelivery) 
}

class SiCepat { 
    -standartRateSiCepat
    +checkRate(expedition:expeditionDelivery)
    +sendRequest(expedition:expeditionDelivery) 
    }

Ecommerce --> expeditionDelivery
expeditionDelivery <|.. JNT
expeditionDelivery <|.. JNE
expeditionDelivery <|.. SiCepat

@enduml


**Penjelasan kode:** 
Dalam pembuatan class diagram menggunakan plantuml.com, hal yang pertama kali dilakukan adalah pembuatan entitas dari class diagram yang telah dirancang sebelumnya. Pembuatan class langsung dilakukan dengan mengetikkan “class” ditambah nama classnya. Untuk atribut dan methodnya dituliskan di dalam masing-masing class menggunakan “{“ dan “}” (kurung kurawal). Terdapat 4 class disini, yaitu class Ecommerce, JNE, JNT, dan SiCepat. Untuk pembuatan interface dilakukan dengan cara mengetikkan “interface” ditambah nama interface. Untuk atribut dan methodnya dituliskan dalam masing-masing interface menggunakan  “{“ dan “}” (kurung kurawal). Setelah mendefinisikan semua entitas yang dibutuhkan, dilanjutkan dengan pengkodean panah untuk merelasikan entitas yang ada. Pembuatan relasi dilakukan dengan menuliskan nama entitas yang dipilih lalu dilanjutkan dengan simbol yang menyimbolkan masing-masing relasi (dalam plant uml) dan dilanjutkan lagi dengan menuliskan nama entitas yang akan direlasikan. Relasi yang kami gunakan dalam kasus ini ada 2 yaitu dependency (-->) dan realization (<|..).

**Penjelasan alur:**
Kasus ini menerapkan beberapa prinsip OOP, yang pertama yaitu metode encapsulation(enkapsulasi). Enkapsulasi (encapsulation) adalah sebuah metode untuk mengatur struktur class dengan cara menyembunyikan alur kerja dari class tersebut. Struktur class yang dimaksud adalah property dan method. Dengan enkapsulasi, kita bisa membuat pembatasan akses kepada property dan method, sehingga hanya property dan method tertentu saja yang bisa diakses dari luar class. Enkapsulasi juga dikenal dengan istilah information hiding. Selain enkapsulasi, kasus ini juga menerapkan metode interface yang merupakan suatu mekanisme untuk mencapai abstraction. Interface hanya mengandung abstract method dan parameternya.

Pada sistem ecommerce terdapat tiga entitas yaitu entitas ecommerce itu sendiri sebagai parent class, entitas expeditionDelivery sebagai interface, dan entitas jenis ekspedisi seperti JNE,J&T, dan SiCepat sebagai child class. Pada entitas eccomerce berisi atribut nama dan produk sebagai state, dan method checkRate dan sendRequest. Semua atribut yang ada pada entitas ecommerce bersifat public yang menandakan dapat diakses oleh siapapun.

Entitas E Commerce memiliki relasi realization ke interface yang menggambarkan dependensi yang berarti class eccommerce dibatasi hanya dapat mengakses objek yang mengimplementasikan interface expeditionDelivery. Panah terbuka dengan garis putus-putus (dependency) pada Class JNT, JNE dan SiCepat menggambarkan bahwa terjadi ketergantungan dalam class tersebut dengan class interface yang menggunakan kelas lain. Class JNT, JNE dan SiCepat masing masing mewarisi method dari interface expeditionDelivery.
