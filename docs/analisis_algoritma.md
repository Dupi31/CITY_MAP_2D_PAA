# Analisis Algoritma

Project ini menyelesaikan masalah pencarian jalur dari satu titik spasial menuju titik spasial lain melalui jaringan jalan. Kendaraan harus bergerak melalui jalan dan tidak boleh menggunakan rute hardcoding.

## Representasi Graph

Peta direpresentasikan sebagai graph berbobot:

- Node merepresentasikan titik pada ruas jalan.
- Edge merepresentasikan hubungan antar-node yang saling bersebelahan.
- Bobot edge merepresentasikan jarak antar-node.

Graph disimpan menggunakan adjacency list. Contoh bentuknya:

```python
graph_adj = {
    0: [(1, 45.2), (2, 70.8)],
    1: [(0, 45.2), (3, 60.0)]
}
```

## Penentuan Bobot

Bobot dihitung menggunakan jarak Euclidean antar dua node:

```text
w = sqrt((x2 - x1)^2 + (y2 - y1)^2)
```

Dengan cara ini, ruas jalan yang lebih panjang memiliki bobot lebih besar.

## Virtual Node

Titik start dan finish dapat dipilih di tengah ruas jalan, bukan hanya tepat pada node. Karena itu sistem membuat node virtual untuk menghubungkan titik start/finish ke node jalan terdekat pada edge yang sama.

## Dijkstra

Dijkstra digunakan untuk mencari rute dengan total bobot paling kecil dari titik asal ke titik tujuan. Langkah umumnya:

1. Masukkan node awal ke priority queue dengan jarak 0.
2. Ambil node dengan jarak terkecil dari priority queue.
3. Periksa semua tetangganya.
4. Jika ditemukan jarak yang lebih kecil, update jarak dan node asalnya.
5. Ulangi sampai node tujuan ditemukan.
6. Rekonstruksi path dari node tujuan ke node awal.

Hasil akhirnya adalah urutan node yang membentuk rute terpendek.
