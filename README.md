# Jagabaya Apps

Aplikasi manajemen bisnis jasa pengamanan pribadi (bodyguard) yang dirancang untuk perusahaan penyedia jasa keamanan di Indonesia.

## Fitur Utama

- Manajemen Personel & HRD
- Penugasan & Tracking Lokasi
- Laporan & Manajemen Insiden
- Manajemen Klien & Layanan
- Keuangan & Administrasi

## Tech Stack

- Frontend Web: React.js (Admin Panel)
- Mobile App: React Native (Bodyguard & Client App) 
- Backend: Laravel 12 (PHP 8.2+)
- Database: MySQL 8.0+
- Authentication: Laravel Sanctum + JWT
- Real-time: Laravel WebSockets
- Storage: Laravel Storage dengan S3/Cloudinary
- Maps: Google Maps API

## Requirements

- PHP 8.2 atau lebih tinggi
- Composer 2.0 atau lebih tinggi
- Node.js 14.0.0 atau lebih tinggi
- MySQL 8.0 atau lebih tinggi
- Google Maps API Key (untuk fitur lokasi)

## Instalasi

### Backend Setup

```bash
# Clone repository
git clone [repository-url]
cd jagabaya-backend

# Install dependencies
composer install

# Copy .env example
cp .env.example .env

# Generate app key
php artisan key:generate

# Setup database
php artisan migrate

# Seed database dengan data awal
php artisan db:seed

# Start server
php artisan serve
```

### Frontend Admin Setup

```bash
# Masuk ke direktori frontend
cd frontend-admin

# Install dependencies
npm install

# Copy .env example
cp .env.example .env

# Start development server
npm run dev
```

### Mobile App Setup

```bash
# Masuk ke direktori mobile
cd mobile-app

# Install dependencies
npm install

# Copy .env example
cp .env.example .env

# Start development server
npm start
```

## Struktur Database

### Users & Authentication
- users
- personel_profiles
- roles_permissions

### Operational
- schedules
- attendances
- locations

### Reporting
- reports
- incidents
- evaluations

### Client Management
- client_requests
- services
- feedback

### Financial
- invoices
- payments
- salary_records

## API Endpoints

### Authentication
- POST /api/login
- POST /api/logout
- POST /api/refresh

### Personnel
- GET /api/personnel
- POST /api/personnel
- GET /api/personnel/{id}
- PUT /api/personnel/{id}
- DELETE /api/personnel/{id}

### Schedules
- GET /api/schedules
- POST /api/schedules
- GET /api/schedules/{id}
- PUT /api/schedules/{id}
- DELETE /api/schedules/{id}

### Attendance
- POST /api/attendance/check-in
- POST /api/attendance/check-out
- GET /api/attendance/history

### Reports
- GET /api/reports
- POST /api/reports
- GET /api/reports/{id}
- PUT /api/reports/{id}
- DELETE /api/reports/{id}

### Client Requests
- GET /api/client-requests
- POST /api/client-requests
- GET /api/client-requests/{id}
- PUT /api/client-requests/{id}
- DELETE /api/client-requests/{id}

## Environment Variables

### Backend (.env)
```
APP_NAME=Jagabaya
APP_ENV=local
APP_KEY=
APP_DEBUG=true
APP_URL=http://localhost

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=jagabaya
DB_USERNAME=root
DB_PASSWORD=

BROADCAST_DRIVER=pusher
CACHE_DRIVER=file
QUEUE_CONNECTION=redis
SESSION_DRIVER=file
SESSION_LIFETIME=120

GOOGLE_MAPS_API_KEY=
```

### Frontend (.env)
```
VITE_APP_NAME=Jagabaya
VITE_API_URL=http://localhost:8000
VITE_GOOGLE_MAPS_API_KEY=
```

### Mobile (.env)
```
APP_NAME=Jagabaya
API_URL=http://localhost:8000
GOOGLE_MAPS_API_KEY=
```

## Development Workflow

1. Pull latest changes dari main branch
2. Buat feature branch baru
3. Implementasi fitur/perubahan
4. Jalankan tests
5. Create pull request
6. Code review
7. Merge ke main branch

## Testing

### Backend
```bash
# Run unit tests
php artisan test

# Run specific test
php artisan test --filter=TestName
```

### Frontend
```bash
# Run tests
npm run test

# Run with coverage
npm run test:coverage
```

### Mobile
```bash
# Run tests
npm run test

# Run with coverage
npm run test:coverage
```

## Deployment

### Backend
1. Pull latest changes
2. Install/update dependencies
3. Run migrations
4. Clear cache
5. Restart services

### Frontend
1. Pull latest changes
2. Install/update dependencies
3. Build production assets
4. Deploy build files

### Mobile
1. Pull latest changes
2. Install/update dependencies
3. Build release version
4. Deploy to stores

## Kontribusi

1. Fork repository
2. Buat feature branch
3. Commit changes
4. Push ke branch
5. Create Pull Request

## Lisensi

Proprietary Software - All Rights Reserved

## Support

Untuk bantuan teknis silakan hubungi:
- Email: support@jagabaya.com
- Phone: (021) xxx-xxxx
