<img width="5299" height="4618" alt="Untitled diagram-2026-01-01-134606" src="https://github.com/user-attachments/assets/dc179a44-e010-4f70-b1c4-cddc6340e486" /># KARAKAM: AI Based Next-Gen Android Malware Analysis Platform

KARAKAM, Android zararlı yazılımlarını tespit etmek için statik analiz, ağ keşfi ve tehdit istihbaratını otonom bir mimaride birleştiren, yapay zeka destekli bir analiz platformudur.

<img width="829" height="990" alt="image" src="https://github.com/user-attachments/assets/b601639d-aed9-4049-88eb-4da4a537c9f0" />


## 🚀 Özellikler

- **Hibrit Analiz:** MobSF (Statik), Subfinder (Network) ve VirusTotal (Intelligence) verilerini birleştirir.
- **Özel Eğitilmiş LLM:** Llama-3.1 8B üzerine siber güvenlik odaklı Fine-Tune edilmiş **Karakam-AI** karar mekanizması.
- **Otonom Karar:** Teknik verileri yorumlayarak BENIGN, SUSPICIOUS veya MALICIOUS sonuçları üretir.
- **Veri Gizliliği:** GGUF ve Ollama desteği sayesinde tamamen yerel (on-premise) çalışma imkanı.
- **Detaylı Raporlama:** Excel formatında toplu analiz çıktısı ve MITRE ATT&CK uyumlu teknik gerekçelendirme.

## 🛠 Mimari Yapı

Uygulama, yüksek performans için **FastAPI** asenkron mimarisi üzerine inşa edilmiştir.


<img width="5299" height="4618" alt="Untitled diagram-2026-01-01-134606" src="https://github.com/user-attachments/assets/a1181345-12e4-41df-90a3-39a80c910de6" />

### Bileşenler

- **Static Analysis:** MobSF API entegrasyonu ile izin ve API çağrısı analizi.
- **Reconnaissance:** Docker üzerinde çalışan Subfinder ile pasif subdomain keşfi.
- **AI Engine:** Hugging Face üzerinde yayınlanan [Karakam-Llama3.1-8B](https://huggingface.co/TolgaTD/karakam-llama3.1-8b-gguf) modeli.

## 🔧 Kurulum

### 1. Gereksinimler

- Python 3.9+
- Docker (Subfinder ve MobSF için)
- Ollama (Modeli yerel çalıştırmak için)
- MobSF Docker Version
- Subfinder Docker Version

### 2. Modeli Hazırlama

Modeli Hugging Face'den indirin ve Ollama ile ayağa kaldırın:

```bash
# Modeli Hugging Face'den indir (veya GGUF dosyasını proje dizinine koy)
# Modelfile oluştur ve modeli build et:
ollama create karakam-ai -f Modelfile
3. Uygulamayı Çalıştırma
Gerekli paketleri yükleyin ve sunucuyu başlatın:

Bash

pip install -r requirements.txt
uvicorn app:app --reload
📊 Ekran Görüntüleri
AI Analiz Sonuçları
<img width="782" height="411" alt="image" src="https://github.com/user-attachments/assets/7f957496-ef81-4a9a-a255-8ee2e56e6c7c" />


İşlenmemiş Uygulama Verileri
<img width="784" height="546" alt="image" src="https://github.com/user-attachments/assets/33e27c02-2ab5-419e-8a9a-f35b470080ab" />


📜 Teşekkür ve Atıflar (Acknowledgements)
Bu projenin hayata geçmesinde katkısı olan kişi ve kurumlara teşekkürlerimizi sunarız:

Akademik Danışmanlık: Proje sürecindeki rehberliği için Prof. Dr. İbrahim Alper DOĞRU'ya teşekkürlerimizi sunarız.

Veri ve Altyapı Desteği:

🛡️ VirusTotal: Akademik araştırmamız için altyapılarını açarak sağladıkları Premium API Key desteği sayesinde tehdit istihbaratı ağımız güçlenmiştir. Destekleri için teşekkür ederiz.

📦 AndroZoo: Geniş ölçekli zararlı yazılım veri setine erişimimiz adına sağladıkları API desteği için teşekkür ederiz.

Açık Kaynak Projeler:

🔍 MobSF & JADX: Statik analiz ve tersine mühendislik süreçlerindeki mükemmel araçları için teşekkür ederiz.

🌐 Subfinder (ProjectDiscovery): Ağ keşif yeteneklerimizi borçlu olduğumuz hızlı ve etkili araçları için teşekkür ederiz.

📄 Lisans
Bu proje akademik kullanım şartlarına tabidir.

Yazar: Tolga Demirel

Kurum: Gazi Üniversitesi, Bilgisayar Mühendisliği Bölümü (2026)
