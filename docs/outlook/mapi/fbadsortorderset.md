---
title: FBadSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadSortOrderSet
api_type:
- COM
ms.assetid: b7f80e0a-8ddd-4b24-ab63-2078a8152058
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0e200ea20c55cfd5729ce4c1f590de2d61ca73bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800041"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="c9c96-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c9c96-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="c9c96-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9c96-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c9c96-105">メモリの割り当てを確認し、設定の並べ替え順序を検証します。</span><span class="sxs-lookup"><span data-stu-id="c9c96-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9c96-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c9c96-106">Header file:</span></span>  <br/> |<span data-ttu-id="c9c96-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c9c96-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c9c96-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="c9c96-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c9c96-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c9c96-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c9c96-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="c9c96-110">Called by:</span></span>  <br/> |<span data-ttu-id="c9c96-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c9c96-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="c9c96-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c9c96-112">Parameters</span></span>

 <span data-ttu-id="c9c96-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="c9c96-113">_lpsos_</span></span>
  
> <span data-ttu-id="c9c96-114">[in]設定を検証する並べ替え順序を識別する[SSortOrderSet](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c9c96-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c9c96-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="c9c96-115">Return value</span></span>

<span data-ttu-id="c9c96-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c9c96-116">TRUE</span></span> 
  
> <span data-ttu-id="c9c96-117">指定した並べ替え順序の設定が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="c9c96-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="c9c96-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c9c96-118">FALSE</span></span> 
  
> <span data-ttu-id="c9c96-119">有効では、指定した並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="c9c96-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c9c96-120">注釈</span><span class="sxs-lookup"><span data-stu-id="c9c96-120">Remarks</span></span>

<span data-ttu-id="c9c96-121">**FBadSortOrderSet**関数は、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドのような並べ替えメソッドへの呼び出しの準備に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c9c96-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

