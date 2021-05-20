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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5b76f9daec89e9229fc7f81e1332c3075c951067
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435678"
---
# <a name="itneffinish"></a><span data-ttu-id="a1d0f-103">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="a1d0f-103">ITnef::Finish</span></span>

  
  
<span data-ttu-id="a1d0f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1d0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1d0f-105">キューに入れ、待機Transport-Neutralのすべてのカプセル化形式 (TNEF) 操作の処理を終了します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-105">Finishes processing for all Transport-Neutral Encapsulation Format (TNEF) operations that are queued and waiting.</span></span> 
  
```cpp
HRESULT Finish(
  ULONG ulFlags,
  WORD FAR * lpKey,
  LPSTnefProblemArray FAR * lpProblem
);
```

## <a name="parameters"></a><span data-ttu-id="a1d0f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1d0f-106">Parameters</span></span>

 <span data-ttu-id="a1d0f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1d0f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a1d0f-108">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="a1d0f-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="a1d0f-109">_lpKey_</span><span class="sxs-lookup"><span data-stu-id="a1d0f-109">_lpKey_</span></span>
  
> <span data-ttu-id="a1d0f-110">[out]添付ファイルの **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) キー プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-110">[out] A pointer to the **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) key property of an attachment.</span></span> <span data-ttu-id="a1d0f-111">TNEF カプセル化オブジェクトは、このキーを使用して、メッセージ内の添付ファイルと添付ファイルの配置タグを一致します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-111">The TNEF encapsulation object uses this key to match an attachment to its attachment placement tag in a message.</span></span> <span data-ttu-id="a1d0f-112">このキーは、添付ファイルごとに一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-112">This key should be unique to each attachment.</span></span>
    
 <span data-ttu-id="a1d0f-113">_lpProblem_</span><span class="sxs-lookup"><span data-stu-id="a1d0f-113">_lpProblem_</span></span>
  
> <span data-ttu-id="a1d0f-114">[out]返される [STnefProblemArray 構造体へのポインターを指すポインター](stnefproblemarray.md) 。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-114">[out] A pointer to a pointer to a returned [STnefProblemArray](stnefproblemarray.md) structure.</span></span> <span data-ttu-id="a1d0f-115">**STnefProblemArray** 構造体は、適切にエンコードされていないプロパティがある場合は、どのプロパティを示します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-115">The **STnefProblemArray** structure indicates which properties, if any, were not encoded properly.</span></span> <span data-ttu-id="a1d0f-116">_lpProblem_ パラメーターに NULL が渡された場合、プロパティの問題の配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-116">If NULL is passed in the  _lpProblem_ parameter, no property problem array is returned.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a1d0f-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="a1d0f-117">Return value</span></span>

<span data-ttu-id="a1d0f-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1d0f-118">S_OK</span></span> 
  
> <span data-ttu-id="a1d0f-119">呼び出しは成功し、予期される値または値を返しました。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-119">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1d0f-120">注釈</span><span class="sxs-lookup"><span data-stu-id="a1d0f-120">Remarks</span></span>

<span data-ttu-id="a1d0f-121">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::Finish** メソッドを呼び出して [、ITnef::AddProps](itnef-addprops.md) メソッドおよび [ITnef::SetProps](itnef-setprops.md) メソッドの呼び出しでエンコードが要求されたすべてのプロパティのエンコードを実行します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-121">Transport providers, message store providers, and gateways call the **ITnef::Finish** method to perform the encoding of all properties for which encoding was requested in calls to the [ITnef::AddProps](itnef-addprops.md) and [ITnef::SetProps](itnef-setprops.md) methods.</span></span> <span data-ttu-id="a1d0f-122">TNEF オブジェクトが [OpenTnefStream](opentnefstream.md) 関数または [OpenTnefStreamEx](opentnefstreamex.md) 関数の TNEF_ENCODE フラグで開いた場合 **、Finish** メソッドは要求されたプロパティをそのオブジェクトに渡されたカプセル化ストリームにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-122">If the TNEF object was opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function, the **Finish** method encodes the requested properties into the encapsulation stream passed to that object.</span></span> <span data-ttu-id="a1d0f-123">TNEF オブジェクトを TNEF_DECODE フラグで開いた場合 **、Finish** メソッドは TNEF ストリームからプロパティをデコードし、所属するメッセージに書き戻します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-123">If the TNEF object was opened with the TNEF_DECODE flag, the **Finish** method decodes the properties from the TNEF stream and writes them back to the message they belong to.</span></span> 
  
<span data-ttu-id="a1d0f-124">Finish 呼 **び出** しの後、カプセル化ストリームへのポインターは TNEF データの末尾を指します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-124">After the **Finish** call, the pointer to the encapsulation stream points to the end of the TNEF data.</span></span> <span data-ttu-id="a1d0f-125">プロバイダーまたはゲートウェイが Finish 呼び出し後に TNEF ストリーム データを使用する必要がある場合は、ストリーム ポインターを TNEF ストリーム データの先頭にリセットする必要があります。 </span><span class="sxs-lookup"><span data-stu-id="a1d0f-125">If the provider or gateway needs to use the TNEF stream data after the **Finish** call, it must reset the stream pointer to the beginning of the TNEF stream data.</span></span> 
  
