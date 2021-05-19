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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424925"
---
# <a name="sguidarray"></a><span data-ttu-id="f1f9a-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="f1f9a-103">SGuidArray</span></span>

  
  
<span data-ttu-id="f1f9a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1f9a-105">型のプロパティを記述するために使用される [GUID](guid.md) 構造体の配列を格納PT_MV_CLSID。</span><span class="sxs-lookup"><span data-stu-id="f1f9a-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f1f9a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f1f9a-106">Header file:</span></span>  <br/> |<span data-ttu-id="f1f9a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f1f9a-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="f1f9a-108">Members</span><span class="sxs-lookup"><span data-stu-id="f1f9a-108">Members</span></span>

 <span data-ttu-id="f1f9a-109">**cValues**</span><span class="sxs-lookup"><span data-stu-id="f1f9a-109">**cValues**</span></span>
  
> <span data-ttu-id="f1f9a-110">lpguid メンバーが指す配列内 **の値の** 数。</span><span class="sxs-lookup"><span data-stu-id="f1f9a-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="f1f9a-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="f1f9a-111">**lpguid**</span></span>
  
> <span data-ttu-id="f1f9a-112">クラス識別子の値を **含** む GUID 構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f1f9a-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f1f9a-113">注釈</span><span class="sxs-lookup"><span data-stu-id="f1f9a-113">Remarks</span></span>

<span data-ttu-id="f1f9a-114">プロパティの詳細については、「PT_MV_CLSIDの [リスト」を参照してください](property-types.md)。</span><span class="sxs-lookup"><span data-stu-id="f1f9a-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f1f9a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1f9a-115">See also</span></span>



[<span data-ttu-id="f1f9a-116">GUID</span><span class="sxs-lookup"><span data-stu-id="f1f9a-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="f1f9a-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f1f9a-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f1f9a-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f1f9a-118">MAPI Structures</span></span>](mapi-structures.md)

