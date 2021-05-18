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
# <a name="adding-a-message-service"></a><span data-ttu-id="091e8-103">メッセージ サービスの追加</span><span class="sxs-lookup"><span data-stu-id="091e8-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="091e8-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="091e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="091e8-105">**プロファイルに新しいメッセージ サービスを追加し、新しいメッセージ サービスにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="091e8-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="091e8-106">[IMsgServiceAdmin2::CreateMsgServiceEx を呼び出します](imsgserviceadmin2-createmsgserviceex.md)。</span><span class="sxs-lookup"><span data-stu-id="091e8-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="091e8-107">**CreateMsgServiceEx は** 、次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="091e8-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="091e8-108">MAPISVC にあるメッセージ サービスに関連するすべての情報をコピーします。INF ファイル。プロバイダー セクションごとにプロファイル セクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="091e8-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="091e8-109">_ulContext_ パラメーターを指定して、メッセージ サービスのエントリ ポイント関数 **MSGSERVICEENTRY** を呼び出MSG_SERVICE_CREATE。</span><span class="sxs-lookup"><span data-stu-id="091e8-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="091e8-110">メッセージ サービスのプロパティ [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md) **PR_SERVICE_UIDを** 設定して取得します。</span><span class="sxs-lookup"><span data-stu-id="091e8-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="091e8-111">**新しく追加されたメッセージ サービスにアクセスするには**</span><span class="sxs-lookup"><span data-stu-id="091e8-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="091e8-112">メッセージ [サービス テーブルを取得するには、IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="091e8-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="091e8-113">メッセージ サービス テーブルの [IMAPITable::Advise](imapitable-advise.md) メソッドを呼び出して、テーブル通知に登録します。</span><span class="sxs-lookup"><span data-stu-id="091e8-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="091e8-114">MAPI が通知を送信TABLE_ROW_ADDED、新しく追加されたメッセージ サービスのエントリ識別子を、新しいメッセージ構造に含まれる [SRow](srow.md) 構造 [TABLE_NOTIFICATION](table_notification.md) します。</span><span class="sxs-lookup"><span data-stu-id="091e8-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

