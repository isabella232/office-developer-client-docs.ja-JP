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
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319174"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="bf36d-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="bf36d-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="bf36d-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bf36d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bf36d-105">フォーム情報オブジェクトへのポインターの配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="bf36d-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bf36d-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bf36d-106">Header file:</span></span>  <br/> |<span data-ttu-id="bf36d-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="bf36d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bf36d-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="bf36d-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="bf36d-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="bf36d-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="bf36d-110">Members</span><span class="sxs-lookup"><span data-stu-id="bf36d-110">Members</span></span>

 <span data-ttu-id="bf36d-111">**cforms**</span><span class="sxs-lookup"><span data-stu-id="bf36d-111">**cForms**</span></span>
  
> <span data-ttu-id="bf36d-112">**aforminfo**メンバーによって示される配列内のポインターの数。</span><span class="sxs-lookup"><span data-stu-id="bf36d-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="bf36d-113">**aforminfo**</span><span class="sxs-lookup"><span data-stu-id="bf36d-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="bf36d-114">フォーム情報オブジェクトへのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bf36d-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bf36d-115">解説</span><span class="sxs-lookup"><span data-stu-id="bf36d-115">Remarks</span></span>

<span data-ttu-id="bf36d-116">**smapiforminfoarray**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="bf36d-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="bf36d-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="bf36d-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="bf36d-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="bf36d-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="bf36d-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="bf36d-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="bf36d-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="bf36d-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="bf36d-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf36d-121">See also</span></span>



[<span data-ttu-id="bf36d-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="bf36d-122">MAPI Structures</span></span>](mapi-structures.md)

