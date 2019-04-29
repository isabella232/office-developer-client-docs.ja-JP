---
title: 必要に応じてメッセージを送信または受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436371"
---
# <a name="sending-or-receiving-a-message-on-demand"></a>必要に応じてメッセージを送信または受信
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通常、クライアントは mapi サブシステム (mapi スプーラーおよびサービスプロバイダー) に依存して、メッセージの送信と受信のタイミングを処理します。 ただし、このタイミングは、MAPI スプーラーまたはトランスポートプロバイダーの status オブジェクトを使用して変更できます。
  
[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドは、1つ以上のトランスポートプロバイダーの受信キューまたは送信キューからすべてのメッセージを削除します。 次の手順では、オンデマンドでメッセージを送受信する2つの方法について説明します。 最初の手順では、MAPI スプーラーの status オブジェクトを使用して、プロファイル内のすべてのトランスポートプロバイダーのキューをフラッシュします。2番目のプロシージャは、1つのトランスポートプロバイダーのキューをフラッシュします。 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a>1回の操作ですべての着信または発信キューをフラッシュするには
  
1. 呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。 
    
2. 状態テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列セットを**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) および**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) に制限します。
    
3. **PR_RESOURCE_TYPE**と MAPI_SPOOLER を一致させるために、 [spropertyrestriction](spropertyrestriction.md)構造を使用してプロパティ制限を構築します。 
    
4. MAPI スプーラーの状態を表す行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出し、 **spropertyrestriction**構造を渡します。 
    
5. **PR_ENTRYID**列を[imapisession:: openentry](imapisession-openentry.md)に渡して、MAPI スプーラーの status オブジェクトを開きます。 
    
6. MAPI スプーラーの[imapistatus:: flushqueues](imapistatus-flushqueues.md)メソッドを呼び出し、FLUSH_NO_UI フラグを渡してユーザーインターフェイスを非表示にし、送信または受信キューをフラッシュする FLUSH_DOWNLOAD または FLUSH_UPLOAD フラグを渡します。 
    
7. status オブジェクトと状態テーブルを解放します。また、テーブルに割り当てられている[srowset](srowset.md)構造も解放します。 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a>着信または発信キューをトランスポートプロバイダーによって個別にフラッシュするには
  
1. 呼び出し[imapisession:: getstatustable](imapisession-getstatustable.md)は状態テーブルにアクセスできます。 
    
2. 状態テーブルの[IMAPITable:: SetColumns](imapitable-setcolumns.md)メソッドを呼び出して、列が**PR_ENTRYID**と**PR_RESOURCE_TYPE**に設定されるように制限します。
    
3. **PR_RESOURCE_TYPE**と MAPI_TRANSPORT_PROVIDER を一致させるために、 [spropertyrestriction](spropertyrestriction.md)構造を使用してプロパティ制限を構築します。 
    
4. トランスポートプロバイダーによって提供される行を取得するには、 [hrqueryallrows](hrqueryallrows.md)を呼び出し、 **spropertyrestriction**構造を渡します。 
    
5. **hrqueryallrows**から返される各行ごとに、次のようにします。
    
    1. **PR_ENTRYID**列を[imapisession:: openentry](imapisession-openentry.md)に渡して、トランスポートプロバイダーの status オブジェクトを開きます。 
        
    2. トランスポート状態オブジェクトが、 **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) プロパティに STATUS_FLUSH_QUEUES フラグが設定されていることを確認して、 **flushqueues**メソッドをサポートしていることを確認してください。 
        
    3. サポートされている場合は、 [imapistatus:: flushqueues](imapistatus-flushqueues.md)を呼び出します。 サポートされていない場合は、MAPI スプーラーの**imapistatus:: flushqueues**メソッドを呼び出して、 _lptargettransport_パラメーターでトランスポートのエントリ識別子を渡します。 MAPI スプーラーの状態オブジェクトにアクセスする手順については、前の手順を参照してください。 送信キューまたは FLUSH_UPLOAD フラグをフラッシュして、受信キューをフラッシュするように FLUSH_DOWNLOAD フラグを設定します。 
        
    4. status オブジェクトと状態テーブルを解放します。また、テーブルに割り当てられている[srowset](srowset.md)構造も解放します。 
    
MAPI スプーラーは、ほとんどの LAN トランスポートプロバイダーと同様に FLUSH_NO_UI フラグを受け入れます。 ただし、すべてのトランスポートプロバイダーがこのフラグを使用するわけではありません。特に、モデムを明示的に使用するものやリモートアクセスサービス (RAS) を使用するものもあります。 RAS は、クライアントがユーザーインターフェイスを抑制することを許可するようには設計されていません。 クライアントがユーザーの操作を必要とせずに接続できるように、クライアントを構成することは可能ですが、これは困難で、クライアントのメッセージサービスを熟知している必要があります。
  

