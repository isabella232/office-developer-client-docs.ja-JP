---
title: メッセージサービスを追加する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328187"
---
# <a name="adding-a-message-service"></a>メッセージサービスを追加する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **新しいメッセージサービスをプロファイルに追加して、新しいメッセージサービスにアクセスするには**
  
[IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を呼び出します。 **CreateMsgServiceEx**は、次のタスクを実行します。 
  
1. mapisvc.inf に含まれるメッセージサービスの関連情報をすべてコピーします。INF ファイル。すべてのプロバイダーセクションのプロファイルセクションを作成します。
    
2. _ulcontext_パラメーターを MSG_SERVICE_CREATE に設定して、メッセージサービスのエントリポイント関数**msgserviceentry**を呼び出します。 
    
3. メッセージサービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティを設定および取得します。
    
 **新しく追加されたメッセージサービスにアクセスするには**
  
1. message service テーブルを取得するには、 [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)を呼び出します。 
    
2. メッセージサービステーブルの[IMAPITable:: アドバイズ](imapitable-advise.md)メソッドを呼び出して、テーブル通知の登録を行います。 
    
3. MAPI が TABLE_ROW_ADDED 通知を送信する場合は、 [TABLE_NOTIFICATION](table_notification.md)構造に含まれている[srow](srow.md)構造で新しく追加されたメッセージサービスのエントリ識別子を見つけます。 
    

