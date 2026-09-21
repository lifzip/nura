# System Requirements - NURA

> **Network & URL Abuse Reporting Application**

Dokumen ini mendefinisikan kebutuhan sistem NURA sebagai dasar
perancangan, pengembangan, dan pengujian aplikasi.

---

## 1. Gambaran Sistem

NURA merupakan aplikasi web yang menyediakan mekanisme untuk
melaporkan, mengelola, meninjau, dan memantau laporan terkait
domain atau URL yang diduga mengalami penyalahgunaan.

Sistem memiliki dua peran utama:

- **Reporter** - pengguna yang mengirim dan memantau laporan.
- **Analyst/Admin** - pengguna yang melakukan review dan mengelola
  laporan.

---

## 2. Functional Requirements

### FR-001 - Registrasi Pengguna

Sistem harus menyediakan fitur registrasi akun pengguna.

**Input:**
- Nama
- Email
- Password

**Ketentuan:**
- Email harus memiliki format yang valid.
- Email tidak boleh terdaftar lebih dari satu kali.
- Password harus memenuhi aturan keamanan yang ditentukan.

---

### FR-002 - Login

Sistem harus menyediakan fitur login untuk pengguna yang telah
memiliki akun.

**Input:**
- Email
- Password

Sistem harus melakukan autentikasi sebelum memberikan akses ke
fitur yang membutuhkan login.

---

### FR-003 - Pelaporan Domain atau URL

Reporter harus dapat membuat laporan penyalahgunaan domain atau URL.

**Data laporan minimal:**
- Domain atau URL
- Jenis penyalahgunaan
- Deskripsi
- Bukti pendukung
- Waktu pelaporan

---

### FR-004 - Validasi Input Laporan

Sistem harus melakukan validasi terhadap data laporan sebelum
disimpan.

Validasi minimal meliputi:

- Format URL/domain.
- Field wajib.
- Panjang input.
- Format dan ukuran file bukti jika upload digunakan.
- Pencegahan input berbahaya.

---

### FR-005 - Penyimpanan Laporan

Sistem harus menyimpan laporan yang berhasil divalidasi ke dalam
database.

Setiap laporan memiliki identitas unik.

---

### FR-006 - Melihat Laporan

Reporter dapat melihat laporan yang telah dibuat olehnya.

Informasi yang ditampilkan minimal:

- ID laporan
- Domain/URL
- Jenis penyalahgunaan
- Tanggal laporan
- Status laporan

---

### FR-007 - Pelacakan Status Laporan

Sistem harus menyediakan status untuk menunjukkan perkembangan
laporan.

Status minimal:

