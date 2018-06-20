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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 2d37898b100398218d4f8762cdd3a16943d8f11a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801226"
---
# <a name="itnefaddprops"></a><span data-ttu-id="cef14-103">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="cef14-103">ITnef::AddProps</span></span>

  
  
<span data-ttu-id="cef14-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cef14-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cef14-105">メッセージまたは添付ファイルをカプセル化するプロパティを追加するのには、呼び出し元のサービス プロバイダーまたはゲートウェイを有効にします。</span><span class="sxs-lookup"><span data-stu-id="cef14-105">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span> 
  
```cpp
HRESULT AddProps(
  ULONG ulFlags,
  ULONG ulElemID,
  LPVOID lpvData,
  LPSPropTagArray lpPropList
);
```

## <a name="parameters"></a><span data-ttu-id="cef14-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="cef14-106">Parameters</span></span>

 <span data-ttu-id="cef14-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cef14-107">_ulFlags_</span></span>
  
> <span data-ttu-id="cef14-108">[in]プロパティに含まれているまたはカプセル化から除外する方法を制御するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="cef14-108">[in] A bitmask of flags that controls how properties are included in or excluded from encapsulation.</span></span> <span data-ttu-id="cef14-109">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="cef14-109">The following flags can be set:</span></span>
    
<span data-ttu-id="cef14-110">TNEF_PROP_ATTACHMENTS_ONLY</span><span class="sxs-lookup"><span data-stu-id="cef14-110">TNEF_PROP_ATTACHMENTS_ONLY</span></span> 
  
> <span data-ttu-id="cef14-111">_LpPropList_パラメーターで、メッセージの添付ファイルの一部であるプロパティだけをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="cef14-111">Encodes only the properties in the  _lpPropList_ parameter that are part of attachments in the message.</span></span> 
    
<span data-ttu-id="cef14-112">TNEF_PROP_CONTAINED</span><span class="sxs-lookup"><span data-stu-id="cef14-112">TNEF_PROP_CONTAINED</span></span> 
  
> <span data-ttu-id="cef14-113">_UlElemID_パラメーターで指定された添付ファイルのプロパティだけをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="cef14-113">Encodes only properties from the attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="cef14-114">_LpvData_パラメーターが NULL でない場合は、 **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) のプロパティで指定されたファイルの添付ファイルのカプセル化に示されるデータが書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="cef14-114">If the  _lpvData_ parameter is not NULL, the data pointed to is written into the attachment's encapsulation in the file indicated by the **PR_ATTACH_TRANSPORT_NAME** ([PidTagAttachTransportName](pidtagattachtransportname-canonical-property.md)) property.</span></span>
    
<span data-ttu-id="cef14-115">TNEF_PROP_CONTAINED_TNEF</span><span class="sxs-lookup"><span data-stu-id="cef14-115">TNEF_PROP_CONTAINED_TNEF</span></span> 
  
> <span data-ttu-id="cef14-116">メッセージまたは添付ファイルの_ulElemID_パラメーターで指定されたプロパティのみをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="cef14-116">Encodes only properties from the message or attachment specified by the  _ulElemID_ parameter.</span></span> <span data-ttu-id="cef14-117">このフラグが設定されている場合、 _lpvData_の値は、 [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx)ポインターをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cef14-117">If this flag is set, the value in  _lpvData_ must be an [IStream](http://msdn.microsoft.com/library/stg.istream%28Office.15%29.aspx) pointer.</span></span> 
    
<span data-ttu-id="cef14-118">TNEF_PROP_EXCLUDE</span><span class="sxs-lookup"><span data-stu-id="cef14-118">TNEF_PROP_EXCLUDE</span></span> 
  
> <span data-ttu-id="cef14-119">_LpPropList_パラメーターで指定されていないすべてのプロパティをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="cef14-119">Encodes all properties not specified in the  _lpPropList_ parameter.</span></span> 
    
<span data-ttu-id="cef14-120">TNEF_PROP_INCLUDE</span><span class="sxs-lookup"><span data-stu-id="cef14-120">TNEF_PROP_INCLUDE</span></span> 
  
