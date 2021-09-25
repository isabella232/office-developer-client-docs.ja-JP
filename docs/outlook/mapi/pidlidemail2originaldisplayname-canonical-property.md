---
title: PidLidEmail2OriginalDisplayName 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidEmail2OriginalDisplayName
api_type:
- COM
ms.assetid: 0b648ef6-86ed-40ee-b068-8fcde7e0fe75
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3e3c71d8eafb077e70535bd8515521eb0734556b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566970"
---
# <a name="pidlidemail2originaldisplayname-canonical-property"></a>PidLidEmail2OriginalDisplayName 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先に指定された電子メール アドレスに対応する 2 番目の表示名を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidEmail2OriginalDisplayName  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008094  <br/> |
|データの種類 :   <br/> |PT_UNICODE  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

**dispidEmail2AddrType** ([PidLidEmail2AddressType)](pidlidemail2addresstype-canonical-property.md)プロパティの値が "SMTP" の場合、それぞれの **PidLidEmail2OriginalDisplayName** プロパティの値は、それぞれの **dispidEmail2EmailAddress** ([PidLidEmail2EmailAddress](pidlidemail2emailaddress-canonical-property.md)) プロパティの値と等しくなります。 このプロパティの目的は **、dispidEmail2EmailAddress** のアドレスと同等の代替のユーザーフレンドリーなアドレスを表示します。
  
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

