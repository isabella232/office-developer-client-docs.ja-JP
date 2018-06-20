---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: 列挙子では、アカウントの数を取得します。
ms.openlocfilehash: dd4152a898bdaa96883bcd27ab3ec0d94e80fd90
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799493"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="cd945-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="cd945-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="cd945-104">列挙子では、アカウントの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="cd945-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cd945-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="cd945-105">Quick info</span></span>

<span data-ttu-id="cd945-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd945-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="cd945-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="cd945-107">Parameters</span></span>

<span data-ttu-id="cd945-108">_pulCount_</span><span class="sxs-lookup"><span data-stu-id="cd945-108">_pulCount_</span></span>
  
> <span data-ttu-id="cd945-109">[out]列挙するオブジェクトの数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cd945-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="cd945-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="cd945-110">Return values</span></span>

<span data-ttu-id="cd945-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="cd945-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cd945-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd945-112">See also</span></span>

- [<span data-ttu-id="cd945-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="cd945-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="cd945-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="cd945-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="cd945-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="cd945-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