> <span data-ttu-id="cef14-121">_LpPropList_で指定されたすべてのプロパティをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="cef14-121">Encodes all properties specified in  _lpPropList_.</span></span> 
    
<span data-ttu-id="cef14-122">TNEF_PROP_MESSAGE_ONLY</span><span class="sxs-lookup"><span data-stu-id="cef14-122">TNEF_PROP_MESSAGE_ONLY</span></span> 
  
> <span data-ttu-id="cef14-123">プロパティのみ_lpPropList_で指定されているメッセージ自体の一部をエンコードします。</span><span class="sxs-lookup"><span data-stu-id="cef14-123">Encodes only those properties specified in  _lpPropList_ that are part of the message itself.</span></span> 
    
 <span data-ttu-id="cef14-124">_ulElemID_</span><span class="sxs-lookup"><span data-stu-id="cef14-124">_ulElemID_</span></span>
  
> <span data-ttu-id="cef14-125">[in]添付ファイルの**PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) プロパティは、一意にその数値が含まれていますが、親メッセージの添付ファイルを識別します。</span><span class="sxs-lookup"><span data-stu-id="cef14-125">[in] An attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property, which contains a number that uniquely identifies the attachment in its parent message.</span></span> <span data-ttu-id="cef14-126">添付ファイルの特別な処理が要求されたときに、 _ulElemID_パラメーターが使用されます。</span><span class="sxs-lookup"><span data-stu-id="cef14-126">The  _ulElemID_ parameter is used when special handling is requested for an attachment.</span></span> <span data-ttu-id="cef14-127">_UlFlags_パラメーターで TNEF_PROP_CONTAINED または TNEF_PROP_CONTAINED_TNEF のフラグが設定されていない限り、 _ulElemID_パラメーターは 0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cef14-127">The  _ulElemID_ parameter should be 0 unless the TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="cef14-128">_lpvData_</span><span class="sxs-lookup"><span data-stu-id="cef14-128">_lpvData_</span></span>
  
> <span data-ttu-id="cef14-129">[in]_UlElemID_で指定された添付ファイルのデータを置き換えるための添付ファイル データへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cef14-129">[in] A pointer to attachment data used to replace the data of the attachment specified in  _ulElemID_.</span></span> <span data-ttu-id="cef14-130">_LpvData_パラメーターは、 _ulFlags_で TNEF_PROP_CONTAINED または TNEF_PROP_CONTAINED_TNEF が設定されていない限り、NULL にすることがあります。</span><span class="sxs-lookup"><span data-stu-id="cef14-130">The  _lpvData_ parameter should be NULL unless TNEF_PROP_CONTAINED or TNEF_PROP_CONTAINED_TNEF is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="cef14-131">_lpPropList_</span><span class="sxs-lookup"><span data-stu-id="cef14-131">_lpPropList_</span></span>
  
> <span data-ttu-id="cef14-132">[in]含めるか、カプセル化から除外するプロパティの一覧へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cef14-132">[in] A pointer to the list of properties to include in or exclude from encapsulation.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cef14-133">�߂�l</span><span class="sxs-lookup"><span data-stu-id="cef14-133">Return value</span></span>

<span data-ttu-id="cef14-134">S_OK</span><span class="sxs-lookup"><span data-stu-id="cef14-134">S_OK</span></span> 
  
> <span data-ttu-id="cef14-135">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="cef14-135">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cef14-136">����</span><span class="sxs-lookup"><span data-stu-id="cef14-136">Remarks</span></span>

