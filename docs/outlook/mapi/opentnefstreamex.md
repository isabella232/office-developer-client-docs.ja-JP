---
title: OpenTnefStreamEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStreamEx
api_type:
- COM
ms.assetid: eb84c408-2d8b-453b-92f4-5fd8851b84ca
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 178ab67875d8fb442500dd412dbafe4403deee16
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348574"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="74519-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="74519-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="74519-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="74519-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="74519-105">トランスポート、ゲートウェイ、およびメッセージストアで使用するために、tnef データストリームにメッセージオブジェクトをエンコードまたはデコードするために使用できるトランスポート中立カプセル化形式 (TNEF) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="74519-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="74519-106">これは、TNEF アクセスのエントリポイントです。</span><span class="sxs-lookup"><span data-stu-id="74519-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="74519-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="74519-107">Header file:</span></span>  <br/> |<span data-ttu-id="74519-108">Tnef</span><span class="sxs-lookup"><span data-stu-id="74519-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="74519-109">実装元:</span><span class="sxs-lookup"><span data-stu-id="74519-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="74519-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="74519-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="74519-111">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="74519-111">Called by:</span></span>  <br/> |<span data-ttu-id="74519-112">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="74519-112">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStreamEx(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName,
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKeyVal,
  LPADDRESSBOOK lpAddressBook,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="74519-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="74519-113">Parameters</span></span>

<span data-ttu-id="74519-114">_lpvsupport_</span><span class="sxs-lookup"><span data-stu-id="74519-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="74519-115">順番サポートオブジェクトを渡すか、または NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="74519-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="74519-116">null の場合、 _lpAddressBook_パラメーターは null 以外である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74519-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="74519-117">_lpstream_</span><span class="sxs-lookup"><span data-stu-id="74519-117">_lpStream_</span></span>
  
> <span data-ttu-id="74519-118">順番TNEF ストリームメッセージのソースまたは送信先を提供する、OLE **IStream**インターフェイスなどのストレージストリームオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="74519-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="74519-119">_lpszstreamname_</span><span class="sxs-lookup"><span data-stu-id="74519-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="74519-120">順番TNEF オブジェクトが使用するデータストリームの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="74519-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="74519-121">呼び出し元が**OpenTnefStream**の呼び出しで TNEF_ENCODE フラグ ( _ulflags_パラメーター) を設定している場合、 _lpszname_パラメーターには、null 以外の文字列へのポインターを指定する必要があります。 null 以外の文字には、ファイルの名前付けに対して有効になっていると見なされます。</span><span class="sxs-lookup"><span data-stu-id="74519-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="74519-122">MAPI では、ファイルシステムで使用が許可されている場合でも、文字 "["、"]"、または ":" を含む文字列名を使用できません。</span><span class="sxs-lookup"><span data-stu-id="74519-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="74519-123">_lpszname_パラメーターに渡される文字列のサイズは、パス名を含む文字列の最大長である MAX_PATH の値を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="74519-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="74519-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="74519-124">_ulFlags_</span></span>
  
> <span data-ttu-id="74519-125">順番関数のモードを示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="74519-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="74519-126">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="74519-126">The following flags can be set:</span></span>
    
<span data-ttu-id="74519-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="74519-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="74519-128">可能なすべてのプロパティは、下位レベルの属性にマップされますが、下位レベルの属性への変換によってデータが失われる可能性がある場合、プロパティも encapsulations でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="74519-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="74519-129">これにより、TNEF ストリーム内の情報が重複することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="74519-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="74519-130">他のモードが指定されていない場合の既定値は TNEF_BEST_DATA です。</span><span class="sxs-lookup"><span data-stu-id="74519-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="74519-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="74519-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="74519-132">以前のクライアントアプリケーションとの下位互換性を提供します。</span><span class="sxs-lookup"><span data-stu-id="74519-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="74519-133">このフラグでエンコードされた TNEF ストリームは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップします。</span><span class="sxs-lookup"><span data-stu-id="74519-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="74519-134">このモードでは、ダウンレベルクライアントに必要な一部のプロパティの既定のプロパティも発生します。</span><span class="sxs-lookup"><span data-stu-id="74519-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="74519-135">このフラグは現在使われていないため、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="74519-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="74519-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="74519-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="74519-137">指定した stream の TNEF オブジェクトは、読み取り専用アクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="74519-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="74519-138">関数がその後のデコードのためにオブジェクトを初期化する場合は、トランスポートプロバイダーがこのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74519-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="74519-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="74519-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="74519-140">指定した stream の TNEF オブジェクトは、読み取り/書き込みアクセス許可で開かれます。</span><span class="sxs-lookup"><span data-stu-id="74519-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="74519-141">この関数が後でエンコードするためにオブジェクトを初期化する場合は、トランスポートプロバイダーがこのフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="74519-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="74519-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="74519-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="74519-143">すべてのプロパティを MAPI カプセル化ブロックにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="74519-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="74519-144">そのため、"pure" TNEF ファイルは、ほとんどの場合、属性 attMAPIProps、attRenddata、および attRecipTable で構成されます。</span><span class="sxs-lookup"><span data-stu-id="74519-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="74519-145">このモードは、下位互換性が必要ない場合に使用するのに適しています。</span><span class="sxs-lookup"><span data-stu-id="74519-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="74519-146">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="74519-146">_lpMessage_</span></span>
  
> <span data-ttu-id="74519-147">順番添付ファイル付きのデコードされたメッセージの送信先としてのメッセージオブジェクトへのポインター、および添付ファイル付きのエンコードされたメッセージのソース。</span><span class="sxs-lookup"><span data-stu-id="74519-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="74519-148">転送先メッセージのすべてのプロパティは、エンコードされたメッセージのプロパティによって上書きできます。</span><span class="sxs-lookup"><span data-stu-id="74519-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="74519-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="74519-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="74519-150">順番TNEF オブジェクトは、メッセージテキストに挿入されたテキストタグに添付ファイルを照合するために使用する検索キーです。</span><span class="sxs-lookup"><span data-stu-id="74519-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="74519-151">この値は、メッセージ間で比較的一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="74519-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="74519-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="74519-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="74519-153">順番エントリ id のアドレス指定情報を取得するために使用されるアドレス帳オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="74519-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="74519-154">_lpptnef_</span><span class="sxs-lookup"><span data-stu-id="74519-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="74519-155">読み上げ新しい TNEF オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="74519-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="74519-156">戻り値</span><span class="sxs-lookup"><span data-stu-id="74519-156">Return value</span></span>

<span data-ttu-id="74519-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="74519-157">S_OK</span></span> 
  
> <span data-ttu-id="74519-158">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="74519-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="74519-159">解説</span><span class="sxs-lookup"><span data-stu-id="74519-159">Remarks</span></span>

<span data-ttu-id="74519-160">**OpenTnefStreamEx**関数は、 [OpenTnefStream](opentnefstream.md)に推奨される代替の方法であり、TNEF アクセスの元のエントリポイントです。</span><span class="sxs-lookup"><span data-stu-id="74519-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="74519-161">後で**OpenTnefStreamEx**関数によって作成された TNEF オブジェクトは、OLE メソッド**IUnknown:: AddRef**を呼び出して、support オブジェクト、stream オブジェクト、および message オブジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="74519-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="74519-162">トランスポートプロバイダーは、TNEF オブジェクトの OLE メソッド**IUnknown:: release**に対して1回の呼び出しで、3つのすべてのオブジェクトの参照を解放できます。</span><span class="sxs-lookup"><span data-stu-id="74519-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="74519-163">**OpenTnefStreamEx**は、プロバイダーが tnef オブジェクトを割り当てて初期化し、それを使用して、tnef ストリームメッセージへの MAPI メッセージのエンコードに使用します。</span><span class="sxs-lookup"><span data-stu-id="74519-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="74519-164">別の方法として、この関数はプロバイダーのオブジェクトを設定して、 [ITnef:: ExtractProps](itnef-extractprops.md)への以降の呼び出しで、TNEF ストリームメッセージを MAPI メッセージにデコードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="74519-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="74519-165">TNEF オブジェクトを解放してセッションを閉じるには、トランスポートプロバイダーは、オブジェクトに対して継承された**IUnknown:: Release**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="74519-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="74519-166">_wKeyVal_パラメーターの基本値を0にすることはできません。また、 **OpenTnefStreamEx**のすべての呼び出しで同じにすることはできません。</span><span class="sxs-lookup"><span data-stu-id="74519-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="74519-167">代わりに、ランタイムライブラリの乱数ジェネレーターから、システム時間に基づいてランダムな番号を使用します。</span><span class="sxs-lookup"><span data-stu-id="74519-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="74519-168">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="74519-168">MFCMAPI reference</span></span>

<span data-ttu-id="74519-169">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="74519-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="74519-170">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="74519-170">**File**</span></span>|<span data-ttu-id="74519-171">**関数**</span><span class="sxs-lookup"><span data-stu-id="74519-171">**Function**</span></span>|<span data-ttu-id="74519-172">**コメント**</span><span class="sxs-lookup"><span data-stu-id="74519-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="74519-173">ファイル .cpp</span><span class="sxs-lookup"><span data-stu-id="74519-173">File.cpp</span></span>  <br/> |<span data-ttu-id="74519-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="74519-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="74519-175">mfcmapi は、 **OpenTnefStreamEx**メソッドを使用して TNEF ファイルのストリームを開くため、プロパティが抽出される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="74519-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="74519-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="74519-176">See also</span></span>

- [<span data-ttu-id="74519-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="74519-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="74519-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="74519-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- <span data-ttu-id="74519-179">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="74519-179">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

