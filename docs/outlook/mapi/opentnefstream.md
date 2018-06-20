---
title: OpenTnefStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenTnefStream
api_type:
- COM
ms.assetid: 912d7799-53ce-42a7-9fbd-f9a6a3a56047
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 866d3be5e1c7a4375db84d1f15802e01f8d10f23
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801696"
---
# <a name="opentnefstream"></a><span data-ttu-id="a0cc8-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="a0cc8-103">OpenTnefStream</span></span>

<span data-ttu-id="a0cc8-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a0cc8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a0cc8-105">MAPI トランスポート ニュートラル カプセル化形式 (TNEF) セッションを開始するトランスポート プロバイダーによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0cc8-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="a0cc8-106">Header file:</span></span>  <br/> |<span data-ttu-id="a0cc8-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="a0cc8-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="a0cc8-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a0cc8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a0cc8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a0cc8-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-110">Called by:</span></span>  <br/> |<span data-ttu-id="a0cc8-111">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="a0cc8-111">Transport providers</span></span>  <br/> |
   
```cpp
HRESULT OpenTnefStream(
  LPVOID lpvSupport,
  LPSTREAM lpStream,
  LPSTR lpszStreamName, 
  ULONG ulFlags,
  LPMESSAGE lpMessage,
  WORD wKey,
  LPITNEF FAR * lppTNEF
);
```

## <a name="parameters"></a><span data-ttu-id="a0cc8-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a0cc8-112">Parameters</span></span>

<span data-ttu-id="a0cc8-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="a0cc8-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="a0cc8-114">[in]サポート オブジェクト、または NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="a0cc8-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="a0cc8-115">_lpStream_</span></span>
  
> <span data-ttu-id="a0cc8-116">[in]ソースまたは TNEF ストリーム メッセージの出力先を提供するストレージ ストリーム オブジェクト OLE の**IStream**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="a0cc8-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="a0cc8-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="a0cc8-118">[in]TNEF オブジェクトを使用するデータ ストリームの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="a0cc8-119">呼び出し元が**OpenTnefStream**の呼び出しで、TNEF_ENCODE フラグ ( _ulFlags_パラメーター) を設定した場合_lpszName_パラメーター ファイルの名前を付けるために有効とみなされる任意の文字で構成される null 以外の文字列に null 以外のポインターを指定してください。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="a0cc8-120">MAPI は、文字を含む文字列の名前を許可しない"["、"]"、または」:」ファイル ・ システムの使用を許可する場合でも。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="a0cc8-121">_LpszName_に渡される文字列のサイズは、パス名を含む文字列の最大長、MAX_PATH の値を超えていない必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="a0cc8-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a0cc8-122">_ulFlags_</span></span>
  
> <span data-ttu-id="a0cc8-123">[in]関数のモードを指定するためのフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="a0cc8-124">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-124">The following flags can be set:</span></span>
    
<span data-ttu-id="a0cc8-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="a0cc8-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="a0cc8-126">使用可能なすべてのプロパティは、その下位レベルの属性にマップされますが、下位レベルの属性への変換により、データ損失の可能性がある場合は、プロパティはエンコードされますが、カプセル化の。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="a0cc8-127">TNEF ストリーム内の情報の重複は、注意してください。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="a0cc8-128">TNEF_BEST_DATA は、他のモードが指定されていない場合のデフォルトです。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="a0cc8-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="a0cc8-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="a0cc8-130">アプリケーションの以前のクライアントとの下位互換性を提供します。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="a0cc8-131">TNEF ストリームがこのフラグを使用してエンコードされたは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップされます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="a0cc8-132">このモードは、下位レベルのクライアントに必要ないくつかのプロパティの既定値にも発生します。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="a0cc8-133">このフラグは廃止されて、使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="a0cc8-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="a0cc8-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="a0cc8-135">TNEF オブジェクトは指定されたストリームは、読み取り専用アクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="a0cc8-136">トランスポート プロバイダーは、それ以降のデコード用のオブジェクトを初期化する関数の場合、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="a0cc8-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="a0cc8-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="a0cc8-138">読み取り/書き込みアクセス許可を指定されたストリームで TNEF オブジェクトが開かれます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="a0cc8-139">トランスポート プロバイダーは、それ以降をエンコードするためのオブジェクトを初期化する関数の場合、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="a0cc8-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="a0cc8-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="a0cc8-141">MAPI のカプセル化のブロックには、すべてのプロパティをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="a0cc8-142">したがって、TNEF ファイルを「純粋な」では、でほとんどの場合 attMAPIProps attAttachment attRenddata、および attRecipTable。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="a0cc8-143">このモードは、下位互換性を維持する必要がないときに使用に最適です。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="a0cc8-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="a0cc8-144">_lpMessage_</span></span>
  
> <span data-ttu-id="a0cc8-145">[in]デコードされた添付ファイル付きメッセージの宛先や添付ファイルのエンコードされたメッセージのソースとして、メッセージのオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="a0cc8-146">複製先のメッセージのプロパティは、エンコードされたメッセージのプロパティによって上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="a0cc8-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="a0cc8-147">_wKey_</span></span>
  
> <span data-ttu-id="a0cc8-148">[in]TNEF オブジェクトを使用して添付ファイルをメッセージのテキストに挿入されたテキストのタグに一致する検索キーです。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="a0cc8-149">この値は、メッセージ間で比較的一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="a0cc8-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="a0cc8-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="a0cc8-151">[out]新しい TNEF オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a0cc8-152">�߂�l</span><span class="sxs-lookup"><span data-stu-id="a0cc8-152">Return value</span></span>

<span data-ttu-id="a0cc8-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="a0cc8-153">S_OK</span></span> 
  
> <span data-ttu-id="a0cc8-154">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="a0cc8-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a0cc8-155">����</span><span class="sxs-lookup"><span data-stu-id="a0cc8-155">Remarks</span></span>

<span data-ttu-id="a0cc8-156">TNEF オブジェクトが後で、 **OpenTnefStream**関数によって作成された OLE メソッド サポート オブジェクト、ストリーム オブジェクト、およびメッセージのオブジェクトへの参照を追加するのには**IUnknown::AddRef**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="a0cc8-157">トランスポート プロバイダーは、OLE**が**オブジェクトのメソッド、TNEF を 1 回の呼び出しですべての 3 つのオブジェクトの参照を解放できます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="a0cc8-158">**OpenTnefStream** TNEF ストリームのメッセージにメッセージの MAPI **IMessage**インターフェイスをエンコードに使用するプロバイダーの TNEF オブジェクトの**ITnef**インターフェイスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="a0cc8-159">代わりに、関数は、MAPI メッセージに TNEF ストリーム メッセージをデコードするのには[ITnef::ExtractProps](itnef-extractprops.md)以降の呼び出しに使用するプロバイダーのオブジェクトを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="a0cc8-160">TNEF オブジェクトを解放し、セッションを閉じる、トランスポート プロバイダーはオブジェクトの継承**が**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="a0cc8-161">この関数は、TNEF のアクセスのための元のエントリ ポイントし[OpenTnefStreamEx](opentnefstreamex.md)によって置き換えられましたが、既に TNEF を使用するために互換性のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a0cc8-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a0cc8-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="a0cc8-162">See also</span></span>

- [<span data-ttu-id="a0cc8-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="a0cc8-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="a0cc8-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="a0cc8-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

