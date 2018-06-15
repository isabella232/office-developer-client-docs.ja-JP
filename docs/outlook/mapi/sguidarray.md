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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19803905"
---
# <a name="sguidarray"></a><span data-ttu-id="f0fe5-103">SGuidArray</span><span class="sxs-lookup"><span data-stu-id="f0fe5-103">SGuidArray</span></span>

  
  
<span data-ttu-id="f0fe5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0fe5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0fe5-105">PT_MV_CLSID の種類のプロパティを説明するために使用する[GUID](guid.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f0fe5-105">Contains an array of [GUID](guid.md) structures that are used to describe a property of type PT_MV_CLSID.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0fe5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f0fe5-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0fe5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f0fe5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a><span data-ttu-id="f0fe5-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="f0fe5-108">Members</span></span>

 <span data-ttu-id="f0fe5-109">**あう**</span><span class="sxs-lookup"><span data-stu-id="f0fe5-109">**cValues**</span></span>
  
> <span data-ttu-id="f0fe5-110">**Lpguid**メンバーが指す配列内の値の数です。</span><span class="sxs-lookup"><span data-stu-id="f0fe5-110">Count of values in the array pointed to by the **lpguid** member.</span></span> 
    
 <span data-ttu-id="f0fe5-111">**lpguid**</span><span class="sxs-lookup"><span data-stu-id="f0fe5-111">**lpguid**</span></span>
  
> <span data-ttu-id="f0fe5-112">クラス識別子の値を格納する**GUID**構造体の配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f0fe5-112">Pointer to an array of **GUID** structures that contains the class identifier values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f0fe5-113">Remarks</span><span class="sxs-lookup"><span data-stu-id="f0fe5-113">Remarks</span></span>

<span data-ttu-id="f0fe5-114">PT_MV_CLSID の詳細については、[プロパティの種類の一覧](property-types.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0fe5-114">For more information about PT_MV_CLSID, see [List of Property Types](property-types.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f0fe5-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="f0fe5-115">See also</span></span>



[<span data-ttu-id="f0fe5-116">GUID</span><span class="sxs-lookup"><span data-stu-id="f0fe5-116">GUID</span></span>](guid.md)
  
[<span data-ttu-id="f0fe5-117">SPropValue</span><span class="sxs-lookup"><span data-stu-id="f0fe5-117">SPropValue</span></span>](spropvalue.md)


[<span data-ttu-id="f0fe5-118">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="f0fe5-118">MAPI Structures</span></span>](mapi-structures.md)

