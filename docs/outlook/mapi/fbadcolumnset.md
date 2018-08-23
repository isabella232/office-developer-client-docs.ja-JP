---
title: FBadColumnSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FBadColumnSet
api_type:
- HeaderDef
ms.assetid: 15be5a8c-4299-4434-b521-c901215b9dda
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800043"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="1799c-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="1799c-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="1799c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1799c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1799c-105">[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドへの後続の呼び出しにサービス ・ プロバイダーがテーブルの列の有効性の設定のテストを使用します。</span><span class="sxs-lookup"><span data-stu-id="1799c-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1799c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1799c-106">Header file:</span></span>  <br/> |<span data-ttu-id="1799c-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="1799c-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="1799c-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="1799c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1799c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1799c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1799c-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="1799c-110">Called by:</span></span>  <br/> |<span data-ttu-id="1799c-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1799c-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="1799c-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1799c-112">Parameters</span></span>

 <span data-ttu-id="1799c-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="1799c-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="1799c-114">[in]検証するテーブルの列を定義するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="1799c-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1799c-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="1799c-115">Return value</span></span>

<span data-ttu-id="1799c-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="1799c-116">TRUE</span></span> 
  
> <span data-ttu-id="1799c-117">指定された列セットを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="1799c-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="1799c-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="1799c-118">FALSE</span></span> 
  
> <span data-ttu-id="1799c-119">指定した列のセットは、有効です。</span><span class="sxs-lookup"><span data-stu-id="1799c-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1799c-120">注釈</span><span class="sxs-lookup"><span data-stu-id="1799c-120">Remarks</span></span>

<span data-ttu-id="1799c-121">**FBadColumnSet**関数は、無効な型 PT_ERROR の列と列として有効な型 PT_NULL を扱います。</span><span class="sxs-lookup"><span data-stu-id="1799c-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

