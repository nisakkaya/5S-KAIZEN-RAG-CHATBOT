# 💬 5S & Kaizen Öğretici Chatbot – Akbank GenAI Bootcamp

## 🚀 Projenin Amacı
Bu proje, **RAG (Retrieval Augmented Generation)** mimarisi kullanarak kullanıcı sorularına doğru ve bağlamsal yanıtlar üretebilen bir chatbot geliştirmeyi amaçlamaktadır.  
Amaç, 5S ve Kaizen metodolojileri ile ilgili bilgileri **dinamik ve bağlamsal olarak** sunabilen, güvenilir bir dijital asistan oluşturmaktır.

---

## 📄 Veri Seti Hakkında
Kullanılan veri seti: **The Ultimate Guide to 5S and 5S Training _ KAIZEN™ Article.pdf**  

- **Format:** PDF  
- **İçerik:** 5S ve Kaizen uygulamaları ile ilgili dokümanlar  
- **Kullanım:** Chatbot, kullanıcı sorularına yanıt üretmek için PDF içeriklerini referans alır  

> ⚠️ Not: Veri seti ve API Key repoya dahil edilmemiştir. Kod çalıştırıldığında PDF dosyası Colab veya lokal ortamda kullanılmalıdır.

---

## 🛠 Kullanılan Yöntemler ve Teknolojiler
- **Generation Model:** Google Gemini API (gemini-2.5-flash)  
- **Embedding Model:** Google Generative AI Embeddings (text-embedding-004)  
- **Vektör Veritabanı:** Chroma (`./chroma_db`)  
- **RAG Pipeline Framework:** LangChain + Google Generative AI API  

**Pipeline Özeti:**  
1. Kullanıcı sorusu embedding modeli ile vektöre dönüştürülür.  
2. Chroma veritabanında PDF chunk’ları üzerinden en benzer içerikler aranır.  
3. Retrieval sonuçları generation modeline iletilir ve Türkçe yanıt üretilir.  
4. Yanıt, Gradio arayüzü üzerinden kullanıcıya sunulur.

---

## ⚙️ Kurulum ve Çalıştırma Kılavuzu

1. Repository'yi klonlayın:  
```bash
git clone https://github.com/nisakkaya/5S-KAIZEN-RAG-CHATBOT.git
cd proje_reposu


🏗 Çözüm Mimarisi

Pipeline Adımları:

Soru Alımı: Kullanıcı Gradio arayüzünden sorusunu girer.

Embedding & Retrieval: Sorular embedding modeline gönderilir ve PDF chunk’ları üzerinden en benzer içerikler getirilir.

Yanıt Üretimi: Retrieval sonuçları generation modeline iletilir ve yanıt üretilir.

Web Arayüzü: Üretilen yanıt Gradio üzerinden kullanıcıya sunulur.

Teknolojiler: Python, LangChain, Chroma, Google Gemini API, pdfplumber, Gradio

🌐 Web Arayüzü & Deploy

Arayüz: Gradio Blocks

Deploy Linki:



Kullanım Adımları:

Web sayfasına gidin.

Soru kutusuna sorularınızı yazın.

"🚀 Gönder" butonuna basın.

Chatbot yanıtını görüntüleyin.



