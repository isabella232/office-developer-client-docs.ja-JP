---
title: IOlkEnumSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e83e409c-f201-df9d-5e30-879adf15318d
description: 列挙子内のアカウントの指定した数をスキップします。
ms.openlocfilehash: 2791f1204cedf5e91d13923e50dfc45b981b7e26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799486"
---
# <a name="iolkenumskip"></a><span data-ttu-id="0366d-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="0366d-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="0366d-104">列挙子内のアカウントの指定した数をスキップします。</span><span class="sxs-lookup"><span data-stu-id="0366d-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="0366d-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="0366d-105">Quick info</span></span>

<span data-ttu-id="0366d-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0366d-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="0366d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0366d-107">Parameters</span></span>

<span data-ttu-id="0366d-108">_cSkip_</span><span class="sxs-lookup"><span data-stu-id="0366d-108">_cSkip_</span></span>
  
> <span data-ttu-id="0366d-109">[in]スキップするアカウントの数です。</span><span class="sxs-lookup"><span data-stu-id="0366d-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="0366d-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="0366d-110">Return values</span></span>

<span data-ttu-id="0366d-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="0366d-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0366d-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="0366d-112">See also</span></span>

- [<span data-ttu-id="0366d-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="0366d-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="0366d-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="0366d-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="0366d-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="0366d-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

