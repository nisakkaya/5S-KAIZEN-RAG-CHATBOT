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

1. Colab notebook’unuzu açın.  
2. Gerekli kütüphaneleri yükleyin:
```python
!pip install -q pdfplumber tqdm chromadb google-generativeai numpy langchain gradio





## **💡 Örnek Sorular (Basitten Zora)**


Bu sorular, chatbot’u test etmek ve 5S & Kaizen konusundaki bilgi tabanını göstermek için kullanılabilir.

### **Basit Sorular**
- 5S nedir?  
- Kaizen metodolojisi neyi amaçlar?  
- 5S’in adımları nelerdir?

### **Orta Seviye Sorular**
- 5S uygulamasında en sık yapılan hatalar nelerdir?  
- Kaizen felsefesini üretim süreçlerine nasıl entegre edebiliriz?  
- 5S ile iş yeri düzeni ve verimlilik arasındaki ilişki nedir?

### **Zorlayıcı Sorular**
- Kaizen ve 5S yöntemlerini aynı anda uygularken yaşanan çatışma noktaları nelerdir ve nasıl çözülür?  
- Bir fabrikanın mevcut süreçlerinde 5S ve Kaizen uygulamalarını optimize etmek için önerdiğiniz somut adımlar nelerdir?  
- 5S & Kaizen çerçevesinde bir çalışan motivasyon programı nasıl tasarlanır ve ölçümlenir?


## 🏗 **Çözüm Mimarisi**

**Pipeline Adımları:**

1. **Soru Alımı:** Kullanıcı Gradio arayüzünden sorusunu girer.  
2. **Embedding & Retrieval:** Sorular embedding modeline gönderilir ve PDF chunk’ları üzerinden en benzer içerikler getirilir.  
3. **Yanıt Üretimi:** Retrieval sonuçları generation modeline iletilir ve yanıt üretilir.  
4. **Web Arayüzü:** Üretilen yanıt Gradio üzerinden kullanıcıya sunulur.  

**Kullanılan Teknolojiler:**  
Google Colab, LangChain, Chroma, Google Gemini API, pdfplumber, Gradio

---

## 🌐 **Web Arayüzü & Deploy**

- **Arayüz:** Gradio Blocks  
- **Deploy Linki:** [Buraya deploy linkinizi ekleyin]

**Kullanım Adımları:**

1. Web sayfasına gidin.  
2. Soru kutusuna sorularınızı yazın.  
3. "🚀 Gönder" butonuna basın.  
4. Chatbot yanıtını görüntüleyin.






