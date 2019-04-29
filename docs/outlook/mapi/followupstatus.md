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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418331"
---
# <a name="followupstatus"></a><span data-ttu-id="15e8f-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="15e8f-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="15e8f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15e8f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15e8f-105">メッセージの別のフォローアップ状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="15e8f-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="15e8f-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="15e8f-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="15e8f-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="15e8f-107">Members</span></span>

 <span data-ttu-id="15e8f-108">_flwupnone_</span><span class="sxs-lookup"><span data-stu-id="15e8f-108">_flwupNone_</span></span>
  
> <span data-ttu-id="15e8f-109">フォローアップは指定されていません。</span><span class="sxs-lookup"><span data-stu-id="15e8f-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="15e8f-110">_flwupcomplete_</span><span class="sxs-lookup"><span data-stu-id="15e8f-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="15e8f-111">メッセージが完成しました。</span><span class="sxs-lookup"><span data-stu-id="15e8f-111">The message is complete.</span></span>
    
 <span data-ttu-id="15e8f-112">_flwupmarked_</span><span class="sxs-lookup"><span data-stu-id="15e8f-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="15e8f-113">メッセージには、フォローアップのマークが付けられます。</span><span class="sxs-lookup"><span data-stu-id="15e8f-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="15e8f-114">_flwupmax_</span><span class="sxs-lookup"><span data-stu-id="15e8f-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="15e8f-115">フォローアップに対してサポートされているさまざまな状態の数。</span><span class="sxs-lookup"><span data-stu-id="15e8f-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="15e8f-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="15e8f-116">See also</span></span>



[<span data-ttu-id="15e8f-117">PidTagFlagStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="15e8f-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

