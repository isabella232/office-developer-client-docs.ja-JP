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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 7008549111f1b914cf2025c8d61ebc07196706fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801235"
---
# <a name="itneffinishcomponent"></a><span data-ttu-id="b3525-103">ITnef::FinishComponent</span><span class="sxs-lookup"><span data-stu-id="b3525-103">ITnef::FinishComponent</span></span>

  
  
<span data-ttu-id="b3525-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3525-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3525-105">トランスポート ニュートラル カプセル化形式 (TNEF) ストリームに同時に 1 つのメッセージからの個々 のコンポーネントを処理します。</span><span class="sxs-lookup"><span data-stu-id="b3525-105">Processes individual components from a message one at a time into a Transport-Neutral Encapsulation Format (TNEF) stream.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b3525-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="b3525-106">Parameters</span></span>

 <span data-ttu-id="b3525-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b3525-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b3525-108">[in]どのコンポーネントが完了するかを制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="b3525-108">[in] A bitmask of flags that controls which component will be finished.</span></span> <span data-ttu-id="b3525-109">いずれか、または次のフラグの一方を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3525-109">One or the other of the following flags must be set:</span></span>
    
<span data-ttu-id="b3525-110">TNEF_COMPONENT_ATTACHMENT</span><span class="sxs-lookup"><span data-stu-id="b3525-110">TNEF_COMPONENT_ATTACHMENT</span></span> 
  
> <span data-ttu-id="b3525-111">添付ファイル オブジェクトの処理を完了します。_ulComponentID_パラメーターには、添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のプロパティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="b3525-111">Processing will be finished for an attachment object; the  _ulComponentID_ parameter contains the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property of the attachment.</span></span> 
    
<span data-ttu-id="b3525-112">TNEF_COMPONENT_MESSAGE</span><span class="sxs-lookup"><span data-stu-id="b3525-112">TNEF_COMPONENT_MESSAGE</span></span> 
  
> <span data-ttu-id="b3525-113">メッセージ オブジェクトの処理を完了します。</span><span class="sxs-lookup"><span data-stu-id="b3525-113">Processing will be finished for a message object.</span></span> 
    
 <span data-ttu-id="b3525-114">_ulComponentID_</span><span class="sxs-lookup"><span data-stu-id="b3525-114">_ulComponentID_</span></span>
  
> <span data-ttu-id="b3525-115">[in] メッセージ、または添付ファイルの**PR_ATTACH_NUM**プロパティを処理するための処理を示すために 0 を返します。</span><span class="sxs-lookup"><span data-stu-id="b3525-115">[in] 0 to indicate processing for a message, or the **PR_ATTACH_NUM** property of an attachment to be processed.</span></span> <span data-ttu-id="b3525-116">_UlFlags_パラメーターに TNEF_COMPONENT_MESSAGE フラグを設定すると、 _ulComponentID_は 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3525-116">If the TNEF_COMPONENT_MESSAGE flag is set in the  _ulFlags_ parameter,  _ulComponentID_ must be 0.</span></span> 
    
 <span data-ttu-id="b3525-117">_lpCustomPropList_</span><span class="sxs-lookup"><span data-stu-id="b3525-117">_lpCustomPropList_</span></span>
  
