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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407502"
---
# <a name="itnefextractprops"></a><span data-ttu-id="d2412-103">ITnef::ExtractProps</span><span class="sxs-lookup"><span data-stu-id="d2412-103">ITnef::ExtractProps</span></span>

  
  
<span data-ttu-id="d2412-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2412-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2412-105">TNEF カプセル化からプロパティを抽出します。</span><span class="sxs-lookup"><span data-stu-id="d2412-105">Extracts the properties from a TNEF encapsulation.</span></span> 
  
```cpp
HRESULT ExtractProps(
  ULONG ulFlags,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lpProblems
);
```

## <a name="parameters"></a><span data-ttu-id="d2412-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d2412-106">Parameters</span></span>

 <span data-ttu-id="d2412-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2412-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d2412-108">[in]プロパティのデコード方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d2412-108">[in] A bitmask of flags that controls how properties are decoded.</span></span> <span data-ttu-id="d2412-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d2412-110">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="d2412-110">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="d2412-111">lpPropList パラメーターで指定されていないすべての  _プロパティをデコード_ します。</span><span class="sxs-lookup"><span data-stu-id="d2412-111">Decodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="d2412-112">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="d2412-112">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="d2412-113">lpPropList で指定されたプロパティ  _をデコードします_。</span><span class="sxs-lookup"><span data-stu-id="d2412-113">Decodes all properties specified in  _lpPropList_.</span></span>
    
 <span data-ttu-id="d2412-114">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="d2412-114">_lpPropList_</span></span>
  
> <span data-ttu-id="d2412-115">[in]デコード操作に含めるプロパティまたはデコード操作から除外するプロパティの一覧へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d2412-115">[in] A pointer to the list of properties to include in or exclude from the decoding operation.</span></span>
    
 <span data-ttu-id="d2412-116">_lpProblems_</span><span class="sxs-lookup"><span data-stu-id="d2412-116">_lpProblems_</span></span>
  
> <span data-ttu-id="d2412-117">[out]返される [STnefProblemArray 構造体へのポインターを指すポインター](stnefproblemarray.md) 。</span><span class="sxs-lookup"><span data-stu-id="d2412-117">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="d2412-118">**STnefProblemArray** 構造体は、適切にエンコードされていないプロパティがある場合は、どのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="d2412-118">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="d2412-119">_lpProblems_ パラメーターに NULL が渡された場合、プロパティの問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="d2412-119">If NULL is passed in the  _lpProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d2412-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="d2412-120">Return value</span></span>

<span data-ttu-id="d2412-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2412-121">S_OK</span></span> 
  
> <span data-ttu-id="d2412-122">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="d2412-122">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="d2412-123">MAPI_E_CORRUPT_DATA</span><span class="sxs-lookup"><span data-stu-id="d2412-123">MAPI_E_CORRUPT_DATA</span></span> 
  
> <span data-ttu-id="d2412-124">ストリームにデコードされるデータが破損しています。</span><span class="sxs-lookup"><span data-stu-id="d2412-124">Data being decoded into a stream is corrupted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2412-125">注釈</span><span class="sxs-lookup"><span data-stu-id="d2412-125">Remarks</span></span>

<span data-ttu-id="d2412-126">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::ExtractProps** メソッドを呼び出して [、OpenTnefStream](opentnefstream.md) 関数に渡されたメッセージまたは添付ファイルのカプセル化からプロパティを抽出 (つまり、デコード) します。</span><span class="sxs-lookup"><span data-stu-id="d2412-126">Transport providers, message store providers, and gateways call the **ITnef::ExtractProps** method to extract (that is, decode) properties from the encapsulation of a message or an attachment that was passed to the [OpenTnefStream](opentnefstream.md) function.</span></span> <span data-ttu-id="d2412-127">呼び出し元プロバイダーまたはゲートウェイは、デコードするプロパティの一覧を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-127">The calling provider or gateway can specify a list of properties to decode.</span></span> <span data-ttu-id="d2412-128">プロバイダーとゲートウェイは **ExtractProps** を使用して、添付ファイルの特別な処理に関する情報を提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="d2412-128">Providers and gateways can also use **ExtractProps** to provide information about any special handling for attachments.</span></span> 
  
 <span data-ttu-id="d2412-129">**ExtractProps は\*\*\*\*、OpenTnefStream** に渡された元のメッセージにデコードされたプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="d2412-129">**ExtractProps** populates the original message passed into **OpenTnefStream** with the decoded properties.</span></span> <span data-ttu-id="d2412-130">後続 **の ExtractProps 呼** び出しはメッセージに戻り、新しいプロパティの一覧を抽出します。</span><span class="sxs-lookup"><span data-stu-id="d2412-130">Subsequent **ExtractProps** calls go back to the message and extract the new list of properties.</span></span> 
  
