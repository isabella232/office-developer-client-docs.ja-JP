---
title: 要求時にメッセージを送受信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 668e1c57c59bf2356be808e0347e1bd5135478a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563892"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>要求時にメッセージを送受信します。
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
通常、クライアントは、MAPI サブシステムに依存して、MAPI スプーラーとサービス ・ プロバイダー-メッセージの送信と受信のタイミングを処理するために。 ただし、MAPI スプーラーを無効またはトランスポート プロバイダーのいずれかの状態オブジェクトを使用して、このタイミングを変更できます。
  
[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドでは、1 つまたは複数トランスポート プロバイダーの受信または送信キューからすべてのメッセージを削除します。 次の手順では、要求時にメッセージを送受信するための 2 つの手法について説明します。 最初の手順は、プロファイル内のすべてのトランスポート プロバイダーのキューをフラッシュするのには、MAPI スプーラーを無効の状態のオブジェクトを使用してください。2 番目の手順では、1 つのトランスポート プロバイダーのキューをフラッシュします。 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>1 回の操作ですべての着信または発信キューをフラッシュするには
  
1. ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。 
    
2. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) と**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) に設定する列を制限するのには、状態テーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出します。
    
3. [SPropertyRestriction](spropertyrestriction.md)構造体を使用して、MAPI_SPOOLER と**PR_RESOURCE_TYPE**を一致するようにプロパティ制約を作成します。 
    
4. [HrQueryAllRows](hrqueryallrows.md)、 **SPropertyRestriction**構造体を渡すことを呼び出し、MAPI スプーラーを無効の状態を表す行を取得するのには。 
    
5. **PR_ENTRYID**の列を MAPI スプーラーを無効の状態のオブジェクトを開くには、 [IMAPISession::OpenEntry](imapisession-openentry.md)に渡します。 
    
6. FLUSH_NO_UI フラグをユーザー インターフェイスを非表示にして、送信または受信キューをフラッシュするのには FLUSH_DOWNLOAD または FLUSH_UPLOAD のいずれかのフラグを渡す、MAPI スプーラーの[IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)メソッドを呼び出します。 
    
7. 状態オブジェクト、状態テーブルとテーブルに割り当てられている[SRowSet](srowset.md)構造体を解放します。 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>トランスポート プロバイダーによって個別に着信または発信のキューをフラッシュするには
  
1. ステータス テーブルにアクセスするのには[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出します。 
    
2. **PR_ENTRYID**と**PR_RESOURCE_TYPE**に設定する列を制限するのには、状態テーブルの[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドを呼び出します。
    
3. [SPropertyRestriction](spropertyrestriction.md)構造体を使用して、MAPI_TRANSPORT_PROVIDER と**PR_RESOURCE_TYPE**を一致するようにプロパティ制約を作成します。 
    
4. [HrQueryAllRows](hrqueryallrows.md)、 **SPropertyRestriction**構造体を渡してトランスポート プロバイダーによって提供されている行を取得するを呼び出します。 
    
5. 行ごとに、 **HrQueryAllRows**から返されます。
    
    1. **PR_ENTRYID**の列をトランスポート プロバイダーの状態のオブジェクトを開くには、 [IMAPISession::OpenEntry](imapisession-openentry.md)に渡します。 
        
    2. トランスポートの状態のオブジェクトが、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティが、STATUS_FLUSH_QUEUES を持っているかを確認することで**FlushQueues**メソッドをサポートすることを確認してフラグを設定します。 
        
    3. サポートされている場合は、 [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)を呼び出します。 サポートされていない場合、は、 _lpTargetTransport_パラメーターで、トランスポートのエントリの識別子を渡す、MAPI スプーラーの**IMAPIStatus::FlushQueues**メソッドを呼び出します。 MAPI スプーラーを無効の状態のオブジェクトにアクセスする手順については上記の手順を参照してください。 発信キューをフラッシュするのには FLUSH_DOWNLOAD フラグまたは受信キューをフラッシュするのには FLUSH_UPLOAD フラグを設定します。 
        
    4. 状態オブジェクト、状態テーブルとテーブルに割り当てられている[SRowSet](srowset.md)構造体を解放します。 
    
LAN トランスポート プロバイダーのほとんどのように FLUSH_NO_UI フラグは、MAPI スプーラーです。 ただし、すべてのトランスポート プロバイダーは、このフラグは、特に明示的にモデムを使用して、リモート アクセス サービス (RAS) を優先します。 RAS は、クライアントがユーザー インターフェイスを非表示にできるように意図していません。 クライアントで、ユーザーとのやり取りを必要とせずに接続できるが、ことは困難であり、クライアントのメッセージ サービスの詳細な知識を必要とするように構成することができます。
  

