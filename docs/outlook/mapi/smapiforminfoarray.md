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
ms.openlocfilehash: 6c09c271fefcf31dcde01526d65091714c0b682d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576275"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="7a526-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="7a526-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="7a526-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a526-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a526-105">フォーム オブジェクトの情報へのポインターの配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7a526-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7a526-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7a526-106">Header file:</span></span>  <br/> |<span data-ttu-id="7a526-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="7a526-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7a526-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="7a526-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="7a526-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="7a526-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="7a526-110">Members</span><span class="sxs-lookup"><span data-stu-id="7a526-110">Members</span></span>

 <span data-ttu-id="7a526-111">**cForms**</span><span class="sxs-lookup"><span data-stu-id="7a526-111">**cForms**</span></span>
  
> <span data-ttu-id="7a526-112">**AFormInfo**メンバーが指す配列内のポインターの数です。</span><span class="sxs-lookup"><span data-stu-id="7a526-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="7a526-113">**aFormInfo**</span><span class="sxs-lookup"><span data-stu-id="7a526-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="7a526-114">フォーム オブジェクトの情報へのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7a526-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a526-115">注釈</span><span class="sxs-lookup"><span data-stu-id="7a526-115">Remarks</span></span>

<span data-ttu-id="7a526-116">**SMAPIFormInfoArray**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="7a526-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="7a526-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7a526-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="7a526-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="7a526-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="7a526-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="7a526-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="7a526-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="7a526-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="7a526-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="7a526-121">See also</span></span>



[<span data-ttu-id="7a526-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="7a526-122">MAPI Structures</span></span>](mapi-structures.md)

