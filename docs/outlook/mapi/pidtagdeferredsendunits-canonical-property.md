---
title: PidTagDeferredSendUnits 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeferredSendUnits
api_type:
- HeaderDef
ms.assetid: 2386be9f-18c9-4949-a2aa-efc8e212801c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: becc076efe0f4f805eb2a8db071b70ad731ee256
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359907"
---
# <a name="pidtagdeferredsendunits-canonical-property"></a>PidTagDeferredSendUnits 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
プロパティ値 [(PidTagDeferredSendNumber)](pidtagdeferredsendnumber-canonical-property.md) **PR_DEFERRED_SEND_NUMBERを乗算** する時間の単位を指定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEFERRED_SEND_UNITS  <br/> |
|識別子:  <br/> |0x3FEC  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

設定されている場合、このプロパティには次のいずれかの値が必要です。
  
|||
|:-----|:-----|
|**PidTagDeferredSendUnits** <br/> |説明  <br/> |
|0  <br/> |分 (60 秒など)  <br/> |
|1  <br/> |時間 (60x60 秒など)  <br/> |
|2  <br/> |Day (24x60x60 秒など)  <br/> |
|3  <br/> |週 (7x24x60x60 秒など)  <br/> |
   
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

