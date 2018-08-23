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
ms.openlocfilehash: 363a85e1c6f111936b16e471eda6b9f962f8b65d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573622"
---
# <a name="sizedsproptagarray"></a><span data-ttu-id="f5747-103">SizedSPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f5747-103">SizedSPropTagArray</span></span>

<span data-ttu-id="f5747-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5747-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5747-105">プロパティ タグの指定された番号を格納する名前付きの[SPropTagArray](sproptagarray.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="f5747-105">Creates a named [SPropTagArray](sproptagarray.md) structure that includes a specified number of property tags.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f5747-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f5747-106">Header file:</span></span>  <br/> |<span data-ttu-id="f5747-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f5747-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f5747-108">関連の構造体。</span><span class="sxs-lookup"><span data-stu-id="f5747-108">Related structure:</span></span>  <br/> |<span data-ttu-id="f5747-109">**SPropTagArray**</span><span class="sxs-lookup"><span data-stu-id="f5747-109">**SPropTagArray**</span></span> <br/> |
   
```cpp
SizedSPropTagArray (_ctag, _name)
```

## <a name="parameters"></a><span data-ttu-id="f5747-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f5747-110">Parameters</span></span>

<span data-ttu-id="f5747-111">__ctag_</span><span class="sxs-lookup"><span data-stu-id="f5747-111">__ctag_</span></span>
  
> <span data-ttu-id="f5747-112">新しい構造体に含まれるプロパティ タグの数。</span><span class="sxs-lookup"><span data-stu-id="f5747-112">Count of property tags to be included in the new structure.</span></span>
    
<span data-ttu-id="f5747-113">__名_</span><span class="sxs-lookup"><span data-stu-id="f5747-113">__name_</span></span>
  
> <span data-ttu-id="f5747-114">新しい構造体の名前です。</span><span class="sxs-lookup"><span data-stu-id="f5747-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5747-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f5747-115">Remarks</span></span>

<span data-ttu-id="f5747-116">**SizedSPropTagArray**マクロを使用すると、明示的な境界を持つプロパティ タグ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="f5747-116">Use the **SizedSPropTagArray** macro to create a property tag array with explicit bounds.</span></span> 
  
<span data-ttu-id="f5747-117">**SPropTagArray**構造体へのポインターとしての**SizedSPropTagArray**マクロの結果を新しい構造体を使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="f5747-117">To use the new structure that results from the **SizedSPropTagArray** macro as a pointer to an **SPropTagArray** structure, perform the following cast:</span></span> 
  
```cpp
lpPropTagArray = (LPPropTagArray) &SizedSPropTagArray;

```

## <a name="see-also"></a><span data-ttu-id="f5747-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="f5747-118">See also</span></span>

- [<span data-ttu-id="f5747-119">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="f5747-119">SPropTagArray</span></span>](sproptagarray.md)
- [<span data-ttu-id="f5747-120">構造体に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="f5747-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

