---
title: メッセージ サービスの追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 6a8b0f8fc8c296fe4022ac28623b83d270472ca3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590695"
---
# <a name="adding-a-message-service"></a>メッセージ サービスの追加

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
 **新しいメッセージ サービスをプロファイルに追加し、新しいメッセージ サービスへのアクセス**
  
[IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を呼び出します。 **CreateMsgServiceEx**は、次のタスクを実行します。 
  
1. MAPISVC 内にあるメッセージ サービスに関連する情報のすべてをコピーします。INF ファイル、プロファイル プロバイダーのすべてのセクションのセクションを作成します。
    
2. メッセージ サービスのエントリ ポイント関数、 **MSGSERVICEENTRY**、 _ulContext_パラメーターを MSG_SERVICE_CREATE に設定が呼び出されます。 
    
3. 設定し、メッセージ サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティを取得します。
    
 **任意のメッセージを新たに追加されたサービスにアクセスするには**
  
1. メッセージ サービス テーブルを取得するために[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出します。 
    
2. テーブルの通知を登録するのには、メッセージ サービス テーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出します。 
    
3. MAPI では、TABLE_ROW_ADDED 通知を送信するときは、 [TABLE_NOTIFICATION](table_notification.md)構造体に含まれる[SRow](srow.md)構造体に新たに追加されたメッセージ サービスのエントリの識別子を探します。 
    

