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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5d1654908c50c348a27e1281168756100b7a88a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800043"
---
# <a name="fbadcolumnset"></a><span data-ttu-id="fb3a4-103">FBadColumnSet</span><span class="sxs-lookup"><span data-stu-id="fb3a4-103">FBadColumnSet</span></span>

  
  
<span data-ttu-id="fb3a4-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb3a4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb3a4-105">[IMAPITable::SetColumns](imapitable-setcolumns.md)メソッドへの後続の呼び出しにサービス ・ プロバイダーがテーブルの列の有効性の設定のテストを使用します。</span><span class="sxs-lookup"><span data-stu-id="fb3a4-105">Tests the validity of a table column set for use by a service provider in a subsequent call to the [IMAPITable::SetColumns](imapitable-setcolumns.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fb3a4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="fb3a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="fb3a4-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="fb3a4-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="fb3a4-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="fb3a4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fb3a4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fb3a4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fb3a4-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fb3a4-110">Called by:</span></span>  <br/> |<span data-ttu-id="fb3a4-111">サービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="fb3a4-111">Service providers</span></span>  <br/> |
   
```cpp
ULONG FBadColumnSet(
  LPSPropTagArray lpptaCols
);
```

## <a name="parameters"></a><span data-ttu-id="fb3a4-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="fb3a4-112">Parameters</span></span>

 <span data-ttu-id="fb3a4-113">_lpptaCols_</span><span class="sxs-lookup"><span data-stu-id="fb3a4-113">_lpptaCols_</span></span>
  
> <span data-ttu-id="fb3a4-114">[in]検証するテーブルの列を定義するプロパティ タグの配列を含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fb3a4-114">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags defining the table columns to validate.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fb3a4-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fb3a4-115">Return value</span></span>

<span data-ttu-id="fb3a4-116">TRUE</span><span class="sxs-lookup"><span data-stu-id="fb3a4-116">TRUE</span></span> 
  
> <span data-ttu-id="fb3a4-117">指定された列セットを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="fb3a4-117">The specified column set is invalid.</span></span> 
    
<span data-ttu-id="fb3a4-118">FALSE</span><span class="sxs-lookup"><span data-stu-id="fb3a4-118">FALSE</span></span> 
  
> <span data-ttu-id="fb3a4-119">指定した列のセットは、有効です。</span><span class="sxs-lookup"><span data-stu-id="fb3a4-119">The specified column set is valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fb3a4-120">備考</span><span class="sxs-lookup"><span data-stu-id="fb3a4-120">Remarks</span></span>

<span data-ttu-id="fb3a4-121">**FBadColumnSet**関数は、無効な型 PT_ERROR の列と列として有効な型 PT_NULL を扱います。</span><span class="sxs-lookup"><span data-stu-id="fb3a4-121">The **FBadColumnSet** function treats columns of type PT_ERROR as invalid and columns of type PT_NULL as valid.</span></span> 
  

