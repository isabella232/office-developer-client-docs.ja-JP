---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: 列挙子内の指定された数のアカウントをスキップします。
ms.openlocfilehash: d4063b0ff4852e6932cf50789eea3caa81d4d586
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404779"
---
# <a name="iolkenumskip"></a><span data-ttu-id="cc6b3-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="cc6b3-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="cc6b3-104">列挙子内の指定された数のアカウントをスキップします。</span><span class="sxs-lookup"><span data-stu-id="cc6b3-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cc6b3-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cc6b3-105">Quick info</span></span>

<span data-ttu-id="cc6b3-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cc6b3-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="cc6b3-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cc6b3-107">Parameters</span></span>

<span data-ttu-id="cc6b3-108">_cskip_</span><span class="sxs-lookup"><span data-stu-id="cc6b3-108">_cSkip_</span></span>
  
> <span data-ttu-id="cc6b3-109">順番スキップするアカウントの数。</span><span class="sxs-lookup"><span data-stu-id="cc6b3-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="cc6b3-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="cc6b3-110">Return values</span></span>

<span data-ttu-id="cc6b3-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="cc6b3-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cc6b3-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="cc6b3-112">See also</span></span>

- [<span data-ttu-id="cc6b3-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="cc6b3-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="cc6b3-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="cc6b3-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="cc6b3-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="cc6b3-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

