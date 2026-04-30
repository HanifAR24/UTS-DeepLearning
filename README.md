# UTS Pengantar Deep Learning

Template pengerjaan 3 kasus Kaggle dengan alur seragam:
EDA -> Preprocessing -> Baseline ML -> Deep Learning -> Evaluasi -> Error Analysis -> Kesimpulan.

Notebook:
- `notebooks/01_titanic_template.ipynb`
- `notebooks/02_mnist_template.ipynb`
- `notebooks/03_tweets_template.ipynb`

## Cara Menjalankan

Wajib gunakan environment terisolasi agar reproducible di device mana pun.

### Windows (PowerShell)
```powershell
py -3.11 -m venv .venv
.venv\Scripts\activate
python -m pip install --upgrade pip
pip install -r requirements.txt
python -m ipykernel install --user --name uts-dl --display-name "Python (uts-dl)"
jupyter notebook
```

Lalu pilih kernel `Python (uts-dl)` saat membuka notebook.

## Quick Verify

Jalankan cek singkat berikut setelah instalasi:

```powershell
python --version
python -c "import torch, sklearn, pandas; print('OK:', torch.__version__)"
```

Jika perintah di atas sukses, notebook siap dijalankan.

## Lokasi Dataset (Fallback Lokal)

Notebook akan auto-download dataset ke cache, dan juga mencari file lokal relatif:
- Titanic: `data/titanic/`
- MNIST: `data/mnist/`
- Tweets: `data/tweets/`

## Catatan Reproducibility

- Seed diset ke `42`.
- Split data dibuat konsisten (train/val/test) untuk perbandingan fair.
- Semua model deep learning di template memakai **PyTorch** (bukan TensorFlow) untuk kompatibilitas VSCode/Windows.
- Notebook tidak melakukan auto-install package; semua dependency dipasang dari `requirements.txt`.
