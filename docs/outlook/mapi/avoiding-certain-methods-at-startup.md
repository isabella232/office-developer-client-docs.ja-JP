---
title: 起動時に特定のメソッドを回避
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: '�ŏI�X�V��: 2015�N12��7��'
ms.openlocfilehash: db327fdd239684140e4feeeb2a6045a2fcd5c410
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799741"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="30ca9-103">起動時に特定のメソッドを回避</span><span class="sxs-lookup"><span data-stu-id="30ca9-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="30ca9-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30ca9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="30ca9-105">起動時にパフォーマンスを向上させるには、次の呼び出しを回避します。</span><span class="sxs-lookup"><span data-stu-id="30ca9-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="30ca9-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="30ca9-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="30ca9-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="30ca9-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="30ca9-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="30ca9-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="30ca9-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="30ca9-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="30ca9-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="30ca9-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="30ca9-111">**IMAPIStatus::ValidateState**への呼び出しでは、MAPI スプーラーを無効または MAPI のサブシステムのいずれかで行われるときにのみ、パフォーマンスに影響します。</span><span class="sxs-lookup"><span data-stu-id="30ca9-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="30ca9-112">これらのメソッドが起動処理を遅く理由は、MAPI スプーラーが、起動時のタスクを完了するまでに完了することはできませんのでです。</span><span class="sxs-lookup"><span data-stu-id="30ca9-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="30ca9-113">起動時にメッセージ ・ ストアを検索しないようにします。</span><span class="sxs-lookup"><span data-stu-id="30ca9-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="30ca9-114">起動処理が終了したときに、 [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md)の呼び出しを確認します。</span><span class="sxs-lookup"><span data-stu-id="30ca9-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

