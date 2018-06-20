---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: 指定した期間内に列挙型を制限します。
ms.openlocfilehash: 6b07fe52a84d6a808ab7400ff3e8982b1cce51ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799325"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="76f94-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="76f94-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="76f94-104">指定した期間内に列挙型を制限します。</span><span class="sxs-lookup"><span data-stu-id="76f94-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="76f94-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="76f94-105">Quick info</span></span>

<span data-ttu-id="76f94-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="76f94-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="76f94-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="76f94-107">Parameters</span></span>

<span data-ttu-id="76f94-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="76f94-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="76f94-109">[in]列挙を制限するのには開始時刻です。</span><span class="sxs-lookup"><span data-stu-id="76f94-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="76f94-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="76f94-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="76f94-111">[in]列挙を制限するのには終了時間です。</span><span class="sxs-lookup"><span data-stu-id="76f94-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="76f94-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="76f94-112">Return values</span></span>

<span data-ttu-id="76f94-113">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="76f94-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76f94-114">解釈</span><span class="sxs-lookup"><span data-stu-id="76f94-114">Remarks</span></span>

<span data-ttu-id="76f94-115">このメソッドは、列挙体をリセットします。</span><span class="sxs-lookup"><span data-stu-id="76f94-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="76f94-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="76f94-116">See also</span></span>

- [<span data-ttu-id="76f94-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="76f94-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="76f94-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="76f94-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="76f94-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="76f94-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="76f94-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="76f94-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="76f94-121">空き時間情報データにアクセスする相対時間を使用します。</span><span class="sxs-lookup"><span data-stu-id="76f94-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

