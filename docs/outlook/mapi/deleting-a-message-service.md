---
title: メッセージサービスの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 27c20242417e51886ab184b1cc87d6ebb185e4bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316864"
---
# <a name="deleting-a-message-service"></a>メッセージサービスの削除

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
 **メッセージサービスをプロファイルから削除するには**
  
1. メッセージサービステーブルにアクセスするには、 **imapisession:: getmsgservicetable**を呼び出します。 
    
2. メッセージサービスの行を探し、 _lpuid_パラメーターの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を[IMsgServiceAdmin::D eletemsgservice](imsgserviceadmin-deletemsgservice.md)に渡します。 
    
 **DeleteMsgService**は、 _ulcontext_パラメーターを MSG_SERVICE_DELETE に設定して、メッセージサービスのエントリポイント関数を呼び出します。 メッセージサービスプロファイルから削除される前に、この時点でクリーンアップタスクを実行します。 
  

