# Inisiasi Kelas Marketplace
**Class Marketplace** 

Dalam class marketplace terdiri dari berbagai field diantaranya,

| Field  | DataType | Visibility
| ----- | --- | --- | 
| asalPengiriman   |String  |private
| tujuanPengiriman |String   |private
| jenisPengiriman   |String  |private
| beratBarang |Int  |private
| hargaProduk   |Int  |private

Dalam class marketplace tersebut juga memiliki Method diantaranya,

| Method  | Visisbility | Params
| ----- | --- | --- | 
| returnTarif   |Public  |beratbarang,asalPengiriman,tujuanPengiriman,ekspedisi
| menerimaRequest |Public   |beratbarang,asalPengiriman,tujuanPengiriman,ekspedisi
