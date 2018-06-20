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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 985b763ade9670c064c6c338953debf7beaa2783
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801148"
---
# <a name="ipropdatahraddobjprops"></a><span data-ttu-id="fab6c-103">IPropData::HrAddObjProps</span><span class="sxs-lookup"><span data-stu-id="fab6c-103">IPropData::HrAddObjProps</span></span>

  
  
<span data-ttu-id="fab6c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fab6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fab6c-105">PT_OBJECT の種類の 1 つまたは複数のプロパティをオブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="fab6c-105">Adds one or more properties of type PT_OBJECT to the object.</span></span>
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="fab6c-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="fab6c-106">Parameters</span></span>

 <span data-ttu-id="fab6c-107">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="fab6c-107">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="fab6c-108">[in]追加するプロパティを指定するプロパティ タグの配列へのポインター。</span><span class="sxs-lookup"><span data-stu-id="fab6c-108">[in] A pointer to an array of property tags that indicate the properties to add.</span></span>
    
 <span data-ttu-id="fab6c-109">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="fab6c-109">_lppProblems_</span></span>
  
> <span data-ttu-id="fab6c-110">[で [チェック アウト]入力がある、 [SPropProblemArray](spropproblemarray.md)構造体への有効なポインターまたは NULL。</span><span class="sxs-lookup"><span data-stu-id="fab6c-110">[in, out] On input, a valid pointer to an [SPropProblemArray](spropproblemarray.md) structure, or NULL.</span></span> <span data-ttu-id="fab6c-111">[出力、追加できませんでしたのプロパティに関する情報を格納する構造体へのポインターへのポインターまたは NULL。</span><span class="sxs-lookup"><span data-stu-id="fab6c-111">On output, a pointer to a pointer to a structure that contains information about properties that could not be added, or NULL.</span></span> <span data-ttu-id="fab6c-112">プロパティの問題の配列の構造体へのポインターが有効なポインターが渡された場合にのみ返されます。</span><span class="sxs-lookup"><span data-stu-id="fab6c-112">A pointer to a property problem array structure is returned only if a valid pointer is passed in.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fab6c-113">�߂�l</span><span class="sxs-lookup"><span data-stu-id="fab6c-113">Return value</span></span>

<span data-ttu-id="fab6c-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="fab6c-114">S_OK</span></span> 
  
> <span data-ttu-id="fab6c-115">プロパティに追加されました。</span><span class="sxs-lookup"><span data-stu-id="fab6c-115">The properties were successfully added.</span></span>
    
<span data-ttu-id="fab6c-116">MAPI_E_INVALID_TYPE</span><span class="sxs-lookup"><span data-stu-id="fab6c-116">MAPI_E_INVALID_TYPE</span></span> 
  
> <span data-ttu-id="fab6c-117">プロパティは、PT_OBJECT は、 _lpPropTagArray_パラメーターが指す配列に渡された以外を入力します。</span><span class="sxs-lookup"><span data-stu-id="fab6c-117">A property type other than PT_OBJECT was passed in the array that the  _lpPropTagArray_ parameter points to.</span></span> 
    
<span data-ttu-id="fab6c-118">MAPI_E_NO_ACCESS</span><span class="sxs-lookup"><span data-stu-id="fab6c-118">MAPI_E_NO_ACCESS</span></span> 
  
> <span data-ttu-id="fab6c-119">オブジェクトは、読み取り/書き込み権限を許可しないように設定されています。</span><span class="sxs-lookup"><span data-stu-id="fab6c-119">The object has been set not to allow read/write permission.</span></span>
    
<span data-ttu-id="fab6c-120">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="fab6c-120">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="fab6c-121">すべてではなく、いくつかのプロパティが追加されました。</span><span class="sxs-lookup"><span data-stu-id="fab6c-121">Some, but not all, of the properties were added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fab6c-122">備考</span><span class="sxs-lookup"><span data-stu-id="fab6c-122">Remarks</span></span>

<span data-ttu-id="fab6c-123">**IPropData::HrAddObjProps**メソッドは、PT_OBJECT の種類の 1 つまたは複数のプロパティをオブジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="fab6c-123">The **IPropData::HrAddObjProps** method adds one or more properties of type PT_OBJECT to the object.</span></span> <span data-ttu-id="fab6c-124">**SetProps**を呼び出すことによってオブジェクトのプロパティを作成することはできませんので、 **HrAddObjProps**は代わりに、オブジェクトのプロパティの[IMAPIProp::SetProps](imapiprop-setprops.md)メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="fab6c-124">**HrAddObjProps** provides an alternative to the [IMAPIProp::SetProps](imapiprop-setprops.md) method for object properties, because object properties cannot be created by calling **SetProps**.</span></span> <span data-ttu-id="fab6c-125">[IMAPIProp::GetPropList](imapiprop-getproplist.md)メソッドで返されるプロパティ タグのリストに含まれているプロパティ タグでオブジェクトのプロパティの結果を追加します。</span><span class="sxs-lookup"><span data-stu-id="fab6c-125">Adding an object property results in the property tag being included in the list of property tags that the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method returns.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fab6c-126">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="fab6c-126">Notes to callers</span></span>

<span data-ttu-id="fab6c-127">**HrAddObjProps** MAPI_W_PARTIAL_COMPLETION を取得する_lppProblems_の有効なポインターを設定した場合、どのプロパティが追加されていないことを確認する返された[SPropProblemArray](spropproblemarray.md)構造体を確認してください。</span><span class="sxs-lookup"><span data-stu-id="fab6c-127">If **HrAddObjProps** returns MAPI_W_PARTIAL_COMPLETION and you have set  _lppProblems_ to a valid pointer, check the returned [SPropProblemArray](spropproblemarray.md) structure to find out which properties were not added.</span></span> <span data-ttu-id="fab6c-128">通常、発生する唯一の問題は、メモリ不足です。</span><span class="sxs-lookup"><span data-stu-id="fab6c-128">Typically, the only problem that occurs is lack of memory.</span></span> <span data-ttu-id="fab6c-129">操作を終了したら、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって、 **SPropProblemArray**構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="fab6c-129">Free the **SPropProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function when you are finished with it.</span></span> 
  
<span data-ttu-id="fab6c-130">プロパティを追加するには、対象のオブジェクトに読み取り/書き込み権限が必要です。</span><span class="sxs-lookup"><span data-stu-id="fab6c-130">To add a property, the target object must have read/write permission.</span></span> <span data-ttu-id="fab6c-131">**HrAddObjProps**では、MAPI_E_NO_ACCESS が返された場合の変更が許可されていないために、オブジェクトにプロパティを追加することはできません。</span><span class="sxs-lookup"><span data-stu-id="fab6c-131">If **HrAddObjProps** returns MAPI_E_NO_ACCESS, you cannot add properties to the object because it does not permit modification.</span></span> <span data-ttu-id="fab6c-132">**HrAddObjProps**を呼び出す前にオブジェクトへの読み取り/書き込み権限を取得するには、 [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md)を呼び出すし、 _ulAccess_パラメーターを IPROP_READWRITE に設定します。</span><span class="sxs-lookup"><span data-stu-id="fab6c-132">To obtain read/write permission to an object prior to calling **HrAddObjProps**, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) and set the  _ulAccess_ parameter to IPROP_READWRITE.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fab6c-133">関連項目</span><span class="sxs-lookup"><span data-stu-id="fab6c-133">See also</span></span>



[<span data-ttu-id="fab6c-134">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="fab6c-134">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="fab6c-135">SPropProblemArray</span><span class="sxs-lookup"><span data-stu-id="fab6c-135">SPropProblemArray</span></span>](spropproblemarray.md)
  
[<span data-ttu-id="fab6c-136">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="fab6c-136">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="fab6c-137">IPropData: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fab6c-137">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

