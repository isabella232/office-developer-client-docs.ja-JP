---
title: PidTagStatusCode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: fcd890f9fa7055abfd4eb6765434992e758ecb32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599397"
---
# <a name="pidtagstatuscode-canonical-property"></a>PidTagStatusCode 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッション リソースの現在の状態を示すフラグのビットマスクが含まれる。 すべてのサービス プロバイダーは、MAPI と同じ状態コードを設定して、サブシステム、MAPI スプーラー、および統合アドレス帳の状態を報告します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS_CODE  <br/> |
|識別子:  <br/> |0x3E04  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

状態コードは、すべてのプロバイダーの Mapisvc.inf ファイルに表示する必要があります。 
  
Status オブジェクトは、MAPI およびすべてのサービス プロバイダーによって実装されます。 状態コードには 2 つの有効な値のセットがあります。1 つはすべての状態オブジェクトに対して設定され、もう 1 つはトランスポート プロバイダー専用のセットです。 すべての状態オブジェクトは、このプロパティを次の値に設定できます。
  
STATUS_AVAILABLE 
  
> リソースが運用可能な状態を示します。
    
STATUS_FAILURE 
  
> リソースに問題が発生している場合を示します。 サービス プロバイダーの場合、STATUS_FAILUREは、プロバイダーが現在のセッションを終了するためにすぐにシャットダウンされる可能性を示します。
    
STATUS_OFFLINE 
  
> ローカル データまたはサービスだけが使用可能な状態を示します。
    
トランスポート プロバイダーは、ステータス オブジェクトのプロパティPR_STATUS_CODE次 **の** 値に設定することもできます。 
  
STATUS_INBOUND_ACTIVE 
  
> トランスポート プロバイダーが受信メッセージを受信中かどうかを示します。 
    
STATUS_INBOUND_ENABLED 
  
> トランスポート プロバイダーが受信メッセージを受信できるかどうかを示します。
    
STATUS_INBOUND_FLUSH 
  
> トランスポート プロバイダーが受信キューからメッセージをダウンロード中かどうかを示します。
    
STATUS_OUTBOUND_ACTIVE 
  
> トランスポート プロバイダーが送信メッセージを受信中かどうかを示します。 
    
STATUS_OUTBOUND_ENABLED 
  
> トランスポート プロバイダーが送信メッセージを処理できるかどうかを示します。
    
STATUS_OUTBOUND_FLUSH 
  
> トランスポート プロバイダーが送信キューからメッセージをアップロード中かどうかを示します。
    
STATUS_REMOTE_ACCESS 
  
> トランスポート プロバイダーがリモート アクセスをサポートします。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[PidTagStatusString 標準プロパティ](pidtagstatusstring-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

