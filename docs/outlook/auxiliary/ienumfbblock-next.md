---
title: IEnumFBBlockNext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b46358c-bcab-f097-8746-fabfd4722b3c
description: 列挙型の中の空き時間情報データ ブロックの次の指定された番号を取得します。
ms.openlocfilehash: ec366cf102d3c75487f9485cfae7764d68695f10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799334"
---
# <a name="ienumfbblocknext"></a><span data-ttu-id="b43ea-103">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="b43ea-103">IEnumFBBlock::Next</span></span>

<span data-ttu-id="b43ea-104">列挙型の中の空き時間情報データ ブロックの次の指定された番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="b43ea-104">Gets the next specified number of blocks of free/busy data in an enumeration.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b43ea-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="b43ea-105">Quick info</span></span>

<span data-ttu-id="b43ea-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b43ea-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Next(  
        LONG celt,
        FBBlock_1 *pblk,
        LONG *pcfetch
);
```

## <a name="parameters"></a><span data-ttu-id="b43ea-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b43ea-107">Parameters</span></span>

<span data-ttu-id="b43ea-108">_celt_</span><span class="sxs-lookup"><span data-stu-id="b43ea-108">_celt_</span></span>
  
> <span data-ttu-id="b43ea-109">[in]*Pblk*を取得するには、空き時間情報データの数がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="b43ea-109">[in] The number of free/busy data blocks in  *pblk*  to retrieve.</span></span> 
    
<span data-ttu-id="b43ea-110">_pblk_</span><span class="sxs-lookup"><span data-stu-id="b43ea-110">_pblk_</span></span>
  
> <span data-ttu-id="b43ea-111">[in]空き時間ブロックの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b43ea-111">[in] A pointer to an array of free/busy blocks.</span></span> <span data-ttu-id="b43ea-112">配列は、 *celt*のサイズが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="b43ea-112">The array is allocated a size of  *celt*  .</span></span> <span data-ttu-id="b43ea-113">要求された空き時間情報のブロックは、この配列で返されます。</span><span class="sxs-lookup"><span data-stu-id="b43ea-113">The requested free/busy blocks are returned in this array.</span></span> 
    
<span data-ttu-id="b43ea-114">_pcfetch_</span><span class="sxs-lookup"><span data-stu-id="b43ea-114">_pcfetch_</span></span>
  
> <span data-ttu-id="b43ea-115">[out]*Pblk*に実際に返される空き時間情報のブロックの数。</span><span class="sxs-lookup"><span data-stu-id="b43ea-115">[out] The number of free/busy blocks actually returned in  *pblk*  .</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="b43ea-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="b43ea-116">Return values</span></span>

|<span data-ttu-id="b43ea-117">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="b43ea-117">**HRESULT**</span></span>|<span data-ttu-id="b43ea-118">**Description**</span><span class="sxs-lookup"><span data-stu-id="b43ea-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b43ea-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="b43ea-119">S_OK</span></span>  <br/> |<span data-ttu-id="b43ea-120">要求されたブロックの数が返されました。</span><span class="sxs-lookup"><span data-stu-id="b43ea-120">The requested number of blocks has been returned.</span></span>  <br/> |
|<span data-ttu-id="b43ea-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="b43ea-121">S_FALSE</span></span>  <br/> |<span data-ttu-id="b43ea-122">要求されたブロックの数が取得できませんでした。</span><span class="sxs-lookup"><span data-stu-id="b43ea-122">The requested number of blocks has not been returned.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b43ea-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b43ea-123">See also</span></span>

- [<span data-ttu-id="b43ea-124">定数 (空き時間情報の API)</span><span class="sxs-lookup"><span data-stu-id="b43ea-124">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)  
- [<span data-ttu-id="b43ea-125">FBBlock_1</span><span class="sxs-lookup"><span data-stu-id="b43ea-125">FBBlock_1</span></span>](fbblock_1.md)  
- [<span data-ttu-id="b43ea-126">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="b43ea-126">IEnumFBBlock::Clone</span></span>](ienumfbblock-clone.md)  
- [<span data-ttu-id="b43ea-127">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="b43ea-127">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="b43ea-128">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="b43ea-128">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="b43ea-129">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="b43ea-129">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