<span data-ttu-id="d2412-131">[ITnef::AddProps](itnef-addprops.md)メソッドとは異なり **、ITnef::Finish** メソッドが呼び出されるまで要求されたアクションをキューに入れる場合 **、ExtractProps** メソッドは、呼び出された際にカプセル化されたプロパティを直ちにデコードします。</span><span class="sxs-lookup"><span data-stu-id="d2412-131">Unlike the [ITnef::AddProps](itnef-addprops.md) method, which queues requested actions until the **ITnef::Finish** method is called, the **ExtractProps** method decodes the encapsulated properties immediately when it is called.</span></span> <span data-ttu-id="d2412-132">このため、カプセル化デコードのターゲット メッセージは比較的空である必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2412-132">For that reason, the target message for encapsulation decoding should be relatively empty.</span></span> <span data-ttu-id="d2412-133">ターゲット メッセージ内の既存のプロパティは、カプセル化されたプロパティによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d2412-133">Existing properties in the target message are overwritten by encapsulated properties.</span></span> 
  
 <span data-ttu-id="d2412-134">**ExtractProps** は **、OpenTnefStream** または [OpenTnefStreamEx](opentnefstreamex.md) 関数の TNEF_DECODE フラグを使用して開くオブジェクトでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="d2412-134">**ExtractProps** is supported only for objects that are opened with the TNEF_DECODE flag for the **OpenTnefStream** or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="d2412-135">TNEF 実装では **、ExtractProps** プロセスを停止せずに TNEF ストリーム エンコードの問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="d2412-135">The TNEF implementation reports TNEF stream encoding problems without stopping the **ExtractProps** process.</span></span> <span data-ttu-id="d2412-136">_lpProblems_ で返される [STnefProblemArray](stnefproblemarray.md)構造体は、処理できない TNEF 属性または MAPI プロパティを示します (指定されている場合)。</span><span class="sxs-lookup"><span data-stu-id="d2412-136">The [STnefProblemArray](stnefproblemarray.md) structure returned in  _lpProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="d2412-137">**STnefProblemArray** に含まれる **STnefProblem** 構造体の scode メンバーで返される値は、特定の問題を示します。 </span><span class="sxs-lookup"><span data-stu-id="d2412-137">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="d2412-138">プロバイダーまたはゲートウェイは **、ExtractProps** が問題レポートを返していないすべてのプロパティまたは属性が正常に処理されたという前提で動作できます。</span><span class="sxs-lookup"><span data-stu-id="d2412-138">The provider or gateway can work on the assumption that all properties or attributes for which **ExtractProps** does not return a problem report were processed successfully.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d2412-139">MAPI カプセル化ブロック内のプロパティを処理できない場合、TNEF ストリームのデコード中にストリームが不当な状態になる場合は、カプセル化ブロックのデコードが停止され、問題が報告されます。</span><span class="sxs-lookup"><span data-stu-id="d2412-139">If a property in the MAPI encapsulation block cannot be processed and leaves the stream unreliable during the decoding of a TNEF stream, decoding of the encapsulation block is stopped and a problem is reported.</span></span> <span data-ttu-id="d2412-140">この種類の問題の問題配列には **、ulPropTag** メンバーの場合は 0L、ulAttribute メンバーの場合は 0L、scode メンバーには MAPI_E_UNABLE_TO_COMPLETE が `attMAPIProps` `attAttachment` **含** まれる。 </span><span class="sxs-lookup"><span data-stu-id="d2412-140">The problem array for this type of problem contains 0L for the **ulPropTag** member,  `attMAPIProps` or  `attAttachment` for the **ulAttribute** member, and MAPI_E_UNABLE_TO_COMPLETE for the **scode** member.</span></span> <span data-ttu-id="d2412-141">ストリームのデコードは停止されません。MAPI カプセル化ブロックのデコードに注意してください。</span><span class="sxs-lookup"><span data-stu-id="d2412-141">Note that the decoding of the stream is not halted, just the decoding of the MAPI encapsulation block.</span></span> <span data-ttu-id="d2412-142">ストリームのデコードは、次の属性ブロックで続行されます。</span><span class="sxs-lookup"><span data-stu-id="d2412-142">The stream decoding continues with the next attribute block.</span></span> 
  
<span data-ttu-id="d2412-143">プロバイダーまたはゲートウェイが問題の配列で動作しない場合は  _、lppProblems で NULL を渡す可能性があります_。この場合、問題のある配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="d2412-143">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="d2412-144">_lpProblems_ で返される値は、呼び出しが無効な値を返すS_OK。</span><span class="sxs-lookup"><span data-stu-id="d2412-144">The value returned in  _lpProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="d2412-145">このS_OK返される場合、プロバイダーまたはゲートウェイは **、STnefProblemArray** 構造体で返される値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2412-145">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="d2412-146">呼び出しでエラーが発生した場合 **、STnefProblemArray** 構造体は入力されないので、呼び出し元プロバイダーまたはゲートウェイは構造体を使用または解放しません。</span><span class="sxs-lookup"><span data-stu-id="d2412-146">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="d2412-147">呼び出しでエラーが発生しない場合、呼び出し元プロバイダーまたはゲートウェイは [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **STnefProblemArray** 構造体のメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2412-147">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** structure by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2412-148">関連項目</span><span class="sxs-lookup"><span data-stu-id="d2412-148">See also</span></span>



[<span data-ttu-id="d2412-149">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="d2412-149">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="d2412-150">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="d2412-150">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="d2412-151">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="d2412-151">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="d2412-152">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="d2412-152">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="d2412-153">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="d2412-153">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="d2412-154">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="d2412-154">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="d2412-155">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="d2412-155">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="d2412-156">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2412-156">ITnef : IUnknown</span></span>](itnefiunknown.md)

