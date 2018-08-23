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
ms.openlocfilehash: 6b344986989a47c4f1159fcf50c1d067ae716e98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802105"
---
# <a name="pidlidpostaladdressid-canonical-property"></a>PidLidPostalAddressId 標準プロパティ

  
  
**適用対象**: Outlook 
  
どの物理アドレスは、連絡先の郵送先住所を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidPostalAddressId  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008022  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

存在する場合、このプロパティは、次の表で、または[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)で指定されている値のいずれかで必要があります。 表示しない場合は、設定、アプリケーションを想定してください値が"0x00000000"であります。
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |住所が郵送先住所として選択されていません。 **PR_STREET_ADDRESS**([PidTagStreetAddress](pidtagstreetaddress-canonical-property.md))、 **PR_COUNTRY** ([ 、 **PR_LOCALITY** ([PidTagLocality](pidtaglocality-canonical-property.md))、 **PR_STATE_OR_PROVINCE** ([PidTagStateOrProvince](pidtagstateorprovince-canonical-property.md))、 **PR_POSTAL_CODE** ([PidTagPostalCode](pidtagpostalcode-canonical-property.md))PidTagCountry](pidtagcountry-canonical-property.md))、 **dispidAddressCountryCode** ([PidLidAddressCountryCode](pidlidaddresscountrycode-canonical-property.md)) と**PR_POSTAL_ADDRESS** ([PidTagPostalAddress](pidtagpostaladdress-canonical-property.md)) のすべてを設定できませんする必要があります。  <br/> |
|0x00000001  <br/> |ホーム アドレスは、郵送先住所です。 **PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 **PR_POST_OFFICE_BOX** ([PidTagPostOfficeBox](pidtagpostofficebox-canonical-property.md))、 **PR_COUNTRY**、 **dispidAddressCountryCode の値**、 **PR_POSTAL_ADDRESS**プロパティは、 **PR_HOME_ADDRESS_STREET** ([PidTagHomeAddressStreet](pidtaghomeaddressstreet-canonical-property.md))、 **PR_HOME_ADDRESS_CITY** ([PidTagHomeAddressCity](pidtaghomeaddresscity-canonical-property.md))、 **PR_HOME_ の値に等しいである必要がありますADDRESS_STATE_OR_PROVINCE** ([PidTagHomeAddressStateOrProvince](pidtaghomeaddressstateorprovince-canonical-property.md))、 **PR_HOME_ADDRESS_POSTAL_CODE** ([PidTagHomeAddressPostalCode](pidtaghomeaddresspostalcode-canonical-property.md))、 **PR_HOME_ADDRESS_POST_OFFICE_BOX** ([PidTagHomeAddressPostOfficeBox](pidtaghomeaddresspostofficebox-canonical-property.md))、 **PR_HOME_ADDRESS_COUNTRY** ([PidTagHomeAddressCountry](pidtaghomeaddresscountry-canonical-property.md))、 **dispidHomeAddressCountryCode** ([PidLidHomeAddressCountryCode](pidlidhomeaddresscountrycode-canonical-property.md)) と**dispidHomeAddress** ([PidLidHomeAddress](pidlidhomeaddress-canonical-property.md))プロパティは、それぞれ。  <br/> |
|0x00000002  <br/> |勤務先住所は、郵送先住所です。 **PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 **PR_POST_OFFICE_BOX**、 **PR_COUNTRY**、 **dispidAddressCountryCode**、および**PR_POSTAL_ADDRESS の値**プロパティは、 **dispidWorkAddressStreet** ([PidLidWorkAddressStreet](pidlidworkaddressstreet-canonical-property.md))、 **dispidWorkAddressCity** ([PidLidWorkAddressCity](pidlidworkaddresscity-canonical-property.md))、 **dispidWorkAddressState** ([の値に等しいである必要がありますPidLidWorkAddressState](pidlidworkaddressstate-canonical-property.md))、 **dispidWorkAddressPostalCode** ([PidLidWorkAddressPostalCode](pidlidworkaddresspostalcode-canonical-property.md))、 **dispidWorkAddressPostOfficeBox** ([PidLidWorkAddressPostOfficeBox](pidlidworkaddresspostofficebox-canonical-property.md)) **dispidWorkAddressCountry**([PidLidWorkAddressCountry](pidlidworkaddresscountry-canonical-property.md))、 **dispidWorkAddressCountryCode** ([PidLidWorkAddressCountryCode](pidlidworkaddresscountrycode-canonical-property.md)) と**dispidWorkAddress** ([PidLidWorkAddress](pidlidworkaddress-canonical-property.md)) プロパティでは、それぞれ。  <br/> |
|0x00000003  <br/> |その他のアドレスは、郵送先住所です。 値の**PR_STREET_ADDRESS**、 **PR_LOCALITY**、 **PR_STATE_OR_PROVINCE**、 **PR_POSTAL_CODE**、 **PR_POST_OFFICE_BOX**、 **PR_COUNTRY**、 **dispidAddressCountryCode**、および**PR_POSTAL_ADDRESS**プロパティは、 **PR_OTHER_ADDRESS_STREET** ([PidTagOtherAddressStreet](pidtagotheraddressstreet-canonical-property.md))、 **PR_OTHER_ADDRESS_CITY** ([PidTagOtherAddressCity](pidtagotheraddresscity-canonical-property.md))、 **PR_OTHER_ADDRESS_STATE_OR_PROVINCE** (の値に等しいである必要があります[PidTagOtherAddressStateOrProvince](pidtagotheraddressstateorprovince-canonical-property.md))、 **PR_OTHER_ADDRESS_POSTAL_CODE** ([PidTagOtherAddressPostalCode](pidtagotheraddresspostalcode-canonical-property.md))、 **PR_OTHER_ADDRESS_POST_OFFICE_BOX** ([PidTagOtherAddressPostOfficeBox](pidtagotheraddresspostofficebox-canonical-property.md))、 **dispidOtherAddressCountryCode** ([PidLidOtherAddressCountryCode](pidlidotheraddresscountrycode-canonical-property.md)) と**dispidOtherAddress** ([PidLidOtherAddress](pidlidotheraddress-canonical-property.md)) プロパティでは、それぞれ。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

