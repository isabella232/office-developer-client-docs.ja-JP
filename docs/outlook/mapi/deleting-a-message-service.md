---
title: メッセージ サービスの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428124"
---
# <a name="deleting-a-message-service"></a>メッセージ サービスの削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **プロファイルからメッセージ サービスを削除するには**
  
1. **IMAPISession::GetMsgServiceTable** を呼び出して、メッセージ サービス テーブルにアクセスします。 
    
2. メッセージ サービスの行を見つけて _、lpuid_ パラメーター **の PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を [IMsgServiceAdmin::D eleteMsgService に渡します](imsgserviceadmin-deletemsgservice.md)。 
    
 **DeleteMsgService は**_、ulContext_ パラメーターを指定してメッセージ サービスのエントリ ポイント関数を呼び出MSG_SERVICE_DELETE。 メッセージ サービスは、プロファイルから削除される前に、この時点でクリーンアップ タスクを実行します。 
  

