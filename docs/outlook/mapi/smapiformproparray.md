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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 50b6581dec8211968a49b204c6d9b1ba1c65bb62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420067"
---
# <a name="smapiformproparray"></a><span data-ttu-id="0c26a-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="0c26a-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="0c26a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c26a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c26a-105">[smapiformprop](smapiformprop.md)構造体の配列を格納します。</span><span class="sxs-lookup"><span data-stu-id="0c26a-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c26a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0c26a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c26a-107">Mapiform</span><span class="sxs-lookup"><span data-stu-id="0c26a-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="0c26a-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="0c26a-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="0c26a-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="0c26a-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="0c26a-110">メンバー</span><span class="sxs-lookup"><span data-stu-id="0c26a-110">Members</span></span>

 <span data-ttu-id="0c26a-111">**cprops**</span><span class="sxs-lookup"><span data-stu-id="0c26a-111">**cProps**</span></span>
  
> <span data-ttu-id="0c26a-112">**aformprop**メンバーの配列内の名前付きプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="0c26a-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="0c26a-113">**ulpad**</span><span class="sxs-lookup"><span data-stu-id="0c26a-113">**ulPad**</span></span>
  
>  <span data-ttu-id="0c26a-114">正しいアラインメントを保証するために使用する8バイトのパディング。</span><span class="sxs-lookup"><span data-stu-id="0c26a-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="0c26a-115">**aformprop**</span><span class="sxs-lookup"><span data-stu-id="0c26a-115">**aFormProp**</span></span>
  
> <span data-ttu-id="0c26a-116">フォームプロパティの配列。</span><span class="sxs-lookup"><span data-stu-id="0c26a-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c26a-117">注釈</span><span class="sxs-lookup"><span data-stu-id="0c26a-117">Remarks</span></span>

<span data-ttu-id="0c26a-118">**smapiformproparray**の構造体は、次のメソッドにパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="0c26a-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="0c26a-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="0c26a-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="0c26a-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="0c26a-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="0c26a-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="0c26a-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="0c26a-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c26a-122">See also</span></span>



[<span data-ttu-id="0c26a-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="0c26a-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="0c26a-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="0c26a-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="0c26a-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="0c26a-125">MAPI Structures</span></span>](mapi-structures.md)

