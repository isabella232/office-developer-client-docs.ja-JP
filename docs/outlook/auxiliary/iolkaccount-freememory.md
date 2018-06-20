---
title: IOlkAccountFreeMemory
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b2ee5aa-7639-d86d-447e-50bda54aa3ec
description: IOlkAccount インターフェイスによって割り当てられたメモリを解放します。
ms.openlocfilehash: ce3046db29cb2cac7d7ee72a3e4e9125346a4ac4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799408"
---
# <a name="iolkaccountfreememory"></a><span data-ttu-id="e9d72-103">IOlkAccount::FreeMemory</span><span class="sxs-lookup"><span data-stu-id="e9d72-103">IOlkAccount::FreeMemory</span></span>

<span data-ttu-id="e9d72-104">[IOlkAccount](iolkaccount.md)インターフェイスによって割り当てられたメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="e9d72-104">Frees memory allocated by the [IOlkAccount](iolkaccount.md) interface.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e9d72-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="e9d72-105">Quick info</span></span>

<span data-ttu-id="e9d72-106">[IOlkAccount](iolkaccount.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9d72-106">See [IOlkAccount](iolkaccount.md).</span></span>
  
```cpp
HRESULT IOlkAccount::FreeMemory (  
    BYTE *pv, 
); 

```

## <a name="parameters"></a><span data-ttu-id="e9d72-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e9d72-107">Parameters</span></span>

<span data-ttu-id="e9d72-108">_pv_</span><span class="sxs-lookup"><span data-stu-id="e9d72-108">_pv_</span></span>
  
> <span data-ttu-id="e9d72-109">[in]解放するメモリへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e9d72-109">[in] A pointer to memory to be freed.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="e9d72-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e9d72-110">Return values</span></span>

<span data-ttu-id="e9d72-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="e9d72-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e9d72-112">解釈</span><span class="sxs-lookup"><span data-stu-id="e9d72-112">Remarks</span></span>

<span data-ttu-id="e9d72-113">[IOlkAccount::GetProp](iolkaccount-getprop.md) (指定されたアカウントのプロパティの値がバイナリまたは文字列型の場合) および[IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md)によって割り当てられたメモリを解放は、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e9d72-113">Use this method to free memory allocated by [IOlkAccount::GetProp](iolkaccount-getprop.md) (if the value of the specified account property is a binary or string type) and [IOlkAccount::GetAccountInfo](iolkaccount-getaccountinfo.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e9d72-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9d72-114">See also</span></span>

- [<span data-ttu-id="e9d72-115">IOlkAccount::GetAccountInfo</span><span class="sxs-lookup"><span data-stu-id="e9d72-115">IOlkAccount::GetAccountInfo</span></span>](iolkaccount-getaccountinfo.md)  
- [<span data-ttu-id="e9d72-116">IOlkAccount::GetProp</span><span class="sxs-lookup"><span data-stu-id="e9d72-116">IOlkAccount::GetProp</span></span>](iolkaccount-getprop.md)

