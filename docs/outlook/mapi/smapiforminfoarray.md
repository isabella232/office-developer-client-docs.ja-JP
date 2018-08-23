---
title: SMAPIFormInfoArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormInfoArray
api_type:
- COM
ms.assetid: f5eeb75d-debb-4ac1-b239-e8e852460ce0
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6389bbf2094f51711d80896db0db9862059826cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803964"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="b238c-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="b238c-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="b238c-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b238c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b238c-105">フォーム オブジェクトの情報へのポインターの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b238c-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b238c-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b238c-106">Header file:</span></span>  <br/> |<span data-ttu-id="b238c-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="b238c-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="b238c-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="b238c-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="b238c-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="b238c-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="b238c-110">Members</span><span class="sxs-lookup"><span data-stu-id="b238c-110">Members</span></span>

 <span data-ttu-id="b238c-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="b238c-111">**cForms**</span></span>
  
> <span data-ttu-id="b238c-112">**AFormInfo**メンバーが指す配列内のポインターの数です。</span><span class="sxs-lookup"><span data-stu-id="b238c-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="b238c-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="b238c-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="b238c-114">フォーム オブジェクトの情報へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b238c-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b238c-115">注釈</span><span class="sxs-lookup"><span data-stu-id="b238c-115">Remarks</span></span>

<span data-ttu-id="b238c-116">**SMAPIFormInfoArray**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="b238c-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="b238c-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="b238c-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="b238c-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="b238c-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="b238c-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="b238c-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="b238c-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="b238c-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="b238c-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="b238c-121">See also</span></span>



[<span data-ttu-id="b238c-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="b238c-122">MAPI Structures</span></span>](mapi-structures.md)

