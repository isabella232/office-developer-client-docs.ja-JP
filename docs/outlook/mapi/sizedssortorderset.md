---
title: SizedSSortOrderSet
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SizedSSortOrderSet
api_type:
- COM
ms.assetid: f0b9c2f4-7011-414d-8e6c-ab22893ef132
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 60a335f85eea8778580e0bd74693a5c28591103c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428607"
---
# <a name="sizedssortorderset"></a><span data-ttu-id="01407-103">SizedSSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="01407-103">SizedSSortOrderSet</span></span>

<span data-ttu-id="01407-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="01407-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="01407-105">指定した数の並べ替え順序を含む、名前付きの[ssortorderset](ssortorderset.md)構造を作成します。</span><span class="sxs-lookup"><span data-stu-id="01407-105">Creates a named [SSortOrderSet](ssortorderset.md) structure that contains a specified number of sort orders.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01407-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="01407-106">Header file:</span></span>  <br/> |<span data-ttu-id="01407-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="01407-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="01407-108">関連する構造:</span><span class="sxs-lookup"><span data-stu-id="01407-108">Related structure:</span></span>  <br/> |<span data-ttu-id="01407-109">**SSortOrderSet**</span><span class="sxs-lookup"><span data-stu-id="01407-109">**SSortOrderSet**</span></span> <br/> |
   
```cpp
SizedSSortOrderSet (_csort,_name)
```

## <a name="parameters"></a><span data-ttu-id="01407-110">パラメーター</span><span class="sxs-lookup"><span data-stu-id="01407-110">Parameters</span></span>

<span data-ttu-id="01407-111">__csort_</span><span class="sxs-lookup"><span data-stu-id="01407-111">__csort_</span></span>
  
> <span data-ttu-id="01407-112">新しい構造に含める並べ替え順序の数。</span><span class="sxs-lookup"><span data-stu-id="01407-112">Count of sort orders to be included in the new structure.</span></span>
    
<span data-ttu-id="01407-113">__名前_</span><span class="sxs-lookup"><span data-stu-id="01407-113">__name_</span></span>
  
> <span data-ttu-id="01407-114">新しい構造の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="01407-114">Name for the new structure.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="01407-115">注釈</span><span class="sxs-lookup"><span data-stu-id="01407-115">Remarks</span></span>

<span data-ttu-id="01407-116">**sizedssortorderset**マクロを使用して、明示的な境界で並べ替え順序セットを作成します。</span><span class="sxs-lookup"><span data-stu-id="01407-116">Use the **SizedSSortOrderSet** macro to create a sort order set with explicit bounds.</span></span> 
  
<span data-ttu-id="01407-117">**sizedssortorderset**マクロの結果として得られる新しい構造を、 **ssortorderset**構造へのポインターとして使用するには、次のキャストを実行します。</span><span class="sxs-lookup"><span data-stu-id="01407-117">To use the new structure that results from the **SizedSSortOrderSet** macro as a pointer to an **SSortOrderSet** structure, perform the following cast:</span></span> 
  
```cpp
lpSSortOrderSet = (LPSSortOrderSet) &SizedSSortOrderSet;

```

## <a name="see-also"></a><span data-ttu-id="01407-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="01407-118">See also</span></span>

- [<span data-ttu-id="01407-119">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="01407-119">SSortOrderSet</span></span>](ssortorderset.md)
- [<span data-ttu-id="01407-120">構造に関連するマクロ</span><span class="sxs-lookup"><span data-stu-id="01407-120">Macros Related to Structures</span></span>](macros-related-to-structures.md)

