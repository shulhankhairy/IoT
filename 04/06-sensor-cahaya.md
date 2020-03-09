# PRAKTIKUM MATA KULIAH INTERNET OF THINGS MINGGU KE-6 (Sensor Cahaya)

Semester Genap 2019/2020

Jurusan Teknologi Informasi

Politeknik Negeri Malang

## Sensor Cahaya

Sensor cahaya adalah sebuah sensor yang digunakan untuk mendeteksi cahaya di sekitar lingkungan kita. Sensor cahaya yang akan kita gunakan menggunakan potensio, fungsi potensio tersebut adalah untuk mengurangi atau menambahkan tingkat kepekaan sensor yang akan kita gunakan. Sensor cahaya sangat berguna kita akan membuat aplikasi pendeteksi tingkat cahaya, misalkan ketika tingkat cahaya tertentu sebuah lampu akan dinyalakan.

## Rangkaian Sensor Cahaya
Berikut ini adalah rangkaian yang dapat digunakan
![](images/esp8266-ldr.png)



## Praktikum 1 - Membaca sensor cahaya

Susunan rangkaian sederhana pada praktikum ini seperti gambar sebelumnya.

Contoh source code

```c++
void setup()
{
  Serial.begin(115200);
  Serial.println("Contoh penerapan sensor cahaya")
}

void loop()
{
  unsigned int AnalogValue;
  AnalogValue = analogRead(PIN_A0);
  Serial.println(AnalogValue);
  delayMicroseconds(10);
}
```

Setelah source code diupload, buka serial monitor pada ArduinoIDE untuk melihat hasil sensor cahaya.

## Tugas
1. Buatlah sebuah rangkaian untuk sensor cahaya dan LED menggunakan fritzing, kemudian buatlah program dengan skenario sebagai berikut
    + LED merah akan menyala ketika cahaya dalam kategori redup pada durasi tertentu
    + LED hijau akan menyala ketika dalam kategori terang pada durasi tertentu
    > tidak harus menggunakan LED hijau dan merah jika tidak memiliki LED hijau dan merah
