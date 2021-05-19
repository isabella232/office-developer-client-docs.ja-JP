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
# <a name="followupstatus"></a><span data-ttu-id="f1520-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="f1520-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="f1520-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1520-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1520-105">メッセージの別のフォローアップ状態を指定します。</span><span class="sxs-lookup"><span data-stu-id="f1520-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f1520-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="f1520-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="f1520-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="f1520-107">Members</span></span>

 <span data-ttu-id="f1520-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="f1520-108">_flwupNone_</span></span>
  
> <span data-ttu-id="f1520-109">フォローアップが指定されていません。</span><span class="sxs-lookup"><span data-stu-id="f1520-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="f1520-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="f1520-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="f1520-111">メッセージが完了しました。</span><span class="sxs-lookup"><span data-stu-id="f1520-111">The message is complete.</span></span>
    
 <span data-ttu-id="f1520-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="f1520-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="f1520-113">メッセージにはフォローアップのマークが付きます。</span><span class="sxs-lookup"><span data-stu-id="f1520-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="f1520-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="f1520-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="f1520-115">フォローアップでサポートされるさまざまな状態の数。</span><span class="sxs-lookup"><span data-stu-id="f1520-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f1520-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1520-116">See also</span></span>



[<span data-ttu-id="f1520-117">PidTagFlagStatus 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="f1520-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

