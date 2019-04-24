---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: 列挙で、次に指定された空き時間情報データのブロック数を取得します。
ms.openlocfilehash: f6ec49a9bac6bcf4fff67991d55c7656f6c8cce2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319594"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="58d88-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="58d88-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="58d88-104">列挙で、次に指定された空き時間情報データのブロック数を取得します。</span><span class="sxs-lookup"><span data-stu-id="58d88-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="58d88-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="58d88-105">Quick info</span></span>

<span data-ttu-id="58d88-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="58d88-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="58d88-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="58d88-107">Parameters</span></span>

<span data-ttu-id="58d88-108">_が大き_</span><span class="sxs-lookup"><span data-stu-id="58d88-108">_celt_</span></span>
  
> <span data-ttu-id="58d88-109">順番取得する*pblk*内の空き時間情報のデータブロックの数。</span><span class="sxs-lookup"><span data-stu-id="58d88-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="58d88-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="58d88-110">_pblk_</span></span>
  
> <span data-ttu-id="58d88-111">順番空き時間ブロックの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="58d88-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="58d88-112">配列のサイズは、1に\*\* 割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="58d88-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="58d88-113">この配列には、要求された空き時間ブロックが返されます。</span><span class="sxs-lookup"><span data-stu-id="58d88-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="58d88-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="58d88-114">_pcfetch_</span></span>
  
> <span data-ttu-id="58d88-115">読み上げ実際に*pblk*で返される空き時間ブロックの数。</span><span class="sxs-lookup"><span data-stu-id="58d88-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="58d88-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="58d88-116">Return values</span></span>

|<span data-ttu-id="58d88-117">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="58d88-117">**HRESULT**</span></span>|<span data-ttu-id="58d88-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="58d88-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58d88-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="58d88-119">S_OK</span></span>  <br/> |<span data-ttu-id="58d88-120">要求されたブロック数が返されました。</span><span class="sxs-lookup"><span data-stu-id="58d88-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="58d88-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="58d88-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="58d88-122">要求されたブロック数が返されていません。</span><span class="sxs-lookup"><span data-stu-id="58d88-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58d88-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="58d88-123">See also</span></span>

- [<span data-ttu-id="58d88-124">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="58d88-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="58d88-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="58d88-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="58d88-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="58d88-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="58d88-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="58d88-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="58d88-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="58d88-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="58d88-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="58d88-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

