---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382730"
---
# <a name="slargeintegerarray"></a><span data-ttu-id="06b32-103">SLargeIntegerArray</span><span class="sxs-lookup"><span data-stu-id="06b32-103">SLargeIntegerArray</span></span>

  
  
<span data-ttu-id="06b32-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06b32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06b32-105">PT_MV_I8 の種類のプロパティを説明するために使用する[LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="06b32-105">Contains an array of [LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) structures that are used to describe a property of type PT_MV_I8.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="06b32-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="06b32-106">Header file:</span></span>  <br/> |<span data-ttu-id="06b32-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="06b32-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a><span data-ttu-id="06b32-108">Members</span><span class="sxs-lookup"><span data-stu-id="06b32-108">Members</span></span>

 <span data-ttu-id="06b32-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="06b32-109">**cValues**</span></span>
  
> <span data-ttu-id="06b32-110">**Lpli**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="06b32-110">Count of values in the array pointed to by the **lpli** member.</span></span> 
    
 <span data-ttu-id="06b32-111">**lpli**</span><span class="sxs-lookup"><span data-stu-id="06b32-111">**lpli**</span></span>
  
> <span data-ttu-id="06b32-112">整数値を保持している**LARGE_INTEGER**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="06b32-112">Pointer to an array of **LARGE_INTEGER** structures holding the integer values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="06b32-113">備考</span><span class="sxs-lookup"><span data-stu-id="06b32-113">Remarks</span></span>

<span data-ttu-id="06b32-114">PT_MV_18 の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="06b32-114">For more information about PT_MV_18, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="06b32-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="06b32-115">See also</span></span>



[<span data-ttu-id="06b32-116">SPropValue</span><span class="sxs-lookup"><span data-stu-id="06b32-116">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="06b32-117">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="06b32-117">MAPI Structures</span></span>](mapi-structures.md)

