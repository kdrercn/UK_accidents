# Veri Seti için:

## https://www.kaggle.com/datasets/daveianhickey/2000-16-traffic-flow-england-scotland-wales/download?datasetVersionNumber=10
## Local UK Authorities data (uk_lad.geojson) : https://files.planning.data.gov.uk/dataset/local-authority-district.geojson

## Source : https://www.gov.uk/government/publications/guide-to-severity-adjustments-for-reported-road-casualty-statistics/guide-to-severity-adjustments-for-reported-road-casualties-great-britain

### Classification of injury severity using the CRaSH reporting system

| Accident Severity | Database Value |
| Killed | 1 |
| Serious | 2 |
| Slight | 3 |
 
*Table 3: Classification of injury severity using the CRaSH reporting system

| Injury in CRASH | Detailed severity | Severity classification |
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

# UK_accidents

03.10.2023:
    
    Üzerinde çalışılacak olan veri seti belirlendi: "UK Accidents 2005 to 2014". 

    Veri seti üzerinde incelemeler yapıldı: Ayrı olan veriler birleştirildi. Kaç veri var?, veri tipleri ne?, hangi veriler boş ya da sıfır? sorguları soruldu.

04.10.2023:
    
    Veri temizlemeleri yapıldı: Tekrarlayan veriler silindi, boş veriler ya silindi ya da yerlerine "belirtilmemiş" gibi değerler girildi.

    Temizlenen veri setinde görselleştirme yapılarak veri anlamlandırıldı.
     