# PRAKTIKUM MATA KULIAH INTERNET OF THINGS MINGGU KE-6 (Sensor Cahaya)

Semester Genap 2019/2020

Jurusan Teknologi Informasi

Politeknik Negeri Malang

## Sensor Cahaya

Sensor cahaya digunakan untuk menangkap intensitas cahaya disekitar. Sensor yang digunakan adalah sensor LDR (Light Dependent Resistor). 

Pin pada sensor cahaya terdapat 3 buah, VCC, ground, dan data. Data yang ditangkap pada sensor cahaya berupa data analog, sehingga kita harus menghubungkan pin data pada pin analog NodeMCU. Struktur pin pada sensor cahaya LDR seperti berikut.
![sensor cahaya](sensor-ldr.jpg)

## Praktikum 1 - Membaca data intensitas cahaya

Pada praktikum pertama, anda akan melakukan percobaan untuk menangkap data intensitas cahaya.

Berikut ini adalah rangkaian yang dapat digunakan
![](images/esp8266-ldr.png)

Contoh source code untuk membaca data intensitas cahaya.

```c++
#define sensorLDR A0
int nilaiSensor;

void setup() {
  Serial.begin(9600);
  delay(3000);
}

void loop() {
  nilaiSensor = analogRead(sensorLDR);
  Serial.print(“Nilai Sensor : “);
  Serial.println(nilaiSensor);
}
```

Setelah source code diupload, buka serial monitor pada ArduinoIDE untuk melihat hasil pembacaan data intensitas cahaya di sekitar sensor.

## Tugas
1. Buatlah rangkaian menggunakan fritzing tentang simulasi lampu yang otomatis menyala dengan lampu LED sebagai gambaran dari sebuah rumah. 1 LED mewakili 1 ruangan dalam rumah. Sehingga ketika waktu sore datang atau ketika mendung dan hujan, lampu otomatis nyala. Begitu pula ketika pagi datang, lampu otomatis mati.
2. Buatlah sebuah rangkaian untuk LED, sensor cahaya dan sensor suhu menggunakan fritzing, kemudian buatlah program dengan skenario sebagai berikut
    + Ketika cahaya redup dan suhu kategori dingin maka LED build akan berkedip
    + Ketika cahaya terang dan suhu tergolong tinggi, LED merah akan menyala.
    > LED build in adalah LED bawaan esp8266, biasanya berwarna biru atau merah
