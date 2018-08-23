---
title: FBadRowSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRowSet
api_type:
- COM
ms.assetid: 3890dd50-e6ca-4859-bada-f6752ab61d41
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: e6963fc373f771289e3dbff3a0b41857352b4b9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800067"
---
# <a name="fbadrowset"></a><span data-ttu-id="85a91-103">FBadRowSet</span><span class="sxs-lookup"><span data-stu-id="85a91-103">FBadRowSet</span></span>

  
  
<span data-ttu-id="85a91-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="85a91-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="85a91-105">テーブルの行のセットに含まれるすべてのテーブルの行を検証します。</span><span class="sxs-lookup"><span data-stu-id="85a91-105">Validates all table rows included in a set of table rows.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="85a91-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="85a91-106">Header file:</span></span>  <br/> |<span data-ttu-id="85a91-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="85a91-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="85a91-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="85a91-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="85a91-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="85a91-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="85a91-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="85a91-110">Called by:</span></span>  <br/> |<span data-ttu-id="85a91-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="85a91-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRowSet(
  LPSRowSet lpRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="85a91-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="85a91-112">Parameters</span></span>

 <span data-ttu-id="85a91-113">_lpRowSet_</span><span class="sxs-lookup"><span data-stu-id="85a91-113">_lpRowSet_</span></span>
  
> <span data-ttu-id="85a91-114">[in][SRowSet](srowset.md)構造体を検証する設定の行を識別するへのポインター。</span><span class="sxs-lookup"><span data-stu-id="85a91-114">[in] Pointer to an [SRowSet](srowset.md) structure identifying the row set to be validated.</span></span> <span data-ttu-id="85a91-115">ポインターが NULL の場合は、構造が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="85a91-115">If the pointer is NULL, the structure is invalid.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="85a91-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="85a91-116">Return value</span></span>

<span data-ttu-id="85a91-117">TRUE</span><span class="sxs-lookup"><span data-stu-id="85a91-117">TRUE</span></span> 
  
> <span data-ttu-id="85a91-118">指定した行セットの行が正しくないか、またはそれ自体を設定した行が有効ではありません。</span><span class="sxs-lookup"><span data-stu-id="85a91-118">A row of the specified row set is invalid, or the row set itself is invalid.</span></span> 
    
<span data-ttu-id="85a91-119">FALSE</span><span class="sxs-lookup"><span data-stu-id="85a91-119">FALSE</span></span> 
  
> <span data-ttu-id="85a91-120">指定した行セットの行と行は設定自体は、すべてに有効です。</span><span class="sxs-lookup"><span data-stu-id="85a91-120">The rows of the specified row set and the row set itself are all valid.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="85a91-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="85a91-121">See also</span></span>



[<span data-ttu-id="85a91-122">FBadRow</span><span class="sxs-lookup"><span data-stu-id="85a91-122">FBadRow</span></span>](fbadrow.md)

