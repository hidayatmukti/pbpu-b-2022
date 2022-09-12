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


