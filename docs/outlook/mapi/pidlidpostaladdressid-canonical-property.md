---
title: PidLidPostalAddressId 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPostalAddressId
api_type:
- COM
ms.assetid: 30fdfb20-1e12-442a-bfa0-8c18c15fa5c3
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 83f3c0559a3317de3789f8c93d024f08ada3e735
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315996"
---
# <a name="pidlidpostaladdressid-canonical-property"></a>PidLidPostalAddressId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先の郵送先住所である物理アドレスを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidPostalAddressId  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008022  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

存在する場合、このプロパティには、以下の表または [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定されている値のいずれかを指定する必要があります。 設定しない場合、アプリケーションは値が "0x00000000" と見な0x00000000。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |郵送先住所としてアドレスが選択されません。 **PR_STREET_ADDRESS** ([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md)) 、 PR_LOCALITY ([PidTagLocality](pidtaglocality-canonical-property.md)) 、 **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md)) 、 **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md)) 、 **PR_COUNTRY** ([PidTagCountry](pidtagcountry-canonical-property.md)) 、 **dispidAddressCountryCode** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)) 、 および **PR_POSTAL_ADDRESS** **(** [PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) はすべて設定する必要があります。  <br/> |
|0x00000001  <br/> |ホーム アドレスは、郵送先アドレスです。 **PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**( PR_POST_OFFICE_BOX [PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md)) 、 **PR_COUNTRY**、 **dispidAddressCountryCode**、 および **PR_POSTAL_ADDRESS** プロパティの値は、 PR_HOME_ADDRESS_STREET **(** [PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md) **)** 、 PR_HOME_ADDRESS_CITY ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md)) 、 **PR_HOME_ADDRESS_STATE_OR_PROVINCE** ( PidTagHomeAddressCity ) の値と等しくする必要があります。TagHomeAddressStateOrProvince )、PR_HOME_ADDRESS_POSTAL_CODE [(PidTagHomeAddressPostalCode)、PR_HOME_ADDRESS_POST_OFFICE_BOX](pidtaghomeaddresspostalcode-canonical-property.md)[](pidtaghomeaddressstateorprovince-canonical-property.md)  (PidTagHomeAddressPostOfficeBox)、PR_HOME_ADDRESS_COUNTRY [](pidtaghomeaddresspostofficebox-canonical-property.md)[(PidTagHomeAddressCountry)、dispidHomeAddressCountryCode](pidtaghomeaddresscountry-canonical-property.md)[(PidLidHomeAddressCountryCode)、](pidlidhomeaddresscountrycode-canonical-property.md)および **dispidHomeAddress** ([PidLidHomeAddress](pidlidhomeaddress-canonical-property.md)) プロパティをそれぞれ示します。     <br/> |
|0x00000002  <br/> |ワーク アドレスは、郵送先アドレスです。 **PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 PR_POST_OFFICE_BOX 、 **PR_COUNTRY**、 **dispidAddressCountryCode**、 および **PR_POSTAL_ADDRESS** プロパティの値は [、dispidWorkAddressStreet ( PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)) **、dispidWorkAddressCity** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md)) **、dispidWorkAddress** ( PiAdDressCity ) の値と等しくする [必要があります。dressState](pidlidworkaddressstate-canonical-property.md)  **)、dispidWorkAddressPostalCode** [(PidLidWorkAddressPostalCode)、dispidWorkAddressPostOfficeBox](pidlidworkaddresspostalcode-canonical-property.md)  (PidLidWorkAddressPostOfficeBox)、dispidWorkAddressCountry [(PidLidWorkAddressCountry)](pidlidworkaddresscountry-canonical-property.md) **、dispidWorkAddressCountryCode** [(PidLidWorkAddressCountryCode)、](pidlidworkaddresscountrycode-canonical-property.md)および **dispidWorkAddress** [(PidLidWorkAddress)](pidlidworkaddress-canonical-property.md)プロパティをそれぞれ示します。[](pidlidworkaddresspostofficebox-canonical-property.md)   <br/> |
|0x00000003  <br/> |その他のアドレスは、郵送先アドレスです。 PR_STREET_ADDRESS 、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 PR_POST_OFFICE_BOX 、  **PR_COUNTRY**、 **dispidAddressCountryCode**、 および **PR_POSTAL_ADDRESS** プロパティの値は **、PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md)) 、PR_OTHER_ADDRESS_CITY ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md)) の値と等しくする必要があります。 **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** ([PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md)) 、 **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md)) 、 **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md)) 、 **dispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)) 、**および dispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) プロパティ、 それぞれ。   <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先と個人用配布リストで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

