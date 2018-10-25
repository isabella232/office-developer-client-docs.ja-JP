---
title: 起動時に特定のメソッドを回避
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '最終更新日: 2015 年 12 月 7 日'
ms.openlocfilehash: 5d26583ad7ad3b4a200daf321a8994e302b75a79
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580636"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="7b5b2-103">起動時に特定のメソッドを回避</span><span class="sxs-lookup"><span data-stu-id="7b5b2-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="7b5b2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b5b2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b5b2-105">起動時のパフォーマンスを向上させるには、次の呼び出しを避けてください。</span><span class="sxs-lookup"><span data-stu-id="7b5b2-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="7b5b2-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="7b5b2-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="7b5b2-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="7b5b2-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="7b5b2-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="7b5b2-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="7b5b2-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="7b5b2-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="7b5b2-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="7b5b2-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="7b5b2-111">**IMAPIStatus::ValidateState** の呼び出しは、MAPI スプーラーまたは MAPI サブシステムのいずれかで行われた場合のみ、パフォーマンスに影響します。</span><span class="sxs-lookup"><span data-stu-id="7b5b2-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="7b5b2-112">これらのメソッドが起動処理を遅らせるのは、MAPI スプーラーが起動タスクを完了するまでそのメソッドが完了できないためです。</span><span class="sxs-lookup"><span data-stu-id="7b5b2-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="7b5b2-113">また、起動時のメッセージ ストアの検索も避ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b5b2-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="7b5b2-114">起動処理が終わってから、[IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) の呼び出しを行ってください。</span><span class="sxs-lookup"><span data-stu-id="7b5b2-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

