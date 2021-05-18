---
title: IOlkAccountManagerFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: acb67186-ab38-e918-5402-2526307a5bd0
description: IOlkAccountManager インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: 3e680e1e26d6c9b12c2dd4a7d48df4dbeae14154
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408489"
---
# <a name="iolkaccountmanagerfreememory"></a><span data-ttu-id="66fba-103">IOlkAccountManager::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="66fba-103">IOlkAccountManager::FreeMemory</span></span>

<span data-ttu-id="66fba-104">[IOlkAccountManager インターフェイスによって割り当てられたメモリを解放](iolkaccountmanager.md)します。</span><span class="sxs-lookup"><span data-stu-id="66fba-104">Frees memory allocated by the [IOlkAccountManager](iolkaccountmanager.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="66fba-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="66fba-105">Quick info</span></span>

<span data-ttu-id="66fba-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="66fba-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::FreeMemory (  
    BYTE *pv, 
);
```

## <a name="parameters"></a><span data-ttu-id="66fba-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="66fba-107">Parameters</span></span>

<span data-ttu-id="66fba-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="66fba-108">_pv_</span></span>
  
> <span data-ttu-id="66fba-109">[in]空きメモリへのポインター。</span><span class="sxs-lookup"><span data-stu-id="66fba-109">[in] A pointer to the memory to free.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="66fba-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="66fba-110">Return values</span></span>

<span data-ttu-id="66fba-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="66fba-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66fba-112">注釈</span><span class="sxs-lookup"><span data-stu-id="66fba-112">Remarks</span></span>

<span data-ttu-id="66fba-113">[IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md)によって割り当てられたメモリを解放するには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="66fba-113">Use this method to release memory allocated by [IOlkAccountManager::GetOrder](iolkaccountmanager-getorder.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66fba-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="66fba-114">See also</span></span>

- [<span data-ttu-id="66fba-115">IOlkAccountManager::GetOrder</span><span class="sxs-lookup"><span data-stu-id="66fba-115">IOlkAccountManager::GetOrder</span></span>](iolkaccountmanager-getorder.md)

