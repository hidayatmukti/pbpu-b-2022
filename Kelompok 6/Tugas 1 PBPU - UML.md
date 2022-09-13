# PERANCANGAN UML MENGENAI SISTEM ANTARA ECOMMERCE SERTA EKSPEDISI PENGIRIMAN

### Dosen Pengampu: Andri Santoso, S.kom., M.Sc.,

#### Kasus :
Buatlah sebuah UML Diagram mengenai alur kerja dari sistem antara e-commerce yang terintegrasi dengan ekspedisi dimana nantinya e-commerce dapat melihat tarif dan mengirim request untuk berbagai ekspedisi yang tersedia.

#### Gambar UML

#### Code UML :
@startuml
pemilihanKurir <-- eCommerce
jne <|.. pemilihanKurir
jnt <|.. pemilihanKurir
siCepat <|.. pemilihanKurir

class eCommerce{
    -userName : String
    -address : String
    -ackages : barang
    __
    +delivery(barang : pemilihanKurir)
}

class jne{
    -name : String
    __
    +pengirimianYES(tarifPengiriman, requestPengiriman)
    +pengirimianREG(tarifPengiriman, requestPengiriman)
    +pengirimianOKE(tarifPengiriman, requestPengiriman)
}

class jnt{
    -name : String
    __
    +pengirimianSuper(tarifPengiriman, requestPengiriman)
    +pengirimianEZ(tarifPengiriman, requestPengiriman)
    +pengirimianECO(tarifPengiriman, requestPengiriman)
}

class siCepat{
    -name : String
    __
    +pengirimianBEST(tarifPengiriman, requestPengiriman)
    +pengirimianGOKIL(tarifPengiriman, requestPengiriman)
    +pengirimianHALU(tarifPengiriman, requestPengiriman)
}

interface pemilihanKurir{
    +tarifPengiriman(price, range, weight): total
    +requestPengiriman(barang, address)
}

@enduml