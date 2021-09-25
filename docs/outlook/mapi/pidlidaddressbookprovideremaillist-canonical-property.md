---
title: PidLidAddressBookProviderEmailList 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b8a89ed265b3208d0476c99bd3fb3dc2c80e394e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584020"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>PidLidAddressBookProviderEmailList 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先に設定する電子アドレスプロパティを指定します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidABPEmailList  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008028  <br/> |
|データの種類 :   <br/> |PT_MV_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

このPT_LONGの各値は、プロパティ内で一意である必要があります。次の表のいずれかの値に設定する必要があります。 このプロパティを設定する場合は **、dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)) プロパティも設定する必要があります。 これら 2 つのプロパティは、互いに同期し続けなければならない。 たとえば **、dispidABPEmailList** の値の 1 つが "0x00000000" の場合 **、dispidABPArrayType** にはビット "0x00000001" が設定されている必要があります。 
  
|**値**|**説明**|
|:-----|:-----|
|0x00000000  <br/> |Email1 は連絡先に対して定義されます。  <br/> |
|0x00000001  <br/> |Email2 は連絡先に対して定義されます。  <br/> |
|0x00000002  <br/> |Email3 は連絡先に対して定義されます。  <br/> |
|0x00000003  <br/> |ビジネス FAX は連絡先に対して定義されます。  <br/> |
|0x00000004  <br/> |ホーム FAX は連絡先に対して定義されます。  <br/> |
|0x00000005  <br/> |プライマリ FAX は連絡先に対して定義されます。  <br/> |
   
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

