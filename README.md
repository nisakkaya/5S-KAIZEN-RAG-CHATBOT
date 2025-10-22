💬 5S & Kaizen Öğretici Chatbot – Akbank GenAI Bootcamp
🚀 Projenin Amacı

Bu proje, RAG (Retrieval Augmented Generation) mimarisi kullanarak kullanıcı sorularına doğru ve bağlamsal yanıtlar üretebilen bir chatbot geliştirmeyi amaçlamaktadır.
Amaç, 5S ve Kaizen metodolojileri ile ilgili bilgileri dinamik ve güvenilir bir şekilde sunabilen dijital bir asistan oluşturmaktır.

📄 Veri Seti Hakkında

Kaynak: Kaizen Institute – The Ultimate Guide to 5S and 5S Training (KAIZEN™ Article)

Dil: İngilizce

Kapsam: 5S adımları, uygulama yöntemleri, Kaizen felsefesi ve iş yeri verimliliği üzerine detaylı açıklamalar

İşleme Süreci:

Web sitesinden alınan İngilizce içerik .pdf formatına dönüştürüldü.

Dosya Google Drive üzerinde saklandı.

Chatbot, PDF içerisindeki metni chunk’lara ayırarak embedding modeli üzerinden vektör veritabanına aktardı.

Kullanıcı Türkçe soru sorduğunda, sistem İngilizce içerikten ilgili bilgileri getirip Türkçe olarak yanıt üretiyor.

📚 Kaynak Güvenilirliği:
Veri kaynağı, Kaizen felsefesinin resmi temsilcisi olan Kaizen Institute (https://kaizen.com
) sitesinden alınmıştır.
Bu kurum, Kaizen metodolojisinin kurucusu Masaaki Imai tarafından 1985’te kurulmuş olup, 5S ve sürekli iyileştirme alanında dünya çapında en güvenilir otoritedir.
Bu nedenle veri seti akademik ve kurumsal olarak güvenilir kabul edilmektedir.

⚠️ Not: PDF dosyası ve API anahtarı (Google Gemini) GitHub deposuna dahil edilmemiştir.
Kod çalıştırıldığında, PDF dosyasının Colab veya lokal ortamda erişilebilir olması gerekmektedir.

🛠 Kullanılan Yöntemler ve Teknolojiler

Generation Model: Google Gemini API (gemini-2.5-flash)

Embedding Model: Google Generative AI Embeddings (text-embedding-004)

Vektör Veritabanı: Chroma (./chroma_db)

Framework: LangChain + Google Generative AI API

Arayüz: Gradio

🔄 Pipeline Özeti

Kullanıcı sorusu embedding modeli ile vektöre dönüştürülür.

Chroma veritabanında PDF parçaları üzerinden en benzer içerikler aranır.

Elde edilen bağlam, Gemini modeline aktarılır ve Türkçe yanıt üretilir.

Sonuç, Gradio arayüzü üzerinden kullanıcıya sunulur.

⚙️ Kurulum ve Çalıştırma Kılavuzu

Google Colab notebook’unuzu açın.

Gerekli kütüphaneleri yükleyin:

!pip install -q pdfplumber tqdm chromadb google-generativeai numpy langchain gradio


PDF dosyanızı Google Drive’a yükleyin ve kodda dosya yolunu belirtin.

Notebook’u çalıştırarak chatbot arayüzünü başlatın.

💡 Örnek Sorular (Basitten Zora)

Bu sorular, chatbot’u test etmek ve 5S & Kaizen bilgi tabanını göstermek için kullanılabilir.

Basit Sorular

5S nedir?

Kaizen metodolojisi neyi amaçlar?

5S’in adımları nelerdir?

Orta Seviye Sorular

5S uygulamasında en sık yapılan hatalar nelerdir?

Kaizen felsefesini üretim süreçlerine nasıl entegre edebiliriz?

5S ile iş yeri düzeni ve verimlilik arasındaki ilişki nedir?

Zorlayıcı Sorular

Kaizen ve 5S yöntemlerini aynı anda uygularken yaşanan çatışma noktaları nelerdir ve nasıl çözülür?

Bir fabrikanın mevcut süreçlerinde 5S ve Kaizen uygulamalarını optimize etmek için hangi somut adımlar atılabilir?

5S & Kaizen çerçevesinde bir çalışan motivasyon programı nasıl tasarlanır ve ölçümlenir?

🏗 Çözüm Mimarisi
Pipeline Adımları

Soru Alımı: Kullanıcı Gradio arayüzünden sorusunu girer.

Embedding & Retrieval: Soru embedding modeline gönderilir ve PDF’ten en benzer içerikler getirilir.

Yanıt Üretimi: Retrieval sonuçları Gemini modeline iletilir ve Türkçe yanıt üretilir.

Arayüz: Yanıt Gradio ekranında kullanıcıya sunulur.

Kullanılan Teknolojiler:
Google Colab, LangChain, Chroma, Google Gemini API, pdfplumber, Gradio

🌐 Web Arayüzü & Deploy

Arayüz: Gradio Blocks

Deploy Linki: https://huggingface.co/spaces/nisakkaya/5S-CHATBOT-NISA linkten chatbotuma ualaşabilirsiniz.

Kullanım Adımları:

Web sayfasına gidin.

Soru kutusuna sorularınızı yazın.

“🚀 Gönder” butonuna basın.

Chatbot’un yanıtını görüntüleyin.

📊 Elde Edilen Sonuçlar

Bu projede geliştirdiğimiz RAG tabanlı chatbot ile 5S ve Kaizen içerikli PDF veri setinden bilgi çekerek kullanıcı sorularına bağlamsal ve doğru yanıtlar üretebiliyoruz.

✅ Bağlamsal Yanıt Üretimi: PDF içeriği üzerinden doğru bilgiye dayalı yanıtlar.

✅ Doğru ve Hedefe Yönelik Bilgi: Her seviyeden soruya uygun açıklamalar.

✅ Hızlı ve Etkileşimli Deneyim: Gradio arayüzü ile anında yanıt.

✅ Kolay Deploy: Colab veya Hugging Face Spaces üzerinde kolay erişim.

✅ Ölçeklenebilir Mimari: Yeni PDF’ler ve kaynaklar eklenerek kolay genişleme.

💡 Özetle: Bu proje hem eğitsel bir araç hem de 5S & Kaizen bilgi tabanı olarak kullanılabilir.
Kullanıcılar sorularına doğru, hızlı ve bağlamsal yanıtlar alarak gerçek bir dijital asistan deneyimi yaşar.



