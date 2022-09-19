# Pengembangan Beroritentasi Penggunaan Ulang

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
