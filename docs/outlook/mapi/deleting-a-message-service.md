---
title: メッセージ サービスの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2ad38e1d5fb483956a387e3b6e001479d7153545
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605049"
---
# <a name="deleting-a-message-service"></a>メッセージ サービスの削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **プロファイルからメッセージ サービスを削除するには**
  
1. **IMAPISession::GetMsgServiceTable** を呼び出して、メッセージ サービス テーブルにアクセスします。 
    
2. メッセージ サービスの行を見つけて _、lpuid_ パラメーター **の PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を [IMsgServiceAdmin::D eleteMsgService に渡します](imsgserviceadmin-deletemsgservice.md)。 
    
 **DeleteMsgService は**_、ulContext_ パラメーターを指定してメッセージ サービスのエントリ ポイント関数を呼び出MSG_SERVICE_DELETE。 メッセージ サービスは、プロファイルから削除される前に、この時点でクリーンアップ タスクを実行します。 
  

