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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 31840923e24cddd0dc3dfa9cc67b610d0dcd7e47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428460"
---
# <a name="fbadsortorderset"></a><span data-ttu-id="c6bc7-103">FBadSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="c6bc7-103">FBadSortOrderSet</span></span>

  
  
<span data-ttu-id="c6bc7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6bc7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6bc7-105">メモリ割り当てを確認して並べ替え順序セットを検証します。</span><span class="sxs-lookup"><span data-stu-id="c6bc7-105">Validates a sort order set by verifying its memory allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6bc7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c6bc7-106">Header file:</span></span>  <br/> |<span data-ttu-id="c6bc7-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c6bc7-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c6bc7-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="c6bc7-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c6bc7-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c6bc7-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c6bc7-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c6bc7-110">Called by:</span></span>  <br/> |<span data-ttu-id="c6bc7-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="c6bc7-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadSortOrderSet(
  LPSSortOrderSet lpsos
);
```

## <a name="parameters"></a><span data-ttu-id="c6bc7-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c6bc7-112">Parameters</span></span>

 <span data-ttu-id="c6bc7-113">_lpsos_</span><span class="sxs-lookup"><span data-stu-id="c6bc7-113">_lpsos_</span></span>
  
> <span data-ttu-id="c6bc7-114">[in]検証する [並べ替え順序セットを識別する SSortOrderSet](ssortorderset.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="c6bc7-114">[in] Pointer to an [SSortOrderSet](ssortorderset.md) structure identifying the sort order set to be validated.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c6bc7-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="c6bc7-115">Return value</span></span>

<span data-ttu-id="c6bc7-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="c6bc7-116">TRUE</span></span> 
  
> <span data-ttu-id="c6bc7-117">指定した並べ替え順序セットが無効です。</span><span class="sxs-lookup"><span data-stu-id="c6bc7-117">The specified sort order set is invalid.</span></span> 
    
<span data-ttu-id="c6bc7-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="c6bc7-118">FALSE</span></span> 
  
> <span data-ttu-id="c6bc7-119">指定した並べ替え順序セットが有効です。</span><span class="sxs-lookup"><span data-stu-id="c6bc7-119">The specified sort order set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c6bc7-120">注釈</span><span class="sxs-lookup"><span data-stu-id="c6bc7-120">Remarks</span></span>

<span data-ttu-id="c6bc7-121">**FBadSortOrderSet** 関数を使用して [、IMAPITable::SortTable](imapitable-sorttable.md)メソッドなどの並べ替えメソッドの呼び出しを準備できます。</span><span class="sxs-lookup"><span data-stu-id="c6bc7-121">The **FBadSortOrderSet** function can be used to prepare for a call to a sort method such as the [IMAPITable::SortTable](imapitable-sorttable.md) method.</span></span> 
  

