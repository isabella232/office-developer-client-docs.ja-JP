---
title: IPropDataHrAddObjProps
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
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="98529-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="98529-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="98529-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98529-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98529-105">オブジェクトの種類のプロパティを 1 つ以上PT_OBJECTオブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="98529-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="98529-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="98529-106">Parameters</span></span>

 <span data-ttu-id="98529-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="98529-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="98529-108">[in]追加するプロパティを示すプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="98529-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="98529-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="98529-109">_lppProblems_</span></span>
  
> <span data-ttu-id="98529-110">[in, out]入力時に [、SPropProblemArray](spropproblemarray.md) 構造体または NULL への有効なポインター。</span><span class="sxs-lookup"><span data-stu-id="98529-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="98529-111">出力時に、追加できないプロパティまたは NULL に関する情報を含む構造体へのポインターを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="98529-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="98529-112">プロパティの問題配列構造へのポインターは、有効なポインターが渡された場合にのみ返されます。</span><span class="sxs-lookup"><span data-stu-id="98529-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="98529-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="98529-113">Return value</span></span>

<span data-ttu-id="98529-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="98529-114">S_OK</span></span> 
  
> <span data-ttu-id="98529-115">プロパティが正常に追加されました。</span><span class="sxs-lookup"><span data-stu-id="98529-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="98529-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="98529-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="98529-117">_lpPropTagArray_ パラメーター PT_OBJECT示す配列に渡されたプロパティ以外のプロパティの種類。</span><span class="sxs-lookup"><span data-stu-id="98529-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="98529-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="98529-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="98529-119">オブジェクトは、読み取り/書き込みアクセス許可を許可しない設定されています。</span><span class="sxs-lookup"><span data-stu-id="98529-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="98529-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="98529-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="98529-121">プロパティの一部が追加されましたが、すべてではありません。</span><span class="sxs-lookup"><span data-stu-id="98529-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="98529-122">注釈</span><span class="sxs-lookup"><span data-stu-id="98529-122">Remarks</span></span>

<span data-ttu-id="98529-123">**IPropData::HrAddObjProps** メソッドは、オブジェクトの種類のプロパティを 1 つ以上PT_OBJECTオブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="98529-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="98529-124">**HrAddObjProps** は **、SetProps** を呼び出してオブジェクト プロパティを作成できないので、オブジェクト プロパティの [IMAPIProp::SetProps](imapiprop-setprops.md)メソッドの代わりに使用できます。</span><span class="sxs-lookup"><span data-stu-id="98529-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="98529-125">オブジェクト プロパティを追加すると [、IMAPIProp::GetPropList](imapiprop-getproplist.md) メソッドが返すプロパティ タグの一覧にプロパティ タグが含まれます。</span><span class="sxs-lookup"><span data-stu-id="98529-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="98529-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="98529-126">Notes to callers</span></span>

<span data-ttu-id="98529-127">**HrAddObjProps** が MAPI_W_PARTIAL_COMPLETION を返し _、lppProblems_ を有効なポインターに設定している場合は、返された [SPropProblemArray](spropproblemarray.md)構造体を確認して、追加されていないプロパティを確認します。</span><span class="sxs-lookup"><span data-stu-id="98529-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="98529-128">通常、発生する唯一の問題はメモリ不足です。</span><span class="sxs-lookup"><span data-stu-id="98529-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="98529-129">終わったら、MAPIFreeBuffer 関数を呼び出して **SPropProblemArray** 構造体を解放します。 [](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="98529-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="98529-130">プロパティを追加するには、ターゲット オブジェクトに読み取り/書き込みアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="98529-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="98529-131">**HrAddObjProps** がオブジェクトをMAPI_E_NO_ACCESS場合は、変更を許可しないので、オブジェクトにプロパティを追加できません。</span><span class="sxs-lookup"><span data-stu-id="98529-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="98529-132">**HrAddObjProps** を呼び出す前にオブジェクトに対する読み取り/書き込みアクセス許可を取得するには [、IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出し _、ulAccess_ パラメーターを IPROP_READWRITE に設定します。</span><span class="sxs-lookup"><span data-stu-id="98529-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="98529-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="98529-133">See also</span></span>



[<span data-ttu-id="98529-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="98529-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="98529-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="98529-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="98529-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="98529-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="98529-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="98529-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

