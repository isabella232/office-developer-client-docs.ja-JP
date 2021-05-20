---
title: IEnumFBBlockRestrict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 887cea55-8f1c-45ec-3100-d03e1213d7c9
description: 列挙を指定した期間に制限します。
ms.openlocfilehash: e7f7a5d846d13422f9ed79ef26f1b9b0008463f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431947"
---
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="fe691-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="fe691-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="fe691-104">列挙を指定した期間に制限します。</span><span class="sxs-lookup"><span data-stu-id="fe691-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fe691-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="fe691-105">Quick info</span></span>

<span data-ttu-id="fe691-106">[「IEnumFBBlock」を参照](ienumfbblock.md)してください。</span><span class="sxs-lookup"><span data-stu-id="fe691-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="fe691-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="fe691-107">Parameters</span></span>

<span data-ttu-id="fe691-108">_ftmStart_</span><span class="sxs-lookup"><span data-stu-id="fe691-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="fe691-109">[in]列挙を制限する開始時刻。</span><span class="sxs-lookup"><span data-stu-id="fe691-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="fe691-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="fe691-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="fe691-111">[in]列挙を制限する終了時刻。</span><span class="sxs-lookup"><span data-stu-id="fe691-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="fe691-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="fe691-112">Return values</span></span>

<span data-ttu-id="fe691-113">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="fe691-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fe691-114">注釈</span><span class="sxs-lookup"><span data-stu-id="fe691-114">Remarks</span></span>

<span data-ttu-id="fe691-115">また、このメソッドは列挙をリセットします。</span><span class="sxs-lookup"><span data-stu-id="fe691-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fe691-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="fe691-116">See also</span></span>

- [<span data-ttu-id="fe691-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="fe691-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="fe691-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="fe691-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="fe691-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="fe691-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="fe691-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="fe691-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="fe691-121">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="fe691-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

