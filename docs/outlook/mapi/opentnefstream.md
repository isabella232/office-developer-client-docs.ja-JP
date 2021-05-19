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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 524b52026010b9a06d5822b48b7c04bbf90a113e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423959"
---
# <a name="opentnefstream"></a><span data-ttu-id="ec348-103">OpenTnefStream</span><span class="sxs-lookup"><span data-stu-id="ec348-103">OpenTnefStream</span></span>

<span data-ttu-id="ec348-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec348-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec348-105">MAPI トランスポート ニュートラル カプセル化形式 (TNEF) セッションを開始するためにトランスポート プロバイダーによって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ec348-105">Called by a transport provider to initiate a MAPI Transport Neutral Encapsulation Format (TNEF) session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ec348-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="ec348-106">Header file:</span></span>  <br/> |<span data-ttu-id="ec348-107">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="ec348-107">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="ec348-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="ec348-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ec348-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ec348-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ec348-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="ec348-110">Called by:</span></span>  <br/> |<span data-ttu-id="ec348-111">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="ec348-111">Transport providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="ec348-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ec348-112">Parameters</span></span>

<span data-ttu-id="ec348-113">_lpvSupport_</span><span class="sxs-lookup"><span data-stu-id="ec348-113">_lpvSupport_</span></span>
  
> <span data-ttu-id="ec348-114">[in]サポート オブジェクトを渡す、または NULL で渡します。</span><span class="sxs-lookup"><span data-stu-id="ec348-114">[in] Passes a support object, or passes in NULL.</span></span> 
    
<span data-ttu-id="ec348-115">_lpStream_</span><span class="sxs-lookup"><span data-stu-id="ec348-115">_lpStream_</span></span>
  
> <span data-ttu-id="ec348-116">[in]TNEF ストリーム メッセージの送信元または宛先を提供する記憶域ストリーム オブジェクト OLE **IStream** インターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec348-116">[in] Pointer to a storage stream object OLE **IStream** interface providing a source or destination for a TNEF stream message.</span></span> 
    
<span data-ttu-id="ec348-117">_lpszStreamName_</span><span class="sxs-lookup"><span data-stu-id="ec348-117">_lpszStreamName_</span></span>
  
> <span data-ttu-id="ec348-118">[in]TNEF オブジェクトが使用するデータ ストリームの名前へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec348-118">[in] Pointer to the name of the data stream that the TNEF object uses.</span></span> <span data-ttu-id="ec348-119">呼び出し元が **OpenTnefStream** への呼び出しで TNEF_ENCODE フラグ ( _ulFlags_ パラメーター) を設定している場合 _、lpszName_ パラメーターは、ファイルの命名に有効と見なされる文字で構成される null 以外の文字列への null 以外のポインターを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec348-119">If the caller has set the TNEF_ENCODE flag ( _ulFlags_ parameter) in its call to **OpenTnefStream**, the  _lpszName_ parameter must specify a non-null pointer to a non-null string consisting of any characters considered valid for naming a file.</span></span> <span data-ttu-id="ec348-120">MAPI では、ファイル システムで使用が許可されている場合でも、"[","]"、または ":"という文字を含む文字列名は許可しません。</span><span class="sxs-lookup"><span data-stu-id="ec348-120">MAPI does not allow string names including the characters "[", "]", or ":", even if the file system permits their use.</span></span> <span data-ttu-id="ec348-121">_lpszName_ に渡される文字列のサイズは、パス名を含む文字列の最大長である MAX_PATH の値を超えないようにしてください。</span><span class="sxs-lookup"><span data-stu-id="ec348-121">The size of the string passed for  _lpszName_ must not exceed the value of MAX_PATH, the maximum length of a string that contains a path name.</span></span> 
    
<span data-ttu-id="ec348-122">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ec348-122">_ulFlags_</span></span>
  
> <span data-ttu-id="ec348-123">[in]関数のモードを示すために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="ec348-123">[in] Bitmask of flags used to indicate the mode of the function.</span></span> <span data-ttu-id="ec348-124">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="ec348-124">The following flags can be set:</span></span>
    
<span data-ttu-id="ec348-125">TNEF_BEST_DATA</span><span class="sxs-lookup"><span data-stu-id="ec348-125">TNEF_BEST_DATA</span></span> 
  
