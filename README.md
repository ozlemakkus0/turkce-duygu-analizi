# turkce-duygu-analizi
Türkçe metinler üzerinde TF-IDF + LSTM ile duygu analizi
# 🇹🇷 Türkçe Duygu Analizi: TF-IDF + LSTM

Bu proje, Türkçe metinlerde (örnek: film yorumları) duygu analizi yapmak için TF-IDF temizliği ve LSTM (Long Short-Term Memory) modeli kullanır. Projede ayrıca model başarımını gösteren grafikler ve confusion matrix bulunmaktadır.

## 📂 Dosyalar

- `Turkce_TF_IDF_LSTM_Notebook_2.ipynb`: Notebook, verileri işler, modeli eğitir ve tahminler yapar.
- `duygu_modeli.h5`: Eğitilmiş LSTM modeli (Keras formatında)
- `README.md`: Açıklamalar

## ⚙️ Kullanılan Teknolojiler

- Python 3
- TensorFlow / Keras
- scikit-learn
- NLTK
- Matplotlib

## 📊 Eğitim & Test Süreci

Model küçük bir Türkçe yorum seti üzerinde eğitilmiştir (örnek: 10 yorum). Eğitim doğruluğu ve doğrulama başarımı takip edilmiş, overfitting'e karşı `EarlyStopping` uygulanmıştır.

## 🔍 Örnek Tahminler

```python
yorum_tahmin_et("Film gerçekten çok etkileyiciydi, bayıldım.")
# -> Tahmin: ~0.89 (Olumlu)

yorum_tahmin_et("Bu ne biçim filmdi ya, hiç beğenmedim.")
# -> Tahmin: ~0.12 (Olumsuz)
