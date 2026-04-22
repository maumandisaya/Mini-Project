# 🚗Prediksi Harga Mobil Bekas di Indonesia Menggunakan Model _Machine Learning_
Harga mobil bekas di Indonesia seringkali ditentukan dari beberapa faktor, seperti daerah asal, tahun pembelian, kelengkapan fitur, serta plat mobil (ganjil/genap). Proyek ini bertujuan untuk mengetahui variabel apa saja yang mempengarhui harga mobil sekaligus memprediksi harga mobil bekas berdasarkan variabel-variabel yang tersebut

## 📁Struktur Repo
* `Copy_of_Projek_Datsa_Branch.ipynb` : notebook untuk melakukan EDA serta pelatihan model
* `SVR.pkl` : model _machine learning_ yang telah dilatih 
* `requirement.txt` : dependensi yang digunakan pada projek ini

# 📊Dataset
Dataset yang digunakan pada projek ini berasal dari [kaggle - Used Car Listings in Indonesia](https://www.kaggle.com/datasets/indraputra21/used-car-listings-in-indonesia/data?select=used_car.csv)
Dataset ini terdiri : 
* `car name`: The name or model of the car.
*  `brand`: The brand or manufacturer of the car.
*  `year`: The year the car was manufactured.age (km):
*  `The mileage`: distance traveled by the car in kilometers (km).
*  `location`: The location where the car is listed for sale.
*  `transmission`: The transmission type, such as "Manual" or "Automatic."
* `plate type`: The type of license plate, which can be an even plate or an odd plate.
* `rear camera`: Indicates whether the car has a rear camera (0 for no, 1 for yes).
* `sun roof`: Indicates whether the car has a sunroof (0 for no, 1 for yes).
* `auto retract mirror`: Indicates whether the car has auto-retracting mirrors (0 for no, 1 for yes).
* `electric parking brake`: Indicates whether the car has an electric parking brake (0 for no, 1 for yes).
* `map navigator`: Indicates whether the car has a built-in map navigator (0 for no, 1 for yes).
* `vehicle stability control`: Indicates whether the car has vehicle stability control (0 for no, 1 for yes).
* `keyless push start`: Indicates whether the car has a keyless push start (0 for no, 1 for yes).
* `sports mode`: Indicates whether the car has a sports mode (0 for no, 1 for yes).
* `360 camera view`: Indicates whether the car has a 360-degree camera view (0 for no, 1 for yes).
* `power sliding door`: Indicates whether the car has a power sliding door (0 for no, 1 for yes).
* `auto cruise control`: Indicates whether the car has auto cruise control (0 for no, 1 for yes).
* `price (Rp)`: The price of the car in Indonesian Rupiah (Rp).
* `instalment (Rp|Monthly)`: The monthly installment amount for the car, in Indonesian Rupiah (Rp).

## 🤖Hasil Training Model
Dari Hasil pelatihan 5 model regresi yang berbeda, didapatkan hasil seperti berikut : 
|     regressor     |  mae_score (train) |  mae_score (test)  |  mse_score (train) |  mse_score (test)  |  r2_score (train)  |   r2_score (test)  |
|:-----------------:|:------------------:|:------------------:|:------------------:|:------------------:|:------------------:|:------------------:|
| SVR               | 11193551.717528354 |  21858459.59082577 | 381869998046099.94 |  892693408322714.6 | 0.8529649178825927 | 0.5885595315060022 |
| AdaBoost          | 13789879.704998719 | 25850447.589642096 |  219603154615222.0 | 1029530007835813.4 | 0.9154440829672279 | 0.5254918376192764 |
| KNN               |  22045614.03508772 | 24094736.842105262 |  901539064327485.4 |  992080601503759.4 |  0.652871733747882 |  0.542752188309031 |
| Extra Trees       | 15328045.745825784 | 24497943.713446014 | 396214383576003.56 | 1018674027589933.9 | 0.8474417610095605 | 0.5304953355242498 |
| Linear Regression | 24875296.107707806 |  24769402.94066151 |  984601464424343.6 |  969572104383420.2 | 0.6208894180865294 | 0.5531263061348684 |
