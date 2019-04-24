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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348924"
---
# <a name="opentnefstream"></a><span data-ttu-id="f7897-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="f7897-103">OpenTnefStream</span></span>

<span data-ttu-id="f7897-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7897-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7897-105">MAPI トランスポートのニュートラルカプセル化形式 (TNEF) セッションを開始するために、トランスポートプロバイダーによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f7897-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f7897-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f7897-106">Header file:</span></span>  <br/> |<span data-ttu-id="f7897-107">Tnef</span><span class="sxs-lookup"><span data-stu-id="f7897-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="f7897-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="f7897-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f7897-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f7897-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f7897-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="f7897-110">Called by:</span></span>  <br/> |<span data-ttu-id="f7897-111">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="f7897-111">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f7897-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7897-112">Parameters</span></span>

<span data-ttu-id="f7897-113">_lpvsupport_</span><span class="sxs-lookup"><span data-stu-id="f7897-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="f7897-114">順番サポートオブジェクトを渡すか、または NULL を渡します。</span><span class="sxs-lookup"><span data-stu-id="f7897-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="f7897-115">_lpstream_</span><span class="sxs-lookup"><span data-stu-id="f7897-115">_lpStream_</span></span>
  
> <span data-ttu-id="f7897-116">順番TNEF ストリームメッセージのソースまたは送信先を提供する、ストレージストリームオブジェクトの OLE **IStream**インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f7897-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="f7897-117">_lpszstreamname_</span><span class="sxs-lookup"><span data-stu-id="f7897-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="f7897-118">順番TNEF オブジェクトが使用するデータストリームの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f7897-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="f7897-119">呼び出し元が**OpenTnefStream**の呼び出しで TNEF_ENCODE フラグ ( _ulflags_パラメーター) を設定している場合、 _lpszname_パラメーターには、null 以外の文字列へのポインターを指定する必要があります。 null 以外の文字には、ファイルの名前付けに対して有効になっていると見なされます。</span><span class="sxs-lookup"><span data-stu-id="f7897-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="f7897-120">MAPI では、ファイルシステムで使用が許可されている場合でも、文字 "["、"]"、または ":" を含む文字列名を使用できません。</span><span class="sxs-lookup"><span data-stu-id="f7897-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="f7897-121">_lpszname_に渡される文字列のサイズは、パス名を含む文字列の最大長である MAX_PATH の値を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="f7897-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="f7897-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f7897-122">_ulFlags_</span></span>
  
> <span data-ttu-id="f7897-123">順番関数のモードを示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="f7897-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="f7897-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7897-124">The following flags can be set:</span></span>
    
<span data-ttu-id="f7897-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="f7897-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="f7897-126">可能なすべてのプロパティは、下位レベルの属性にマップされますが、下位レベルの属性への変換によってデータが失われる可能性がある場合、プロパティも encapsulations でエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="f7897-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="f7897-127">これにより、TNEF ストリーム内の情報が重複することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="f7897-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="f7897-128">他のモードが指定されていない場合の既定値は TNEF_BEST_DATA です。</span><span class="sxs-lookup"><span data-stu-id="f7897-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="f7897-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="f7897-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="f7897-130">以前のクライアントアプリケーションとの下位互換性を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7897-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="f7897-131">このフラグでエンコードされた TNEF ストリームは、使用可能なすべてのプロパティを対応する下位レベルの属性にマップします。</span><span class="sxs-lookup"><span data-stu-id="f7897-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="f7897-132">このモードでは、ダウンレベルクライアントに必要な一部のプロパティの既定のプロパティも発生します。</span><span class="sxs-lookup"><span data-stu-id="f7897-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="f7897-133">このフラグは現在使われていないため、使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f7897-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="f7897-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="f7897-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="f7897-135">指定した stream の TNEF オブジェクトは、読み取り専用アクセスで開かれます。</span><span class="sxs-lookup"><span data-stu-id="f7897-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="f7897-136">トランスポートプロバイダーは、このフラグを設定して、関数がオブジェクトを初期化して以降のデコードを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7897-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="f7897-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="f7897-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="f7897-138">指定した stream の TNEF オブジェクトは、読み取り/書き込みアクセス許可で開かれます。</span><span class="sxs-lookup"><span data-stu-id="f7897-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="f7897-139">このフラグを設定する必要がある場合は、トランスポートプロバイダーは、オブジェクトを初期化して後続のエンコーディングを行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7897-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="f7897-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="f7897-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="f7897-141">すべてのプロパティを MAPI カプセル化ブロックにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="f7897-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="f7897-142">そのため、"純粋な" TNEF ファイルは、最大で、attMAPIProps、/添付ファイル、attRenddata、および attRecipTable で構成されます。</span><span class="sxs-lookup"><span data-stu-id="f7897-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="f7897-143">このモードは、下位互換性が必要ない場合に使用するのに適しています。</span><span class="sxs-lookup"><span data-stu-id="f7897-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="f7897-144">_lpmessage_</span><span class="sxs-lookup"><span data-stu-id="f7897-144">_lpMessage_</span></span>
  
