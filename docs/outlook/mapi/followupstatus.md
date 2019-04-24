---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2280ae9271ca73af33f395bf9e41a9ee8fa62f96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327525"
---
# <a name="followupstatus"></a><span data-ttu-id="eb1ac-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="eb1ac-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="eb1ac-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb1ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb1ac-105">メッセージの別のフォローアップ状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="eb1ac-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="eb1ac-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="eb1ac-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="eb1ac-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="eb1ac-107">Members</span></span>

 <span data-ttu-id="eb1ac-108">_flwupnone_</span><span class="sxs-lookup"><span data-stu-id="eb1ac-108">_flwupNone_</span></span>
  
> <span data-ttu-id="eb1ac-109">フォローアップは指定されていません。</span><span class="sxs-lookup"><span data-stu-id="eb1ac-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="eb1ac-110">_flwupcomplete_</span><span class="sxs-lookup"><span data-stu-id="eb1ac-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="eb1ac-111">メッセージが完成しました。</span><span class="sxs-lookup"><span data-stu-id="eb1ac-111">The message is complete.</span></span>
    
 <span data-ttu-id="eb1ac-112">_flwupmarked_</span><span class="sxs-lookup"><span data-stu-id="eb1ac-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="eb1ac-113">メッセージには、フォローアップのマークが付けられます。</span><span class="sxs-lookup"><span data-stu-id="eb1ac-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="eb1ac-114">_flwupmax_</span><span class="sxs-lookup"><span data-stu-id="eb1ac-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="eb1ac-115">フォローアップに対してサポートされているさまざまな状態の数。</span><span class="sxs-lookup"><span data-stu-id="eb1ac-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="eb1ac-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb1ac-116">See also</span></span>



[<span data-ttu-id="eb1ac-117">PidTagFlagStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="eb1ac-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

