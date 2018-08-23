---
title: ITnefExtractProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.ExtractProps
api_type:
- COM
ms.assetid: 9169a5be-21dd-4938-8db3-522bea165c92
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0765e46a6f0545682b16e484d08d296ea13e2136
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571347"
---
# <a name="itnefextractprops"></a><span data-ttu-id="94fa6-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="94fa6-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="94fa6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="94fa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="94fa6-105">TNEF のカプセル化のプロパティを抽出します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="94fa6-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="94fa6-106">Parameters</span></span>

 <span data-ttu-id="94fa6-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="94fa6-107">_ulFlags_</span></span>
  
> <span data-ttu-id="94fa6-108">[in]プロパティをデコードする方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="94fa6-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="94fa6-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="94fa6-109">The following flags can be set:</span></span>
    
<span data-ttu-id="94fa6-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="94fa6-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="94fa6-111">_LpPropList_パラメーターで指定されていないすべてのプロパティをデコードします。</span><span class="sxs-lookup"><span data-stu-id="94fa6-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="94fa6-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="94fa6-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="94fa6-113">_LpPropList_で指定されたすべてのプロパティをデコードします。</span><span class="sxs-lookup"><span data-stu-id="94fa6-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="94fa6-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="94fa6-114">_lpPropList_</span></span>
  
> <span data-ttu-id="94fa6-115">[in]含めるか、デコード処理から除外するプロパティの一覧へのポインター。</span><span class="sxs-lookup"><span data-stu-id="94fa6-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="94fa6-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="94fa6-116">_lpProblems_</span></span>
  
> <span data-ttu-id="94fa6-117">[out]返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="94fa6-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="94fa6-118">**STnefProblemArray**構造体は、どのプロパティでは、存在する場合、されたエンコードされません正しくを示します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="94fa6-119">_LpProblems_パラメーターに NULL を渡した場合、プロパティの問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="94fa6-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="94fa6-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="94fa6-120">Return value</span></span>

<span data-ttu-id="94fa6-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="94fa6-121">S_OK</span></span> 
  
> <span data-ttu-id="94fa6-122">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="94fa6-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="94fa6-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="94fa6-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="94fa6-124">ストリームにデコードされたデータが壊れています。</span><span class="sxs-lookup"><span data-stu-id="94fa6-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="94fa6-125">注釈</span><span class="sxs-lookup"><span data-stu-id="94fa6-125">Remarks</span></span>

<span data-ttu-id="94fa6-126">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイ メソッドを呼び出す**ITnef::ExtractProps**を抽出する (これをデコード) は、プロパティをメッセージまたは[OpenTnefStream](opentnefstream.md)関数に渡された添付ファイルをカプセル化します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="94fa6-127">呼び出し元のプロバイダーまたはゲートウェイには、デコードするためのプロパティの一覧を指定できます。</span><span class="sxs-lookup"><span data-stu-id="94fa6-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="94fa6-128">プロバイダーとゲートウェイも使用できます**ExtractProps**の添付ファイルに対して特別な処理情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="94fa6-129">**ExtractProps**には、デコードされたプロパティを使用して、 **OpenTnefStream**に渡された元のメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="94fa6-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="94fa6-130">**ExtractProps**の後続の呼び出しはメッセージに戻るし、プロパティの新しいリストを抽出します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="94fa6-131">キューにアクションが要求されるは、 **ITnef::Finish**メソッドが呼び出されるまで、 [ITnef::AddProps](itnef-addprops.md)メソッドとは異なり、 **ExtractProps**メソッドは、呼び出されたときにすぐにカプセル化されたプロパティをデコードします。</span><span class="sxs-lookup"><span data-stu-id="94fa6-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="94fa6-132">そのため、移行先のメッセージのカプセル化をデコードすることが比較的空でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="94fa6-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="94fa6-133">カプセル化されたプロパティでは、移行先のメッセージ内の既存のプロパティが上書きされます。</span><span class="sxs-lookup"><span data-stu-id="94fa6-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="94fa6-134">**ExtractProps**は、 **OpenTnefStream**または[OpenTnefStreamEx](opentnefstreamex.md)関数の場合、TNEF_DECODE フラグを使用して開かれているオブジェクトでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="94fa6-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="94fa6-135">TNEF の実装では、 **ExtractProps**プロセスを停止することがなく TNEF ストリームのエンコーディングの問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="94fa6-136">_LpProblems_で返された[STnefProblemArray](stnefproblemarray.md)構造体は、どの TNEF 属性または MAPI プロパティでは、存在する場合、処理できませんでしたを示します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="94fa6-137">**STnefProblemArray**に含まれている**STnefProblem**の構造体のいずれかの**scode**メンバーの戻り値は、特定の問題を示します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="94fa6-138">プロバイダーまたはゲートウェイは、すべてのプロパティまたは属性の**ExtractProps**が、問題レポートを返さないが正常に処理されたことを前提として処理できます。</span><span class="sxs-lookup"><span data-stu-id="94fa6-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="94fa6-139">MAPI のカプセル化のブロック内のプロパティを処理できません、TNEF ストリームのデコード時に、ストリームの信頼性が低いままのカプセル化のブロックをデコードすることを停止して、問題が報告されました。</span><span class="sxs-lookup"><span data-stu-id="94fa6-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="94fa6-140">この種の問題の問題の配列には、 **ulPropTag**メンバーの 0 L が含まれています`attMAPIProps`または`attAttachment` **ulAttribute**のメンバー、および**scode**メンバーの MAPI_E_UNABLE_TO_COMPLETE のです。</span><span class="sxs-lookup"><span data-stu-id="94fa6-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="94fa6-141">MAPI のカプセル化のブロックのデコードだけ、ストリームのデコードではないメモが停止しました。</span><span class="sxs-lookup"><span data-stu-id="94fa6-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="94fa6-142">ストリームのデコードは、次の属性ブロックを続行します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="94fa6-143">_LppProblems_; で NULL を渡すことができます問題の配列を持つプロバイダーまたはゲートウェイが機能しない場合この例では、問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="94fa6-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="94fa6-144">_LpProblems_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="94fa6-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="94fa6-145">S_OK が返されると、プロバイダーまたはゲートウェイは**STnefProblemArray**構造体で返される値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="94fa6-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="94fa6-146">呼び出しでエラーが発生した場合**STnefProblemArray**構造体が記入されていませんし、プロバイダーまたはゲートウェイが呼び出し元する必要があります使用または構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="94fa6-147">呼び出しでエラーが発生しなかった場合、呼び出し元のプロバイダーまたはゲートウェイ必要があります[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって**STnefProblemArray**構造体のメモリを解放します。</span><span class="sxs-lookup"><span data-stu-id="94fa6-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="94fa6-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="94fa6-148">See also</span></span>



[<span data-ttu-id="94fa6-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="94fa6-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="94fa6-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="94fa6-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="94fa6-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="94fa6-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="94fa6-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="94fa6-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="94fa6-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="94fa6-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="94fa6-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="94fa6-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="94fa6-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="94fa6-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="94fa6-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="94fa6-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

