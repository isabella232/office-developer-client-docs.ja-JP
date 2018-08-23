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
ms.openlocfilehash: b651a913855e99e2f26dfd99fb725cc332201932
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565187"
---
# <a name="opentnefstreamex"></a><span data-ttu-id="ff38c-103">OpenTnefStreamEx</span><span class="sxs-lookup"><span data-stu-id="ff38c-103">OpenTnefStreamEx</span></span>

<span data-ttu-id="ff38c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff38c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff38c-105">エンコードまたは TNEF データ ストリームを使用するメッセージ オブジェクトをデコードするトランスポートまたはゲートウェイとメッセージ ストアで使用できるトランスポート ニュートラル カプセル化形式 (TNEF) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ff38c-105">Creates a Transport-Neutral Encapsulation Format (TNEF) object that can be used to encode or decode a message object into a TNEF data stream for use by transports or gateways and message stores.</span></span> <span data-ttu-id="ff38c-106">これは、TNEF のアクセスのエントリ ポイントです。</span><span class="sxs-lookup"><span data-stu-id="ff38c-106">This is the entry point for TNEF access.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ff38c-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ff38c-107">Header file:</span></span>  <br/> |<span data-ttu-id="ff38c-108">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="ff38c-108">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="ff38c-109">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-109">Implemented by:</span></span>  <br/> |<span data-ttu-id="ff38c-110">MAPI</span><span class="sxs-lookup"><span data-stu-id="ff38c-110">MAPI</span></span>  <br/> |
|<span data-ttu-id="ff38c-111">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-111">Called by:</span></span>  <br/> |<span data-ttu-id="ff38c-112">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ff38c-112">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ff38c-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ff38c-113">Parameters</span></span>

<span data-ttu-id="ff38c-114">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="ff38c-114">_lpvSupport_</span></span>
  
> <span data-ttu-id="ff38c-115">[in]サポート オブジェクト、または NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="ff38c-115">[in] Passes a support object, or passes in NULL.</span></span> <span data-ttu-id="ff38c-116">NULL の場合、 _lpAddressBook_パラメーターは、null のはずです。</span><span class="sxs-lookup"><span data-stu-id="ff38c-116">If NULL, the  _lpAddressBook_ parameter should be non-null.</span></span> 
    
<span data-ttu-id="ff38c-117">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="ff38c-117">_lpStream_</span></span>
  
> <span data-ttu-id="ff38c-118">[in]ソースまたは TNEF ストリーム メッセージの出力先を提供する、OLE の**IStream**インターフェイスなど、ストレージのストリーム オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff38c-118">[in] Pointer to a storage stream object, such as an OLE **IStream** interface, providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="ff38c-119">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="ff38c-119">_lpszStreamName_</span></span>
  
> <span data-ttu-id="ff38c-120">[in]TNEF オブジェクトを使用するデータ ストリームの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff38c-120">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="ff38c-121">呼び出し元が**OpenTnefStream**の呼び出しで、TNEF_ENCODE フラグ ( _ulFlags_パラメーター) を設定した場合_lpszName_パラメーター ファイルの名前を付けるために有効とみなされる任意の文字で構成される null 以外の文字列に null 以外のポインターを指定してください。</span><span class="sxs-lookup"><span data-stu-id="ff38c-121">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="ff38c-122">MAPI は、文字を含む文字列の名前を許可しない"["、"]"、または」:」ファイル ・ システムの使用を許可する場合でも。</span><span class="sxs-lookup"><span data-stu-id="ff38c-122">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="ff38c-123">_LpszName_パラメーターに渡される文字列のサイズは、パス名を含む文字列の最大長、MAX_PATH の値を超えていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff38c-123">The size of the string passed for the  _lpszName_ parameter must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="ff38c-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ff38c-124">_ulFlags_</span></span>
  
> <span data-ttu-id="ff38c-125">[in]関数のモードを指定するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="ff38c-125">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="ff38c-126">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-126">The following flags can be set:</span></span>
    