> <span data-ttu-id="ec348-126">考えられるすべてのプロパティは、ダウンレベルの属性にマップされますが、ダウンレベル属性への変換によってデータが失われる可能性がある場合は、カプセル化でもプロパティがエンコードされます。</span><span class="sxs-lookup"><span data-stu-id="ec348-126">All possible properties are mapped into their down-level attributes, but when there is a possible data loss due to the conversion to a down-level attribute, the property is also encoded in the encapsulations.</span></span> <span data-ttu-id="ec348-127">これにより、TNEF ストリーム内の情報が重複する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec348-127">Note that this will cause the duplication of information in the TNEF stream.</span></span> <span data-ttu-id="ec348-128">TNEF_BEST_DATAモードが指定されていない場合は、既定値を指定します。</span><span class="sxs-lookup"><span data-stu-id="ec348-128">TNEF_BEST_DATA is the default if no other modes are specified.</span></span> 
    
<span data-ttu-id="ec348-129">TNEF_COMPATIBILITY</span><span class="sxs-lookup"><span data-stu-id="ec348-129">TNEF_COMPATIBILITY</span></span> 
  
> <span data-ttu-id="ec348-130">古いクライアント アプリケーションとの下位互換性を提供します。</span><span class="sxs-lookup"><span data-stu-id="ec348-130">Provides backward compatibility with the older client applications.</span></span> <span data-ttu-id="ec348-131">このフラグでエンコードされた TNEF ストリームは、可能なすべてのプロパティを対応するダウンレベル属性にマップします。</span><span class="sxs-lookup"><span data-stu-id="ec348-131">TNEF streams encoded with this flag will map all possible properties into their corresponding down-level attribute.</span></span> <span data-ttu-id="ec348-132">また、このモードでは、ダウンレベル のクライアントに必要な一部のプロパティの既定値も発生します。</span><span class="sxs-lookup"><span data-stu-id="ec348-132">This mode also causes the defaulting of some properties that are required by down-level clients.</span></span> 
    
  > [!CAUTION]
  > <span data-ttu-id="ec348-133">このフラグは廃止され、使用できません。</span><span class="sxs-lookup"><span data-stu-id="ec348-133">This flag is obsolete and should not be used.</span></span> 
  
<span data-ttu-id="ec348-134">TNEF_DECODE</span><span class="sxs-lookup"><span data-stu-id="ec348-134">TNEF_DECODE</span></span> 
  
> <span data-ttu-id="ec348-135">指定されたストリームの TNEF オブジェクトは、読み取り専用アクセスで開きます。</span><span class="sxs-lookup"><span data-stu-id="ec348-135">The TNEF object on the indicated stream is opened with read-only access.</span></span> <span data-ttu-id="ec348-136">トランスポート プロバイダーは、関数が後続のデコードのためにオブジェクトを初期化する場合は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec348-136">The transport provider must set this flag if it wants the function to initialize the object for subsequent decoding.</span></span>
    
<span data-ttu-id="ec348-137">TNEF_ENCODE</span><span class="sxs-lookup"><span data-stu-id="ec348-137">TNEF_ENCODE</span></span> 
  
> <span data-ttu-id="ec348-138">指定されたストリームの TNEF オブジェクトは、読み取り/書き込みアクセス許可のために開きます。</span><span class="sxs-lookup"><span data-stu-id="ec348-138">The TNEF object on the indicated stream is opened for read/write permission.</span></span> <span data-ttu-id="ec348-139">トランスポート プロバイダーは、関数が後続のエンコード用にオブジェクトを初期化する場合は、このフラグを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec348-139">The transport provider must set this flag if it wants the function to initialize the object for subsequent encoding.</span></span>
    
<span data-ttu-id="ec348-140">TNEF_PURE</span><span class="sxs-lookup"><span data-stu-id="ec348-140">TNEF_PURE</span></span> 
  
> <span data-ttu-id="ec348-141">すべてのプロパティを MAPI カプセル化ブロックにエンコードします。</span><span class="sxs-lookup"><span data-stu-id="ec348-141">Encodes all properties into the MAPI encapsulation blocks.</span></span> <span data-ttu-id="ec348-142">したがって、"純粋な" TNEF ファイルは、多くの場合、attMAPIProps、attAttachment、attRenddata、および attRecipTable で構成されます。</span><span class="sxs-lookup"><span data-stu-id="ec348-142">Therefore, a "pure" TNEF file will consist of, at most, attMAPIProps, attAttachment, attRenddata, and attRecipTable.</span></span> <span data-ttu-id="ec348-143">このモードは、下位互換性が必要ない場合に使用する場合に最適です。</span><span class="sxs-lookup"><span data-stu-id="ec348-143">This mode is ideal for use when no backward compatibility is required.</span></span>
    
<span data-ttu-id="ec348-144">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="ec348-144">_lpMessage_</span></span>
  
