# Project Plan - NURA

## Tujuan Pengembangan

Pengembangan NURA dilakukan untuk menghasilkan aplikasi web
pelaporan dan pengelolaan domain/URL abuse yang dapat digunakan
sebagai proyek akademik dengan menerapkan SDLC dan DevSecOps.

## Metodologi

Pengembangan menggunakan tahapan:

```text
Planning
   ↓
Requirements
   ↓
Design
   ↓
Development
   ↓
Security Scanning
   ↓
Testing
   ↓
Deployment
   ↓
Monitoring & Evaluation
````

Aspek keamanan diterapkan sepanjang proses pengembangan.

## Rencana Pekerjaan

| Tahap            | Aktivitas                                         | Output                                       |
| ---------------- | ------------------------------------------------- | -------------------------------------------- |
| **Planning**     | Menentukan tujuan, scope, stakeholder, dan risiko | Project Charter, Project Plan, Risk Register |
| **Requirements** | Menentukan kebutuhan sistem dan keamanan          | Requirements                                 |
| **Design**       | Merancang arsitektur, flow, database, dan UI      | Blueprint                                    |
| **Development**  | Implementasi frontend, backend, dan database      | Source Code                                  |
| **Security**     | Scanning dan security testing                     | Security Results                             |
| **Testing**      | Functional, integration, dan security testing     | Test Report                                  |
| **Deployment**   | Build dan deployment aplikasi                     | Deployed Application                         |
| **Monitoring**   | Evaluasi dan pencatatan feedback                  | Evaluation                                   |

## Jadwal Pengembangan

| Tanggal         | Tahap                           | Target                                 |
| --------------- | ------------------------------- | -------------------------------------- |
| **21 Sep 2026** | Planning, Requirements & Design | Planning dan Blueprint selesai         |
| **22 Sep 2026** | Development                     | Database & backend dasar               |
| **23 Sep 2026** | Development                     | Fitur pelaporan                        |
| **24 Sep 2026** | Development                     | Dashboard & pengelolaan laporan        |
| **25 Sep 2026** | Development                     | Review, status & integrasi             |
| **26 Sep 2026** | Testing & Security              | Testing, security testing & bug fixing |
| **27 Sep 2026** | Finalisasi & Deployment         | Retest, deploy & dokumentasi           |

## Security Activities

| Tahap            | Aktivitas                        |
| ---------------- | -------------------------------- |
| **Planning**     | Identifikasi risiko keamanan     |
| **Requirements** | Security requirements            |
| **Design**       | Identifikasi ancaman dan kontrol |
| **Development**  | Secure coding & input validation |
| **Build**        | Dependency/code scanning         |
| **Testing**      | Security testing                 |
| **Deployment**   | Secure configuration             |
| **Monitoring**   | Logging & monitoring             |

## Deliverables

### Planning

* Project Charter
* Project Plan
* Risk Register

### Requirements

* Requirements Documentation

### Design

* System Architecture
* Use Case Diagram
* System Flow
* ERD
* Wireframe/UI

### Development

* Source Code
* Database
* Web Application

### Testing

* Test Plan
* Test Case
* Test Result
* Test Report
* Security Testing Report

### Deployment

* Deployed Application
* Deployment Documentation

## Definition of Done

Fitur dianggap selesai apabila:

* Telah diimplementasikan.
* Berjalan sesuai requirement.
* Telah dilakukan validasi input.
* Aspek keamanan yang relevan telah diperiksa.
* Telah diuji.
* Bug kritis telah diperbaiki.
* Perubahan telah disimpan ke repository.

Proyek dianggap selesai apabila fitur inti telah diimplementasikan,
diuji, didokumentasikan, dan berhasil di-deploy.