<span data-ttu-id="ff38c-127">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="ff38c-127">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="ff38c-128">使用可能なすべてのプロパティは、その下位レベルの属性にマップされますが、下位レベルの属性への変換により、データ損失の可能性がある場合は、プロパティはエンコードされますが、カプセル化の。</span><span class="sxs-lookup"><span data-stu-id="ff38c-128">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="ff38c-129">TNEF ストリーム内の情報の重複は、注意してください。</span><span class="sxs-lookup"><span data-stu-id="ff38c-129">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="ff38c-130">TNEF_BEST_DATA は、他のモードが指定されていない場合のデフォルトです。</span><span class="sxs-lookup"><span data-stu-id="ff38c-130">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="ff38c-131">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="ff38c-131">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="ff38c-132">古いバージョンのクライアント アプリケーションとの下位互換性を提供します。</span><span class="sxs-lookup"><span data-stu-id="ff38c-132">Provides backward compatibility with older client applications.</span></span> <span data-ttu-id="ff38c-133">TNEF ストリームがこのフラグを使用してエンコードされたは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップされます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-133">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="ff38c-134">このモードは、下位レベルのクライアントに必要ないくつかのプロパティの既定値にも発生します。</span><span class="sxs-lookup"><span data-stu-id="ff38c-134">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="ff38c-135">このフラグは廃止されて、使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff38c-135">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="ff38c-136">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="ff38c-136">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="ff38c-137">TNEF オブジェクトは指定されたストリームは、読み取り専用アクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-137">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="ff38c-138">トランスポート プロバイダーは、機能は、それ以降のデコード用のオブジェクトを初期化する場合、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff38c-138">The transport provider must set this flag if the function is to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="ff38c-139">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="ff38c-139">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="ff38c-140">読み取り/書き込みアクセス許可を指定されたストリームで TNEF オブジェクトが開かれます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-140">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="ff38c-141">トランスポート プロバイダーは、機能は、それ以降をエンコードするためのオブジェクトを初期化する場合、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff38c-141">The transport provider must set this flag if the function is to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="ff38c-142">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="ff38c-142">TNEF_PURE</span></span> 
  
> <span data-ttu-id="ff38c-143">MAPI のカプセル化のブロックには、すべてのプロパティをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="ff38c-143">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="ff38c-144">したがって、TNEF ファイルを「純粋な」では、多くて属性の attMAPIProps attAttachment attRenddata、および attRecipTable。</span><span class="sxs-lookup"><span data-stu-id="ff38c-144">Therefore, a "pure" TNEF file will consist of, at most, the attributes attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="ff38c-145">このモードは、下位互換性を維持する必要がないときに使用に最適です。</span><span class="sxs-lookup"><span data-stu-id="ff38c-145">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="ff38c-146">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ff38c-146">_lpMessage_</span></span>
  
> <span data-ttu-id="ff38c-147">[in]デコードされた添付ファイル付きメッセージの宛先や添付ファイルのエンコードされたメッセージのソースとして、メッセージのオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff38c-147">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="ff38c-148">エンコードされたメッセージのプロパティでは、複製先のメッセージのプロパティを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-148">Any properties of a destination message can be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="ff38c-149">_wKeyVal_</span><span class="sxs-lookup"><span data-stu-id="ff38c-149">_wKeyVal_</span></span>
  
> <span data-ttu-id="ff38c-150">[in]TNEF オブジェクトを使用して添付ファイルをメッセージのテキストに挿入されたテキストのタグに一致する検索キーです。</span><span class="sxs-lookup"><span data-stu-id="ff38c-150">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="ff38c-151">この値は、メッセージ間で比較的一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff38c-151">This value should be relatively unique across messages.</span></span> 
    
<span data-ttu-id="ff38c-152">_lpAddressBook_</span><span class="sxs-lookup"><span data-stu-id="ff38c-152">_lpAddressBook_</span></span>
  
> <span data-ttu-id="ff38c-153">[in]アドレスのエントリの識別子の情報を取得するために使用するアドレス帳のオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff38c-153">[in] Pointer to an address book object used to get addressing information for entry identifiers.</span></span> 
    
<span data-ttu-id="ff38c-154">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="ff38c-154">_lppTNEF_</span></span>
  
> <span data-ttu-id="ff38c-155">[out]新しい TNEF オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ff38c-155">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ff38c-156">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ff38c-156">Return value</span></span>

