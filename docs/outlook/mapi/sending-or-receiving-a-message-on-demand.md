---
title: 必要に応じてメッセージを送信または受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f239b996d157ba5d15c5f2af22b4ea585d09d47
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609482"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>必要に応じてメッセージを送信または受信
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
クライアントは通常、MAPI サブシステム (MAPI スプーラーとサービス プロバイダー) を使用して、メッセージの送受信のタイミングを処理します。 ただし、MAPI スプーラーまたはトランスポート プロバイダーの status オブジェクトを使用して、このタイミングを変更できます。
  
[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドは、1 つ以上のトランスポート プロバイダーの受信キューまたは送信キューからすべてのメッセージを削除します。 次の手順では、オンデマンドでメッセージを送受信する 2 つの手法について説明します。 最初の手順では、MAPI スプーラーの status オブジェクトを使用して、プロファイル内のすべてのトランスポート プロバイダーのキューをフラッシュします。2 番目の手順では、1 つのトランスポート プロバイダーのキューをフラッシュします。 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>1 回の操作ですべての受信キューまたは送信キューをフラッシュするには
  
1. [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。 
    
2. 状態テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)) および **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))**に** 制限します。
    
3. [SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を構築し、プロパティと **PR_RESOURCE_TYPE一致** MAPI_SPOOLER。 
    
4. [HrQueryAllRows](hrqueryallrows.md)を呼び出し **、SPropertyRestriction** 構造体を渡して、MAPI スプーラーの状態を表す行を取得します。 
    
5. MAPI ス **プー PR_ENTRYID** の状態オブジェクトを開く場合は、この列を [IMAPISession::OpenEntry](imapisession-openentry.md) に渡します。 
    
6. MAPI スプーラーの [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) メソッドを呼び出し、FLUSH_NO_UI フラグを渡してユーザー インターフェイスを抑制し、FLUSH_DOWNLOAD または FLUSH_UPLOAD フラグを使用して送信キューまたは着信キューをフラッシュします。 
    
7. status オブジェクトと状態テーブル、およびテーブルに割り当てられている [SRowSet](srowset.md) 構造を解放します。 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>トランスポート プロバイダーによって受信キューまたは送信キューを個別にフラッシュするには
  
1. [IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出して、状態テーブルにアクセスします。 
    
2. 状態テーブルの [IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを列セットの値 **PR_ENTRYIDおよび** PR_RESOURCE_TYPE。
    
3. [SPropertyRestriction](spropertyrestriction.md)構造体を使用してプロパティ制限を構築し、プロパティと **PR_RESOURCE_TYPE一致** MAPI_TRANSPORT_PROVIDER。 
    
4. [HrQueryAllRows](hrqueryallrows.md)を呼び出し **、SPropertyRestriction** 構造体を渡して、トランスポート プロバイダーによって提供される行を取得します。 
    
5. **HrQueryAllRows** から返される各行について、
    
    1. **[PR_ENTRYID]** 列を [IMAPISession::OpenEntry](imapisession-openentry.md)に渡して、トランスポート プロバイダーの状態オブジェクトを開きます。 
        
    2. トランスポート状態オブジェクトが **FlushQueues** メソッドをサポートしている場合は **、PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグが設定STATUS_FLUSH_QUEUES確認します。 
        
    3. サポートされている場合は [、IMAPIStatus::FlushQueues を呼び出します](imapistatus-flushqueues.md)。 サポートされていない場合は、MAPI スプーラーの **IMAPIStatus::FlushQueues** メソッドを呼び出し  _、lpTargetTransport_ パラメーターでトランスポートのエントリ識別子を渡します。 MAPI スプーラーの状態オブジェクトにアクセスする手順については、前の手順を参照してください。 送信キュー FLUSH_DOWNLOADフラッシュする場合は FLUSH_UPLOADフラグを設定して、受信キューをフラッシュします。 
        
    4. status オブジェクトと状態テーブル、およびテーブルに割り当てられている [SRowSet](srowset.md) 構造を解放します。 
    
MAPI スプーラーは、ほとんどの LAN FLUSH_NO_UIと同様に、このフラグを使用します。 ただし、すべてのトランスポート プロバイダーが、特に明示的にモデムとリモート アクセス サービス (RAS) を使用する場合は、このフラグを受け入れるわけではありません。 RAS は、クライアントがユーザー インターフェイスを抑制するように設計されていない。 ユーザーの操作を必要とせずに接続できるようクライアントを構成することは可能ですが、難しく、クライアントのメッセージ サービスに関する深い知識が必要です。
  

