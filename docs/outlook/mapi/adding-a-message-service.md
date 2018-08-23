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
# <a name="adding-a-message-service"></a><span data-ttu-id="8408e-103">メッセージ サービスの追加</span><span class="sxs-lookup"><span data-stu-id="8408e-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="8408e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8408e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8408e-105">**新しいメッセージ サービスをプロファイルに追加し、新しいメッセージ サービスへのアクセス**</span><span class="sxs-lookup"><span data-stu-id="8408e-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="8408e-106">[IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8408e-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="8408e-107">**CreateMsgServiceEx**は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="8408e-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="8408e-108">MAPISVC 内にあるメッセージ サービスに関連する情報のすべてをコピーします。INF ファイル、プロファイル プロバイダーのすべてのセクションのセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="8408e-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="8408e-109">メッセージ サービスのエントリ ポイント関数、 **MSGSERVICEENTRY**、 _ulContext_パラメーターを MSG_SERVICE_CREATE に設定が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8408e-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="8408e-110">設定し、メッセージ サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="8408e-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="8408e-111">**任意のメッセージを新たに追加されたサービスにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="8408e-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="8408e-112">メッセージ サービス テーブルを取得するために[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8408e-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="8408e-113">テーブルの通知を登録するのには、メッセージ サービス テーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8408e-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="8408e-114">MAPI では、TABLE_ROW_ADDED 通知を送信するときは、 [TABLE_NOTIFICATION](table_notification.md)構造体に含まれる[SRow](srow.md)構造体に新たに追加されたメッセージ サービスのエントリの識別子を探します。</span><span class="sxs-lookup"><span data-stu-id="8408e-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