<span data-ttu-id="a1d0f-126">TNEF 実装は、終了プロセスを停止せずに TNEF ストリーム エンコードの問題を **報告** します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-126">The TNEF implementation reports TNEF stream encoding problems without stopping the **Finish** process.</span></span> <span data-ttu-id="a1d0f-127">_lpProblem_ パラメーターで返される [STnefProblemArray](stnefproblemarray.md)構造体は、処理できない TNEF 属性または MAPI プロパティを示します (指定されている場合)。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-127">The [STnefProblemArray](stnefproblemarray.md) structure returned in the  _lpProblem_ parameter indicates which TNEF attributes or MAPI properties, if any, could not be processed.</span></span> <span data-ttu-id="a1d0f-128">**STnefProblemArray** に含まれる **STnefProblem** 構造体の scode メンバーで返される値は、特定の問題を示します。 </span><span class="sxs-lookup"><span data-stu-id="a1d0f-128">The value returned in the **scode** member of the one of the **STnefProblem** structures contained in **STnefProblemArray** indicates the specific problem.</span></span> <span data-ttu-id="a1d0f-129">プロバイダーまたはゲートウェイは **、Finish** が問題レポートを返していないすべてのプロパティまたは属性が正常に処理されたという前提で作業できます。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-129">The provider or gateway can work on the assumption that all properties or attributes for which **Finish** does not return a problem report were processed successfully.</span></span> 
  
<span data-ttu-id="a1d0f-130">プロバイダーまたはゲートウェイが問題の配列で動作しない場合は  _、lpProblem で NULL を渡す可能性があります_。この場合、問題のある配列は返されません。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-130">If a provider or gateway does not work with problem arrays, it can pass NULL in  _lpProblem_; in this case, no problem array is returned.</span></span> 
  
<span data-ttu-id="a1d0f-131">_lpProblem_ で返される値は、呼び出しが無効な値を返すS_OK。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-131">The value returned in  _lpProblem_ is valid only if the call returns S_OK.</span></span> <span data-ttu-id="a1d0f-132">このS_OK返される場合、プロバイダーまたはゲートウェイは **、STnefProblemArray** 構造体で返される値を確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-132">When S_OK is returned, the provider or gateway should check the values returned in the **STnefProblemArray** structure.</span></span> <span data-ttu-id="a1d0f-133">呼び出しでエラーが発生した場合 **、STnefProblemArray** 構造体は入力されないので、呼び出し元プロバイダーまたはゲートウェイは構造体を使用または解放しません。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-133">If an error occurs on the call, the **STnefProblemArray** structure is not filled in and the calling provider or gateway should not use or free the structure.</span></span> <span data-ttu-id="a1d0f-134">呼び出しでエラーが発生しない場合、呼び出し元プロバイダーまたはゲートウェイは [、MAPIFreeBuffer](mapifreebuffer.md)関数を呼び出すことによって **STnefProblemArray** のメモリを解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-134">If no error occurs on the call, the calling provider or gateway must release the memory for the **STnefProblemArray** by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="a1d0f-135">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a1d0f-135">MFCMAPI reference</span></span>

<span data-ttu-id="a1d0f-136">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a1d0f-137">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a1d0f-137">**File**</span></span>|<span data-ttu-id="a1d0f-138">**関数**</span><span class="sxs-lookup"><span data-stu-id="a1d0f-138">**Function**</span></span>|<span data-ttu-id="a1d0f-139">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a1d0f-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a1d0f-140">File.cpp</span><span class="sxs-lookup"><span data-stu-id="a1d0f-140">File.cpp</span></span>  <br/> |<span data-ttu-id="a1d0f-141">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="a1d0f-141">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="a1d0f-142">MFCMAPI は **、ITnef::Finish** メソッドを使用して、新しい TNEF ストリームの処理を終了します。</span><span class="sxs-lookup"><span data-stu-id="a1d0f-142">MFCMAPI uses the **ITnef::Finish** method to finish processing of the new TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1d0f-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1d0f-143">See also</span></span>



[<span data-ttu-id="a1d0f-144">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="a1d0f-144">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="a1d0f-145">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a1d0f-145">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a1d0f-146">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="a1d0f-146">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="a1d0f-147">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="a1d0f-147">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="a1d0f-148">PidTagAttachNumber 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="a1d0f-148">PidTagAttachNumber Canonical Property</span></span>](pidtagattachnumber-canonical-property.md)
  
[<span data-ttu-id="a1d0f-149">STnefProblemArray</span><span class="sxs-lookup"><span data-stu-id="a1d0f-149">STnefProblemArray</span></span>](stnefproblemarray.md)
  
[<span data-ttu-id="a1d0f-150">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1d0f-150">ITnef : IUnknown</span></span>](itnefiunknown.md)


<span data-ttu-id="a1d0f-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a1d0f-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

