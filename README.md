# Rekomendasi-Dosen-Pembimbing
Tugas Project Temu Kembali Informasi, Prodi Sistem dan Teknologi Informasi, Universitas Negeri Jakarta (UNJ).

Sistem menerima ide judul/topik skripsi lalu merangking dosen yang paling sesuai, lengkap dengan skor,
penjelasan (kata kunci yang cocok dan judul pendukung), serta beban bimbingan dosen.

## Anggota dan pembagian tugas
| Anggota | Peran | Bagian utama |
|---|---|---|
| Muhammad Naufal Athallah | Data engineer & pre-processing | Mengumpulkan data dosen, publikasi (SINTA, Google Scholar, Garuda), dan skripsi; membersihkan dan menganonimkan data serta melakukan pre-processing. |
| Naufal Hibatullah Thariq | Core IR developer | Membangun sistem Inverted index, dua model ranking, dan penjelasan rekomendasi |
| Naila Shabrina | Evaluation & testing | Menyusun 20-30 query uji, penilaian relevansi, implementasi metrik evaluasi, dan analisis kegagalan |
| Muhammad Naufal Razan | Full-stack & integrasi | Membangun antarmuka web menggunakan Streamlit, mengatur repositori GitHub, membuat video demo, mengkoordinasi laporan |

Catatan: Setiap anggota tidak terpaku pada peran dan tugas utamanya masing-masing, jadi bisa saling membantu tugas anggota lain jika ada kesulitan.
Setiap anggota wajib memahami dan mampu menjelaskan seluruh kode.

## Fitur
- Inverted index buatan sendiri (tanpa library pencarian siap pakai).
- Dua model ranking: **TF-IDF (cosine)** dan **BM25** (k1=1.5, b=0.75).
- Dua representasi profil dosen: **publikasi saja** dan **gabungan** (publikasi + judul skripsi yang dibimbing).
- Penjelasan rekomendasi: kata kunci yang cocok dan judul pendukung.
- Bonus (opsional): **pertimbangan beban bimbingan** (slider; skripsi dibimbing dibanding kuota) dan **tampilan perbandingan berdampingan** profil publikasi vs gabungan.

## Struktur repo
menyusul

## Cara menjalankan
menyusul

## Data
Dataset berisi 22 dosen, 329 publikasi (241 publikasi unik), dan 310 skripsi (545 baris skripsi-pembimbing, karena satu skripsi bisa punya dua pembimbing)

**Sumber (informasi publik):**
- Skripsi dan nama pembimbing: Repositori UNJ (repository.unj.ac.id), program studi S1 Sistem dan Teknologi Informasi dan S1 PTIK.
- Publikasi dosen: Google Scholar, Garuda (garuda.kemdiktisaintek.go.id), dan SINTA (sinta.kemdiktisaintek.go.id).
- Tanggal pengambilan: **11-12, dan 17 November 2026**.

## Evaluasi
menyusul

## Penggunaan alat AI dan Etika Data
Kelompok menggunakan Claude (Anthropic) untuk membantu pengerjaan proyek baik struktur kode maupun query, serta menulis skrip pengumpulan data. Seluruh keluaran AI ditinjau, diuji, dan disesuaikan oleh anggota kelompok. Setiap anggota akan tetap memahami dan wajib bisa menjelaskan seluruh kode dan hasil saat presentasi.

Data skripsi dikumpulkan dari halaman publik repositori UNJ untuk prodi Sistem dan Teknologi Informasi dan Pendidikan Teknik Informatika dan Komputer, periode 2024-2026 menggunakan script python lewat google collab. Pengambilan data mematuhi robots.txt situs bersangkutan, dengan jeda 1,5 detik antar permintaan agar tidak memberatkan server. Data yang disimpan hanya judul, tahun, dan nama dosen pembimbing. Data mahasiswa tidak disimpan maupun ditampilkan. Nama dosen pembimbing merupakan informasi publik yang tercantum di repositori. Sumber dan tanggal pengambilan data dicatat dalam README. Untuk data publikasi dosen diambil dari SINTA, Google Scholar, dan GARUDA secara manual. 

