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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 389984f9d98ece6b2040edd741e3028fd7d766ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579313"
---
# <a name="smapiformproparray"></a><span data-ttu-id="608aa-103">SMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="608aa-103">SMAPIFormPropArray</span></span>

  
  
<span data-ttu-id="608aa-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="608aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="608aa-105">[SMAPIFormProp](smapiformprop.md)構造体の配列が含まれています。</span><span class="sxs-lookup"><span data-stu-id="608aa-105">Contains an array of [SMAPIFormProp](smapiformprop.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="608aa-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="608aa-106">Header file:</span></span>  <br/> |<span data-ttu-id="608aa-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="608aa-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="608aa-108">関連するマクロ:</span><span class="sxs-lookup"><span data-stu-id="608aa-108">Related macro:</span></span>  <br/> |[<span data-ttu-id="608aa-109">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="608aa-109">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md) <br/> |
   
```cpp
typedef struct
{
  ULONG cProps;
  ULONG ulPad;
  SMAPIFormProp aFormProp[MAPI_DIM];
} SMAPIFormPropArray, FAR * LPMAPIFORMPROPARRAY;

```

## <a name="members"></a><span data-ttu-id="608aa-110">Members</span><span class="sxs-lookup"><span data-stu-id="608aa-110">Members</span></span>

 <span data-ttu-id="608aa-111">**cProps**</span><span class="sxs-lookup"><span data-stu-id="608aa-111">**cProps**</span></span>
  
> <span data-ttu-id="608aa-112">**AFormProp**メンバーの配列の名前付きプロパティの数。</span><span class="sxs-lookup"><span data-stu-id="608aa-112">Count of named properties in the array in the **aFormProp** member.</span></span> 
    
 <span data-ttu-id="608aa-113">**ulPad**</span><span class="sxs-lookup"><span data-stu-id="608aa-113">**ulPad**</span></span>
  
>  <span data-ttu-id="608aa-114">適切なアライメントを保証するために使用される埋め込みの 8 バイトです。</span><span class="sxs-lookup"><span data-stu-id="608aa-114">Eight bytes of padding used to guarantee correct alignment.</span></span> 
    
 <span data-ttu-id="608aa-115">**aFormProp**</span><span class="sxs-lookup"><span data-stu-id="608aa-115">**aFormProp**</span></span>
  
> <span data-ttu-id="608aa-116">フォームのプロパティの配列です。</span><span class="sxs-lookup"><span data-stu-id="608aa-116">Array of form properties.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="608aa-117">注釈</span><span class="sxs-lookup"><span data-stu-id="608aa-117">Remarks</span></span>

<span data-ttu-id="608aa-118">**SMAPIFormPropArray**構造体は次の方法をパラメーターとして渡されます。</span><span class="sxs-lookup"><span data-stu-id="608aa-118">The **SMAPIFormPropArray** structure is passed as a parameter to the following methods:</span></span> 
  
- [<span data-ttu-id="608aa-119">IMAPIFormInfo::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="608aa-119">IMAPIFormInfo::CalcFormPropSet</span></span>](imapiforminfo-calcformpropset.md)
    
- [<span data-ttu-id="608aa-120">IMAPIFormMgr::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="608aa-120">IMAPIFormMgr::CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md)
    
- [<span data-ttu-id="608aa-121">IMAPIFormContainer::CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="608aa-121">IMAPIFormContainer::CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md)
    
## <a name="see-also"></a><span data-ttu-id="608aa-122">関連項目</span><span class="sxs-lookup"><span data-stu-id="608aa-122">See also</span></span>



[<span data-ttu-id="608aa-123">CbMAPIFormPropArray</span><span class="sxs-lookup"><span data-stu-id="608aa-123">CbMAPIFormPropArray</span></span>](cbmapiformproparray.md)
  
[<span data-ttu-id="608aa-124">SMAPIFormProp</span><span class="sxs-lookup"><span data-stu-id="608aa-124">SMAPIFormProp</span></span>](smapiformprop.md)


[<span data-ttu-id="608aa-125">MAPI の構造</span><span class="sxs-lookup"><span data-stu-id="608aa-125">MAPI Structures</span></span>](mapi-structures.md)

