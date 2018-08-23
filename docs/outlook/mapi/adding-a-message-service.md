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
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799626"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="9afde-103">メッセージ サービスの追加</span><span class="sxs-lookup"><span data-stu-id="9afde-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="9afde-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9afde-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="9afde-105">**新しいメッセージ サービスをプロファイルに追加し、新しいメッセージ サービスへのアクセス**</span><span class="sxs-lookup"><span data-stu-id="9afde-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="9afde-106">[IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9afde-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="9afde-107">**CreateMsgServiceEx**は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="9afde-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="9afde-108">MAPISVC 内にあるメッセージ サービスに関連する情報のすべてをコピーします。INF ファイル、プロファイル プロバイダーのすべてのセクションのセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="9afde-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="9afde-109">メッセージ サービスのエントリ ポイント関数、 **MSGSERVICEENTRY**、 _ulContext_パラメーターを MSG_SERVICE_CREATE に設定が呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9afde-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="9afde-110">設定し、メッセージ サービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) のプロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="9afde-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="9afde-111">**任意のメッセージを新たに追加されたサービスにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="9afde-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="9afde-112">メッセージ サービス テーブルを取得するために[IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9afde-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="9afde-113">テーブルの通知を登録するのには、メッセージ サービス テーブルの[IMAPITable::Advise](imapitable-advise.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9afde-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="9afde-114">MAPI では、TABLE_ROW_ADDED 通知を送信するときは、 [TABLE_NOTIFICATION](table_notification.md)構造体に含まれる[SRow](srow.md)構造体に新たに追加されたメッセージ サービスのエントリの識別子を探します。</span><span class="sxs-lookup"><span data-stu-id="9afde-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

