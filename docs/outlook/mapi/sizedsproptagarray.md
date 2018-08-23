---
title: SizedSPropTagArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSPropTagArray
api_type:
- COM
ms.assetid: 1d2dc6e9-735d-4b5b-af6f-adf6a32a666d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 7505c5dbcfc98a8b868424ae51cbe9c47b1d4338
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803930"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="5ac0c-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5ac0c-103">SizedSPropTagArray</span></span>

<span data-ttu-id="5ac0c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5ac0c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5ac0c-105">プロパティ タグの指定された番号を格納する名前付きの[SPropTagArray](sproptagarray.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="5ac0c-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5ac0c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="5ac0c-106">Header file:</span></span>  <br/> |<span data-ttu-id="5ac0c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="5ac0c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="5ac0c-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="5ac0c-108">Related structure:</span></span>  <br/> |<span data-ttu-id="5ac0c-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="5ac0c-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="5ac0c-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5ac0c-110">Parameters</span></span>

<span data-ttu-id="5ac0c-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="5ac0c-111">__ctag_</span></span>
  
> <span data-ttu-id="5ac0c-112">新しい構造体に含まれるプロパティ タグの数。</span><span class="sxs-lookup"><span data-stu-id="5ac0c-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="5ac0c-113">__名_</span><span class="sxs-lookup"><span data-stu-id="5ac0c-113">__name_</span></span>
  
> <span data-ttu-id="5ac0c-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="5ac0c-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5ac0c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="5ac0c-115">Remarks</span></span>

<span data-ttu-id="5ac0c-116">**SizedSPropTagArray**マクロを使用すると、明示的な境界を持つプロパティ タグ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="5ac0c-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="5ac0c-117">**SPropTagArray**構造体へのポインターとしての**SizedSPropTagArray**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="5ac0c-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="5ac0c-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="5ac0c-118">See also</span></span>

- [<span data-ttu-id="5ac0c-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="5ac0c-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="5ac0c-120">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="5ac0c-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

