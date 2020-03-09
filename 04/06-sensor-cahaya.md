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
1. Buatlah simulasi lampu yang otomatis menyala (menggunakan lampu LED 1 buah) ketika intensitas cahaya mulai redup dan sebaliknya, lampu mati otomatis ketika intensitas cahaya mulai terang.
2. Dari soal tugas nomor 1, tambahkan beberapa lampu LED sebagai simulasi dari sebuah rumah. 1 LED mewakili 1 ruangan dalam rumah. Sehingga ketika waktu sore datang atau ketika mendung dan hujan, lampu otomatis nyala. Begitu pula ketika pagi datang, lampu otomatis mati.