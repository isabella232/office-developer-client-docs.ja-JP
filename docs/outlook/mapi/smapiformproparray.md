---
title: SMAPIFormPropArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIFormPropArray
api_type:
- COM
ms.assetid: bb243bc4-4974-4ad6-aa76-2426c1ebe84b
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d907f2e8ecb9b6126898ff35b13427b088af9561
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803956"
---
# <a name="smapiformproparray"></a><span data-ttu-id="bd399-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="bd399-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="bd399-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bd399-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bd399-105">[SMAPIFormProp](smapiformprop.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bd399-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd399-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="bd399-106">Header file:</span></span>  <br/> |<span data-ttu-id="bd399-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="bd399-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="bd399-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="bd399-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="bd399-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="bd399-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="bd399-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="bd399-110">Members</span></span>

 <span data-ttu-id="bd399-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="bd399-111">**cProps**</span></span>
  
> <span data-ttu-id="bd399-112">**AFormProp**メンバーの配列の名前付きプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="bd399-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="bd399-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="bd399-113">**ulPad**</span></span>
  
>  <span data-ttu-id="bd399-114">適切なアライメントを保証するために使用される埋め込みの 8 バイトです。</span><span class="sxs-lookup"><span data-stu-id="bd399-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="bd399-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="bd399-115">**aFormProp**</span></span>
  
> <span data-ttu-id="bd399-116">フォームのプロパティの配列です。</span><span class="sxs-lookup"><span data-stu-id="bd399-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd399-117">備考</span><span class="sxs-lookup"><span data-stu-id="bd399-117">Remarks</span></span>

<span data-ttu-id="bd399-118">**SMAPIFormPropArray**構造体は次の方法をパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="bd399-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="bd399-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="bd399-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="bd399-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="bd399-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="bd399-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="bd399-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="bd399-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="bd399-122">See also</span></span>



[<span data-ttu-id="bd399-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="bd399-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="bd399-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="bd399-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="bd399-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="bd399-125">MAPI Structures</span></span>](mapi-structures.md)