<span data-ttu-id="cef14-137">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイは、リストのプロパティに含まれているか、トランスポート ニュートラル カプセル化形式 (TNEF) の処理、メッセージまたは添付ファイルから除外するに**ITnef::AddProps**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cef14-137">Transport providers, message store providers, and gateways call the **ITnef::AddProps** method to list properties to be included in or excluded from the Transport-Neutral Encapsulation Format (TNEF) processing of a message or an attachment.</span></span> <span data-ttu-id="cef14-138">連続呼び出しを使用すると、プロバイダーまたはゲートウェイを追加し、エンコード、またはエンコードの対象から除外するプロパティの一覧を指定できます。</span><span class="sxs-lookup"><span data-stu-id="cef14-138">By using successive calls, the provider or gateway can specify a list of properties to add and encode or to exclude from being encoded.</span></span> <span data-ttu-id="cef14-139">プロバイダーおよびゲートウェイ ・ モデルの特別な処理の添付ファイルに関する情報を指定する必要がありますを提供するのに**AddProps**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="cef14-139">Providers and gateways can also use **AddProps** to provide information about any special handling attachments should be given.</span></span> 
  
 <span data-ttu-id="cef14-140">**AddProps**は、 [OpenTnefStream](opentnefstream.md)または[OpenTnefStreamEx](opentnefstreamex.md)関数の場合、TNEF_ENCODE フラグを使用して開かれている TNEF オブジェクトでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="cef14-140">**AddProps** is supported only for TNEF objects that are opened with the TNEF_ENCODE flag for the [OpenTnefStream](opentnefstream.md) or [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
  
<span data-ttu-id="cef14-141">実際の TNEF エンコードが行われない**AddProps**の[ITnef::Finish](itnef-finish.md)メソッドが呼び出されるまでに注意してください。</span><span class="sxs-lookup"><span data-stu-id="cef14-141">Note that no actual TNEF encoding happens for **AddProps** until the [ITnef::Finish](itnef-finish.md) method is called.</span></span> <span data-ttu-id="cef14-142">この機能は、 **AddProps**に渡されたポインターに保つように有効期限**を終了**する呼び出しが行われた後を意味します。</span><span class="sxs-lookup"><span data-stu-id="cef14-142">This functionality means that pointers passed into **AddProps** must remain valid until after the call to **Finish** is made.</span></span> <span data-ttu-id="cef14-143">その時点で、すべてのオブジェクトと**AddProps**の呼び出しで渡されるデータは、リリースまたは解放されます。</span><span class="sxs-lookup"><span data-stu-id="cef14-143">At that point, all objects and data passed in with **AddProps** calls can be released or freed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cef14-144">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="cef14-144">MFCMAPI reference</span></span>

<span data-ttu-id="cef14-145">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="cef14-145">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cef14-146">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="cef14-146">**File**</span></span>|<span data-ttu-id="cef14-147">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="cef14-147">**Function**</span></span>|<span data-ttu-id="cef14-148">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="cef14-148">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cef14-149">File.cpp</span><span class="sxs-lookup"><span data-stu-id="cef14-149">File.cpp</span></span>  <br/> |<span data-ttu-id="cef14-150">SaveToTNEF</span><span class="sxs-lookup"><span data-stu-id="cef14-150">SaveToTNEF</span></span>  <br/> |<span data-ttu-id="cef14-151">MFCMAPI では、 **ITnef::AddProps**メソッドを使用して、TNEF ストリームにメッセージからプロパティをコピーします。</span><span class="sxs-lookup"><span data-stu-id="cef14-151">MFCMAPI uses the **ITnef::AddProps** method to copy properties from a message to a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cef14-152">関連項目</span><span class="sxs-lookup"><span data-stu-id="cef14-152">See also</span></span>



[<span data-ttu-id="cef14-153">ITnef::Finish</span><span class="sxs-lookup"><span data-stu-id="cef14-153">ITnef::Finish</span></span>](itnef-finish.md)
  
[<span data-ttu-id="cef14-154">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="cef14-154">OpenTnefStream</span></span>](opentnefstream.md)
  
[<span data-ttu-id="cef14-155">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="cef14-155">OpenTnefStreamEx</span></span>](opentnefstreamex.md)
  
[<span data-ttu-id="cef14-156">PidTagAttachTransportName の標準的なプロパティ</span><span class="sxs-lookup"><span data-stu-id="cef14-156">PidTagAttachTransportName Canonical Property</span></span>](pidtagattachtransportname-canonical-property.md)
  
[<span data-ttu-id="cef14-157">ITnef: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cef14-157">ITnef : IUnknown</span></span>](itnefiunknown.md)


<span data-ttu-id="cef14-158">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cef14-158">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

