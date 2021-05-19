---
title: ITnefAddProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.AddProps
api_type:
- COM
ms.assetid: e85641fb-6d3c-494a-981c-01781c7bf5bb
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6a7bb7265d29d2acfce17a1a09c95f7f7b539064
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348623"
---
# <a name="itnefaddprops"></a><span data-ttu-id="95514-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="95514-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="95514-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95514-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95514-105">呼び出し元のサービス プロバイダーまたはゲートウェイが、メッセージまたは添付ファイルのカプセル化にプロパティを追加できます。</span><span class="sxs-lookup"><span data-stu-id="95514-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="95514-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="95514-106">Parameters</span></span>

 <span data-ttu-id="95514-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="95514-107">_ulFlags_</span></span>
  
> <span data-ttu-id="95514-108">[in]カプセル化にプロパティを含めるか、カプセル化から除外する方法を制御するフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="95514-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="95514-109">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="95514-109">The following flags can be set:</span></span>
    
<span data-ttu-id="95514-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="95514-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="95514-111">メッセージの添付ファイルの一部である  _lpPropList_ パラメーターのプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="95514-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="95514-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="95514-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="95514-113">_ulElemID_ パラメーターで指定された添付ファイルのプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="95514-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="95514-114">_lpvData_ パラメーターが NULL ではない場合、指すデータは **、PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) プロパティで示されるファイル内の添付ファイルのカプセル化に書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="95514-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="95514-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="95514-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="95514-116">_ulElemID_ パラメーターで指定されたメッセージまたは添付ファイルのプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="95514-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="95514-117">このフラグが設定されている場合  _、lpvData の値は_ [IStream ポインターである必要](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) があります。</span><span class="sxs-lookup"><span data-stu-id="95514-117">If this flag is set, the value in  _lpvData_ must be an [IStream](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream) pointer.</span></span> 
    
<span data-ttu-id="95514-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="95514-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="95514-119">lpPropList パラメーターで指定されていないすべての  _プロパティをエンコード_ します。</span><span class="sxs-lookup"><span data-stu-id="95514-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="95514-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="95514-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="95514-121">lpPropList で指定されたプロパティ  _をエンコードします_。</span><span class="sxs-lookup"><span data-stu-id="95514-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="95514-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="95514-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="95514-123">メッセージ自体の一部である  _lpPropList_ で指定されたプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="95514-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="95514-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="95514-124">_ulElemID_</span></span>
  
> <span data-ttu-id="95514-125">[in]添付ファイル **のPR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティで、親メッセージ内の添付ファイルを一意に識別する番号が含まれる。</span><span class="sxs-lookup"><span data-stu-id="95514-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="95514-126">_ulElemID パラメーター_ は、添付ファイルに対して特別な処理が要求される場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="95514-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="95514-127">_ulElemID_ パラメーターは _、ulFlags_ パラメーターで TNEF_PROP_CONTAINEDまたはTNEF_PROP_CONTAINED_TNEFフラグが設定されていない限り、0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="95514-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="95514-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="95514-128">_lpvData_</span></span>
  
> <span data-ttu-id="95514-129">[in]  _ulElemID_ で指定された添付ファイルのデータを置き換えるのに使用される添付ファイル データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="95514-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="95514-130">_lpvData パラメーター_ は _、ulFlags_ でTNEF_PROP_CONTAINEDまたはTNEF_PROP_CONTAINED_TNEF場合をTNEF_PROP_CONTAINED_TNEF NULL である必要があります。</span><span class="sxs-lookup"><span data-stu-id="95514-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="95514-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="95514-131">_lpPropList_</span></span>
  
> <span data-ttu-id="95514-132">[in]カプセル化に含める、またはカプセル化から除外するプロパティの一覧へのポインター。</span><span class="sxs-lookup"><span data-stu-id="95514-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95514-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="95514-133">Return value</span></span>

<span data-ttu-id="95514-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="95514-134">S_OK</span></span> 
  
> <span data-ttu-id="95514-135">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="95514-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95514-136">注釈</span><span class="sxs-lookup"><span data-stu-id="95514-136">Remarks</span></span>

<span data-ttu-id="95514-137">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは **、ITnef::AddProps** メソッドを呼び出して、メッセージまたは添付ファイルの Transport-Neutral カプセル化形式 (TNEF) 処理に含まれるプロパティまたは除外されるプロパティを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="95514-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="95514-138">プロバイダーまたはゲートウェイは、連続した呼び出しを使用して、追加およびエンコードまたはエンコードから除外するプロパティの一覧を指定できます。</span><span class="sxs-lookup"><span data-stu-id="95514-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="95514-139">プロバイダーとゲートウェイは **、AddProps** を使用して、特別な処理添付ファイルに関する情報を提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="95514-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="95514-140">**AddProps** は [、OpenTnefStream または OpenTnefStreamEx](opentnefstream.md) 関数の TNEF_ENCODE フラグで開いた TNEF オブジェクト [でのみサポート](opentnefstreamex.md) されます。</span><span class="sxs-lookup"><span data-stu-id="95514-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="95514-141">[ITnef::Finish](itnef-finish.md)メソッドが呼び出されるまで **、AddProps** の実際の TNEF エンコードは発生しない点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="95514-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="95514-142">この機能は **、AddProps** に渡されるポインターは、Finish の呼び出しが行われた後まで有効なまま **である必要があります** 。</span><span class="sxs-lookup"><span data-stu-id="95514-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="95514-143">その時点で **、AddProps** 呼び出しで渡されたオブジェクトとデータはすべて解放または解放できます。</span><span class="sxs-lookup"><span data-stu-id="95514-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="95514-144">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="95514-144">MFCMAPI reference</span></span>

<span data-ttu-id="95514-145">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="95514-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="95514-146">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="95514-146">**File**</span></span>|<span data-ttu-id="95514-147">**関数**</span><span class="sxs-lookup"><span data-stu-id="95514-147">**Function**</span></span>|<span data-ttu-id="95514-148">**コメント**</span><span class="sxs-lookup"><span data-stu-id="95514-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="95514-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="95514-149">File.cpp</span></span>  <br/> |<span data-ttu-id="95514-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="95514-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="95514-151">MFCMAPI は **、ITnef::AddProps** メソッドを使用して、メッセージから TNEF ストリームにプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="95514-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="95514-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="95514-152">See also</span></span>



[<span data-ttu-id="95514-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="95514-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="95514-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="95514-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="95514-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="95514-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="95514-156">PidTagAttachTransportName 標準プロパティ</span><span class="sxs-lookup"><span data-stu-id="95514-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="95514-157">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="95514-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


<span data-ttu-id="95514-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="95514-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

