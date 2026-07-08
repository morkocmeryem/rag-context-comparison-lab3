# Step 3: Comparison of Results


## Amaç
Bu adımda, 1. ve 2. adımlarda elde edilen Gemini yanıtları, net değerlendirme kriterleri kullanılarak karşılaştırılır.


## Karşılaştırma

### 1. Doğruluk

Belge olmadan verilen cevaplar genel olarak doğruydu. Ancak bu cevaplar Gemini’nin genel AI bilgisine dayanıyordu ve doğrudan kurs PDF’iyle bağlantılı değildi.

Belge bağlamıyla verilen cevaplar ise yüklenen PDF’deki bilgilerle daha uyumluydu. Özellikle foundation model tanımı, pre-training, fine-tuning, RAG ve vertical AI gibi kavramlar ders materyaline daha yakın şekilde açıklandı.

### 2. Spesifiklik

Belgesiz cevaplar daha genel ve geniş kapsamlıydı. Gemini, GPT-4, Claude, BERT, PEFT ve LoRA gibi örnekler verdi. Bu örnekler konuyla ilgili olsa da doğrudan yüklenen PDF’e bağlı değildi.

Belgeyle verilen cevaplar daha spesifikti. Stanford HAI tanımı, RAG + Agent, Vector DB, general-purpose AI ve vertical AI gibi PDF’de geçen kavramlar kullanıldı.

### 3. Dayanak

Belgesiz cevaplarda net bir kaynak veya belge desteği yoktu. Model, kendi genel bilgisine göre açıklama yaptı.

Belge bağlamıyla verilen cevaplarda ise yanıtlar yüklenen kurs PDF’ine dayandırıldı. Bu nedenle cevapların hangi bilgiye göre üretildiği daha anlaşılır hale geldi.

### 4. Halüsinasyon Riski

Belge olmadan halüsinasyon riski daha yüksekti. Çünkü model, doğru gibi görünen ama belgeyle desteklenmeyen ek bilgiler verebilir.

Belge bağlamı kullanıldığında bu risk azaldı. Çünkü modelden yalnızca yüklenen PDF’e göre cevap vermesi istendi.

### 5. Güvenilirlik

Belgesiz cevaplar anlaşılır ve yararlıydı; ancak kurumsal kullanım için yeterince güvenilir değildi. Çünkü cevapların kaynağı açık değildi.

Belgeyle verilen cevaplar daha güvenilirdi. Çünkü yanıtlar belirli bir dokümana bağlıydı ve ders materyaliyle daha uyumluydu.

## Sonuç

Bu karşılaştırma, RAG mantığının AI cevaplarını daha güvenilir hale getirdiğini göstermektedir.

Belge bağlamı kullanıldığında cevaplar daha doğru, daha spesifik ve daha dayanaklı olur. Özellikle kurumsal kullanım senaryolarında bu önemlidir. Çünkü şirket politikaları, teknik dokümanlar, raporlar veya ürün bilgileri gibi konularda AI’ın genel tahminlere değil, güvenilir belgelere dayanarak cevap vermesi gerekir.

Bu nedenle belge bağlamı, halüsinasyon riskini azaltır ve AI yanıtlarının güvenilirliğini artırır.





