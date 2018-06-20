---
title: IOlkAccountHelperGetMapiSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a431787c-6e9a-9be1-165f-98c778d12e3e
description: MAPI セッションを開くし、アカウント マネージャーのセッションへの参照を保持します。
ms.openlocfilehash: 50809a00d13fd9f2a93bebc2961a134b3625e82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799483"
---
# <a name="iolkaccounthelpergetmapisession"></a><span data-ttu-id="e572b-103">IOlkAccountHelper::GetMapiSession</span><span class="sxs-lookup"><span data-stu-id="e572b-103">IOlkAccountHelper::GetMapiSession</span></span>

<span data-ttu-id="e572b-104">MAPI セッションを開くし、アカウント マネージャーのセッションへの参照を保持します。</span><span class="sxs-lookup"><span data-stu-id="e572b-104">Opens a MAPI session and maintains a reference to the session for the account manager.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e572b-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e572b-105">Quick info</span></span>

<span data-ttu-id="e572b-106">[IOlkAccountHelper](iolkaccounthelper.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e572b-106">See [IOlkAccountHelper](iolkaccounthelper.md).</span></span>
  
```cpp
HRESULT IOlkAccountHelper::GetMapiSession(  
    LPUNKNOWN *ppmsess 
);
```

## <a name="parameters"></a><span data-ttu-id="e572b-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e572b-107">Parameters</span></span>

<span data-ttu-id="e572b-108">_ppmsess_</span><span class="sxs-lookup"><span data-stu-id="e572b-108">_ppmsess_</span></span>
  
> <span data-ttu-id="e572b-109">[out]現在の MAPI セッションです。</span><span class="sxs-lookup"><span data-stu-id="e572b-109">[out] The current MAPI session.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e572b-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e572b-110">Return values</span></span>

<span data-ttu-id="e572b-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="e572b-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e572b-112">解釈</span><span class="sxs-lookup"><span data-stu-id="e572b-112">Remarks</span></span>

<span data-ttu-id="e572b-113">循環参照の問題があるため、アカウント マネージャー自体は MAPI セッションの参照を維持できません。</span><span class="sxs-lookup"><span data-stu-id="e572b-113">Because of circular reference problems, the account manager itself cannot maintain the reference for the MAPI session.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e572b-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e572b-114">See also</span></span>

- [<span data-ttu-id="e572b-115">IOlkAccountHelper::HandsOffSession</span><span class="sxs-lookup"><span data-stu-id="e572b-115">IOlkAccountHelper::HandsOffSession</span></span>](iolkaccounthelper-handsoffsession.md)
- [<span data-ttu-id="e572b-116">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e572b-116">IMAPISession : IUnknown</span></span>](http://msdn.microsoft.com/library/5650fa2a-6e62-451c-964e-363f7bee2344%28Office.15%29.aspx)

