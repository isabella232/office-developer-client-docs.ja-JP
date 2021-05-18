---
title: メッセージ サービスの追加
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407236"
---
# <a name="adding-a-message-service"></a>メッセージ サービスの追加

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **プロファイルに新しいメッセージ サービスを追加し、新しいメッセージ サービスにアクセスするには**
  
[IMsgServiceAdmin2::CreateMsgServiceEx を呼び出します](imsgserviceadmin2-createmsgserviceex.md)。 **CreateMsgServiceEx は** 、次のタスクを実行します。 
  
1. MAPISVC にあるメッセージ サービスに関連するすべての情報をコピーします。INF ファイル。プロバイダー セクションごとにプロファイル セクションを作成します。
    
2. _ulContext_ パラメーターを指定して、メッセージ サービスのエントリ ポイント関数 **MSGSERVICEENTRY** を呼び出MSG_SERVICE_CREATE。 
    
3. メッセージ サービスのプロパティ [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md) **PR_SERVICE_UIDを** 設定して取得します。
    
 **新しく追加されたメッセージ サービスにアクセスするには**
  
1. メッセージ [サービス テーブルを取得するには、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) を呼び出します。 
    
2. メッセージ サービス テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して、テーブル通知に登録します。 
    
3. MAPI が通知を送信TABLE_ROW_ADDED、新しく追加されたメッセージ サービスのエントリ識別子を、新しいメッセージ構造に含まれる [SRow](srow.md) 構造 [TABLE_NOTIFICATION](table_notification.md) します。 
    

