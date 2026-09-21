# Project Charter — NURA

## 1. Project Overview

**Project Name:** NURA  
**Full Name:** Network & URL Abuse Reporting Application  
**Project Type:** Web Application  
**Methodology:** SDLC + DevSecOps

NURA adalah aplikasi web yang dirancang untuk membantu pengguna
melaporkan domain atau URL yang diduga terlibat dalam aktivitas
penyalahgunaan, serta membantu administrator/analyst dalam melakukan
review dan pengelolaan laporan.

---

## 2. Background

Penyalahgunaan domain dan URL dapat digunakan dalam berbagai aktivitas
berbahaya seperti phishing, malware distribution, scam, dan bentuk
penyalahgunaan lainnya.

Proses pelaporan yang tidak terstruktur dapat menyebabkan laporan sulit
dikelola, diverifikasi, dan dipantau statusnya.

Oleh karena itu, NURA dikembangkan sebagai platform edukatif untuk
mensimulasikan proses pelaporan dan pengelolaan laporan domain/URL secara
terstruktur.

---

## 3. Problem Statement

Permasalahan yang ingin ditangani:

1. Belum adanya sistem sederhana untuk mengelola laporan domain/URL
   secara terstruktur dalam proyek ini.
2. Informasi laporan dapat sulit dilacak apabila tidak memiliki status
   dan riwayat pengelolaan.
3. Proses review laporan perlu memiliki alur yang jelas antara reporter
   dan analyst.

---

## 4. Project Objectives

NURA bertujuan untuk:

- menyediakan fitur pelaporan domain/URL;
- melakukan validasi terhadap data laporan;
- menyediakan sistem pengelolaan laporan;
- menyediakan proses review oleh analyst;
- menyediakan status untuk memantau perkembangan laporan;
- menerapkan prinsip keamanan dalam proses pengembangan aplikasi.

---

## 5. Project Scope

### In Scope

- Pelaporan domain/URL.
- Validasi input laporan.
- Penyimpanan data laporan.
- Dashboard laporan.
- Review laporan oleh analyst.
- Perubahan status laporan.
- Riwayat/status laporan.
- Authentication dan authorization.
- Security testing.

### Out of Scope

- Melakukan takedown domain secara langsung.
- Menghubungi registrar secara otomatis.
- Melakukan investigasi malware secara mendalam.
- Menggantikan platform resmi seperti IDADX.
- Melakukan pemblokiran domain secara langsung.

---

## 6. Stakeholders & User Roles

| Role | Responsibility |
|---|---|
| Reporter | Mengirim dan memantau laporan |
| Analyst/Admin | Melakukan review dan mengelola laporan |
| Developer | Mengembangkan dan memelihara aplikasi |
| Tester | Melakukan pengujian aplikasi |

---

## 7. High-Level Requirements

NURA harus menyediakan:

- Form pelaporan domain/URL.
- Validasi data.
- Penyimpanan laporan.
- Daftar laporan.
- Fitur pencarian/filter.
- Review laporan.
- Status laporan.
- Authentication dan authorization.
- Audit/logging aktivitas penting.

---

## 8. Technology / Resources

Teknologi yang direncanakan:

- Frontend: Next.js
- Database: PostgreSQL
- Version Control: Git & GitHub
- Deployment: Vercel
- Security/CI: GitHub Actions

*Technology stack dapat berubah selama tahap development.*

---

## 9. Project Constraints

Beberapa batasan proyek:

- Dikembangkan sebagai proyek akademik.
- Waktu pengembangan terbatas.
- Sumber daya pengembangan terbatas.
- Tidak melakukan tindakan terhadap domain/URL di dunia nyata.

---

## 10. Risks

| Risk | Impact | Mitigation |
|---|---|---|
| Scope terlalu luas | High | Membatasi fitur berdasarkan scope |
| Vulnerability pada aplikasi | High | Security testing & code review |
| Data laporan tidak valid | Medium | Input validation |
| Kehilangan data | High | Backup database |
| Keterlambatan development | Medium | Membagi pekerjaan berdasarkan fase SDLC |

---

## 11. Deliverables

Output proyek:

1. Source code aplikasi NURA.
2. Database.
3. Dokumentasi SDLC.
4. Dokumentasi DevSecOps.
5. Test Plan.
6. Test Case.
7. Test Report.
8. Security testing report.
9. Deployment aplikasi.

---

## 12. Success Criteria

Proyek dianggap mencapai tujuan apabila:

- pengguna dapat mengirim laporan domain/URL;
- data laporan dapat tersimpan dan dikelola;
- analyst dapat melakukan review laporan;
- status laporan dapat diperbarui;
- fitur utama dapat diuji;
- vulnerability kritis yang ditemukan selama pengujian ditangani;
- dokumentasi proyek tersedia di repository.

---

## 13. Project Timeline

| Phase | Output |
|---|---|
| Planning | Project Charter & Project Plan |
| Requirements | Requirements Specification |
| Design | Blueprint, Architecture, ERD, UI |
| Development | Source Code |
| Security | Security Scan & Security Testing |
| Testing | Test Plan, Test Case & Test Report |
| Deployment | Deployed Application |
| Monitoring | Monitoring & Feedback |
