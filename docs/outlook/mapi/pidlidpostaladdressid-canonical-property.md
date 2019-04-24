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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 83f3c0559a3317de3789f8c93d024f08ada3e735
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315996"
---
# <a name="pidlidpostaladdressid-canonical-property"></a>PidLidPostalAddressId 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先の郵送先住所にする物理的な住所を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidPostalAddressId  <br/> |
|プロパティセット:  <br/> |PSETID_Address  <br/> |
|ロング ID (LID):  <br/> |0x00008022  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |連絡先  <br/> |
   
## <a name="remarks"></a>解説

このプロパティが指定されている場合、このプロパティには、次の表に示す値のいずれか、または[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定する必要があります。 設定されていない場合、アプリケーションは、値が "0x00000000" であると想定する必要があります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |住所が郵送先住所として選択されていません。 **PR_STREET_ADDRESS**([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md))、 **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))、 **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md))、 **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md))、 **PR_COUNTRY** ([PidTagCountry](pidtagcountry-canonical-property.md))、 **dispidAddressCountryCode** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md))、および**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) を設定することはできません。  <br/> |
|0x00000001  <br/> |自宅住所は郵送先住所です。 **PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md))、 **PR_COUNTRY**、dispidAddressCountryCode の値。 ****、 **PR_POSTAL_ADDRESS**プロパティは、 **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md))、 **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md))、PR_HOME_ の値と等しくなければなりません。 **ADDRESS_STATE_OR_PROVINCE** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md))、 **PR_HOME_ADDRESS_POSTAL_CODE** ([PidTagHomeAddressPostalCode](pidtaghomeaddresspostalcode-canonical-property.md))、 **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md))、 **PR_HOME_ADDRESS_COUNTRY** ([PidTagHomeAddressCountry](pidtaghomeaddresscountry-canonical-property.md))、 **dispidHomeAddressCountryCode** ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md))、および**dispidホームアドレス**([PidLidHomeAddress](pidlidhomeaddress-canonical-property.md))プロパティ、それぞれ。  <br/> |
|0x00000002  <br/> |勤務先の住所は郵送先住所です。 **PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 **PR_POST_OFFICE_BOX**、 **PR_COUNTRY**、 **dispidAddressCountryCode**、および PR_POSTAL_ADDRESS の値**** プロパティは、 **dispidwork addressストリート**([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md)) の値、 **dispidwork addresscdisp(** [PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md))、 **dispidwork addressstate** ([PidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md))、 **dispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md))、 **dispidWorkAddressPostOfficeBox** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md))、 **dispidwork addresscountry**([PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md))、 **dispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md))、および**dispidwork address** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md)) の各プロパティをそれぞれ表します。  <br/> |
|0x00000003  <br/> |もう1つは郵送先住所の住所です。 、 **PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 **PR_POST_OFFICE_BOX**、 **PR_COUNTRY**、dispidAddressCountryCode、および**** **PR_POSTAL_ADDRESS の値**プロパティは、 **PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md))、 **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md))、 **PR_OTHER_ADDRESS_STATE_OR_PROVINCE**の値と等しくなければなりません ([PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md))、 **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md))、 **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md))、 **dispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md))、および**dispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) の各プロパティをそれぞれ表します。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティセットの定義と、関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