> <span data-ttu-id="f7897-145">順番添付ファイル付きのデコードされたメッセージの送信先としてのメッセージオブジェクトへのポインター、および添付ファイル付きのエンコードされたメッセージのソース。</span><span class="sxs-lookup"><span data-stu-id="f7897-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="f7897-146">転送先メッセージのすべてのプロパティは、エンコードされたメッセージのプロパティによって上書きされる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f7897-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="f7897-147">_wkey_</span><span class="sxs-lookup"><span data-stu-id="f7897-147">_wKey_</span></span>
  
> <span data-ttu-id="f7897-148">順番TNEF オブジェクトは、メッセージテキストに挿入されたテキストタグに添付ファイルを照合するために使用する検索キーです。</span><span class="sxs-lookup"><span data-stu-id="f7897-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="f7897-149">この値は、メッセージ間で比較的一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7897-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="f7897-150">_lpptnef_</span><span class="sxs-lookup"><span data-stu-id="f7897-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="f7897-151">読み上げ新しい TNEF オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f7897-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f7897-152">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7897-152">Return value</span></span>

<span data-ttu-id="f7897-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7897-153">S_OK</span></span> 
  
> <span data-ttu-id="f7897-154">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f7897-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f7897-155">解説</span><span class="sxs-lookup"><span data-stu-id="f7897-155">Remarks</span></span>

<span data-ttu-id="f7897-156">後で**OpenTnefStream**関数によって作成された TNEF オブジェクトは、OLE メソッド**IUnknown:: AddRef**を呼び出して、support オブジェクト、stream オブジェクト、および message オブジェクトへの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="f7897-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="f7897-157">トランスポートプロバイダーは、TNEF オブジェクトの OLE メソッド**IUnknown:: release**に対して1回の呼び出しで、3つのすべてのオブジェクトの参照を解放できます。</span><span class="sxs-lookup"><span data-stu-id="f7897-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="f7897-158">**OpenTnefStream**は、MAPI メッセージ**IMessage**インターフェイスを tnef ストリームメッセージにエンコードする際に使用するために、プロバイダー用の tnef オブジェクト**ITnef**インターフェイスを割り当てて初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7897-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="f7897-159">または、この関数は、プロバイダーが[ITnef:: ExtractProps](itnef-extractprops.md)への以降の呼び出しで使用するオブジェクトを設定して、TNEF ストリームメッセージを MAPI メッセージにデコードすることもできます。</span><span class="sxs-lookup"><span data-stu-id="f7897-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="f7897-160">TNEF オブジェクトを解放してセッションを閉じるには、トランスポートプロバイダーは、オブジェクトに対して継承された**IUnknown:: Release**メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7897-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="f7897-161">この関数は、tnef アクセスの元のエントリポイントであり、 [OpenTnefStreamEx](opentnefstreamex.md)に置き換えられていますが、既に tnef を使用している場合の互換性のためにも使用されています。</span><span class="sxs-lookup"><span data-stu-id="f7897-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f7897-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="f7897-162">See also</span></span>

- [<span data-ttu-id="f7897-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f7897-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="f7897-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="f7897-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

