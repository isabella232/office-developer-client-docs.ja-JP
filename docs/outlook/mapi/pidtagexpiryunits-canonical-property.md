---
title: PidTagExpiryUnits 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExpiryUnits
api_type:
- HeaderDef
ms.assetid: f6a1ca22-cf4c-4e59-8846-6bd937fa8f6e
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 8e8deb67990ce25b10a3b0fc1d373f635f958013
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316409"
---
# <a name="pidtagexpiryunits-canonical-property"></a>PidTagExpiryUnits 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
**PR_EXPIRY_NUMBER** ([PidTagExpiryNumber](pidtagexpirynumber-canonical-property.md)) プロパティが乗算する時間の単位を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_EXPIRY_UNITS  <br/> |
|識別子:  <br/> |0x3fee  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>解説

このプロパティを設定する場合は、次のいずれかの値を指定する必要があります。
  
|||
|:-----|:-----|
|PidTagExpiryUnits  <br/> |説明 (timeof)  <br/> |
|0x00000000  <br/> |分 (60 秒など)  <br/> |
|0x00000001  <br/> |時間 (例: 60x60 秒)  <br/> |
|0x00000002  <br/> |日 (たとえば24x60x60 秒)  <br/> |
|0x00000003  <br/> |週 (7x24x60x60 秒など)  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> 電子メールメッセージオブジェクトに対して許容されるプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

