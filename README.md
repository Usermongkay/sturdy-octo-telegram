# translate

[![Repository](https://img.shields.io/badge/Repository-translate-blue?style=flat-square)](https://github.com/Usermongkay/translate)
[![Workflow](https://img.shields.io/badge/Workflow-v4.yml-green?style=flat-square)](https://raw.githubusercontent.com/Usermongkay/translate/refs/heads/main/.github/workflows/v4.yml)

Ini hanya sekedar script & workflows untuk mentranslasikan file `.rpy` dengan jumlah yang agak banyak.

## 🚀 Tatacara Penggunaan

### 1. Persiapan File
- Taruh file `.rpy` yang akan diterjemahkan pada folder `tl/batch_1-8`
- Jika file `.rpy` yang akan diterjemahkan hanya ada 2 file, maka:
  - `file1.rpy` → taruh di folder `tl/batch_1`
  - `file2.rpy` → taruh di folder `tl/batch_2`

> ⚠️ **Penting:** Hanya buat folder batch yang dibutuhkan saja!

### 2. Struktur Folder
```
tl/
├── batch_1/
│   └── file1.rpy
├── batch_2/
│   └── file2.rpy
├── batch_3/
│   └── file3.rpy
└── ...
```

## ⚡ Optimasi Kecepatan

### Jika Translate Terasa Lambat
Modifikasi file `py/translate.py` dengan:

1. **Menggunakan API AI atau Google Translate**
2. **Lakukan batch translate per 10 line**

```python
# Contoh optimasi di translate.py
BATCH_SIZE = 10  # Translate per 10 baris
API_PROVIDER = "google"  # atau "openai", "deepl"
```

## 📁 File Penting

| File | Deskripsi |
|------|-----------|
| `py/translate.py` | Script utama untuk translasi |
| `.github/workflows/v4.yml` | Workflow automation |
| `tl/batch_*/` | Folder untuk file .rpy |

## 🔗 Links

- **Repository:** [https://github.com/Usermongkay/translate](https://github.com/Usermongkay/translate)
- **Raw Workflow:** [v4.yml](https://raw.githubusercontent.com/Usermongkay/translate/refs/heads/main/.github/workflows/v4.yml)

## 📝 Catatan

Script ini dirancang khusus untuk menangani file `.rpy` (Ren'Py script files) dengan volume besar secara otomatis menggunakan GitHub Actions.

---
*Happy translating! 🌐*