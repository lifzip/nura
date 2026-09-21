# Project Charter — NURA

> **Network & URL Abuse Reporting Application**

## 1. Informasi Proyek

| Item | Keterangan |
|---|---|
| **Nama Proyek** | NURA |
| **Nama Lengkap** | Network & URL Abuse Reporting Application |
| **Jenis Proyek** | Aplikasi Web |
| **Metodologi** | SDLC + DevSecOps |
| **Periode Pengembangan** | 21–27 September 2026 |

## 2. Latar Belakang

Penyalahgunaan domain dan URL dapat dimanfaatkan untuk berbagai
aktivitas berbahaya seperti phishing, penipuan, distribusi malware,
dan bentuk penyalahgunaan lainnya.

NURA dikembangkan sebagai aplikasi berbasis web untuk membantu proses
pelaporan dan pengelolaan informasi domain atau URL yang diduga
mengalami penyalahgunaan secara lebih terstruktur.

## 3. Permasalahan

Proses pelaporan domain atau URL dapat menjadi sulit dikelola apabila
informasi laporan tidak tersusun secara terstruktur.

Permasalahan yang ingin ditangani:

- Data laporan belum terkelola secara terstruktur.
- Laporan sulit dipantau perkembangannya.
- Proses review laporan membutuhkan alur yang jelas.
- Status laporan perlu dapat dipantau oleh pengguna.

## 4. Tujuan

NURA bertujuan untuk:

1. Menyediakan fitur pelaporan domain atau URL.
2. Mengelola data laporan secara terstruktur.
3. Menyediakan proses review laporan.
4. Menyediakan status untuk memantau laporan.
5. Menerapkan prinsip keamanan dalam pengembangan aplikasi.

## 5. Ruang Lingkup

### In Scope

- Pelaporan domain atau URL.
- Validasi input.
- Penyimpanan laporan.
- Pengelolaan laporan.
- Review laporan.
- Perubahan status laporan.
- Pemantauan status.
- Dashboard.
- Authentication dan Authorization.

### Out of Scope

- Takedown domain secara langsung.
- Pemblokiran domain secara langsung.
- Investigasi malware secara mendalam.
- Menggantikan platform resmi domain abuse reporting.

## 6. Stakeholder dan Peran

| Stakeholder | Peran |
|---|---|
| **Reporter** | Mengirim dan memantau laporan |
| **Analyst/Admin** | Meninjau dan mengelola laporan |
| **Developer** | Mengembangkan aplikasi |
| **Tester** | Melakukan pengujian aplikasi |

## 7. Batasan

- Waktu pengembangan terbatas.
- Proyek dikembangkan untuk kebutuhan akademik.
- Fokus pada fitur inti pelaporan dan pengelolaan laporan.
- Sistem tidak melakukan tindakan langsung terhadap domain/URL.

## 8. Target Proyek

Pada akhir periode pengembangan, NURA diharapkan:

- Memiliki fitur inti pelaporan.
- Memiliki proses review.
- Memiliki status laporan.
- Telah melalui pengujian.
- Telah di-deploy.