```text
Submitted
    ↓
Under Review
    ↓
Verified / Rejected
    ↓
Resolved
````

---

### FR-008 - Review Laporan

Analyst/Admin harus dapat melihat laporan yang masuk dan melakukan
review.

Analyst/Admin dapat:

* Melihat detail laporan.
* Memeriksa informasi yang diberikan.
* Menambahkan catatan review.
* Mengubah status laporan.

---

### FR-009 - Pengelolaan Laporan

Analyst/Admin harus dapat mengelola laporan berdasarkan status dan
informasi yang tersedia.

Sistem harus menyediakan kemampuan untuk:

* Melihat daftar laporan.
* Mencari laporan.
* Memfilter laporan.
* Melihat detail laporan.
* Memperbarui status laporan.

---

### FR-010 - Dashboard

Sistem harus menyediakan dashboard untuk Analyst/Admin.

Dashboard minimal menampilkan:

* Total laporan.
* Laporan baru.
* Laporan dalam proses review.
* Laporan terverifikasi.
* Laporan ditolak.
* Laporan selesai.

---

### FR-011 - Role-Based Access Control

Sistem harus membatasi akses berdasarkan role pengguna.

| Fitur                   | Reporter | Analyst/Admin |
| ----------------------- | :------: | :-----------: |
| Registrasi              |     ✓    |       ✓       |
| Login                   |     ✓    |       ✓       |
| Membuat laporan         |     ✓    |       ✓       |
| Melihat laporan sendiri |     ✓    |       ✓       |
| Melihat seluruh laporan |     -    |       ✓       |
| Review laporan          |     -    |       ✓       |
| Mengubah status         |     -    |       ✓       |
| Dashboard               |     -    |       ✓       |

---

### FR-012 - Logout

Sistem harus menyediakan fitur logout untuk mengakhiri sesi
pengguna.

---

## 3. Non-Functional Requirements

### NFR-001 - Usability

Antarmuka harus mudah dipahami dan dapat digunakan oleh pengguna
tanpa memerlukan pengetahuan teknis khusus.

### NFR-002 - Performance

Sistem harus memberikan respons yang wajar untuk operasi umum seperti
login, pengiriman laporan, pencarian, dan pengambilan data.

### NFR-003 - Availability

Aplikasi harus dapat diakses melalui lingkungan deployment yang
telah ditentukan.

### NFR-004 - Maintainability

Source code harus memiliki struktur yang terorganisasi sehingga
mudah dipelihara dan dikembangkan.

### NFR-005 - Compatibility

Aplikasi harus dapat digunakan pada browser modern seperti Chrome,
Edge, dan Firefox.

### NFR-006 - Responsiveness

Antarmuka harus dapat menyesuaikan tampilan pada perangkat desktop
dan mobile.

---

## 4. Security Requirements

### SR-001 - Authentication

Sistem harus memastikan bahwa fitur yang membutuhkan autentikasi
hanya dapat diakses oleh pengguna yang telah login.

### SR-002 - Authorization

Sistem harus memverifikasi hak akses pengguna berdasarkan role.

### SR-003 - Password Security

Password pengguna tidak boleh disimpan dalam bentuk plaintext.

### SR-004 - Input Validation

Seluruh input dari pengguna harus divalidasi sebelum diproses atau
disimpan.

### SR-005 - Protection Against Injection

Sistem harus menerapkan mekanisme untuk mencegah serangan injection
pada input pengguna.

### SR-006 - Protection Against XSS

Data yang berasal dari pengguna harus ditangani dengan aman untuk
mengurangi risiko Cross-Site Scripting.

### SR-007 - Session Security

Session atau token autentikasi harus dikelola secara aman dan akses
yang tidak sah harus ditolak.

### SR-008 - Sensitive Data Protection

Data sensitif tidak boleh ditampilkan atau disimpan secara tidak
aman.

### SR-009 - File Upload Security

Jika sistem menyediakan upload bukti, file harus divalidasi
berdasarkan tipe, ukuran, dan karakteristik yang diizinkan.

---

## 5. Business Rules

### BR-001

Setiap laporan harus memiliki status.

### BR-002

Reporter hanya dapat melihat laporan yang dibuat oleh akunnya.

### BR-003

Analyst/Admin dapat melihat seluruh laporan.

### BR-004

Perubahan status laporan hanya dapat dilakukan oleh
Analyst/Admin.

### BR-005

Laporan yang belum memenuhi informasi wajib tidak dapat dikirim.

### BR-006

Sistem tidak melakukan pemblokiran atau takedown domain secara
langsung.

### BR-007

Laporan yang dikirim melalui NURA merupakan data untuk proses
review dan tidak secara otomatis menyatakan bahwa domain atau URL
tersebut terbukti melakukan penyalahgunaan.

---

## 6. Data Requirements

Data utama yang dikelola sistem meliputi:

| Data       | Keterangan                  |
| ---------- | --------------------------- |
| User       | Data akun pengguna          |
| Role       | Hak akses pengguna          |
| Report     | Data laporan                |
| Abuse Type | Jenis penyalahgunaan        |
| Evidence   | Bukti pendukung laporan     |
| Review     | Catatan hasil review        |
| Status     | Status perkembangan laporan |

---

## 7. Scope Requirements

### In Scope

* Registrasi dan login.
* Pelaporan domain/URL.
* Validasi laporan.
* Penyimpanan laporan.
* Pelacakan status.
* Review laporan.
* Dashboard Analyst/Admin.
* Role-based access control.
* Security testing.

### Out of Scope

* Takedown domain secara otomatis.
* Pemblokiran domain secara langsung.
* Investigasi malware secara mendalam.
* Integrasi langsung dengan registrar.
* Penggantian platform resmi domain abuse reporting.

---

## 8. Acceptance Criteria

Sistem dianggap memenuhi requirement apabila:

* Pengguna dapat melakukan registrasi dan login.
* Reporter dapat mengirim laporan domain/URL.
* Sistem melakukan validasi terhadap input laporan.
* Laporan tersimpan dengan benar.
* Reporter dapat melihat status laporan miliknya.
* Analyst/Admin dapat melihat dan melakukan review laporan.
* Analyst/Admin dapat mengubah status laporan.
* Dashboard menampilkan informasi laporan.
* Hak akses berdasarkan role berjalan sesuai ketentuan.
* Pengujian keamanan terhadap fitur utama telah dilakukan.
* Tidak terdapat bug kritis yang belum ditangani sebelum deployment.

