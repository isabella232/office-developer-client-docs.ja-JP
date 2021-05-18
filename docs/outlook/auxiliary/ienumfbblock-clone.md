---
title: IEnumFBBlockClone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5af36a87-e782-df63-4190-a608758fef50
description: 同じ時間制限を使用して、列挙子のコピーを作成しますが、カーソルを列挙子の先頭に設定します。
ms.openlocfilehash: 1a279430bf6a29611fa223bebbf8023c34967139
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413403"
---
# <a name="ienumfbblockclone"></a><span data-ttu-id="57811-103">IEnumFBBlock::Clone</span><span class="sxs-lookup"><span data-stu-id="57811-103">IEnumFBBlock::Clone</span></span>

<span data-ttu-id="57811-104">同じ時間制限を使用して、列挙子のコピーを作成しますが、カーソルを列挙子の先頭に設定します。</span><span class="sxs-lookup"><span data-stu-id="57811-104">Creates a copy of the enumerator, using the same time restriction but setting the cursor to the beginning of the enumerator.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="57811-105">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="57811-105">Quick info</span></span>

<span data-ttu-id="57811-106">[「IEnumFBBlock」を参照](ienumfbblock.md)してください。</span><span class="sxs-lookup"><span data-stu-id="57811-106">See [IEnumFBBlock](ienumfbblock.md).</span></span>
  
```cpp
HRESULT Clone(  
     IEnumFBBlock **ppclone 
); 
```

## <a name="parameters"></a><span data-ttu-id="57811-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="57811-107">Parameters</span></span>

<span data-ttu-id="57811-108">_ppclone_</span><span class="sxs-lookup"><span data-stu-id="57811-108">_ppclone_</span></span>
  
> <span data-ttu-id="57811-109">[out] [IEnumFBBlock](ienumfbblock.md) インターフェイスのコピーへのポインター。</span><span class="sxs-lookup"><span data-stu-id="57811-109">[out] A pointer to pointer to the copy of [IEnumFBBlock](ienumfbblock.md) interface.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="57811-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="57811-110">Return values</span></span>

|<span data-ttu-id="57811-111">**HRESULT 型**</span><span class="sxs-lookup"><span data-stu-id="57811-111">**HRESULT**</span></span>|<span data-ttu-id="57811-112">**Description**</span><span class="sxs-lookup"><span data-stu-id="57811-112">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57811-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="57811-113">S_OK</span></span>  <br/> |<span data-ttu-id="57811-114">呼び出しが成功しました。</span><span class="sxs-lookup"><span data-stu-id="57811-114">The call succeeded.</span></span>  <br/> |
|<span data-ttu-id="57811-115">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="57811-115">E_OUTOFMEMORY</span></span>  <br/> |<span data-ttu-id="57811-116">コピーを作成するメモリが不足しています。</span><span class="sxs-lookup"><span data-stu-id="57811-116">There is insufficient memory for making the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="57811-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="57811-117">See also</span></span>

- [<span data-ttu-id="57811-118">定数 (空き時間情報 API)</span><span class="sxs-lookup"><span data-stu-id="57811-118">Constants (Free/busy API)</span></span>](constants-free-busy-api.md)
- [<span data-ttu-id="57811-119">IEnumFBBlock::Next</span><span class="sxs-lookup"><span data-stu-id="57811-119">IEnumFBBlock::Next</span></span>](ienumfbblock-next.md)  
- [<span data-ttu-id="57811-120">IEnumFBBlock::Reset</span><span class="sxs-lookup"><span data-stu-id="57811-120">IEnumFBBlock::Reset</span></span>](ienumfbblock-reset.md)  
- [<span data-ttu-id="57811-121">IEnumFBBlock::Restrict</span><span class="sxs-lookup"><span data-stu-id="57811-121">IEnumFBBlock::Restrict</span></span>](ienumfbblock-restrict.md)  
- [<span data-ttu-id="57811-122">IEnumFBBlock::Skip</span><span class="sxs-lookup"><span data-stu-id="57811-122">IEnumFBBlock::Skip</span></span>](ienumfbblock-skip.md)

