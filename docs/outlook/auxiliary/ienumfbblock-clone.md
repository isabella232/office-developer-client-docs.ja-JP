---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: 同じ時間制限を使用していますが、列挙子の先頭にカーソルを設定する、列挙子のコピーを作成します。
ms.openlocfilehash: 51503be2091fa01da6f636bf6944274068617f05
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799328"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="80907-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="80907-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="80907-104">同じ時間制限を使用していますが、列挙子の先頭にカーソルを設定する、列挙子のコピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="80907-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="80907-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="80907-105">Quick info</span></span>

<span data-ttu-id="80907-106">[IEnumFBBlock](ienumfbblock.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="80907-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="80907-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="80907-107">Parameters</span></span>

<span data-ttu-id="80907-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="80907-108">_ppclone_</span></span>
  
> <span data-ttu-id="80907-109">[out]A [IEnumFBBlock](ienumfbblock.md)インターフェイスのコピーへのポインターへのポインターがあります。</span><span class="sxs-lookup"><span data-stu-id="80907-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="80907-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="80907-110">Return values</span></span>

|<span data-ttu-id="80907-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="80907-111">**HRESULT**</span></span>|<span data-ttu-id="80907-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="80907-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="80907-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="80907-113">S_OK</span></span>  <br/> |<span data-ttu-id="80907-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="80907-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="80907-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="80907-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="80907-116">コピーを作成するためのメモリが不足があります。</span><span class="sxs-lookup"><span data-stu-id="80907-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80907-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="80907-117">See also</span></span>

- [<span data-ttu-id="80907-118">定数 (空き時間情報の API)</span><span class="sxs-lookup"><span data-stu-id="80907-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="80907-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="80907-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="80907-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="80907-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="80907-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="80907-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="80907-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="80907-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

