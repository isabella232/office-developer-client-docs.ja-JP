---
title: ipropdatahraddobjprops
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416385"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="345dd-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="345dd-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="345dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="345dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="345dd-105">オブジェクトに PT_OBJECT 型の1つ以上のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="345dd-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="345dd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="345dd-106">Parameters</span></span>

 <span data-ttu-id="345dd-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="345dd-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="345dd-108">順番追加するプロパティを示すプロパティタグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="345dd-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="345dd-109">_lppproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="345dd-109">_lppProblems_</span></span>
  
> <span data-ttu-id="345dd-110">[入力]入力時、 [spropの配列](spropproblemarray.md)構造体への有効なポインター、または NULL。</span><span class="sxs-lookup"><span data-stu-id="345dd-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="345dd-111">出力時に、追加できなかったプロパティに関する情報を含む構造体へのポインター、または NULL。</span><span class="sxs-lookup"><span data-stu-id="345dd-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="345dd-112">プロパティ問題の配列構造体へのポインターは、有効なポインターが渡された場合にのみ返されます。</span><span class="sxs-lookup"><span data-stu-id="345dd-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="345dd-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="345dd-113">Return value</span></span>

<span data-ttu-id="345dd-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="345dd-114">S_OK</span></span> 
  
> <span data-ttu-id="345dd-115">プロパティが正常に追加されました。</span><span class="sxs-lookup"><span data-stu-id="345dd-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="345dd-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="345dd-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="345dd-117">PT_OBJECT 以外のプロパティの種類が、 _lpPropTagArray_パラメーターが指す配列に渡されました。</span><span class="sxs-lookup"><span data-stu-id="345dd-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="345dd-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="345dd-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="345dd-119">オブジェクトには、読み取り/書き込みアクセス許可が設定されていません。</span><span class="sxs-lookup"><span data-stu-id="345dd-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="345dd-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="345dd-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="345dd-121">プロパティのいくつかは追加されていますが、全部ではありません。</span><span class="sxs-lookup"><span data-stu-id="345dd-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="345dd-122">注釈</span><span class="sxs-lookup"><span data-stu-id="345dd-122">Remarks</span></span>

<span data-ttu-id="345dd-123">**ipropdata:: hraddobjprops**メソッドは、オブジェクトに PT_OBJECT 型の1つ以上のプロパティを追加します。</span><span class="sxs-lookup"><span data-stu-id="345dd-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="345dd-124">**hraddobjprops**は、オブジェクトプロパティの[imapiprop:: setprops](imapiprop-setprops.md)メソッドに代わる方法を提供します。これは、 **setprops**を呼び出すことでオブジェクトのプロパティを作成できないためです。</span><span class="sxs-lookup"><span data-stu-id="345dd-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="345dd-125">[imapiprop:: getproplist](imapiprop-getproplist.md)メソッドによって返される property タグのリストに含まれる property タグに、オブジェクトプロパティの結果が追加されました。</span><span class="sxs-lookup"><span data-stu-id="345dd-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="345dd-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="345dd-126">Notes to callers</span></span>

<span data-ttu-id="345dd-127">**hraddobjprops**が MAPI_W_PARTIAL_COMPLETION を返し、 _lppproblems 問題_を有効なポインターに設定している場合は、返された[spropprops 配列](spropproblemarray.md)構造を調べて、追加されなかったプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="345dd-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="345dd-128">通常、発生する問題はメモリが不足していることだけです。</span><span class="sxs-lookup"><span data-stu-id="345dd-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="345dd-129">完了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 **spropの配列**構造を解放します。</span><span class="sxs-lookup"><span data-stu-id="345dd-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="345dd-130">プロパティを追加するには、ターゲットオブジェクトが読み取り/書き込みアクセス許可を持っている必要があります。</span><span class="sxs-lookup"><span data-stu-id="345dd-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="345dd-131">**hraddobjprops**が MAPI_E_NO_ACCESS を返す場合は、変更が許可されていないため、オブジェクトにプロパティを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="345dd-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="345dd-132">**hraddobjprops**を呼び出す前に、オブジェクトへの読み取り/書き込みアクセス許可を取得するには、 [ipropdata:: HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出し、 _ulaccess_パラメーターを IPROP_READWRITE に設定します。</span><span class="sxs-lookup"><span data-stu-id="345dd-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="345dd-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="345dd-133">See also</span></span>



[<span data-ttu-id="345dd-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="345dd-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="345dd-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="345dd-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="345dd-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="345dd-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="345dd-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="345dd-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

