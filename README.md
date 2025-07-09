#  Waypoint Tracker
English Description
日本語は下にあります。
現在（2025年　７月現在制作中）
---

##  Project Overview
A real-time GPS-based participant tracking system built with React Native (Expo) and Laravel.
Admins manage GPX routes, and participants receive turn-by-turn directional guidance without full map exposure.
**Real-life participant tracking system with Laravel backend and React Native mobile app.**  
Participants receive directional guidance; admins manage GPX routes and track progress.

Waypoint Tracker enables organizers to guide and monitor participants along predefined routes using GPS coordinates and directional arrows. The system ensures:

 Admin control over route management via GPX uploads  
 Participants receive real-time directional assistance, without exposing full waypoint maps  
 Secure role-based access for Admins and Participants  


---

##  Technologies

- **Frontend:** React Native (Expo)  
- **Backend:** Laravel (PHP, recommended with Sanctum for token authentication)  
- **Database:** MySQL or PostgreSQL  
- **Authentication:** Token-based login (Laravel Sanctum preferred)  

---

##  Core Features

- **User Registration & Login with Role Selection**  
- **Role-Specific Screens**  
   - **Admin:**  
     - Upload GPX route files  
     - Monitor participant status (future improvement)  
   - **Participant:**  
     - Directional arrows for route guidance  
     - Coordinates display, without full map view  

- **GPX File Upload & Parsing**  
- **Real-time waypoint tracking (directional focus only)**  

---

##  Setup Instructions

## Backend: Laravel API
```bash
cd your-backend-folder
composer install

```
Sample .env settings:
```bash
DB_CONNECTION=mysql
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

```bash 
php artisan migrate

composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate

php artisan serve --host=192.168.0.101 --port=8001
```
---

## Frontend: React Native with Expo:
1.Navigate to frontend folder:
```bash
cd your-frontend-folder
npm install
npx expo start --tunnel
 ```

3.Start Expo development server:
```bash
npx expo start --tunnel
Use Expo Go app on your mobile device (connected to same Wi-Fi as backend) to run the application.
 ```

# 🧭 Waypoint Tracker

## 🇯🇵 日本語説明

リアルタイムGPSベースの参加者追跡アプリケーション。  
React Native (Expo) と Laravel によるクロスプラットフォーム対応。  
管理者はGPXファイルをアップロードしてルートを設定し、参加者は進行方向のみを案内されながらルートを進みます。

---

### 🔍 概要

Waypoint Tracker は、以下の2つの視点から構築されたシステムです：

- **管理者（Admin）**: GPXファイルでルートを設定・管理  
- **参加者（Participant）**: 現在地と進行方向のみを確認しながらルートを進行

---

### 🎯 主な特徴

- ロール選択付きのログイン（Admin / Participant）
- GPXファイルのアップロード・解析
- 進行方向の矢印によるガイド（地図は非表示）
- モバイルでのリアルタイム位置情報処理
- Laravel Sanctum によるトークン認証対応（推奨）

---

### 🧰 使用技術

| 分類 | 技術 |
|------|------|
| フロントエンド | React Native (Expo) |
| バックエンド | Laravel (PHP) |
| データベース | MySQL / PostgreSQL / H2 |
| 認証 | Laravel Sanctum（トークンベース） |

---

### 🚀 セットアップ手順

#### 📦 バックエンド（Laravel）

```bash
cd your-backend-folder
composer install
```

## .env 設定例：

```bash
DB_CONNECTION=mysql
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```
# スタート
```bash
php artisan migrate
```

# Sanctum のインストール
composer require laravel/sanctum
php artisan vendor:publish --provider="Laravel\Sanctum\SanctumServiceProvider"
php artisan migrate

php artisan serve --host=192.168.0.101 --port=8001


# 📱 フロントエンド（React Native + Expo）
```bash
cd your-frontend-folder
npm install
npx expo start --tunnel
```
### 同一Wi-Fiネットワーク上で Expo Go を使用してください。
