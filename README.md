# inSign

Adalah sebuah projek aplikasi penerjemah alfabet bahasa isyarat menggunakan Python, openCV dan model dari TensorFlow InceptionV3, sebuah model klasifikasi Convolutional Neural Network (CNN).

Untuk penjelasan lebih detail mengenai script silahkan buka Jupyter Notebook vie link berikut:
[inSign.ipynb online viewer](https://nbviewer.jupyter.org/github/trastanechora/digitalent2018/blob/master/Tugas/inSign.ipynb)

Framework yang digunakan untuk pengimplementasian CNN ini bisa ditemukan di link berikut:

[Simple transfer learning with an Inception V3 architecture model](https://github.com/xuetsing/image-classification-tensorflow) by xuetsing

Di dalam proyek ini terdapat dataset gambar yang cukup banyak (1Gb+). Jika anda tertarik hanya pada jalannya aplikasi tanpa proses training maka anda hanya perlu clone/copy/download beberapa file saja.

Untuk demo bisa disimak pada link berikut:
[Demo inSign](https://drive.google.com/file/d/1u1mIu0xGdyY7WcE-vTTuzwTdj44ub-CE/view)

## Requirements

Projek ini menggunakan Python 3.5 dan beberapa PIP package sebagai berikut:
* opencv
* tensorflow
* matplotlib
* numpy

Silahkan lihat file requirements.txt untuk versi dan package API yang dibutuhkan

## How to Install

```
pip install -r requirements.txt
```

atau jika gagal maka gunakan pip3

```
pip3 install -r requirements.txt
```

## Training process

Untuk melakukan training pada model inceptionv3 dapat menggunakan command sebagai berikut:

```
  python train.py --bottleneck_dir=logs/bottlenecks --how_many_training_steps=2000 --model_dir=inception --summaries_dir=logs/training_summaries/basic --output_graph=logs/trained_graph.pb  --output_labels=logs/trained_labels.txt --image_dir=./dataset
```

jika gagal maka coba gunakan python3

Jika Anda menggunakan dataset yang telah disediakan, maka akan membutuhkan waktu proses training yang cukup lama, tergantung kemampuan komputer Anda. Kami melakukan proses training kurang lebih sekitar 3-4 jam.

## Running the Application

Untuk menjalankan programnya, lakukan dengan command berikut:
```
python classify_webcam.py
```

atau gunakan python3 jika command di atas gagal.

Tangan harus tepat berada di dalam kotak untuk dapat dibaca.

## How to run without training process

Jika Anda tidak ingin melakukan proses training yang sangat lama maka jangan clone folder ``dataset`` namun clone folder ``demo`` kemudian masukkan semua isinya ke dalam folder ``log``