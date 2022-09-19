# Pengembangan Beroritentasi Penggunaan Ulang
<plantuml>
@startuml

Ecommerce --> SupportMultipleDelivery
SupportMultipleDelivery <|.. JNT
SupportMultipleDelivery <|.. JNE
SupportMultipleDelivery <|.. SiCepat
                             
class Ecommerce {
 +nameProduct
 +productCategory
 +price
 +method2(Application:supportMultipleDelivery)
}
interface SupportMultipleDelivery {
 +tarifPengiriman(range, weight)
 +requestPengiriman(destination)
}
class JNE {
 +tarifPengiriman(range, weight)
 +requestPengiriman(destination)
}
class JNT {
 +tarifPengiriman(range, weight)
 +requestPengiriman(destination)
}
class SiCepat {
 +tarifPengiriman(range, weight)
 +requestPengiriman(destination)
}

@enduml
</plantuml>
