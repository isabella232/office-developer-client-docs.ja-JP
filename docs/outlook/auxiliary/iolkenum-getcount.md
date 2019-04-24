---
title: IOlkEnumGetCount
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dd7a7e62-4cf2-bdd3-8a00-4fff5ac575d3
description: 列挙子内のアカウントの数を取得します。
ms.openlocfilehash: 8571d5ff01501d980c8b6543607a658ad99085ca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322016"
---
# <a name="iolkenumgetcount"></a><span data-ttu-id="39a90-103">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="39a90-103">IOlkEnum::GetCount</span></span>

<span data-ttu-id="39a90-104">列挙子内のアカウントの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="39a90-104">Gets the number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="39a90-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="39a90-105">Quick info</span></span>

<span data-ttu-id="39a90-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="39a90-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::GetCount ( 
    DWORD *pulCount 
);

```

## <a name="parameters"></a><span data-ttu-id="39a90-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="39a90-107">Parameters</span></span>

<span data-ttu-id="39a90-108">_出てきた回数_</span><span class="sxs-lookup"><span data-stu-id="39a90-108">_pulCount_</span></span>
  
> <span data-ttu-id="39a90-109">読み上げ列挙されるオブジェクトの数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="39a90-109">[out] A pointer to the number of objects being enumerated.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="39a90-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="39a90-110">Return values</span></span>

<span data-ttu-id="39a90-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="39a90-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="39a90-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="39a90-112">See also</span></span>

- [<span data-ttu-id="39a90-113">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="39a90-113">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="39a90-114">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="39a90-114">IOlkEnum::Reset</span></span>](iolkenum-reset.md) 
- [<span data-ttu-id="39a90-115">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="39a90-115">IOlkEnum::Skip</span></span>](iolkenum-skip.md)

