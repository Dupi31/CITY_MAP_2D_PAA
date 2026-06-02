# Skenario Pengujian

## Pengujian 1: Random Posisi
Program diuji dengan mengacak titik asal dan titik tujuan. Sistem harus mampu menemukan rute tanpa hardcoding.

## Pengujian 2: Random Peta
Program diuji dengan mengacak bentuk peta. Algoritma tetap harus dapat mencari jalur selama graph jalan saling terhubung.

## Pengujian 3: Kendaraan Mengikuti Jalan
Kendaraan harus bergerak mengikuti rute hasil Dijkstra dan tidak keluar dari jalur jalan.

## Pengujian 4: Zoom dan Pan
Pengguna dapat memperbesar, memperkecil, dan menggeser peta tanpa mengubah posisi asli node pada world coordinate.

## Pengujian 5: Rute Terpendek
Program menampilkan rute dengan total bobot jarak terkecil berdasarkan hasil algoritma Dijkstra.

## Pengujian 6: Start dan Finish Manual
User dapat memilih titik awal dengan klik kiri dan titik tujuan dengan klik kanan. Program harus menghitung ulang rute berdasarkan titik yang dipilih.
