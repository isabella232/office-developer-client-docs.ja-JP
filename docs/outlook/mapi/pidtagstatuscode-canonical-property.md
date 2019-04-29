---
title: PidTagStatusCode 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418515"
---
# <a name="pidtagstatuscode-canonical-property"></a>PidTagStatusCode 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
セッションリソースの現在の状態を示すフラグのビットマスクを含みます。 すべてのサービスプロバイダーは mapi として状態コードを設定し、サブシステム、mapi スプーラー、および統合アドレス帳の状態に関するレポートを作成します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS_CODE  <br/> |
|識別子:  <br/> |0x3e04  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |MAPI の状態  <br/> |
   
## <a name="remarks"></a>注釈

状態コードは、すべてのプロバイダーの mapisvc.inf ファイルに表示される必要があります。 
  
状態オブジェクトは、MAPI およびすべてのサービスプロバイダーによって実装されます。 状態コードには2つの有効な値があり、すべての状態オブジェクトに1つ、トランスポートプロバイダーに対して別のセットが設定されています。 すべての status オブジェクトは、このプロパティを次の値に設定できます。
  
STATUS_AVAILABLE 
  
> リソースが稼働していることを示します。
    
STATUS_FAILURE 
  
> リソースに問題が発生していることを示します。 サービスプロバイダーの場合、STATUS_FAILURE は、プロバイダーがすぐにシャットダウンして現在のセッションを終了する可能性があることを示します。
    
STATUS_OFFLINE 
  
> ローカルデータまたはサービスのみが利用可能であることを示します。
    
また、トランスポートプロバイダーは、状態オブジェクトの**PR_STATUS_CODE**プロパティを次の値に設定することもできます。 
  
STATUS_INBOUND_ACTIVE 
  
> トランスポートプロバイダーが受信メッセージを受信していることを示します。 
    
STATUS_INBOUND_ENABLED 
  
> トランスポートプロバイダーが受信メッセージを受信できることを示します。
    
STATUS_INBOUND_FLUSH 
  
> トランスポートプロバイダーが受信キューからメッセージをダウンロードしていることを示します。
    
STATUS_OUTBOUND_ACTIVE 
  
> トランスポートプロバイダーが送信メッセージを受信していることを示します。 
    
STATUS_OUTBOUND_ENABLED 
  
> トランスポートプロバイダーが送信メッセージを処理できることを示します。
    
STATUS_OUTBOUND_FLUSH 
  
> トランスポートプロバイダーが送信キューからメッセージをアップロードしていることを示します。
    
STATUS_REMOTE_ACCESS 
  
> トランスポートプロバイダーがリモートアクセスをサポートしていることを示します。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStatusString 標準プロパティ](pidtagstatusstring-canonical-property.md)


[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

