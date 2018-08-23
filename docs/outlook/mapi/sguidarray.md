---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585571"
---
# <a name="sguidarray"></a><span data-ttu-id="7dcd7-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="7dcd7-103">SGuidArray</span></span>

  
  
<span data-ttu-id="7dcd7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dcd7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dcd7-105">PT_MV_CLSID の種類のプロパティを説明するために使用する[GUID](guid.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7dcd7-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7dcd7-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7dcd7-106">Header file:</span></span>  <br/> |<span data-ttu-id="7dcd7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7dcd7-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="7dcd7-108">Members</span><span class="sxs-lookup"><span data-stu-id="7dcd7-108">Members</span></span>

 <span data-ttu-id="7dcd7-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="7dcd7-109">**cValues**</span></span>
  
> <span data-ttu-id="7dcd7-110">**Lpguid**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="7dcd7-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="7dcd7-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="7dcd7-111">**lpguid**</span></span>
  
> <span data-ttu-id="7dcd7-112">クラス識別子の値を格納する**GUID**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7dcd7-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7dcd7-113">注釈</span><span class="sxs-lookup"><span data-stu-id="7dcd7-113">Remarks</span></span>

<span data-ttu-id="7dcd7-114">PT_MV_CLSID の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7dcd7-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="7dcd7-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="7dcd7-115">See also</span></span>



[<span data-ttu-id="7dcd7-116">GUID</span><span class="sxs-lookup"><span data-stu-id="7dcd7-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="7dcd7-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="7dcd7-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="7dcd7-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7dcd7-118">MAPI Structures</span></span>](mapi-structures.md)

