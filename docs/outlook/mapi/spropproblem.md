---
title: SPropProblem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SPropProblem
api_type:
- COM
ms.assetid: 55943197-fd11-442d-bb4b-0bff565b846e
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b3a0872c94459fc7c24d13e35adf335ef8012182
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407775"
---
# <a name="spropproblem"></a><span data-ttu-id="31cc5-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="31cc5-103">SPropProblem</span></span>

  
  
<span data-ttu-id="31cc5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31cc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31cc5-105">プロパティに関連する操作に関連するエラーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="31cc5-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="31cc5-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="31cc5-106">Header file:</span></span>  <br/> |<span data-ttu-id="31cc5-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31cc5-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="31cc5-108">Members</span><span class="sxs-lookup"><span data-stu-id="31cc5-108">Members</span></span>

 <span data-ttu-id="31cc5-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="31cc5-109">**ulIndex**</span></span>
  
> <span data-ttu-id="31cc5-110">プロパティ タグの配列内のインデックス。</span><span class="sxs-lookup"><span data-stu-id="31cc5-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="31cc5-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="31cc5-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="31cc5-112">エラーが発生したプロパティのプロパティ タグ。</span><span class="sxs-lookup"><span data-stu-id="31cc5-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="31cc5-113">**scode**</span><span class="sxs-lookup"><span data-stu-id="31cc5-113">**scode**</span></span>
  
> <span data-ttu-id="31cc5-114">プロパティの問題を説明するエラー値。</span><span class="sxs-lookup"><span data-stu-id="31cc5-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="31cc5-115">この値には、任意の MAPI [SCODE 値を指定](scode.md) できます。</span><span class="sxs-lookup"><span data-stu-id="31cc5-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="31cc5-116">注釈</span><span class="sxs-lookup"><span data-stu-id="31cc5-116">Remarks</span></span>

<span data-ttu-id="31cc5-117">**SPropProblem** 構造体の配列は、次のメソッドから返されます。</span><span class="sxs-lookup"><span data-stu-id="31cc5-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="31cc5-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="31cc5-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="31cc5-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="31cc5-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="31cc5-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="31cc5-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="31cc5-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="31cc5-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="31cc5-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="31cc5-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="31cc5-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="31cc5-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="31cc5-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="31cc5-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="31cc5-125">**SPropProblem** 構造体には、MAPI プロパティを変更または削除しようとする操作によって発生する **SCODE** エラー値が含まれる。</span><span class="sxs-lookup"><span data-stu-id="31cc5-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="31cc5-126">**SPropProblem** 構造体がプロパティに関連するエラーでどのように動作する方法の詳細については、「MAPI 名前付きプロパティ」[を参照してください](mapi-named-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="31cc5-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="31cc5-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="31cc5-127">See also</span></span>



[<span data-ttu-id="31cc5-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="31cc5-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="31cc5-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="31cc5-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="31cc5-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="31cc5-130">MAPI Structures</span></span>](mapi-structures.md)

