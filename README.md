# 5S-KAIZEN-RAG-CHATBOT
# 5S & Kaizen Öğretici Chatbot – Akbank GenAI Bootcamp

## Projenin Amacı
Bu proje, RAG (Retrieval Augmented Generation) mimarisi kullanarak kullanıcı sorularına doğru ve bağlamsal yanıtlar üretebilen bir chatbot geliştirmeyi hedeflemektedir. Amaç, 5S ve Kaizen metodolojisi ile ilgili bilgileri dinamik olarak sağlayabilen bir sistem oluşturmaktır.

## Veri Seti Hakkında
Proje kapsamında kullanılan veri seti: **GAIH GenAI Bootcamp Proje Dosyası.pdf**  
- Veri formatı: PDF  
- İçerik: 5S ve Kaizen uygulamaları ile ilgili dokümanlar  
- Kullanım: Chatbot, kullanıcı sorularına yanıt üretmek için PDF içeriğini referans olarak kullanır  

> Not: Veri seti repoya eklenmemiştir. Kod çalıştırıldığında PDF dosyası Colab veya lokal ortamda kullanılabilir.

## Kullanılan Yöntemler
- **Generation Model:** Google Gemini API (gemini-2.5-flash)  
- **Embedding Model:** Google Generative AI Embeddings (text-embedding-004)  
- **Vektör Veritabanı:** Chroma (persist directory: `./chroma_db`)  
- **RAG Pipeline Framework:** LangChain / Google Generative AI API  

**Pipeline Özeti:**  
1. Kullanıcının sorusu embedding modeli ile vektöre dönüştürülür.  
2. Chroma veritabanında en benzer PDF chunk’ları aranır (retrieval).  
3. Elde edilen içerikler generation modeline iletilir ve yanıt üretilir.  
4. Sonuç, Gradio arayüzü üzerinden kullanıcıya gösterilir.

## Kurulum ve Çalıştırma Kılavuzu
1. Repository'yi klonlayın:  
```bash
git clone https://github.com/nisakkaya/5S-KAIZEN-RAG-CHATBOT.git
cd proje_reposu
