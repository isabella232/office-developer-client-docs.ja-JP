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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321988"
---
# <a name="iolkenumskip"></a><span data-ttu-id="ce51c-103">IOlkEnum::Skip</span><span class="sxs-lookup"><span data-stu-id="ce51c-103">IOlkEnum::Skip</span></span>

<span data-ttu-id="ce51c-104">列挙子内の指定された数のアカウントをスキップします。</span><span class="sxs-lookup"><span data-stu-id="ce51c-104">Skips a specified number of accounts in the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ce51c-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="ce51c-105">Quick info</span></span>

<span data-ttu-id="ce51c-106">[IOlkEnum](iolkenum.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ce51c-106">See [IOlkEnum](iolkenum.md).</span></span>
  
```cpp
HRESULT IOlkEnum::Skip(  
    DWORD cSkip 
);
```

## <a name="parameters"></a><span data-ttu-id="ce51c-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ce51c-107">Parameters</span></span>

<span data-ttu-id="ce51c-108">_cskip_</span><span class="sxs-lookup"><span data-stu-id="ce51c-108">_cSkip_</span></span>
  
> <span data-ttu-id="ce51c-109">順番スキップするアカウントの数。</span><span class="sxs-lookup"><span data-stu-id="ce51c-109">[in] The number of accounts to be skipped.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="ce51c-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="ce51c-110">Return values</span></span>

<span data-ttu-id="ce51c-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="ce51c-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce51c-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="ce51c-112">See also</span></span>

- [<span data-ttu-id="ce51c-113">IOlkEnum::GetCount</span><span class="sxs-lookup"><span data-stu-id="ce51c-113">IOlkEnum::GetCount</span></span>](iolkenum-getcount.md) 
- [<span data-ttu-id="ce51c-114">IOlkEnum::GetNext</span><span class="sxs-lookup"><span data-stu-id="ce51c-114">IOlkEnum::GetNext</span></span>](iolkenum-getnext.md)  
- [<span data-ttu-id="ce51c-115">IOlkEnum::Reset</span><span class="sxs-lookup"><span data-stu-id="ce51c-115">IOlkEnum::Reset</span></span>](iolkenum-reset.md)

