---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: IOlkAccount インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: a7f763ba4fc260a517f8b7df4d3791f4a8fd23b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406200"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="66dfe-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="66dfe-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="66dfe-104">[IOlkAccount](iolkaccount.md)インターフェイスによって割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="66dfe-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="66dfe-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="66dfe-105">Quick info</span></span>

<span data-ttu-id="66dfe-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="66dfe-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="66dfe-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="66dfe-107">Parameters</span></span>

<span data-ttu-id="66dfe-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="66dfe-108">_pv_</span></span>
  
> <span data-ttu-id="66dfe-109">順番解放するメモリへのポインター。</span><span class="sxs-lookup"><span data-stu-id="66dfe-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="66dfe-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="66dfe-110">Return values</span></span>

<span data-ttu-id="66dfe-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="66dfe-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66dfe-112">注釈</span><span class="sxs-lookup"><span data-stu-id="66dfe-112">Remarks</span></span>

<span data-ttu-id="66dfe-113">このメソッドを使用して、 [IOlkAccount:: getprop](iolkaccount-getprop.md) (指定した account プロパティの値がバイナリまたは文字列型の場合) および[IOlkAccount:: getaccountinfo](iolkaccount-getaccountinfo.md)で割り当てられているメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="66dfe-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="66dfe-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="66dfe-114">See also</span></span>

- [<span data-ttu-id="66dfe-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="66dfe-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="66dfe-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="66dfe-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

