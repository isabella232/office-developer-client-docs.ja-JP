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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: a60bc55686e883cabd144af3a9badfb55f835472
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593124"
---
# <a name="pidtagstatuscode-canonical-property"></a>PidTagStatusCode 標準プロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
セッション リソースの現在の状態を示すフラグのビットマスクを格納します。 すべてのサービス プロバイダーは、MAPI サブシステム、MAPI スプーラーを無効、および統合されたアドレス帳のステータスを報告するように、ステータス コードを設定します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_STATUS_CODE  <br/> |
|識別子:  <br/> |0x3E04  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>注釈

ステータス コードは必要があります、すべてのプロバイダー、Mapisvc.inf ファイルに表示されます。 
  
状態オブジェクトは、MAPI とすべてのサービス プロバイダーによって実装されます。 ステータス コード、ステータスのすべてのオブジェクトのセットを 1 つだけのトランスポート プロバイダーの別のセットの有効な値の 2 つのセットがあります。 ステータスのすべてのオブジェクトは、次の値にこのプロパティを設定できます。
  
STATUS_AVAILABLE 
  
> リソースを運用することを示します。
    
STATUS_FAILURE 
  
> リソースに問題が発生していることを示します。 STATUS_FAILURE では、サービス プロバイダーは、プロバイダー可能性がありますすぐに、シャット ダウンしている現在のセッションを終了することを示します。
    
STATUS_OFFLINE 
  
> ローカルのデータやサービスが利用できることを示します。
    
トランスポート プロバイダー プロパティも設定できます、状態オブジェクトの**PR_STATUS_CODE**に次の値。 
  
STATUS_INBOUND_ACTIVE 
  
> トランスポート プロバイダーが、受信メッセージを受信していることを示します。 
    
STATUS_INBOUND_ENABLED 
  
> トランスポート プロバイダーは、受信メッセージを受信できることを示します。
    
STATUS_INBOUND_FLUSH 
  
> トランスポート プロバイダーが受信キューからメッセージをダウンロードしていることを示します。
    
STATUS_OUTBOUND_ACTIVE 
  
> トランスポート プロバイダーが送信メッセージを受信していることを示します。 
    
STATUS_OUTBOUND_ENABLED 
  
> トランスポート プロバイダーが送信メッセージを処理できることを示します。
    
STATUS_OUTBOUND_FLUSH 
  
> トランスポート プロバイダーが送信キューからメッセージをアップロードすることを示します。
    
STATUS_REMOTE_ACCESS 
  
> トランスポート プロバイダーがリモート アクセスをサポートしていることを示します。
    
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[PidTagStatusString 標準プロパティ](pidtagstatusstring-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

