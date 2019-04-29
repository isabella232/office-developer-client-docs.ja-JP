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
# <a name="spropproblem"></a><span data-ttu-id="560a4-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="560a4-103">SPropProblem</span></span>

  
  
<span data-ttu-id="560a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="560a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="560a4-105">プロパティを含む操作に関連するエラーを記述します。</span><span class="sxs-lookup"><span data-stu-id="560a4-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="560a4-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="560a4-106">Header file:</span></span>  <br/> |<span data-ttu-id="560a4-107">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="560a4-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="560a4-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="560a4-108">Members</span></span>

 <span data-ttu-id="560a4-109">**ulindex**</span><span class="sxs-lookup"><span data-stu-id="560a4-109">**ulIndex**</span></span>
  
> <span data-ttu-id="560a4-110">プロパティタグの配列内のインデックス。</span><span class="sxs-lookup"><span data-stu-id="560a4-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="560a4-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="560a4-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="560a4-112">エラーが発生したプロパティのプロパティタグ。</span><span class="sxs-lookup"><span data-stu-id="560a4-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="560a4-113">**scode as scode**</span><span class="sxs-lookup"><span data-stu-id="560a4-113">**scode**</span></span>
  
> <span data-ttu-id="560a4-114">プロパティに関する問題を説明するエラー値。</span><span class="sxs-lookup"><span data-stu-id="560a4-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="560a4-115">この値には、任意の MAPI の[SCODE](scode.md)値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="560a4-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="560a4-116">注釈</span><span class="sxs-lookup"><span data-stu-id="560a4-116">Remarks</span></span>

<span data-ttu-id="560a4-117">**spropproblem**構造体の配列は、次のメソッドから返されます。</span><span class="sxs-lookup"><span data-stu-id="560a4-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="560a4-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="560a4-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="560a4-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="560a4-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="560a4-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="560a4-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="560a4-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="560a4-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="560a4-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="560a4-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="560a4-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="560a4-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="560a4-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="560a4-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="560a4-125">**spropproblem**構造体には、MAPI プロパティを変更または削除しようとした操作の結果として返される**SCODE**エラー値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="560a4-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="560a4-126">**spropproblem**構造がプロパティに関連するエラーとどのように連動するかの詳細については、「 [MAPI の名前付きプロパティ](mapi-named-properties.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="560a4-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="560a4-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="560a4-127">See also</span></span>



[<span data-ttu-id="560a4-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="560a4-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="560a4-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="560a4-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="560a4-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="560a4-130">MAPI Structures</span></span>](mapi-structures.md)

