---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406522"
---
# <a name="openimsgonistg"></a><span data-ttu-id="e192f-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="e192f-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="e192f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e192f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e192f-105">メッセージ セッション内で使用する、既存の OLE **IStorage** オブジェクトの上に新しい [IMessage](imessageimapiprop.md)オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="e192f-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e192f-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e192f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e192f-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="e192f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="e192f-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="e192f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e192f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e192f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e192f-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e192f-110">Called by:</span></span>  <br/> |<span data-ttu-id="e192f-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="e192f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a><span data-ttu-id="e192f-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e192f-112">Parameters</span></span>

<span data-ttu-id="e192f-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="e192f-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="e192f-114">[in]新しい **IMessage**-on- **IStorage** オブジェクトを作成するメッセージ セッション オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="e192f-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e192f-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e192f-116">[in]メモリの割 [り当てに使用する MAPIAllocateBuffer](mapiallocatebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="e192f-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e192f-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e192f-118">[in]追加のメモリ [の割り当てに使用する MAPIAllocateMore](mapiallocatemore.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="e192f-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e192f-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e192f-120">[in]メモリを解放するために使用する [MAPIFreeBuffer](mapifreebuffer.md) 関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="e192f-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="e192f-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="e192f-122">[in]OLE **IMalloc** インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="e192f-123">**IMessage インターフェイスは\*\*\*\*、IStorage** や IStream などのインターフェイスを操作するときに、この割り当て方法を使用 **する必要があります**。</span><span class="sxs-lookup"><span data-stu-id="e192f-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="e192f-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="e192f-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="e192f-125">[in]サービス プロバイダーが [IMAPISupport : IUnknown](imapisupportiunknown.md) インターフェイスのメソッドを呼び出す場合に使用できる MAPI サポート オブジェクトへのオプションのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="e192f-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="e192f-126">_lpStg_</span></span>
  
> <span data-ttu-id="e192f-127">[in, out]開いている、読 **み取り専用** または読み取り/書き込みアクセス許可を持つ OLE IStorage オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="e192f-128">**IMessage は書** き込み専用アクセスをサポートしないので **、OpenIMsgOnIStg** は書き込み専用モードで開いたストレージ オブジェクトを受け入れません。</span><span class="sxs-lookup"><span data-stu-id="e192f-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="e192f-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="e192f-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="e192f-130">[in]**IMessage**-on- **IStorage** オブジェクトの最後のリリースに従って MAPI が呼び出す [MSGCALLRELEASE](msgcallrelease.md)プロトタイプに基づくコールバック関数へのオプションのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="e192f-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="e192f-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="e192f-132">[in] **IMessage**-on- **IStorage** オブジェクトを使用して MAPI によって保存され **、MSGCALLRELEASE** ベースのコールバック関数に渡された呼び出し元データ。</span><span class="sxs-lookup"><span data-stu-id="e192f-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="e192f-133">データは、リリースされる **IMessage** オブジェクトと、その上に作成された **IStorage** オブジェクトに関するコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="e192f-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="e192f-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e192f-134">_ulFlags_</span></span>
  
> <span data-ttu-id="e192f-135">[in]クライアント アプリケーションまたはサービス プロバイダーが **IMessage::SaveChanges** メソッドを呼び出す場合に OLE **IStorage::Commit** メソッドを呼び出すかどうかを制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="e192f-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="e192f-136">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e192f-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="e192f-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="e192f-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="e192f-138">OLE メソッド **IStorage::Commit** は、クライアントまたはプロバイダーが SaveChanges を呼び出す場合は呼 [び出されません](imapiprop-savechanges.md)。</span><span class="sxs-lookup"><span data-stu-id="e192f-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="e192f-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e192f-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="e192f-140">Unicode .msg ファイルの作成を有効にする。</span><span class="sxs-lookup"><span data-stu-id="e192f-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="e192f-141">結果の [IMessage](imessageimapiprop.md) ファイルは、そのSTORE_UNICODE_OKにPR_STORE_SUPPORT_MASK [Unicode](pidtagstoresupportmask-canonical-property.md) プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e192f-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="e192f-142">このMAPI_UNICODEフラグは、2003 以上のOutlookでのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e192f-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="e192f-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="e192f-143">_lppMsg_</span></span>
  
> <span data-ttu-id="e192f-144">[out]開いた **IMessage** オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="e192f-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e192f-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="e192f-145">Return value</span></span>

<span data-ttu-id="e192f-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="e192f-146">S_OK</span></span> 
  
> <span data-ttu-id="e192f-147">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="e192f-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e192f-148">注釈</span><span class="sxs-lookup"><span data-stu-id="e192f-148">Remarks</span></span>

<span data-ttu-id="e192f-149">プロパティ属性にアクセスできるのは、プロパティ オブジェクト、つまり [IMAPIProp : IUnknown](imapipropiunknown.md) インターフェイスを実装するオブジェクトのみです。</span><span class="sxs-lookup"><span data-stu-id="e192f-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="e192f-150">OLE 構造化ストレージ オブジェクトで MAPI プロパティを使用するために **、OpenIMsgOnIStg** は OLE **IStorage** オブジェクトの上に [IMessage : IMAPIProp](imessageimapiprop.md)オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="e192f-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="e192f-151">このようなオブジェクトのプロパティ属性は [、SetAttribIMsgOnIStg](setattribimsgonistg.md) を使用して設定または変更し [、GetAttribIMsgOnIStg](getattribimsgonistg.md)を使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="e192f-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e192f-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="e192f-152">Notes to callers</span></span>

<span data-ttu-id="e192f-153">**OpenIMsgOnIStg** が呼び出される前に [、OpenIMsgSession](openimsgsession.md)でメッセージ セッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="e192f-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="e192f-154">有効な  _lpMsgSess_ パラメーターを指定すると、新しいメッセージがメッセージ セッション内に作成され、セッションが閉じられます。</span><span class="sxs-lookup"><span data-stu-id="e192f-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="e192f-155">_lpMsgSess が_ NULL の場合、メッセージはメッセージ セッションとは別に作成されます。</span><span class="sxs-lookup"><span data-stu-id="e192f-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="e192f-156">メッセージを作成したクライアント アプリケーションまたはサービス プロバイダーが、メッセージを解放しない場合、添付ファイルと開いているテーブルのすべてが解放されない場合、メモリがリークされ、アプリケーションが終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e192f-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="e192f-157">MAPI では、ほとんどのメモリ割り当ておよび割り当て解除に _lpAllocateBuffer_ _、lpAllocateMore、lpFreeBuffer_ が指す関数を使用して、特に [IMAPIProp::GetProps](imapiprop-getprops.md)や [IMAPITable::QueryRows](imapitable-queryrows.md)などのオブジェクト インターフェイスを呼び出す際にクライアント アプリケーションで使用するメモリを割り当てる。 </span><span class="sxs-lookup"><span data-stu-id="e192f-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="e192f-158">**OpenIMsgOnIStg** 関数が有効な _lpMapiSup_ パラメーターで呼び出される場合 _、lpAllocateBuffer_ _、lpAllocateMore、_ および _lpFreeBuffer_ ポインターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="e192f-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="e192f-159">基になる OLE オブジェクトを扱うので、MAPI では OLE メモリ割り当てを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e192f-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="e192f-160">OLE 構造化ストレージ オブジェクトと OLE メモリ割り当ての詳細については  _、「OLE プログラマリファレンス」を参照してください_。</span><span class="sxs-lookup"><span data-stu-id="e192f-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="e192f-161">_lpMapiSup_ に対して有効な値が指定されている場合 **、IMessage** は [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出して [IMAPIProp::CopyTo](imapiprop-copyto.md)メソッドと [IMessage::D eleteAttach](imessage-deleteattach.md)メソッドの進行状況ユーザー インターフェイスを指定することで、MAPI_DIALOG フラグと ATTACH_DIALOG フラグをサポートします。</span><span class="sxs-lookup"><span data-stu-id="e192f-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="e192f-162">[また、IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドは[、IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)メソッドを呼び出し、結果のアドレス帳オブジェクトを呼び出すことによって、短期エントリ識別子を長期エントリ識別子に変換します。</span><span class="sxs-lookup"><span data-stu-id="e192f-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="e192f-163">_lpMapiSup_ に NULL が渡された場合 **、IMessage** は MAPI_DIALOG および ATTACH_DIALOG を無視し、変換なしで短期エントリ識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="e192f-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="e192f-164">**lpStg パラメーターが** 指す _IStorage_ オブジェクトは、STGM_READモードSTGM_READWRITEがあります。</span><span class="sxs-lookup"><span data-stu-id="e192f-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="e192f-165">このモードSTGM_READWRITE場合は、STGM_TRANSACTEDモードも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e192f-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="e192f-166">_lpfMsgCallRelease_ パラメーターが指すコールバック関数はオプションです。指定されている場合は [、MSGCALLRELEASE 関数プロトタイプに基づく](msgcallrelease.md)必要があります。</span><span class="sxs-lookup"><span data-stu-id="e192f-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="e192f-167">**IMessage** インターフェイスは **、IMessage**-on- **IStorage** オブジェクトの参照カウントが Release メソッドの最後の呼び出しによって 0 に設定されている場合に呼び **出** します。</span><span class="sxs-lookup"><span data-stu-id="e192f-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="e192f-168">コールバック関数は、基になる **IStorage** インターフェイスを解放するために一般的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="e192f-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="e192f-169">**IMessage** は、コールバックを行った後 _、lpStg_ パラメーターが指す **IStorage** オブジェクトにアクセスしようとは行ないます。</span><span class="sxs-lookup"><span data-stu-id="e192f-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="e192f-170">一部のクライアントまたはプロバイダーは [、SaveChanges](imapiprop-savechanges.md)メソッドの呼び出し時に IMessage 自体が書き込むデータを超えて **、IStorage** オブジェクトに追加のデータを書き込む場合があります。 </span><span class="sxs-lookup"><span data-stu-id="e192f-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="e192f-171">クライアントまたはプロバイダーは、IMSG_NO_ISTG_COMMIT フラグを使用して **、SaveChanges** 呼び出しの処理中に **IMessage** が OLE **IStorage::Commit** メソッドを呼び出すのを防止できます。この場合、クライアントまたはプロバイダーは、追加のデータの書き込み時に **IStorage** オブジェクトをコミットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e192f-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="e192f-172">これを支援するために **、IMessage** 実装では **、IStorage** オブジェクトで作成するサブストルジの名前は、文字列 "__"、つまり 2 つのアンダースコアで始まります。</span><span class="sxs-lookup"><span data-stu-id="e192f-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="e192f-173">クライアントまたはプロバイダーは、サブストラージュ名をこの名前空間から外して名前の競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="e192f-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="e192f-174">MAPI は、添付ファイル、ストリーム、埋め込みメッセージなど、メッセージのサブオブジェクトに対して実行される複数の開いている操作の動作を定義しません。</span><span class="sxs-lookup"><span data-stu-id="e192f-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="e192f-175">MAPI は現在、既に開いているサブオブジェクトをもう一度開くことを許可していますが、MAPI は、既存の開いているオブジェクトの参照カウントを増やし [、IMessage::OpenAttach](imessage-openattach.md) メソッドまたは [IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出したクライアントまたはプロバイダーに返して、開いている操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="e192f-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="e192f-176">つまり、サブオブジェクトの最初の開いている操作に対して要求されたアクセスは、操作によって要求されたアクセスに関係なく、後続のすべての開いている操作に対して提供されるアクセスです。</span><span class="sxs-lookup"><span data-stu-id="e192f-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="e192f-177">メッセージを添付ファイルに配置する正しい手順は [、IMAPIProp::OpenProperty](imapiprop-openproperty.md) メソッドを呼び出し、インターフェイス識別子を使用して IID_IMessage。</span><span class="sxs-lookup"><span data-stu-id="e192f-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="e192f-178">**OpenProperty は** 現在、OLE **IStorage** インターフェイスで直接使用できるメッセージ添付ファイルの作成 (つまり、このインターフェイス識別子を使用IID_IStorageサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e192f-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="e192f-179">**IStorage** アクセスは、OLE IStream インターフェイスに変換したり、OLE **IStream** インターフェイスから変換したりすることなく、Microsoft Word ドキュメントを添付ファイルに簡単に挿入するためのサポートされています。</span><span class="sxs-lookup"><span data-stu-id="e192f-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="e192f-180">ただし **、OpenIMsgOnIStg** が添付ファイル データに **IStorage** ポインターを渡され、オブジェクトが間違った順序で解放された場合 **、IMessage** は予測可能に動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e192f-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e192f-181">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="e192f-181">MFCMAPI reference</span></span>

<span data-ttu-id="e192f-182">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e192f-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e192f-183">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="e192f-183">**File**</span></span>|<span data-ttu-id="e192f-184">**関数**</span><span class="sxs-lookup"><span data-stu-id="e192f-184">**Function**</span></span>|<span data-ttu-id="e192f-185">**コメント**</span><span class="sxs-lookup"><span data-stu-id="e192f-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e192f-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="e192f-186">File.cpp</span></span>  <br/> |<span data-ttu-id="e192f-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="e192f-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="e192f-188">MFCMAPI は **OpenIMsgOnIStg** メソッドを使用して、 の上に IMessage インターフェイスを開きます。ファイルが MAPI で操作される可能性がある MSG ファイル。</span><span class="sxs-lookup"><span data-stu-id="e192f-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e192f-189">関連項目</span><span class="sxs-lookup"><span data-stu-id="e192f-189">See also</span></span>

- <span data-ttu-id="e192f-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="e192f-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

