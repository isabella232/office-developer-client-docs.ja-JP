---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: IOlkAccountManager インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: 85ba4d0d47eb5c879fa562e3147860533ef59f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799464"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="cf097-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="cf097-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="cf097-104">[IOlkAccountManager](iolkaccountmanager.md)インターフェイスによって割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="cf097-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="cf097-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cf097-105">Quick info</span></span>

<span data-ttu-id="cf097-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="cf097-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="cf097-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cf097-107">Parameters</span></span>

<span data-ttu-id="cf097-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="cf097-108">_pv_</span></span>
  
> <span data-ttu-id="cf097-109">[in]解放するメモリへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf097-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="cf097-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="cf097-110">Return values</span></span>

<span data-ttu-id="cf097-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="cf097-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf097-112">解釈</span><span class="sxs-lookup"><span data-stu-id="cf097-112">Remarks</span></span>

<span data-ttu-id="cf097-113">[IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)によって割り当てられたメモリを解放するのにには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf097-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cf097-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf097-114">See also</span></span>

- [<span data-ttu-id="cf097-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="cf097-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

