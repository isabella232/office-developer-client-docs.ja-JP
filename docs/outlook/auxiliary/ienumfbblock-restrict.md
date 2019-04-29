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
# <a name="ienumfbblockrestrict"></a><span data-ttu-id="df995-103">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="df995-103">IEnumFBBlock::Restrict</span></span>

<span data-ttu-id="df995-104">列挙を指定した期間に制限します。</span><span class="sxs-lookup"><span data-stu-id="df995-104">Restricts the enumeration to a specified time period.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="df995-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="df995-105">Quick info</span></span>

<span data-ttu-id="df995-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df995-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Restrict(  
    FILETIME ftmStart, 
    FILETIME ftmEnd 
);

```

## <a name="parameters"></a><span data-ttu-id="df995-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="df995-107">Parameters</span></span>

<span data-ttu-id="df995-108">_ftmstart_</span><span class="sxs-lookup"><span data-stu-id="df995-108">_ftmStart_</span></span>
  
>  <span data-ttu-id="df995-109">順番列挙を制限する開始時刻。</span><span class="sxs-lookup"><span data-stu-id="df995-109">[in] The start time to restrict the enumeration.</span></span> 
    
<span data-ttu-id="df995-110">_ftmEnd_</span><span class="sxs-lookup"><span data-stu-id="df995-110">_ftmEnd_</span></span>
  
> <span data-ttu-id="df995-111">順番列挙を制限する終了時刻。</span><span class="sxs-lookup"><span data-stu-id="df995-111">[in] The end time to restrict the enumeration.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="df995-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="df995-112">Return values</span></span>

<span data-ttu-id="df995-113">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="df995-113">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df995-114">注釈</span><span class="sxs-lookup"><span data-stu-id="df995-114">Remarks</span></span>

<span data-ttu-id="df995-115">このメソッドは、列挙をリセットすることもできます。</span><span class="sxs-lookup"><span data-stu-id="df995-115">This method also resets the enumeration.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df995-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="df995-116">See also</span></span>

- [<span data-ttu-id="df995-117">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="df995-117">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="df995-118">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="df995-118">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="df995-119">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="df995-119">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="df995-120">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="df995-120">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)  
- [<span data-ttu-id="df995-121">空き時間情報データにアクセスするのに相対時間を使用する</span><span class="sxs-lookup"><span data-stu-id="df995-121">Use relative time to access free/busy data</span></span>](how-to-use-relative-time-to-access-free-busy-data.md)

