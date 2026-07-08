### Step 1: Without Documents

## Amaç
Bu adımda, Gemini’ye herhangi bir belge yüklenmeden veya belgeye atıfta bulunulmadan sorular soruldu.  
Amaç, modelin yalnızca genel bilgisini kullanarak nasıl yanıt verdiğini gözlemlemekti.

## Prompt I used

1. Temel model nedir ve farklı alt görevlere nasıl uyarlanabilir?

2. Genel amaçlı yapay zeka ile dikey yapay zeka arasındaki temel farklar nelerdir?

3. Kurumsal yapay zeka kullanım senaryolarında halüsinasyon riski neden önemlidir ve belgeye dayandırma güvenilirliği nasıl artırabilir?

Lütfen açık ve öz bir şekilde cevap verin.

### Gemini'nin Yanıtı

## 1. Temel Model (Foundation Model) Nedir ve Nasıl Uyarlanır?

Temel Model, devasa miktarda veri üzerinde, genellikle gözetimsiz veya yarı gözetimli öğrenme yöntemleriyle eğitilmiş, çok amaçlı büyük yapay zeka modelleridir (Örn: GPT-4, Claude, BERT). Bu modeller doğrudan tek bir iş için değil, genel bir dil veya örüntü anlayışı kazanması için eğitilirler.

Bu genel modeller, farklı alt görevlere (downstream tasks) şu yöntemlerle uyarlanır:

* İnce Ayar (Fine-Tuning):** Modelin mevcut ağırlıklarını, belirli bir alana ait (örneğin hukuk veya tıp) daha küçük ve özelleştirilmiş bir veri setiyle yeniden eğiterek o alanda uzmanlaşmasını sağlamak.
* Parametre Verimli İnce Ayar (PEFT / LoRA):** Modelin ana ağırlıklarını dondurup, sadece araya eklenen küçük ve eğitilebilir katmanları güncelleyerek maliyetsiz bir şekilde optimize etmek.
* İpucu Mühendisliği (Prompt Engineering):** Modelin ağırlıklarını hiç değiştirmeden, girdiye (prompt) net talimatlar, kurallar veya örnekler (Few-shot learning) ekleyerek modeli anlık olarak yönlendirmek.

## 2. Genel Amaçlı Yapay Zeka vs. Dikey Yapay Zeka

Bu iki yaklaşım, yapay zekanın "kapsamı" ve "derinliği" arasındaki farkı temsil eder.

| Özellik | Genel Amaçlı Yapay Zeka (General-Purpose AI) | Dikey Yapay Zeka (Vertical AI) |
| --- | --- | --- |
| **Kapsam** | Geniştir; şiir yazmaktan kodlamaya kadar her şeyi yapabilir. | Dardır; sadece belirli bir sektöre veya iş akışına odaklanır. |
| **Veri Kaynağı** | İnternetteki genel ve açık kaynaklı verilerle eğitilir. | Sektöre özel, tescilli ve derinlemesine verilerle eğitilir. |
| **Kullanım Amacı** | İsviçre çakısı gibidir; esneklik ve yaratıcılık gerektiren işler. | Lazer gibidir; radyoloji raporu analizi veya sözleşme incelemesi. |
| **Başarı Kriteri** | Farklı görevlere hızlıca uyum sağlayabilmesi. | Kendi niş alanında hatasız ve uzman seviyesinde çalışması. |


## 3. Kurumsal Yapay Zeka ve Halüsinasyon Riski

Halüsinasyon, bir yapay zeka modelinin kulağa son derece mantıklı gelen ancak tamamen uydurma veya yanlış olan bilgiler üretmesidir.

Kurumsal Dünyada Halüsinasyon Neden Önemlidir?

Bireysel kullanımda bir yapay zekanın yanlış bir tarihi hatırlaması önemsiz olabilir. Ancak kurumsal senaryolarda halüsinasyon; **maddi kayıplara**, **yasal sorumluluklara (hukuki davalar)** ve en önemlisi **marka itibarının zedelenmesine** yol açar. Bir bankacılık yapay zekasının yanlış bir faiz oranı söylemesi veya bir medikal yapay zekanın yanlış dozaj önermesi tolere edilemez.

Belgeye Dayandırma (Grounding / RAG) Güvenilirliği Nasıl Artırır?

Belgeye dayandırma —genellikle RAG (Retrieval-Augmented Generation / Veri Geri Getirmeyle Artırılmış Üretim)** mimarisiyle yapılır— yapay zekanın sadece kendi "hafızasına" güvenmesini engeller.

Süreç şu şekilde işler ve güvenilirliği artırır:

1. Doğruluk Zinciri:Kullanıcı bir soru sorduğunda, sistem önce şirketin güvenilir iç kaynaklarında (PDF'ler, veri tabanları, kılavuzlar) arama yapar.
2. Sınırlandırma:Bulunan doğru bilgi (bağlam/context) yapay zekaya iletilir ve modele *"Sadece bu belgelere sadık kalarak cevap ver, dışına çıkma"* talimatı verilir.
3. Sonuç:Model yaratıcılığını sıfırlayarak bir "arama ve özetleme" motoru gibi çalışır. Bu da halüsinasyon riskini neredeyse tamamen ortadan kaldırır ve verilen cevapların kaynağının (referansının) gösterilebilmesini sağlar.




