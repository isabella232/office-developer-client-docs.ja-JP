---
title: IEnumFBBlockSkip
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 70fbdb41-46ea-d016-25a2-37e94962095d
description: 空き時間情報データの指定した数のブロックをスキップします。
ms.openlocfilehash: cf8ae18b5ed2c24a48d44d9e8d461da7d95054d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425723"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="15b87-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="15b87-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="15b87-104">空き時間情報データの指定した数のブロックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="15b87-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="15b87-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="15b87-105">Quick info</span></span>

<span data-ttu-id="15b87-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="15b87-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="15b87-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15b87-107">Parameters</span></span>

<span data-ttu-id="15b87-108">_が大き_</span><span class="sxs-lookup"><span data-stu-id="15b87-108">_celt_</span></span>
  
>  <span data-ttu-id="15b87-109">順番スキップする空き時間ブロックの数。</span><span class="sxs-lookup"><span data-stu-id="15b87-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="15b87-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="15b87-110">Return values</span></span>

<span data-ttu-id="15b87-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="15b87-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15b87-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="15b87-112">See also</span></span>

- [<span data-ttu-id="15b87-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="15b87-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="15b87-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="15b87-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="15b87-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="15b87-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="15b87-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="15b87-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

