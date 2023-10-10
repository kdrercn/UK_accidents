# Veri Seti için:

## https://www.kaggle.com/datasets/daveianhickey/2000-16-traffic-flow-england-scotland-wales/download?datasetVersionNumber=10
## Local UK Authorities data (uk_lad.geojson) : https://files.planning.data.gov.uk/dataset/local-authority-district.geojson

### Classification of injury severity using the CRaSH reporting system

## Sources : 

https://www.gov.uk/government/publications/guide-to-severity-adjustments-for-reported-road-casualty-statistics/guide-to-severity-adjustments-for-reported-road-casualties-great-britain

https://www.kaggle.com/datasets/tsiaras/uk-road-safety-accidents-and-vehicles

| Accident Severity | Database Value |
| ----------------- | -------------- |
| Killed | 1 |
| Serious | 2 |
| Slight | 3 |
 
*Table 3: Classification of injury severity using the CRaSH reporting system

| Injury in CRASH | Detailed severity | Severity classification |
| --------------- | ----------------- | ----------------------- |
| Deceased | Killed | Killed |
| Broken neck or back |	Very Serious | Serious |
| Severe head injury, unconscious | Very Serious | Serious |
| Severe chest injury, any difficulty breathing | Very Serious | Serious |
| Internal injuries | Very Serious | Serious |
| Multiple severe injuries, unconscious | Very Serious | Serious |
| Loss of arm or leg (or part)	| Moderately Serious | Serious |
| Fractured pelvis or upper leg	| Moderately Serious | Serious |
| Other chest injury (not bruising)	| Moderately Serious | Serious |
| Deep penetrating wound | Moderately Serious | Serious |
| Multiple severe injuries, conscious |Moderately Serious | Serious |
| Fractured lower leg / ankle / foot | Less Serious | Serious |
| Fractured arm / collarbone / hand	| Less Serious | Serious |
| Deep cuts / lacerations | Less Serious | Serious |
| Other head injury	| Less Serious | Serious |
| Whiplash or neck pain	| Slight | Slight |
| Shallow cuts / lacerations / abrasions | Slight | Slight |
| Sprains and strains | Slight | Slight |
| Bruising | Slight | Slight |
| Shock	| Slight |Slight |


**Işıklandırma**
--------------------
| Veri | Mapping |
| --------------- | ----------------- | 
| Daylight: Street light present | 0 | 
| Darkness: Street lights present and lit |1 | 
| Darkness: Street lighting unknown | 2 |
| Darkness: Street lights present but unlit | 2 |
| Darkeness: No street lighting | 2 |

**Hava Durumu**
----------------
| Veri | Mapping |
| --------------- | ----------------- | 
| Raining without high winds | No High winds | 
| Fine without high winds | No High winds | 
| Snowing without high winds | No High winds |
| Other | No High winds |
| Fine with high winds | High winds |
| Raining with high winds | High winds |
| Fog or mist | Fog |
| Snowing with high winds | High winds |

| Veri | Mapping |
| --------------- | ----------------- | 
| No High wind | 0 |
| High winds | 2 |
| Fog | 0 |
| Unknown | 0 |

**Yol Yüzey Durumu**
----------------

| Veri | Mapping |
| --------------- | ----------------- | 
| Dry | 5 |
| Wet/Damp | 4 |
| Frost/Ice | 3 |
| Snow | 2 |
| Flood (Over 3cm of water) | 1 |
| Not Specified | 0 |

***Algoritmalar***
------------------
**Jenks Natural Breaks**
------------------
Jenks Natural Breaks ya da Jenks Natural Breaks Sınıflandırma Metodu, veri değerlerini farklı sınıflara en iyi şekilde kümelemek için tasarlanmıştır.

Metod bu işlemi her sınıfın diğer sınıfların ortalamasından sapmasını maksimuma çıkarırken, her sınıfın sınıf  ortalamasından ortalama sapmasını en aza indirmeye çalışarak yapar.

**Apriori Algoritması**
------------------
Bu algoritma temelinde iteratif (tekrarlayan) bir niteliğe sahiptir ve hareket bilgileri içeren veri tabanlarında sık geçen öğe kümelerinin keşfedilmesinde kullanılır.

Birliktelik kuralı madenciliği, tüm sık geçen öğelerin bulunması ve sık geçen bu öğelerden güçlü birliktelik kurallarının üretilmesi olmak üzere iki aşamalıdır.

**ECLAT Algoritması**
------------------
Apriori algoritması ile benzer çalışır. Apriori algoritmasında eleman bazlı işlem (alışveriş sepetindeki ürün 1,2,3 gibi) yapılır ancak Eclat algoritmasında elemanların geçtiği kayıtlar ( alışveriş sepeti 100,200,.. ) baz alınır. Apriori yöntemine göre daha küçük veri setleri için uygundur. Apriori algoritmasına göre çok hızlıdır.

# UK_accidents logs

03.10.2023:
    
    Üzerinde çalışılacak olan veri seti belirlendi: "UK Accidents 2005 to 2014". 

    Veri seti üzerinde incelemeler yapıldı: Ayrı olan veriler birleştirildi. Kaç veri var?, veri tipleri ne?, hangi veriler boş ya da sıfır? sorguları soruldu.

04.10.2023:
    
    Veri temizlemeleri yapıldı: Tekrarlayan veriler silindi, boş veriler ya silindi ya da yerlerine "belirtilmemiş" gibi değerler girildi.

    Temizlenen veri setinde görselleştirme yapılarak veri anlamlandırıldı.

05.10.2023:

    Veri görselleştirmedeki hatalar düzeltildi. Bir kaç tane daha grafik görselleştirme eklendi.

    Kaza noktaları harita üzerine yerleştirildi. Harita görselleştirmeleri yapıldı.

    Veri setinden bir bölge üzerinde K-Means ve DBSCAN ile kümeleme işlemleri yapıldı ve görselleştirildi.

06.10.2023:

    Kümeleme görselleştirmeleri kullanıcının gireceği şehir adıyla oluşturuldu.

    Jenks Natural Breaks, Apriori ve ECLAT algoritması hakkında bilgi edinildi.

09.10.2023:

    Önceki yapılan işlemler kontrol edildi ve eklemeler yapıldı.

    Korelasyon ve algoritma işlemleri için One Hot Encoding yapıldı.

10.10.2023:

    Yazılan kodların okunabilirliği arttırıldı.

    Outlier veriler tespit edildi.

    Apriori, FP Growth algoritmalarına veri seti üzerinde giriş yapıldı.
    
