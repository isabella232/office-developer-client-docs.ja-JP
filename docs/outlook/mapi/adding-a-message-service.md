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
# <a name="adding-a-message-service"></a><span data-ttu-id="70089-103">メッセージサービスを追加する</span><span class="sxs-lookup"><span data-stu-id="70089-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="70089-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70089-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="70089-105">**新しいメッセージサービスをプロファイルに追加して、新しいメッセージサービスにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="70089-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="70089-106">[IMsgServiceAdmin2:: CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="70089-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="70089-107">**CreateMsgServiceEx**は、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="70089-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="70089-108">mapisvc.inf に含まれるメッセージサービスの関連情報をすべてコピーします。INF ファイル。すべてのプロバイダーセクションのプロファイルセクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="70089-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="70089-109">_ulcontext_パラメーターを MSG_SERVICE_CREATE に設定して、メッセージサービスのエントリポイント関数**msgserviceentry**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="70089-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="70089-110">メッセージサービスの**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) プロパティを設定および取得します。</span><span class="sxs-lookup"><span data-stu-id="70089-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="70089-111">**新しく追加されたメッセージサービスにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="70089-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="70089-112">message service テーブルを取得するには、 [IMsgServiceAdmin:: getmsgservicetable](imsgserviceadmin-getmsgservicetable.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="70089-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="70089-113">メッセージサービステーブルの[IMAPITable:: アドバイズ](imapitable-advise.md)メソッドを呼び出して、テーブル通知の登録を行います。</span><span class="sxs-lookup"><span data-stu-id="70089-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="70089-114">MAPI が TABLE_ROW_ADDED 通知を送信する場合は、 [TABLE_NOTIFICATION](table_notification.md)構造に含まれている[srow](srow.md)構造で新しく追加されたメッセージサービスのエントリ識別子を見つけます。</span><span class="sxs-lookup"><span data-stu-id="70089-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

