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
ms.openlocfilehash: 3b3f88495cafbd6ea764ca8901ac67c23749aebe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578578"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="914ed-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="914ed-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="914ed-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="914ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="914ed-105">メモリの割り当てを確認し、設定の並べ替え順序を検証します。</span><span class="sxs-lookup"><span data-stu-id="914ed-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="914ed-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="914ed-106">Header file:</span></span>  <br/> |<span data-ttu-id="914ed-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="914ed-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="914ed-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="914ed-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="914ed-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="914ed-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="914ed-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="914ed-110">Called by:</span></span>  <br/> |<span data-ttu-id="914ed-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="914ed-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="914ed-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="914ed-112">Parameters</span></span>

 <span data-ttu-id="914ed-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="914ed-113">_lpsos_</span></span>
  
> <span data-ttu-id="914ed-114">[in]設定を検証する並べ替え順序を識別する[SSortOrderSet](ssortorderset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="914ed-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="914ed-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="914ed-115">Return value</span></span>

<span data-ttu-id="914ed-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="914ed-116">TRUE</span></span> 
  
> <span data-ttu-id="914ed-117">指定した並べ替え順序の設定が正しくありません。</span><span class="sxs-lookup"><span data-stu-id="914ed-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="914ed-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="914ed-118">FALSE</span></span> 
  
> <span data-ttu-id="914ed-119">有効では、指定した並べ替え順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="914ed-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="914ed-120">注釈</span><span class="sxs-lookup"><span data-stu-id="914ed-120">Remarks</span></span>

<span data-ttu-id="914ed-121">**FBadSortOrderSet**関数は、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドのような並べ替えメソッドへの呼び出しの準備に使用できます。</span><span class="sxs-lookup"><span data-stu-id="914ed-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

