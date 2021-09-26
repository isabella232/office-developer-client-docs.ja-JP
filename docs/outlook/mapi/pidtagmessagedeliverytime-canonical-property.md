---
title: PidTagMessageDeliveryTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageDeliveryTime
api_type:
- HeaderDef
ms.assetid: 4f9d44f2-4faa-4f16-9e33-22f80c17db85
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 19a777423d97976212f487c2e2624b158d0be352
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583367"
---
# <a name="pidtagmessagedeliverytime-canonical-property"></a>PidTagMessageDeliveryTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージが配信された日時を格納します。 
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_MESSAGE_DELIVERY_TIME  <br/> |
|識別子:  <br/> |0x0E06  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |メッセージ時刻  <br/> |
   
## <a name="remarks"></a>注釈

このプロパティは、トランスポート プロバイダーがサーバーからローカル ストアにメッセージをコピーしたダウンロード時間ではなく、メッセージがサーバーに保存された時刻を表します。
  
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

