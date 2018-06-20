---
title: メッセージ サービスを削除します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 34d9d6d428f39765e739ce856f3666d07b457d52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799900"
---
# <a name="deleting-a-message-service"></a>メッセージ サービスを削除します。

  
  
**適用されます**: Outlook 
  
 **メッセージ サービスをプロファイルから削除するのには**
  
1. メッセージ サービス テーブルにアクセスするのには**IMAPISession::GetMsgServiceTable**を呼び出します。 
    
2. メッセージ サービス用の行を検索し、 _lpuid_パラメーターで、 **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) の列を[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)に渡します。 
    
 **DeleteMsgService**は、MSG_SERVICE_DELETE に_ulContext_パラメーターを使用して、メッセージ サービスのエントリ ポイント関数を呼び出します。 メッセージ サービスは、プロファイルから削除される前に、この時点で、タスクのクリーンアップを実行します。 
  

