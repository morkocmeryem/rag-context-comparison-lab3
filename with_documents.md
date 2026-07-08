# 2. Adım: With Document Context

## Amaç
Bu adımda, kurs PDF’si yüklendikten sonra aynı sorular tekrar soruldu.  
Amaç, belge bağlamının cevapları daha spesifik, temellendirilmiş ve güvenilir hale getirip getirmediğini gözlemlemekti.

## Prompt I use

Yalnızca yüklenen kurs PDF'sini kullanarak aşağıdaki soruları yanıtlayın:

1. Temel model nedir ve farklı alt görevlere nasıl uyarlanabilir?

2. Genel amaçlı yapay zeka ile dikey yapay zeka arasındaki temel farklar nelerdir?

3. Kurumsal AI kullanım senaryolarında halüsinasyon riski neden önemlidir ve belgeye dayandırma güvenilirliği nasıl artırabilir?

Önemli:
- Cevaplarınızı yalnızca yüklenen belgeye dayandırın.
- Cevap belgede bulunmuyorsa, belgede mevcut olmadığını belirtin.
- Mümkün olduğunda belgeye dayalı ayrıntılara değinin.

## Gemini Yanıtı
Yüklenen kurs belgesinde yer alan bilgilere göre sorularınızın yanıtları aşağıdadır:

# 1. Temel Model (Foundation Model) Nedir ve Farklı Alt Görevlere Nasıl Uyarlanabilir?

Tanımı: Stanford HAI kaynaklarına göre temel model; büyük ölçekte (genellikle kendi kendine denetim / self-supervision yöntemiyle) geniş kapsamlı veriler üzerinde eğitilmiş ve çok çeşitli alt görevlere (downstream tasks) uyarlanabilen modellerdir.
Temel Mekanizması: Süreç, tabanın oluşturulduğu "Ön Eğitim" (Pre-training) ile başlar ve ardından belirli görevlere uyarlamanın yapıldığı aşamalarla devam eder.
Alt Görevlere/Uygulamalara Uyarlanma Yöntemleri:Belgeye göre modeller, neyin değiştirilmek istendiğine bağlı olarak dört farklı stratejiyle uyarlanabilir:


1. Doğrudan Kullanım (API): Modelin çağrılma şeklini değiştirir; hızlı görevler ve genel üretkenlik sağlamak amacıyla doğrudan istemler (prompt) üzerinden yürütülür.
2. İnce Ayar (Fine-Tuning):Modelin davranış şeklini değiştirir; modeli sıfırdan inşa etmek yerine alana özgü verilerle eğiterek belirli bir göreve, kurumsal kurallara veya tutarlı bir tona göre ayarlar.
3. RAG (Veri Geri Getirmeyle Artırılmış Üretim): Modelin ne bildiğini genişletir; modele harici kaynaklardan doğru ve güncel bilgi aktarımı sağlar.
4. RAG + Ajan (Agent):Modelin ne bildiğini ve ne yapabildiğini genişletir; araçları çağırabilen ve çok adımlı iş akışlarını/otomasyonları yürütebilen sistemler kurmak için uygulanır.


# 2. Genel Amaçlı Yapay Zeka ile Dikey Yapay Zeka Arasındaki Temel Farklar Nelerdir?

Belgede iki yaklaşım arasındaki farklar net bir tablo ile şu şekilde kategorize edilmiştir:

Bilgi Kapsamı (Knowledge Scope): Genel amaçlı yapay zeka birçok alanda geniş ve genel bir bilgiye (Vikipedi benzeri) sahipken; dikey yapay zeka derin ve sektöre/alana özgü bir uzmanlığa (uzman benzeri) sahiptir.
Birincil Veri Kaynağı (Primary Data Source): Genel amaçlı yapay zeka büyük ölçekli kamuya açık internet verileriyle eğitilirken; dikey yapay zeka şirkete özel, tescilli, denetlenen ve sektöre özgü verileri kaynak alır.
Temel Güçlü Yön (Core Strength):Genel amaçlı yapay zekanın gücü çok yönlülük, yaratıcılık ve doğal dil akıcılığı iken; dikey yapay zekanın gücü yüksek hassasiyet, tutarlılık ve alan doğruluğudur.
Kritik Faktör (Critical Factor): Genel amaçlı yapay zekada halüsinasyon veya olgusal belirsizlik riski daha yüksektir; dikey yapay zeka ise sıkı uyumluluk, doğrulama ve uzman hizalaması gerektirir.


# 3. Kurumsal Yapay Zeka Kullanım Senaryolarında Halüsinasyon Riski Neden Önemlidir ve Belgeye Dayandırma Güvenilirliği Nasıl Artırabilir?

Halüsinasyonun Nedeni: Yapay zekanın bir "Olgu Denetleyicisi" (Fact Checker) değil, "Olasılıksal Metin Tamamlayıcısı" (Probabilistic Text Completer) olmasından kaynaklanır. Model bir gerçeği bilmediğinde, sadece gerçek bir atıf modeline benzediği için sahte kaynaklar uydurmak gibi "en makul görünen" kelime dizilimlerini üretir.
Kurumsal Senaryolarda Neden Önemlidir:Kurumsal iş akışlarında bağlamdan bağımsız (context-free) yapay zeka yanıtlarının yapısal sınırları ve yetersizlikleri vardır. Yanlış strateji seçimi veya halüsinasyonlar; istikrarsız sonuçlara, gereksiz maliyetlere ve operasyonel karmaşıklıklara yol açar. Özellikle mevzuatlar, düzenlemeler veya ürün verileri gibi sürekli güncellenen ya da hassas bilgi içeren kurumsal senaryolarda yapay zekanın hata yapmaması ve güvenilir olması kritik bir gereksinimdir.
Belgeye Dayandırmanın (Grounding / RAG) Güvenilirliği Artırma Yolu: Belgeye dayandırma, modeli yalnızca harici kaynaklara bağlı kalarak cevap vermeye zorlar. Bu doğrultuda RAG (Retrieval-Augmented Generation) mimarisi şu adımlarla güvenilirliği artırır:


1. Kullanıcı sorgusu alınır.
2. Kelimelerin tam eşleşmesine değil, anlamsal benzerliğine göre arama yapan bir Vektör Veri Tabanından (Vector DB) ilgili kurumsal belgeler getirilir.
3. Getirilen bu net ve doğru belgelerle yeni bir bilgi istemi (prompt) inşa edilir.
4. Büyük dil modeli (LLM), kendi hafızasından uydurmak yerine yalnızca kendisine sunulan bu bağlamı (context) kullanarak doğrulanabilir, dayanağı olan yanıtlar üretir. Bu sayede model yeniden eğitilmeye gerek kalmadan bilgiye dayalı görevlerde halüsinasyon riski büyük ölçüde azaltılmış olur.
