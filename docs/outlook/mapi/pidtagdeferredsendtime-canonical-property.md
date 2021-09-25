---
title: PidTagDeferredSendTime 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagDeferredSendTime
api_type:
- HeaderDef
ms.assetid: ee206c2d-8371-4d19-b42b-78f6479e13ca
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fb9d3b46f742b8940ccaace5ce0a60e1246eafc8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600247"
---
# <a name="pidtagdeferredsendtime-canonical-property"></a>PidTagDeferredSendTime 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントがメッセージの送信を延期する時刻を示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_DEFERRED_SEND_TIME  <br/> |
|識別子:  <br/> |0x3FEF  <br/> |
|データの種類 :   <br/> |PT_SYSTIME  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

**PR_DEFERRED_SEND_UNITS** ([PidTagDeferredSendUnits](pidtagdeferredsendunits-canonical-property.md)) プロパティと **PR_DEFERRED_SEND_NUMBER** ([PidTagDeferredSendNumber](pidtagdeferredsendnumber-canonical-property.md)) プロパティが存在する場合、このプロパティの値は次の数式を使用して再計算され、古い値は無視されます。
  
 **PR_DEFERRED_SEND_TIME**  = **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) **+** PR_DEFERRED_SEND_NUMBER * TimeOf(PR_DEFERRED_SEND_UNITS )
  
値 **PR_DEFERRED_SEND_TIME** 現在の時刻 (UTC) より前の場合、メッセージはすぐに送信されます。 
  
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

