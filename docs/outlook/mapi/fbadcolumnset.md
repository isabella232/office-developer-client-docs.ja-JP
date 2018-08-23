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
ms.openlocfilehash: 4e5f19258fb7716e741928f02a0a87f3939c74e0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575099"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="4e7a5-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="4e7a5-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="4e7a5-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e7a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e7a5-105">[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドへの後続の呼び出しにサービス ・ プロバイダーがテーブルの列の有効性の設定のテストを使用します。</span><span class="sxs-lookup"><span data-stu-id="4e7a5-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4e7a5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="4e7a5-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e7a5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="4e7a5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="4e7a5-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="4e7a5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4e7a5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4e7a5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4e7a5-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="4e7a5-110">Called by:</span></span>  <br/> |<span data-ttu-id="4e7a5-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="4e7a5-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="4e7a5-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="4e7a5-112">Parameters</span></span>

 <span data-ttu-id="4e7a5-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="4e7a5-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="4e7a5-114">[in]検証するテーブルの列を定義するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4e7a5-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e7a5-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="4e7a5-115">Return value</span></span>

<span data-ttu-id="4e7a5-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="4e7a5-116">TRUE</span></span> 
  
> <span data-ttu-id="4e7a5-117">指定された列セットを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="4e7a5-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="4e7a5-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="4e7a5-118">FALSE</span></span> 
  
> <span data-ttu-id="4e7a5-119">指定した列のセットは、有効です。</span><span class="sxs-lookup"><span data-stu-id="4e7a5-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e7a5-120">注釈</span><span class="sxs-lookup"><span data-stu-id="4e7a5-120">Remarks</span></span>

<span data-ttu-id="4e7a5-121">**FBadColumnSet**関数は、無効な型 PT_ERROR の列と列として有効な型 PT_NULL を扱います。</span><span class="sxs-lookup"><span data-stu-id="4e7a5-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

