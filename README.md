# 🧪 Studi Kasus Backend
## 🚚 Sistem Pengiriman Paket (Delivery Service)

---

## 📖 Deskripsi

Sebuah perusahaan logistik bernama **FastSend** ingin membuat sistem backend untuk menghitung **biaya akhir pengiriman paket**.

Setiap pelanggan dapat mengirim paket dengan berbagai pilihan layanan dan jarak tujuan. Sistem harus menghitung total biaya berdasarkan aturan yang berlaku.

---

## 🎯 Ketentuan Sistem

### 📦 1. Jenis Layanan Pengiriman

Terdapat 3 jenis layanan:

#### 🟢 Regular
- Harga dasar: Rp10.000 per kg

#### 🔵 Express
- Harga dasar: Rp15.000 per kg

#### 🟣 SameDay
- Harga dasar: Rp20.000 per kg
- Diskon 10% dari total biaya (sebelum biaya lain)

---

### 🌍 2. Jarak Pengiriman

#### 📍 Local
- Tidak ada biaya tambahan

#### 🌐 Intercity
- Tambahan biaya Rp5.000

---

### ⚖️ 3. Berat Paket

- Berat (`weight`) dalam kilogram
- Harus lebih dari 0

---

### 🎁 4. Kode Promo (Opsional)

| Kode       | Efek           |
|------------|----------------|
| DISKON10   | Diskon 10%     |
| POTONG5K   | Potong Rp5.000 |

📌 Promo diterapkan **setelah semua perhitungan layanan dan jar ak selesai**

---

## 📥 Request Body

```json
{
  "name": "Gabriel",
  "serviceType": "SameDay",
  "weight": 2,
  "distanceType": "Intercity",
  "promo": "DISKON10"
}
```
## 📌 Endpoint
