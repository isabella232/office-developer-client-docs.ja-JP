---
title: ITnefFinish
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.Finish
api_type:
- COM
ms.assetid: 01a868f4-afda-43ba-bc17-c33ae56b7b7d
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 2b95e0dd62d83dd83a064ee4627811fcb24af921
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801244"
---
# <a name="itneffinish"></a><span data-ttu-id="1f6ab-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="1f6ab-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="1f6ab-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f6ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f6ab-105">完了するとキューに登録されたすべてのトランスポート ニュートラル カプセル化形式 (TNEF) 操作を処理し、待機しています。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="1f6ab-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="1f6ab-106">Parameters</span></span>

 <span data-ttu-id="1f6ab-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f6ab-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1f6ab-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="1f6ab-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1f6ab-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="1f6ab-109">_lpKey_</span></span>
  
> <span data-ttu-id="1f6ab-110">[out]添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) のキーのプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="1f6ab-111">TNEF カプセル化オブジェクトは、メッセージ内の添付ファイルの配置タグの添付ファイルに一致するようにこのキーを使用します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="1f6ab-112">このキーは、添付ファイルごとに一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="1f6ab-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="1f6ab-113">_lpProblem_</span></span>
  
> <span data-ttu-id="1f6ab-114">[out]返された[STnefProblemArray](stnefproblemarray.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="1f6ab-115">**STnefProblemArray**構造体は、どのプロパティでは、存在する場合、されたエンコードされません正しくを示します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="1f6ab-116">_LpProblem_パラメーターに NULL を渡した場合、プロパティの問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f6ab-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="1f6ab-117">Return value</span></span>

<span data-ttu-id="1f6ab-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f6ab-118">S_OK</span></span> 
  
> <span data-ttu-id="1f6ab-119">呼び出しが成功し、予期される値または値が返されます。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f6ab-120">注釈</span><span class="sxs-lookup"><span data-stu-id="1f6ab-120">Remarks</span></span>

<span data-ttu-id="1f6ab-121">プロバイダー、メッセージ ストア プロバイダーでは、どのエンコーディングのすべてのプロパティのエンコーディングを実行する**ITnef::Finish**メソッドは、 [ITnef::AddProps](itnef-addprops.md)メソッドと[ITnef::SetProps](itnef-setprops.md)メソッドの呼び出しで要求されたゲートウェイの呼び出しを転送します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="1f6ab-122">TNEF オブジェクトは、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の TNEF_ENCODE フラグを使用して開かれた、**完了**メソッドは要求されたプロパティをそのオブジェクトに渡されるカプセル化のストリームにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="1f6ab-123">TNEF_DECODE フラグを使用して、TNEF オブジェクトが開かれた場合、**終了**メソッドは TNEF ストリームからプロパティをデコードしに属しているメッセージに書き戻されます。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="1f6ab-124">**終了**の呼び出しの後は、カプセル化のストリームへのポインターは、TNEF データの末尾を指します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="1f6ab-125">プロバイダーまたはゲートウェイは、呼び出しの**完了**後は、TNEF ストリーム データを使用する必要があるは TNEF ストリーム データの先頭に、ストリームのポインターをリセットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="1f6ab-126">TNEF の実装では、**終了**処理を停止することがなく TNEF ストリームのエンコーディングの問題を報告します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="1f6ab-127">_LpProblem_パラメーターに返された[STnefProblemArray](stnefproblemarray.md)構造体は、どの TNEF 属性または MAPI プロパティでは、存在する場合、処理できませんでしたを示します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="1f6ab-128">**STnefProblemArray**に含まれている**STnefProblem**の構造体のいずれかの**scode**メンバーの戻り値は、特定の問題を示します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="1f6ab-129">プロバイダーまたはゲートウェイは、すべてのプロパティまたは属性の対象の**終了**を返さない問題レポートが正常に処理されたことを前提として処理できます。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="1f6ab-130">_LpProblem_; で NULL を渡すことができます問題の配列を持つプロバイダーまたはゲートウェイが機能しない場合この例では、問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="1f6ab-131">_LpProblem_で返される値は、呼び出しが S_OK を返す場合にのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="1f6ab-132">S_OK が返されると、プロバイダーまたはゲートウェイは**STnefProblemArray**構造体で返される値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="1f6ab-133">呼び出しでエラーが発生した場合**STnefProblemArray**構造体が記入されていませんし、プロバイダーまたはゲートウェイが呼び出し元する必要があります使用または構造体を解放します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="1f6ab-134">呼び出しでエラーが発生しなかった場合、呼び出し元のプロバイダーまたはゲートウェイ必要がありますメモリを解放**STnefProblemArray**の[MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1f6ab-135">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="1f6ab-135">MFCMAPI reference</span></span>

<span data-ttu-id="1f6ab-136">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="1f6ab-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1f6ab-137">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-137">**File**</span></span>|<span data-ttu-id="1f6ab-138">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-138">**Function**</span></span>|<span data-ttu-id="1f6ab-139">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1f6ab-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="1f6ab-140">File.cpp</span></span>  <br/> |<span data-ttu-id="1f6ab-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="1f6ab-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="1f6ab-142">MFCMAPI では、 **ITnef::Finish**メソッドを使用して、新しい TNEF ストリームの処理を完了します。</span><span class="sxs-lookup"><span data-stu-id="1f6ab-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1f6ab-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="1f6ab-143">See also</span></span>



[<span data-ttu-id="1f6ab-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="1f6ab-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="1f6ab-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="1f6ab-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="1f6ab-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="1f6ab-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="1f6ab-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="1f6ab-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="1f6ab-148">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="1f6ab-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="1f6ab-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="1f6ab-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="1f6ab-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f6ab-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


<span data-ttu-id="1f6ab-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="1f6ab-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

