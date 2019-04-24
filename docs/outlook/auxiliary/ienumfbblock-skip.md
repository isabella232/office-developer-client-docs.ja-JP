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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317550"
---
# <a name="ienumfbblockskip"></a><span data-ttu-id="b4cc0-103">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="b4cc0-103">IEnumFBBlock::Skip</span></span>

<span data-ttu-id="b4cc0-104">空き時間情報データの指定した数のブロックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="b4cc0-104">Skips a specified number of blocks of free/busy data.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b4cc0-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b4cc0-105">Quick info</span></span>

<span data-ttu-id="b4cc0-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4cc0-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Skip(  
    LONG celt 
);
```

## <a name="parameters"></a><span data-ttu-id="b4cc0-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b4cc0-107">Parameters</span></span>

<span data-ttu-id="b4cc0-108">_が大き_</span><span class="sxs-lookup"><span data-stu-id="b4cc0-108">_celt_</span></span>
  
>  <span data-ttu-id="b4cc0-109">順番スキップする空き時間ブロックの数。</span><span class="sxs-lookup"><span data-stu-id="b4cc0-109">[in] The number of free/busy blocks to skip.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b4cc0-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="b4cc0-110">Return values</span></span>

<span data-ttu-id="b4cc0-111">呼び出しが成功した場合は S_OKそれ以外の場合はエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="b4cc0-111">S_OK if the call succeeded; otherwise, an error code.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b4cc0-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4cc0-112">See also</span></span>

- [<span data-ttu-id="b4cc0-113">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="b4cc0-113">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="b4cc0-114">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="b4cc0-114">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="b4cc0-115">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="b4cc0-115">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="b4cc0-116">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="b4cc0-116">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)

