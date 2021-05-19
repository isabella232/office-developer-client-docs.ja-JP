---
title: ITnefFinishComponent
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.FinishComponent
api_type:
- COM
ms.assetid: bcdd0688-0897-47d7-9601-f592ba453b39
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c8dc10bdb8bcde15dccf7bab4d9e10d2481cef11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416441"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="a74a4-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="a74a4-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="a74a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a74a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a74a4-105">メッセージの個々のコンポーネントを一度に 1 つ処理して、Transport-Neutralカプセル化形式 (TNEF) ストリームに処理します。</span><span class="sxs-lookup"><span data-stu-id="a74a4-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
```cpp
HRESULT FinishComponent(
  ULONG ulFlags,
  ULONG ulComponentID,
  LPSPropTagArray lpCustomPropList,
  LPSPropValue lpCustomProps,
  LPSPropTagArray lpPropList,
  LPSTnefProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a><span data-ttu-id="a74a4-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a74a4-106">Parameters</span></span>

 <span data-ttu-id="a74a4-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a74a4-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a74a4-108">[in]終了するコンポーネントを制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="a74a4-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="a74a4-109">次のいずれかのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a74a4-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="a74a4-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="a74a4-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="a74a4-111">添付ファイル オブジェクトの処理が完了します。  _ulComponentID_ パラメーターには、添付 **ファイルPR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティが含まれる。</span><span class="sxs-lookup"><span data-stu-id="a74a4-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="a74a4-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="a74a4-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="a74a4-113">メッセージ オブジェクトの処理が完了します。</span><span class="sxs-lookup"><span data-stu-id="a74a4-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="a74a4-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="a74a4-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="a74a4-115">[in] 0 メッセージの処理を示す場合、 **または** PR_ATTACH_NUM添付ファイルのプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="a74a4-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="a74a4-116">_ulFlags_ パラメーター TNEF_COMPONENT_MESSAGEフラグが設定されている場合 _、ulComponentID_ は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a74a4-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="a74a4-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="a74a4-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="a74a4-118">[in]_lpCustomProps_ パラメーターで渡されるプロパティを識別するプロパティ タグを含む [SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a74a4-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="a74a4-119">_lpCustomProps_ の各プロパティ値と _lpCustomPropList_ パラメーターのプロパティ タグの間には、1 対 1 の対応が必要です。</span><span class="sxs-lookup"><span data-stu-id="a74a4-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="a74a4-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="a74a4-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="a74a4-121">[in]エンコードするプロパティのプロパティ値を含む [SPropValue](spropvalue.md) 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a74a4-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="a74a4-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="a74a4-122">_lpPropList_</span></span>
  
> <span data-ttu-id="a74a4-123">[in]エンコードするプロパティのプロパティ タグを含む **SPropTagArray** 構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a74a4-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="a74a4-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="a74a4-124">_lppProblems_</span></span>
  
> <span data-ttu-id="a74a4-125">[out]返される [STnefProblemArray 構造体へのポインターを指すポインター](stnefproblemarray.md) 。</span><span class="sxs-lookup"><span data-stu-id="a74a4-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="a74a4-126">**STnefProblemArray** 構造体は、適切にエンコードされていないプロパティがある場合は、どのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="a74a4-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="a74a4-127">_lppProblems_ パラメーターに NULL が渡された場合、プロパティの問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="a74a4-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a74a4-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="a74a4-128">Return value</span></span>

<span data-ttu-id="a74a4-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="a74a4-129">S_OK</span></span> 
  
> <span data-ttu-id="a74a4-130">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a74a4-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a74a4-131">注釈</span><span class="sxs-lookup"><span data-stu-id="a74a4-131">Remarks</span></span>

<span data-ttu-id="a74a4-132">トランスポート プロバイダー、メッセージ ストア プロバイダー、ゲートウェイは **ITnef::FinishComponent** メソッドを呼び出して  _、ulFlags_ パラメーターで設定されたフラグで示されているメッセージまたは添付ファイルのどちらかの 1 つのコンポーネントに対して TNEF 処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="a74a4-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="a74a4-133">コンポーネント処理を有効にする場合、呼び出し元プロバイダーまたはゲートウェイは、エンコードを受け取るオブジェクトを開いた [OpenTnefStream](opentnefstream.md)または [OpenTnefStreamEx](opentnefstreamex.md)関数の _ulFlags_ で TNEF_COMPONENT_ENCODING フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="a74a4-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="a74a4-134">_lpCustomPropList_ パラメーターと _lpCustomProps_ パラメーターで値を渡す場合 [、ITnef::SetProps](itnef-setprops.md)メソッドで行われるコンポーネント エンコードと同等のコンポーネント エンコードが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a74a4-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="a74a4-135">_lpPropList_ パラメーターに値を渡す場合 _、ulFlags_ で TNEF_PROP_INCLUDE フラグが設定された [ITnef::AddProps](itnef-addprops.md)メソッドで行われるのと同等のコンポーネント エンコードが実行されます。</span><span class="sxs-lookup"><span data-stu-id="a74a4-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="a74a4-136">これらの値を渡すと、複数の呼び出しではなく、1 回の呼び出しでエンコードを実行できます。</span><span class="sxs-lookup"><span data-stu-id="a74a4-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="a74a4-137">TNEF 実装では **、FinishComponent** プロセスを停止せずに TNEF ストリーム エンコードの問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="a74a4-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="a74a4-138">_lppProblems_ で返される **STnefProblemArray** 構造体は、処理できない TNEF 属性または MAPI プロパティを示します(指定されている場合)。</span><span class="sxs-lookup"><span data-stu-id="a74a4-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="a74a4-139">**STnefProblemArray** に含まれる **STnefProblem** 構造体の scode メンバーで返される値は、特定の問題を示します。 </span><span class="sxs-lookup"><span data-stu-id="a74a4-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="a74a4-140">プロバイダーまたはゲートウェイは **、FinishComponent** が問題レポートを返さないすべてのプロパティまたは属性が正常に処理されたという前提で動作できます。</span><span class="sxs-lookup"><span data-stu-id="a74a4-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="a74a4-141">プロバイダーまたはゲートウェイが問題の配列で動作しない場合は  _、lppProblems で NULL を渡す可能性があります_。この場合、問題のある配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="a74a4-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="a74a4-142">_lppProblems_ で返される値は、呼び出しが無効な値を返すS_OK。</span><span class="sxs-lookup"><span data-stu-id="a74a4-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="a74a4-143">このS_OK返される場合、プロバイダーまたはゲートウェイは [、STnefProblemArray](stnefproblemarray.md) 構造体で返される値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a74a4-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="a74a4-144">呼び出しでエラーが発生した場合 **、STnefProblemArray** 構造体は入力されないので、呼び出し元プロバイダーまたはゲートウェイは構造体を使用または解放しません。</span><span class="sxs-lookup"><span data-stu-id="a74a4-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="a74a4-145">呼び出しでエラーが発生しない場合、呼び出し元プロバイダーまたはゲートウェイは [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **STnefProblemArray** のメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a74a4-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a74a4-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="a74a4-146">See also</span></span>



[<span data-ttu-id="a74a4-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="a74a4-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="a74a4-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="a74a4-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="a74a4-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a74a4-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a74a4-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="a74a4-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="a74a4-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="a74a4-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="a74a4-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="a74a4-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="a74a4-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="a74a4-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="a74a4-154">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a74a4-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