<span data-ttu-id="ff38c-157">S_OK</span><span class="sxs-lookup"><span data-stu-id="ff38c-157">S_OK</span></span> 
  
> <span data-ttu-id="ff38c-158">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ff38c-158">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ff38c-159">����</span><span class="sxs-lookup"><span data-stu-id="ff38c-159">Remarks</span></span>

<span data-ttu-id="ff38c-160">**OpenTnefStreamEx** [OpenTnefStream](opentnefstream.md)TNEF のアクセスのための元のエントリ ポイントの交換をお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ff38c-160">The **OpenTnefStreamEx** function is the recommended replacement for [OpenTnefStream](opentnefstream.md), the original entry point for TNEF access.</span></span> 
  
<span data-ttu-id="ff38c-161">TNEF オブジェクトが後で、 **OpenTnefStreamEx**関数によって作成された OLE メソッド サポート オブジェクト、ストリーム オブジェクト、およびメッセージのオブジェクトへの参照を追加するのには**IUnknown::AddRef**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ff38c-161">A TNEF object created by the **OpenTnefStreamEx** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="ff38c-162">トランスポート プロバイダーは、OLE**が**オブジェクトのメソッド、TNEF を 1 回の呼び出しですべての 3 つのオブジェクトの参照を解放できます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-162">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="ff38c-163">**OpenTnefStreamEx** TNEF ストリーム メッセージを MAPI メッセージのエンコードに使用するプロバイダーの TNEF のオブジェクトを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ff38c-163">**OpenTnefStreamEx** allocates and initializes a TNEF object for the provider to use in encoding a MAPI message into a TNEF stream message.</span></span> <span data-ttu-id="ff38c-164">代わりに、この関数は、MAPI メッセージに TNEF ストリーム メッセージをデコードするのには[ITnef::ExtractProps](itnef-extractprops.md)以降の呼び出しに使用するプロバイダーのオブジェクトを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ff38c-164">Alternatively, this function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="ff38c-165">TNEF オブジェクトを解放し、セッションを閉じる、トランスポート プロバイダーはオブジェクトの継承**が**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff38c-165">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="ff38c-166">_WKeyVal_パラメーターの基本値は 0 にできませんする必要があり、 **OpenTnefStreamEx**を呼び出すたびに同じにしないで。</span><span class="sxs-lookup"><span data-stu-id="ff38c-166">The base value for the  _wKeyVal_ parameter must not be zero and should not be the same for every call to **OpenTnefStreamEx**.</span></span> <span data-ttu-id="ff38c-167">代わりに、実行時ライブラリの乱数生成器からのシステム時間に基づく乱数を使用します。</span><span class="sxs-lookup"><span data-stu-id="ff38c-167">Instead, use random numbers based on the system time from the run-time library's random number generator.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ff38c-168">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ff38c-168">MFCMAPI reference</span></span>

<span data-ttu-id="ff38c-169">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ff38c-169">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ff38c-170">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ff38c-170">**File**</span></span>|<span data-ttu-id="ff38c-171">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ff38c-171">**Function**</span></span>|<span data-ttu-id="ff38c-172">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ff38c-172">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ff38c-173">File.cpp</span><span class="sxs-lookup"><span data-stu-id="ff38c-173">File.cpp</span></span>  <br/> |<span data-ttu-id="ff38c-174">LoadFromTNEF</span><span class="sxs-lookup"><span data-stu-id="ff38c-174">LoadFromTNEF</span></span>  <br/> |<span data-ttu-id="ff38c-175">MFCMAPI では、 **OpenTnefStreamEx**メソッドを使用して、プロパティを抽出することがありますので、TNEF ファイル ストリームをオープンします。</span><span class="sxs-lookup"><span data-stu-id="ff38c-175">MFCMAPI uses the **OpenTnefStreamEx** method to open a stream on the TNEF file so properties may be extracted.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ff38c-176">関連項目</span><span class="sxs-lookup"><span data-stu-id="ff38c-176">See also</span></span>

- [<span data-ttu-id="ff38c-177">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ff38c-177">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="ff38c-178">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="ff38c-178">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
- <span data-ttu-id="ff38c-179">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ff38c-179">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

