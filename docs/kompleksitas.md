# Analisis Kompleksitas

Algoritma utama yang digunakan adalah Dijkstra dengan priority queue / heap.

Misalkan:

- `V` = jumlah node atau titik pada graph jalan.
- `E` = jumlah edge atau ruas penghubung antar-node.

## Kompleksitas Waktu Dijkstra

Dijkstra dengan priority queue memiliki kompleksitas waktu:

```text
O((V + E) log V)
```

Penjelasan:

- Setiap node dapat masuk ke priority queue.
- Setiap edge dapat diperiksa ketika proses relaksasi.
- Operasi push/pop pada priority queue membutuhkan waktu `log V`.

## Kompleksitas Ruang

Graph disimpan menggunakan adjacency list, sehingga kompleksitas ruangnya:

```text
O(V + E)
```

Selain graph, program juga menyimpan struktur tambahan:

- Dictionary jarak terpendek sementara.
- Dictionary asal node untuk membangun ulang path.
- Set visited.
- Priority queue / heap.

Struktur tambahan tersebut membutuhkan ruang sekitar `O(V)`. Maka total ruang tetap didominasi oleh adjacency list, yaitu `O(V + E)`.

## Kompleksitas Pencarian Jalan Terdekat

Saat user klik pada peta, sistem mencari edge terdekat dari posisi mouse. Proses ini memeriksa semua edge.

```text
O(E)
```

Karena setiap ruas jalan diperiksa untuk menentukan proyeksi titik mouse ke edge.
