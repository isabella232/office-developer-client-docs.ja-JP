---
title: PidTagExpiryUnits 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c978fb3b23955d37c34c8f78f9a9a974245e0d8f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59579083"
---
# <a name="pidtagexpiryunits-canonical-property"></a>PidTagExpiryUnits 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ [(PidTagExpiryNumber)](pidtagexpirynumber-canonical-property.md)プロパティ **PR_EXPIRY_NUMBER** 乗算する時間の単位を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXPIRY_UNITS  <br/> |
|識別子:  <br/> |0x3FEE  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティを設定する場合は、次のいずれかの値を指定する必要があります。
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |説明 (TimeOf)  <br/> |
|0x00000000  <br/> |分 (60 秒など)  <br/> |
|0x00000001  <br/> |時間 (60x60 秒など)  <br/> |
|0x00000002  <br/> |Day (24x60x60 秒など)  <br/> |
|0x00000003  <br/> |週 (7x24x60x60 秒など)  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メール メッセージ オブジェクトで許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

