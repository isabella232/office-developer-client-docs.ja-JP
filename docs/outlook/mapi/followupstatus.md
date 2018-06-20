---
title: FollowUpStatus
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c3d0f6c4-4597-784f-8d44-6e5d905895b4
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: e59c0ba7810741943883b9e86e84c6fe141f3050
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800084"
---
# <a name="followupstatus"></a><span data-ttu-id="7bf1e-103">FollowUpStatus</span><span class="sxs-lookup"><span data-stu-id="7bf1e-103">FollowUpStatus</span></span>

  
  
<span data-ttu-id="7bf1e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7bf1e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7bf1e-105">メッセージの別のフォロー アップのステータスを指定します。</span><span class="sxs-lookup"><span data-stu-id="7bf1e-105">Specifies the different follow-up statuses for a message.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7bf1e-106">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="7bf1e-106">Quick info</span></span>

```cpp
enum FollowUpStatus { 
    flwupNone = 0, 
    flwupComplete, 
    flwupMarked, 
    flwupMAX}; 

```

## <a name="members"></a><span data-ttu-id="7bf1e-107">メンバー</span><span class="sxs-lookup"><span data-stu-id="7bf1e-107">Members</span></span>

 <span data-ttu-id="7bf1e-108">_flwupNone_</span><span class="sxs-lookup"><span data-stu-id="7bf1e-108">_flwupNone_</span></span>
  
> <span data-ttu-id="7bf1e-109">フラグが指定されていません。</span><span class="sxs-lookup"><span data-stu-id="7bf1e-109">No follow-up has been specified.</span></span>
    
 <span data-ttu-id="7bf1e-110">_flwupComplete_</span><span class="sxs-lookup"><span data-stu-id="7bf1e-110">_flwupComplete_</span></span>
  
> <span data-ttu-id="7bf1e-111">メッセージは完了です。</span><span class="sxs-lookup"><span data-stu-id="7bf1e-111">The message is complete.</span></span>
    
 <span data-ttu-id="7bf1e-112">_flwupMarked_</span><span class="sxs-lookup"><span data-stu-id="7bf1e-112">_flwupMarked_</span></span>
  
> <span data-ttu-id="7bf1e-113">メッセージは、フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="7bf1e-113">The message is marked for follow-up.</span></span>
    
 <span data-ttu-id="7bf1e-114">_flwupMAX_</span><span class="sxs-lookup"><span data-stu-id="7bf1e-114">_flwupMAX_</span></span>
  
> <span data-ttu-id="7bf1e-115">フォロー アップのためにサポートされている別の状態の数です。</span><span class="sxs-lookup"><span data-stu-id="7bf1e-115">The number of different statuses supported for follow-up.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7bf1e-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="7bf1e-116">See also</span></span>



[<span data-ttu-id="7bf1e-117">PidTagFlagStatus の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="7bf1e-117">PidTagFlagStatus Canonical Property</span></span>](pidtagflagstatus-canonical-property.md)

