---
title: メッセージ サービスの削除
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 346608d7-f7de-497e-9852-4d4d7696177e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f39f721d434f4e54cbfa5d25a3ba626858f2b13e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583569"
---
# <a name="deleting-a-message-service"></a><span data-ttu-id="d4e28-103">メッセージ サービスの削除</span><span class="sxs-lookup"><span data-stu-id="d4e28-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="d4e28-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d4e28-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="d4e28-105">**メッセージ サービスをプロファイルから削除するのには**</span><span class="sxs-lookup"><span data-stu-id="d4e28-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="d4e28-106">メッセージ サービス テーブルにアクセスするのには**IMAPISession::GetMsgServiceTable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d4e28-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="d4e28-107">メッセージ サービス用の行を検索し、 _lpuid_パラメーターで、 **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) の列を[IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md)に渡します。</span><span class="sxs-lookup"><span data-stu-id="d4e28-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="d4e28-108">**DeleteMsgService**は、MSG_SERVICE_DELETE に_ulContext_パラメーターを使用して、メッセージ サービスのエントリ ポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d4e28-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="d4e28-109">メッセージ サービスは、プロファイルから削除される前に、この時点で、タスクのクリーンアップを実行します。</span><span class="sxs-lookup"><span data-stu-id="d4e28-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

