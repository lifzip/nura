# Risk Register - NURA

> Daftar risiko yang dapat memengaruhi pengembangan NURA selama periode
> 21–27 September 2026.

## Daftar Risiko

| ID | Risiko | Penyebab | Likelihood | Impact | Risk Level | Mitigasi | Status |
|---|---|---|---|---|---|---|---|
| R-001 | Development terlambat | Waktu pengembangan terbatas | High | High | Critical | Memprioritaskan fitur inti dan menghindari perubahan scope | Open |
| R-002 | Scope proyek terlalu luas | Penambahan fitur di luar kebutuhan utama | High | High | Critical | Menetapkan dan mempertahankan batasan scope | Open |
| R-003 | Fitur tidak sesuai requirement | Requirement kurang jelas atau berubah | Medium | High | High | Melakukan review requirement sebelum development | Open |
| R-004 | Bug ditemukan pada tahap akhir | Testing tidak dilakukan secara bertahap | High | Medium | High | Melakukan testing dan retesting secara berkala | Open |
| R-005 | Vulnerability ditemukan | Kesalahan implementasi atau secure coding yang kurang | Medium | High | High | Melakukan security testing dan perbaikan vulnerability | Open |
| R-006 | Database bermasalah | Kesalahan konfigurasi atau implementasi database | Medium | High | High | Validasi konfigurasi, struktur database, dan backup data | Open |
| R-007 | Deployment gagal | Konfigurasi environment production tidak sesuai | Medium | High | High | Melakukan deployment verification sebelum demonstrasi | Open |
| R-008 | Kehilangan perubahan kode | Kesalahan penggunaan Git atau kerusakan environment | Low | High | Medium | Menggunakan GitHub sebagai repository dan melakukan commit secara berkala | Open |
| R-009 | Waktu testing tidak mencukupi | Development selesai terlalu dekat dengan deadline | Medium | High | High | Menyediakan waktu khusus untuk testing dan bug fixing | Open |

## Kriteria Penilaian

### Likelihood

| Level | Keterangan |
|---|---|
| **Low** | Kemungkinan risiko terjadi relatif kecil |
| **Medium** | Risiko memiliki kemungkinan terjadi |
| **High** | Risiko sangat mungkin terjadi |

### Impact

| Level | Keterangan |
|---|---|
| **Low** | Dampak kecil dan tidak mengganggu target utama |
| **Medium** | Mengganggu sebagian proses atau fitur |
| **High** | Dapat menghambat target utama proyek |

### Risk Level

Risk level ditentukan berdasarkan kombinasi antara
**Likelihood** dan **Impact**.

| Likelihood | Impact | Risk Level |
|---|---|---|
| High | High | **Critical** |
| High | Medium | **High** |
| Medium | High | **High** |
| Medium | Medium | **Medium** |
| Low | High | **Medium** |
| Low | Medium | **Low** |
| Low | Low | **Low** |

## Strategi Penanganan Risiko

### Critical

Risiko harus menjadi prioritas utama karena berpotensi menghambat
pencapaian target proyek.

Tindakan:

- Memprioritaskan fitur inti.
- Menghindari penambahan scope.
- Memantau progres pengembangan secara berkala.

### High

Risiko harus dipantau dan ditangani selama proses pengembangan.

Tindakan:

- Melakukan testing secara bertahap.
- Melakukan security testing.
- Melakukan validasi requirement.
- Menyediakan waktu untuk bug fixing dan retesting.

### Medium dan Low

Risiko tetap dipantau dan ditangani apabila mulai memberikan dampak
terhadap proyek.

## Status Risiko

| Status | Keterangan |
|---|---|
| **Open** | Risiko masih aktif dan belum ditangani sepenuhnya |
| **Mitigated** | Tindakan mitigasi telah dilakukan |
| **Occurred** | Risiko telah terjadi |
| **Closed** | Risiko sudah tidak relevan atau telah selesai ditangani |

## Pemantauan Risiko

Risk register diperbarui apabila:

- Risiko baru ditemukan.
- Likelihood atau impact berubah.
- Tindakan mitigasi dilakukan.
- Risiko terjadi.
- Risiko sudah tidak relevan.