> <span data-ttu-id="b3525-118">[in]_LpCustomProps_パラメーターで渡されたプロパティを識別するプロパティ タグを含む[SPropTagArray](sproptagarray.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b3525-118">[in] A pointer to an [SPropTagArray](sproptagarray.md) structure that contains property tags that identify the properties passed in the  _lpCustomProps_ parameter.</span></span> <span data-ttu-id="b3525-119">_LpCustomProps_の各プロパティの値と、 _lpCustomPropList_パラメーター内のプロパティ タグの間の 1 対 1 の対応をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3525-119">There must be a one-to-one correspondence between each property value in  _lpCustomProps_ and a property tag in the  _lpCustomPropList_ parameter.</span></span> 
    
 <span data-ttu-id="b3525-120">_lpCustomProps_</span><span class="sxs-lookup"><span data-stu-id="b3525-120">_lpCustomProps_</span></span>
  
> <span data-ttu-id="b3525-121">[in]エンコードするためにプロパティのプロパティ値を含む[SPropValue](spropvalue.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b3525-121">[in] A pointer to an [SPropValue](spropvalue.md) structure that contains property values for the properties to encode.</span></span> 
    
 <span data-ttu-id="b3525-122">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="b3525-122">_lpPropList_</span></span>
  
> <span data-ttu-id="b3525-123">[in]エンコードするにはプロパティのプロパティ タグを含む**SPropTagArray**構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b3525-123">[in] A pointer to an **SPropTagArray** structure that contains property tags for the properties to encode.</span></span> 
    
 <span data-ttu-id="b3525-124">_lppProblems_</span><span class="sxs-lookup"><span data-stu-id="b3525-124">_lppProblems_</span></span>
  
> <span data-ttu-id="b3525-125">[out]返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b3525-125">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="b3525-126">**STnefProblemArray**構造体は、どのプロパティでは、存在する場合、されたエンコードされません正しくを示します。</span><span class="sxs-lookup"><span data-stu-id="b3525-126">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="b3525-127">_LppProblems_パラメーターに NULL を渡した場合、プロパティの問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="b3525-127">If NULL is passed in the  _lppProblems_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b3525-128">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b3525-128">Return value</span></span>

<span data-ttu-id="b3525-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="b3525-129">S_OK</span></span> 
  
> <span data-ttu-id="b3525-130">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="b3525-130">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3525-131">����</span><span class="sxs-lookup"><span data-stu-id="b3525-131">Remarks</span></span>

<span data-ttu-id="b3525-132">プロバイダー、メッセージ ストア プロバイダー、および_ulFlags_パラメーターで設定するフラグで示されるように、TNEF は、メッセージまたは添付ファイルのいずれか 1 つのコンポーネントの処理を実行するのにはゲートウェイの呼び出し、 **ITnef::FinishComponent**メソッドを転送します。</span><span class="sxs-lookup"><span data-stu-id="b3525-132">Transport providers, message store providers, and gateways call the **ITnef::FinishComponent** method to perform TNEF processing for one component, either a message or an attachment, as indicated by the flag set in the  _ulFlags_ parameter.</span></span> 
  
<span data-ttu-id="b3525-133">有効にするコンポーネントで処理するため、呼び出し元のプロバイダーまたはゲートウェイはエンコードを受け取るオブジェクトを開く、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の_ulFlags_で TNEF_COMPONENT_ENCODING フラグを渡します。</span><span class="sxs-lookup"><span data-stu-id="b3525-133">For component processing to be enabled, the calling provider or gateway pass the TNEF_COMPONENT_ENCODING flag in  _ulFlags_ for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function that opened the object to receive encoding.</span></span> 
  
<span data-ttu-id="b3525-134">_LpCustomPropList_および_lpCustomProps_パラメーターに値を渡すことは、コンポーネントの[ITnef::SetProps](itnef-setprops.md)メソッドによって実行されるのと同じエンコーディングを実行します。</span><span class="sxs-lookup"><span data-stu-id="b3525-134">Passing values in the  _lpCustomPropList_ and  _lpCustomProps_ parameters performs component encoding equivalent to that done by the [ITnef::SetProps](itnef-setprops.md) method.</span></span> <span data-ttu-id="b3525-135">_UlFlags_で設定 TNEF_PROP_INCLUDE フラグを使用して、 [ITnef::AddProps](itnef-addprops.md)メソッドによって実行されるコンポーネントのエンコードと同じを実行する_lpPropList_パラメーターに値を渡すことです。</span><span class="sxs-lookup"><span data-stu-id="b3525-135">Passing a value in the  _lpPropList_ parameter performs component encoding equivalent to that done by the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag set in  _ulFlags_.</span></span> <span data-ttu-id="b3525-136">これらの値を渡すことを使用すると、複数の呼び出しではなく単一の呼び出しを使用してエンコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="b3525-136">Passing these values enables you to perform encodings with a single call instead of multiple calls.</span></span>
  
<span data-ttu-id="b3525-137">TNEF の実装では、 **FinishComponent**プロセスを停止することがなく TNEF ストリームのエンコーディングの問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="b3525-137">The TNEF implementation reports TNEF stream encoding problems without stopping the **FinishComponent** process.</span></span> <span data-ttu-id="b3525-138">_LppProblems_で返された**STnefProblemArray**構造体は、どの TNEF 属性または MAPI プロパティでは、存在する場合、処理できませんでしたを示します。</span><span class="sxs-lookup"><span data-stu-id="b3525-138">The **STnefProblemArray** structure returned in  _lppProblems_ indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="b3525-139">**STnefProblemArray**に含まれている**STnefProblem**の構造体のいずれかの**scode**メンバーの戻り値は、特定の問題を示します。</span><span class="sxs-lookup"><span data-stu-id="b3525-139">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="b3525-140">プロバイダーまたはゲートウェイは、すべてのプロパティまたは属性の**FinishComponent**が、問題レポートを返さないが正常に処理されたことを前提として処理できます。</span><span class="sxs-lookup"><span data-stu-id="b3525-140">The provider or gateway can work on the assumption that all properties or attributes for which **FinishComponent** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="b3525-141">_LppProblems_; で NULL を渡すことができます問題の配列を持つプロバイダーまたはゲートウェイが機能しない場合この例では、問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="b3525-141">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lppProblems_; in this case, no problem array is returned.</span></span>
  
<span data-ttu-id="b3525-142">_LppProblems_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="b3525-142">The value returned in  _lppProblems_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="b3525-143">S_OK が返されると、プロバイダーまたはゲートウェイは[STnefProblemArray](stnefproblemarray.md)構造体で返される値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b3525-143">When S_OK is returned, the provider or gateway should check the values returned in the [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="b3525-144">呼び出しでエラーが発生した場合、 **STnefProblemArray**構造体が入っていませんと、プロバイダーまたはゲートウェイが呼び出し元する必要があります使用または構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="b3525-144">If an error occurs on the call, the **STnefProblemArray** structure is not filled in, and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="b3525-145">呼び出しでエラーが発生しなかった場合、呼び出し元のプロバイダーまたはゲートウェイ必要がありますメモリを解放**STnefProblemArray**の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって。</span><span class="sxs-lookup"><span data-stu-id="b3525-145">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b3525-146">関連項目</span><span class="sxs-lookup"><span data-stu-id="b3525-146">See also</span></span>



[<span data-ttu-id="b3525-147">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="b3525-147">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="b3525-148">ITnef::SetProps</span><span class="sxs-lookup"><span data-stu-id="b3525-148">ITnef::SetProps</span></span>](itnef-setprops.md)
  
[<span data-ttu-id="b3525-149">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b3525-149">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b3525-150">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="b3525-150">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="b3525-151">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="b3525-151">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="b3525-152">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="b3525-152">SPropTagArray</span></span>](sproptagarray.md)
  
[<span data-ttu-id="b3525-153">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="b3525-153">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="b3525-154">ITnef: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3525-154">ITnef : IUnknown</span></span>](itnefiunknown.md)

