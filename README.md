# City Map 2D PAA - Smart Courier

Project ini dibuat untuk mata kuliah **Perancangan dan Analisa Algoritma (PAA)**. Program mensimulasikan kendaraan/kurir yang bergerak dari titik asal menuju titik tujuan melalui jaringan jalan pada peta 2D.

Peta, titik asal, dan titik tujuan dapat diacak sehingga rute tidak dibuat secara hardcoding. Algoritma utama yang digunakan adalah **Dijkstra** untuk mencari rute terpendek berdasarkan bobot jarak antar-node.

## Struktur Project

```text
CITY_MAP_2D_PAA/
├── main.py
├── app_simulasi.py
├── map_generator.py
├── pathfinding.py
├── vehicle.py
├── camera.py
├── docs/
│   ├── pembagian_tugas.md
│   ├── analisis_algoritma.md
│   ├── kompleksitas.md
│   └── skenario_pengujian.md
└── README.md
```

## File Utama

- `main.py` menjalankan aplikasi.
- `app_simulasi.py` mengintegrasikan UI, render peta, tombol kontrol, random map, random posisi, dan animasi.
- `map_generator.py` membangkitkan peta, ruas jalan, node, edge, adjacency list, dan bobot edge.
- `pathfinding.py` berisi pencarian titik jalan terdekat, virtual node untuk titik start/finish, dan algoritma Dijkstra.
- `vehicle.py` berisi bentuk kendaraan, rotasi, dan visualisasi kendaraan.
- `camera.py` berisi transformasi koordinat, zoom, pan, dan pembatas kamera.

## Algoritma Utama

Algoritma utama yang digunakan adalah **Dijkstra** dengan struktur data **priority queue / heap**.

Bobot edge dihitung berdasarkan jarak Euclidean antar-node jalan:

```text
w = sqrt((x2 - x1)^2 + (y2 - y1)^2)
```

## Pembagian Tugas

1. **Vito** — Integrasi aplikasi, UI simulasi, kontrol tombol, render, dan animasi loop.
2. **Abdul Hafidz** — Visualisasi kendaraan, rotasi kendaraan, dan pergerakan kendaraan mengikuti rute.
3. **Rahman** — Graph, bobot edge, virtual node, dan algoritma Dijkstra.
4. **Adib** — Kamera, world coordinate, screen coordinate, zoom, pan, dan interaksi klik.

## Cara Menjalankan

```bash
python main.py
```

Jika menggunakan Linux dan `tkinter` belum tersedia, install paket Tkinter terlebih dahulu sesuai distro.

Contoh Fedora:

```bash
sudo dnf install python3-tkinter
```
