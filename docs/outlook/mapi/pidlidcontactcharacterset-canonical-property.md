---
title: PidLidContactCharacterSet 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidContactCharacterSet
api_type:
- COM
ms.assetid: a167e199-a9b2-47f9-a90e-2abc7c29828c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b471b87c789faf82491f88864d7bb7e5ac6a2f16
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563974"
---
# <a name="pidlidcontactcharacterset-canonical-property"></a>PidLidContactCharacterSet 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この連絡先に使用する文字セットを指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidContactCharSet  <br/> |
|プロパティ セット:  <br/> |PSETID_Address  <br/> |
|長い ID (LID):  <br/> |0x00008023  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>注釈

アプリケーションは、このプロパティを使用して **、dispidFileUnder** [(PidLidFileUnder)](pidlidfileunder-canonical-property.md)プロパティ **、dispidFileUnderList** ([PidLidFileUnderList](pidlidfileunderlist-canonical-property.md)) プロパティ、 **および dispidFileUnderId** ([PidLidFileUnderId](pidlidfileunderid-canonical-property.md)) プロパティの文字セット依存リストを生成できます。 プロパティの値が "0x00000000" または "0x00000001" の場合、アプリケーションはプロパティを設定されていないと処理する必要があります。
  
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