> <span data-ttu-id="ec348-145">[in]添付ファイルを含むデコードされたメッセージの宛先として、または添付ファイルを含むエンコードされたメッセージのソースとしてメッセージ オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec348-145">[in] Pointer to a message object as a destination for a decoded message with attachments or a source for an encoded message with attachments.</span></span> <span data-ttu-id="ec348-146">宛先メッセージのプロパティは、エンコードされたメッセージのプロパティによって上書きされる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="ec348-146">Any properties of a destination message might be overwritten by the properties of an encoded message.</span></span>
    
<span data-ttu-id="ec348-147">_wKey_</span><span class="sxs-lookup"><span data-stu-id="ec348-147">_wKey_</span></span>
  
> <span data-ttu-id="ec348-148">[in]TNEF オブジェクトがメッセージ テキストに挿入されたテキスト タグに添付ファイルを一致するために使用する検索キー。</span><span class="sxs-lookup"><span data-stu-id="ec348-148">[in] A search key that the TNEF object uses to match attachments to the text tags inserted in the message text.</span></span> <span data-ttu-id="ec348-149">この値は、メッセージ間で比較的一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec348-149">This value should be relatively unique across messages.</span></span>
    
<span data-ttu-id="ec348-150">_lppTNEF_</span><span class="sxs-lookup"><span data-stu-id="ec348-150">_lppTNEF_</span></span>
  
> <span data-ttu-id="ec348-151">[out]新しい TNEF オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ec348-151">[out] Pointer to the new TNEF object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec348-152">戻り値</span><span class="sxs-lookup"><span data-stu-id="ec348-152">Return value</span></span>

<span data-ttu-id="ec348-153">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec348-153">S_OK</span></span> 
  
> <span data-ttu-id="ec348-154">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="ec348-154">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ec348-155">注釈</span><span class="sxs-lookup"><span data-stu-id="ec348-155">Remarks</span></span>

<span data-ttu-id="ec348-156">**OpenTnefStream** 関数によって作成された TNEF オブジェクトは、後で OLE メソッド **IUnknown::AddRef** を呼び出して、サポート オブジェクト、ストリーム オブジェクト、およびメッセージ オブジェクトの参照を追加します。</span><span class="sxs-lookup"><span data-stu-id="ec348-156">A TNEF object created by the **OpenTnefStream** function later calls the OLE method **IUnknown::AddRef** to add references for the support object, the stream object, and the message object.</span></span> <span data-ttu-id="ec348-157">トランスポート プロバイダーは、TNEF オブジェクトの OLE メソッド **IUnknown::Release** を 1 回呼び出して、3 つすべてのオブジェクトの参照を解放できます。</span><span class="sxs-lookup"><span data-stu-id="ec348-157">The transport provider can release the references for all three objects with a single call to the OLE method **IUnknown::Release** on the TNEF object.</span></span> 
  
<span data-ttu-id="ec348-158">**OpenTnefStream** は、プロバイダーが MAPI メッセージ **IMessage** インターフェイスを TNEF ストリーム メッセージにエンコードする場合に使用する TNEF オブジェクト **ITnef** インターフェイスを割り当て、初期化します。</span><span class="sxs-lookup"><span data-stu-id="ec348-158">**OpenTnefStream** allocates and initializes a TNEF object **ITnef** interface for the provider to use in encoding a MAPI message **IMessage** interface into a TNEF stream message.</span></span> <span data-ttu-id="ec348-159">または、この関数は、プロバイダーが [ITnef::ExtractProps](itnef-extractprops.md) への後続の呼び出しで使用するオブジェクトをセットアップして、TNEF ストリーム メッセージを MAPI メッセージにデコードできます。</span><span class="sxs-lookup"><span data-stu-id="ec348-159">Alternatively, the function can set up the object for the provider to use in subsequent calls to [ITnef::ExtractProps](itnef-extractprops.md) to decode a TNEF stream message into a MAPI message.</span></span> <span data-ttu-id="ec348-160">TNEF オブジェクトを解放し、セッションを閉じるには、トランスポート プロバイダーはオブジェクトの継承 **された IUnknown::Release** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ec348-160">To free the TNEF object and close the session, the transport provider must call the inherited **IUnknown::Release** method on the object.</span></span> 
  
<span data-ttu-id="ec348-161">この関数は TNEF アクセスの元のエントリ ポイントであり [、OpenTnefStreamEx](opentnefstreamex.md) に置き換えられたが、TNEF を既に使用しているユーザーの互換性のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ec348-161">This function is the original entry point for TNEF access and has been replaced by [OpenTnefStreamEx](opentnefstreamex.md) but is still used for compatibility for those already using TNEF.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ec348-162">関連項目</span><span class="sxs-lookup"><span data-stu-id="ec348-162">See also</span></span>

- [<span data-ttu-id="ec348-163">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec348-163">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
- [<span data-ttu-id="ec348-164">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="ec348-164">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)

