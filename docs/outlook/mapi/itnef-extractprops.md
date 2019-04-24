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
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 5a01c65bbec061248537558257c66d1a90128b5e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348651"
---
# <a name="itnefextractprops"></a><span data-ttu-id="d0f3a-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="d0f3a-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="d0f3a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0f3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0f3a-105">TNEF のカプセル化からプロパティを抽出します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="d0f3a-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d0f3a-106">Parameters</span></span>

 <span data-ttu-id="d0f3a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d0f3a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d0f3a-108">順番プロパティのデコード方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="d0f3a-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d0f3a-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="d0f3a-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="d0f3a-111">_lpproplist_パラメーターで指定されていないすべてのプロパティをデコードします。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="d0f3a-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="d0f3a-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="d0f3a-113">_lpproplist_で指定されたすべてのプロパティをデコードします。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="d0f3a-114">_lpproplist_</span><span class="sxs-lookup"><span data-stu-id="d0f3a-114">_lpPropList_</span></span>
  
> <span data-ttu-id="d0f3a-115">順番デコード操作に含めるまたは除外するプロパティのリストへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="d0f3a-116">_lpproblems 問題_</span><span class="sxs-lookup"><span data-stu-id="d0f3a-116">_lpProblems_</span></span>
  
> <span data-ttu-id="d0f3a-117">読み上げ返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="d0f3a-118">**STnefProblemArray**構造体は、どのプロパティが適切にエンコードされなかったかを示します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="d0f3a-119">lpproblems パラメーターで NULL が__ 渡された場合、プロパティ問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d0f3a-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="d0f3a-120">Return value</span></span>

<span data-ttu-id="d0f3a-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d0f3a-121">S_OK</span></span> 
  
> <span data-ttu-id="d0f3a-122">呼び出しが成功し、予想される値または値が返されました。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="d0f3a-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="d0f3a-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="d0f3a-124">ストリームにデコードされるデータが破損しています。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d0f3a-125">解説</span><span class="sxs-lookup"><span data-stu-id="d0f3a-125">Remarks</span></span>

<span data-ttu-id="d0f3a-126">トランスポートプロバイダー、メッセージストアプロバイダー、ゲートウェイは、 **ITnef:: ExtractProps**メソッドを呼び出して、メッセージまたは[OpenTnefStream](opentnefstream.md)関数に渡された添付ファイルのカプセル化から、プロパティを抽出 (デコード) します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="d0f3a-127">呼び出し元プロバイダーまたはゲートウェイは、デコードするプロパティのリストを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="d0f3a-128">プロバイダーとゲートウェイでは、 **ExtractProps**を使用して、添付ファイルの特別な処理に関する情報を提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="d0f3a-129">**ExtractProps**は、デコードされたプロパティを使用して、 **OpenTnefStream**に渡される元のメッセージを設定します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="d0f3a-130">後続の**ExtractProps**呼び出しは、メッセージに戻り、プロパティの新しいリストを抽出します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="d0f3a-131">[ITnef:: addprops](itnef-addprops.md)メソッドとは異なり、 **ITnef::: Finish**メソッドが呼び出されるまで、要求されたアクションをキューに入れます。 **ExtractProps**メソッドは、カプセル化されたプロパティを呼び出した直後にデコードします。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="d0f3a-132">そのため、カプセル化デコードのターゲットメッセージは、比較的空である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="d0f3a-133">ターゲットメッセージ内の既存のプロパティは、カプセル化されたプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="d0f3a-134">**ExtractProps**は、 **OpenTnefStream**または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_DECODE フラグを使用して開かれたオブジェクトに対してのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="d0f3a-135">tnef 実装は、 **ExtractProps**プロセスを停止することなく、tnef ストリームエンコードの問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="d0f3a-136">_lpproblems_で返される[STnefProblemArray](stnefproblemarray.md)構造は、どの TNEF 属性または MAPI プロパティ (もしあれば) を処理できなかったかを示します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="d0f3a-137">**STnefProblemArray**に含まれている**STnefProblem**構造体の**scode**メンバーで返される値は、特定の問題を示します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="d0f3a-138">プロバイダーまたはゲートウェイは、 **ExtractProps**が問題レポートを返さないすべてのプロパティまたは属性が正常に処理されたことを前提として機能します。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d0f3a-139">MAPI カプセル化ブロックのプロパティを処理できず、TNEF ストリームのデコード中にストリームが信頼されていない場合、カプセル化ブロックのデコードが停止され、問題が報告されます。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="d0f3a-140">この種の問題に対する問題の配列には、 **ulPropTag** `attMAPIProps` `attAttachment`メンバーの0L、 **ulattribute**メンバー、および**scode**メンバーの MAPI_E_UNABLE_TO_COMPLETE が含まれています。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="d0f3a-141">なお、ストリームのデコードは停止されず、MAPI カプセル化ブロックのデコードだけになります。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="d0f3a-142">ストリームのデコードは、次の属性ブロックで続行されます。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="d0f3a-143">プロバイダーまたはゲートウェイが問題のある配列で機能しない場合は、 _lppproblems_で NULL を渡すことができます。この場合、問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="d0f3a-144">_lpproblems 問題_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="d0f3a-145">S_OK が返された場合、プロバイダーまたはゲートウェイは、 **STnefProblemArray**構造体で返される値をチェックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="d0f3a-146">呼び出しでエラーが発生した場合、 **STnefProblemArray**構造体は入力されず、呼び出しプロバイダーまたはゲートウェイは構造を使用したり、解放したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="d0f3a-147">呼び出しでエラーが発生しない場合は、 [MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出して、 **STnefProblemArray**構造体のメモリを呼び出しプロバイダーまたはゲートウェイが解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d0f3a-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d0f3a-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="d0f3a-148">See also</span></span>



[<span data-ttu-id="d0f3a-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="d0f3a-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="d0f3a-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="d0f3a-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="d0f3a-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="d0f3a-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="d0f3a-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d0f3a-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d0f3a-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="d0f3a-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="d0f3a-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="d0f3a-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="d0f3a-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="d0f3a-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="d0f3a-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d0f3a-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

