---
title: PidTagStatusCode の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803584"
---
# <a name="pidtagstatuscode-canonical-property"></a>PidTagStatusCode の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
セッション リソースの現在の状態を示すフラグのビットマスクを格納します。 すべてのサービス プロバイダーは、MAPI サブシステム、MAPI スプーラーを無効、および統合されたアドレス帳のステータスを報告するように、ステータス コードを設定します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_STATUS_CODE  <br/> |
|識別子:  <br/> |0x3E04  <br/> |
|データを入力します。  <br/> |PT_LONG  <br/> |
|領域:  <br/> |MAPI のステータス  <br/> |
   
## <a name="remarks"></a>備考

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



[PidTagStatusString の標準的なプロパティ](pidtagstatusstring-canonical-property.md)


[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
