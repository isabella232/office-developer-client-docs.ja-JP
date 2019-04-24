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
# <a name="deleting-a-message-service"></a><span data-ttu-id="2d16a-103">メッセージサービスの削除</span><span class="sxs-lookup"><span data-stu-id="2d16a-103">Deleting a Message Service</span></span>

  
  
<span data-ttu-id="2d16a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d16a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2d16a-105">**メッセージサービスをプロファイルから削除するには**</span><span class="sxs-lookup"><span data-stu-id="2d16a-105">**To delete a message service from a profile**</span></span>
  
1. <span data-ttu-id="2d16a-106">メッセージサービステーブルにアクセスするには、 **imapisession:: getmsgservicetable**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2d16a-106">Call **IMAPISession::GetMsgServiceTable** to access the message service table.</span></span> 
    
2. <span data-ttu-id="2d16a-107">メッセージサービスの行を探し、 _lpuid_パラメーターの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) 列を[IMsgServiceAdmin::D eletemsgservice](imsgserviceadmin-deletemsgservice.md)に渡します。</span><span class="sxs-lookup"><span data-stu-id="2d16a-107">Locate the row for the message service and pass its **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) column in the  _lpuid_ parameter to [IMsgServiceAdmin::DeleteMsgService](imsgserviceadmin-deletemsgservice.md).</span></span> 
    
 <span data-ttu-id="2d16a-108">**DeleteMsgService**は、 _ulcontext_パラメーターを MSG_SERVICE_DELETE に設定して、メッセージサービスのエントリポイント関数を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="2d16a-108">**DeleteMsgService** calls the message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_DELETE.</span></span> <span data-ttu-id="2d16a-109">メッセージサービスプロファイルから削除される前に、この時点でクリーンアップタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="2d16a-109">Message services perform any clean up tasks at this time before they are removed from the profile.</span></span> 
  

