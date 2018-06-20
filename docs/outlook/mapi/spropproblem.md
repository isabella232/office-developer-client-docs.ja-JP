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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 32aa91d43e4674c0de20a0dbb670dcb9e2c782cf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803980"
---
# <a name="spropproblem"></a><span data-ttu-id="7f7be-103">SPropProblem</span><span class="sxs-lookup"><span data-stu-id="7f7be-103">SPropProblem</span></span>

  
  
<span data-ttu-id="7f7be-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f7be-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f7be-105">プロパティを含む操作に関連するエラーについて説明します。</span><span class="sxs-lookup"><span data-stu-id="7f7be-105">Describes an error that relate to an operation involving a property.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f7be-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7f7be-106">Header file:</span></span>  <br/> |<span data-ttu-id="7f7be-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7f7be-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SPropProblem
{
  ULONG ulIndex;
  ULONG ulPropTag;
  SCODE scode;
} SPropProblem, FAR *LPSPropProblem;

```

## <a name="members"></a><span data-ttu-id="7f7be-108">メンバー</span><span class="sxs-lookup"><span data-stu-id="7f7be-108">Members</span></span>

 <span data-ttu-id="7f7be-109">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="7f7be-109">**ulIndex**</span></span>
  
> <span data-ttu-id="7f7be-110">プロパティ タグの配列のインデックス。</span><span class="sxs-lookup"><span data-stu-id="7f7be-110">An index in an array of property tags.</span></span>
    
 <span data-ttu-id="7f7be-111">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="7f7be-111">**ulPropTag**</span></span>
  
> <span data-ttu-id="7f7be-112">エラーを持つプロパティのプロパティ タグです。</span><span class="sxs-lookup"><span data-stu-id="7f7be-112">Property tag for the property that has the error.</span></span>
    
 <span data-ttu-id="7f7be-113">**scode**</span><span class="sxs-lookup"><span data-stu-id="7f7be-113">**scode**</span></span>
  
> <span data-ttu-id="7f7be-114">エラー値がプロパティを使用して問題を説明します。</span><span class="sxs-lookup"><span data-stu-id="7f7be-114">Error value describing the problem with the property.</span></span> <span data-ttu-id="7f7be-115">この値は、任意の MAPI [SCODE](scode.md)の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="7f7be-115">This value can be any MAPI [SCODE](scode.md) value.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7f7be-116">備考</span><span class="sxs-lookup"><span data-stu-id="7f7be-116">Remarks</span></span>

<span data-ttu-id="7f7be-117">**SPropProblem**構造体の配列は次のメソッドから返されます。</span><span class="sxs-lookup"><span data-stu-id="7f7be-117">An array of **SPropProblem** structures is returned from the following methods:</span></span> 
  
- [<span data-ttu-id="7f7be-118">IMAPISupport::DoCopyTo</span><span class="sxs-lookup"><span data-stu-id="7f7be-118">IMAPISupport::DoCopyTo</span></span>](imapisupport-docopyto.md)
    
- [<span data-ttu-id="7f7be-119">IMAPISupport::DoCopyProps</span><span class="sxs-lookup"><span data-stu-id="7f7be-119">IMAPISupport::DoCopyProps</span></span>](imapisupport-docopyprops.md)
    
- [<span data-ttu-id="7f7be-120">IMAPIProp::DeleteProps</span><span class="sxs-lookup"><span data-stu-id="7f7be-120">IMAPIProp::DeleteProps</span></span>](imapiprop-deleteprops.md)
    
- [<span data-ttu-id="7f7be-121">IMAPIProp::SetProps</span><span class="sxs-lookup"><span data-stu-id="7f7be-121">IMAPIProp::SetProps</span></span>](imapiprop-setprops.md)
    
- [<span data-ttu-id="7f7be-122">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="7f7be-122">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
- [<span data-ttu-id="7f7be-123">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="7f7be-123">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="7f7be-124">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="7f7be-124">IPropData::HrAddObjProps</span></span>](ipropdata-hraddobjprops.md)
    
<span data-ttu-id="7f7be-125">**SPropProblem**構造体には、変更または MAPI プロパティを削除しようとしています。 操作に起因する**SCODE**エラー値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7f7be-125">An **SPropProblem** structure contains an **SCODE** error value that results from an operation trying to modify or delete a MAPI property.</span></span> 
  
<span data-ttu-id="7f7be-126">エラーのプロパティに関連する**SPropProblem**構造体のしくみに関する詳細については、 [MAPI 名前付きプロパティ](mapi-named-properties.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7f7be-126">For more information about how the **SPropProblem** structure works with errors related to properties, see [MAPI Named Properties](mapi-named-properties.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f7be-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f7be-127">See also</span></span>



[<span data-ttu-id="7f7be-128">SCODE</span><span class="sxs-lookup"><span data-stu-id="7f7be-128">SCODE</span></span>](scode.md)
  
[<span data-ttu-id="7f7be-129">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="7f7be-129">SPropProblemArray</span></span>](spropproblemarray.md)


[<span data-ttu-id="7f7be-130">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7f7be-130">MAPI Structures</span></span>](mapi-structures.md)

