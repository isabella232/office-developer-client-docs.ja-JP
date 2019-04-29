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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e274e24d9aff30bb39b1865306477164d413d9a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416973"
---
# <a name="smapiforminfoarray"></a><span data-ttu-id="24ead-103">SMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="24ead-103">SMAPIFormInfoArray</span></span>

  
  
<span data-ttu-id="24ead-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="24ead-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="24ead-105">フォーム情報オブジェクトへのポインターの配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="24ead-105">Contains an array of pointers to form information objects.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24ead-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="24ead-106">Header file:</span></span>  <br/> |<span data-ttu-id="24ead-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="24ead-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="24ead-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="24ead-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="24ead-109">CbMAPIFormInfoArray</span><span class="sxs-lookup"><span data-stu-id="24ead-109">CbMAPIFormInfoArray</span></span>](cbmapiforminfoarray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cForms;
  LPMAPIFORMINFO aFormInfo[MAPI_DIM];
} SMAPIFormInfoArray, FAR * LPSMAPIFORMINFOARRAY;

```

## <a name="members"></a><span data-ttu-id="24ead-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="24ead-110">Members</span></span>

 <span data-ttu-id="24ead-111">**cforms**</span><span class="sxs-lookup"><span data-stu-id="24ead-111">**cForms**</span></span>
  
> <span data-ttu-id="24ead-112">**aforminfo**メンバーによって示される配列内のポインターの数。</span><span class="sxs-lookup"><span data-stu-id="24ead-112">Count of pointers in the array pointed to by the **aFormInfo** member.</span></span> 
    
 <span data-ttu-id="24ead-113">**aforminfo**</span><span class="sxs-lookup"><span data-stu-id="24ead-113">**aFormInfo**</span></span>
  
> <span data-ttu-id="24ead-114">フォーム情報オブジェクトへのポインターの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="24ead-114">Pointer to an array of pointers to form information objects.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="24ead-115">注釈</span><span class="sxs-lookup"><span data-stu-id="24ead-115">Remarks</span></span>

<span data-ttu-id="24ead-116">**smapiforminfoarray**構造体は、次のメソッドのパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="24ead-116">The **SMAPIFormInfoArray** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="24ead-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="24ead-117">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="24ead-118">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="24ead-118">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="24ead-119">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="24ead-119">IMAPIFormMgr::SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md)
    
- [<span data-ttu-id="24ead-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="24ead-120">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="24ead-121">関連項目</span><span class="sxs-lookup"><span data-stu-id="24ead-121">See also</span></span>



[<span data-ttu-id="24ead-122">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="24ead-122">MAPI Structures</span></span>](mapi-structures.md)

