---
title: PidLidAddressBookProviderEmailList 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390360"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>PidLidAddressBookProviderEmailList 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先に設定する電子メール アドレスのプロパティを指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidABPEmailList  <br/> |
|プロパティを設定します。  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008028  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>備考

このプロパティでは、各 PT_LONG 値は、プロパティ内で一意である必要があり、次の表の値のいずれかに設定する必要があります。 このプロパティが設定されている場合、 **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) のプロパティも設定しなければなりません。 互いに同期された 2 つのプロパティを保持する必要があります。 たとえば、 **dispidABPEmailList**の値のいずれかが"0x00000000"の場合、 **dispidABPArrayType**が"0x00000001"のビットに設定します。 
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |連絡先の Email1 が定義されています。  <br/> |
|0x00000001  <br/> |連絡先の電子メール 2 が定義されています。  <br/> |
|0x00000002  <br/> |連絡先の電子メール 3 が定義されています。  <br/> |
|0x00000003  <br/> |連絡先の勤務先ファックスが定義されています。  <br/> |
|0x00000004  <br/> |連絡先の自宅の fax が定義されています。  <br/> |
|0x00000005  <br/> |連絡先のプライマリ fax が定義されています。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

