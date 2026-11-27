# Elistreaming — Starter Project

Starter aplikasi katalog dan streaming anime Android dengan backend milik sendiri.

## Isi proyek
- `flutter_app/`: source Flutter untuk Android.
- `backend/`: REST API Node.js + Express dengan penyimpanan JSON sederhana.
- `docs/PANDUAN_ANDROID.md`: panduan membuat APK dari HP Android.
- `docs/DEPLOY_BACKEND.md`: panduan menjalankan API di server sendiri.

> Penting: aplikasi ini tidak menyertakan video anime, tautan bajakan, atau sumber streaming pihak ketiga. Isi server hanya dengan video yang kamu miliki atau yang memang kamu punya izin untuk distribusikan.

## Arsitektur
Flutter Android → REST API Node.js → katalog JSON + file video HLS/MP4 di server.

Untuk penggunaan serius, ganti penyimpanan JSON dengan PostgreSQL dan gunakan object storage/CDN untuk file video. Jangan menaruh token admin di dalam APK.

## Mulai cepat
1. Baca `docs/PANDUAN_ANDROID.md`.
2. Jalankan backend mengikuti `docs/DEPLOY_BACKEND.md`.
3. Atur `API_BASE_URL` di `flutter_app/lib/config.dart`.
4. Buat proyek Flutter Android, salin source `flutter_app/lib/` dan `pubspec.yaml`, lalu build APK.

## API ringkas
- `GET /health`
- `GET /api/anime`
- `GET /api/anime/:id`
- `GET /api/anime/:id/episodes`
- `POST /api/admin/anime` (header `x-admin-token`)
- `POST /api/admin/anime/:id/episodes` (header `x-admin-token`)

Contoh data anime dan episode hanya data demonstrasi. Ganti dengan metadata dan video berizin milikmu.
