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
# <a name="openimsgonistg"></a><span data-ttu-id="d3664-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="d3664-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="d3664-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d3664-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d3664-105">メッセージセッション内で使用するために、既存の OLE **IStorage**オブジェクトの上に新しい[IMessage](imessageimapiprop.md)オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="d3664-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3664-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="d3664-106">Header file:</span></span>  <br/> |<span data-ttu-id="d3664-107">Imessage</span><span class="sxs-lookup"><span data-stu-id="d3664-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="d3664-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="d3664-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d3664-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d3664-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d3664-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="d3664-110">Called by:</span></span>  <br/> |<span data-ttu-id="d3664-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="d3664-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="d3664-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d3664-112">Parameters</span></span>

<span data-ttu-id="d3664-113">_lpmsgsess_</span><span class="sxs-lookup"><span data-stu-id="d3664-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="d3664-114">順番新しい**IMessage**オブジェクトが作成されるメッセージセッションオブジェクトへのポインターを\*\*\*\* 指定します。</span><span class="sxs-lookup"><span data-stu-id="d3664-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="d3664-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="d3664-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="d3664-116">順番メモリの割り当てに使用される[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3664-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="d3664-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="d3664-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="d3664-118">順番追加のメモリを割り当てるために使用される[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3664-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="d3664-119">_lpfreebuffer_</span><span class="sxs-lookup"><span data-stu-id="d3664-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="d3664-120">順番メモリを解放するために使用される[MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3664-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="d3664-121">_lpmalloc_</span><span class="sxs-lookup"><span data-stu-id="d3664-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="d3664-122">順番OLE **imalloc**インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3664-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="d3664-123">**IMessage**インターフェイスは、 **IStorage**や**IStream**などのインターフェイスを使用するときに、この割り当て方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="d3664-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="d3664-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="d3664-125">順番(オプション) サービスプロバイダーが[imapisupport: IUnknown](imapisupportiunknown.md)インターフェイスのメソッドを呼び出すために使用できる MAPI サポートオブジェクトを指すポインターです。</span><span class="sxs-lookup"><span data-stu-id="d3664-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="d3664-126">_lpstg_</span><span class="sxs-lookup"><span data-stu-id="d3664-126">_lpStg_</span></span>
  
> <span data-ttu-id="d3664-127">[入力]読み取り専用または読み取り/書き込みのアクセス許可を持つ、開いている OLE **IStorage**オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3664-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="d3664-128">**IMessage**は書き込み専用アクセスをサポートしていないため、 **OpenIMsgOnIStg**は書き込み専用モードで開かれたストレージオブジェクトを受け入れません。</span><span class="sxs-lookup"><span data-stu-id="d3664-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="d3664-129">_lpfmsgcallrelease_</span><span class="sxs-lookup"><span data-stu-id="d3664-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="d3664-130">順番オプションのコールバック関数へのポインター。 [](msgcallrelease.md) MAPI は、 **IMessage**オブジェクト上の最後のリリースを呼び出した後に呼び出されます。 \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="d3664-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="d3664-131">_ulcallerdata_</span><span class="sxs-lookup"><span data-stu-id="d3664-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="d3664-132">順番**IMessage**オブジェクトを使用して MAPI によって保存\*\*\*\* され、 **msgcallrelease**ベースのコールバック関数に渡される発信者データ。</span><span class="sxs-lookup"><span data-stu-id="d3664-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="d3664-133">このデータは、解放される**IMessage**オブジェクトと、それが作成された最初の**IStorage**オブジェクトに関するコンテキストを提供します。</span><span class="sxs-lookup"><span data-stu-id="d3664-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="d3664-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3664-134">_ulFlags_</span></span>
  
> <span data-ttu-id="d3664-135">順番クライアントアプリケーションまたはサービスプロバイダーが**IMessage:: SaveChanges**メソッドを呼び出すときに、OLE **IStorage:: Commit**メソッドが呼び出されるかどうかを制御するために使用されるフラグのビットマスク。</span><span class="sxs-lookup"><span data-stu-id="d3664-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="d3664-136">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="d3664-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="d3664-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="d3664-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="d3664-138">OLE メソッド**IStorage:: Commit**は、クライアントまたはプロバイダーが[SaveChanges](imapiprop-savechanges.md)を呼び出したときには呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="d3664-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="d3664-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d3664-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="d3664-140">Unicode .msg ファイルの作成を有効にします。</span><span class="sxs-lookup"><span data-stu-id="d3664-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="d3664-141">生成された[IMessage](imessageimapiprop.md)ファイルは、 [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)に STORE_UNICODE_OK を表示し、UNICODE プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="d3664-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="d3664-142">MAPI_UNICODE フラグは、Outlook 2003 以降でのみ、この関数でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3664-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="d3664-143">_lppmsg_</span><span class="sxs-lookup"><span data-stu-id="d3664-143">_lppMsg_</span></span>
  
> <span data-ttu-id="d3664-144">読み上げ開いている**IMessage**オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="d3664-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d3664-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="d3664-145">Return value</span></span>

<span data-ttu-id="d3664-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3664-146">S_OK</span></span> 
  
> <span data-ttu-id="d3664-147">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="d3664-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3664-148">注釈</span><span class="sxs-lookup"><span data-stu-id="d3664-148">Remarks</span></span>

<span data-ttu-id="d3664-149">property 属性は、プロパティオブジェクト (つまり、 [imapiprop: IUnknown](imapipropiunknown.md)インターフェイスを実装するオブジェクト) にのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="d3664-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="d3664-150">ole 構造化ストレージオブジェクトで MAPI プロパティを使用できるようにするために、 **OpenIMsgOnIStg**は、ole **IStorage**オブジェクトの先頭に[IMessage: imapiprop](imessageimapiprop.md)オブジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="d3664-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="d3664-151">このようなオブジェクトのプロパティ属性は、 [SetAttribIMsgOnIStg](setattribimsgonistg.md)を使用して設定または変更したり、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)で取得したりできます。</span><span class="sxs-lookup"><span data-stu-id="d3664-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="d3664-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="d3664-152">Notes to callers</span></span>

<span data-ttu-id="d3664-153">**OpenIMsgOnIStg**を呼び出す前に、 [OpenIMsgSession](openimsgsession.md)を使用してメッセージセッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="d3664-154">有効な_lpmsgsess_パラメーターを指定すると、新しいメッセージがメッセージセッション内に作成され、セッションが閉じられるときに閉じられるようになります。 sures を実行してください。</span><span class="sxs-lookup"><span data-stu-id="d3664-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="d3664-155">_lpmsgsess_が NULL の場合、メッセージはメッセージセッションとは独立して作成されます。</span><span class="sxs-lookup"><span data-stu-id="d3664-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="d3664-156">メッセージを作成したクライアントアプリケーションまたはサービスプロバイダーが、そのメッセージをリリースしておらず、すべての添付ファイルと開いているテーブルを解放していない場合は、メモリがリークし、アプリケーションが終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="d3664-157">MAPI では、特に、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_が指す関数を使用して、オブジェクトインターフェイスを呼び出すときに使用するメモリをクライアントアプリケーションに割り当てます。[imapiprop:: GetProps](imapiprop-getprops.md) and [IMAPITable:: QueryRows](imapitable-queryrows.md)など。</span><span class="sxs-lookup"><span data-stu-id="d3664-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="d3664-158">_lpAllocateBuffer_、 _lpAllocateMore_、および_lpfreebuffer_の各ポインターは、有効な_lpMapiSup_パラメーターを指定して**OpenIMsgOnIStg**関数を呼び出した場合にオプションです。</span><span class="sxs-lookup"><span data-stu-id="d3664-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="d3664-159">基になる ole オブジェクトを処理しているため、MAPI では ole メモリ割り当ても使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="d3664-160">ole 構造化ストレージオブジェクトと ole メモリ割り当ての詳細については、「 _ole プログラマーズリファレンス_」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3664-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="d3664-161">_lpMapiSup_に有効な値が指定されている場合、 **IMessage**は[imapisupport::D oprogress DIALOG](imapisupport-doprogressdialog.md)メソッドを呼び出して、imapisupport [:: CopyTo](imapiprop-copyto.md)の進行状況ユーザーインターフェイスを提供することにより、MAPI_DIALOG および ATTACH_DIALOG フラグをサポートします。[IMessage::D eleteattach](imessage-deleteattach.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="d3664-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="d3664-162">また、 [IMessage:: modifyrecipients](imessage-modifyrecipients.md)メソッドは、 [imapisupport:: OpenAddressBook](imapisupport-openaddressbook.md)メソッドを呼び出して、生成されたアドレス帳オブジェクトに対して呼び出しを行うことによって、短期エントリ識別子を長期エントリ識別子に変換しようとします。</span><span class="sxs-lookup"><span data-stu-id="d3664-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="d3664-163">_lpMapiSup_に NULL が渡された場合、 **IMessage**は MAPI_DIALOG と ATTACH_DIALOG を無視し、短い用語エントリ識別子を変換せずに格納します。</span><span class="sxs-lookup"><span data-stu-id="d3664-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="d3664-164">_lpstg_パラメーターが指す**IStorage**オブジェクトは、STGM_READ または STGM_READWRITE モードのどちらかで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="d3664-165">STGM_READWRITE モードが使用されている場合は、STGM_TRANSACTED モードも設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="d3664-166">_lpfmsgcallrelease_パラメーターで指定されたコールバック関数はオプションです。指定する場合は、 [msgcallrelease](msgcallrelease.md)関数プロトタイプに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="d3664-167">**IMessage**インターフェイスは、 **IMessage**オブジェクトの参照カウントが、 **Release**メソッドへの\*\*\*\* 最後の呼び出しによって0に設定されたときに、それを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d3664-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="d3664-168">通常、コールバック関数は、基になる**IStorage**インターフェイスを解放するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d3664-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="d3664-169">**IMessage**は、コールバック後に_lpstg_パラメーターが指す**IStorage**オブジェクトへのアクセスを試みません。</span><span class="sxs-lookup"><span data-stu-id="d3664-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="d3664-170">一部のクライアントまたはプロバイダーは、 [SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されたときに**IMessage**自体が書き込みを超える、 **IStorage**オブジェクトに追加のデータを書き込む場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="d3664-171">クライアントまたはプロバイダーは、IMSG_NO_ISTG_COMMIT フラグを使用して、 **IMessage**が**SaveChanges**呼び出しの処理中に OLE **IStorage:: COMMIT**メソッドを呼び出さないようにすることができます。この場合、追加のデータが書き込まれたときに、クライアントまたはプロバイダー自体が**IStorage**オブジェクトをコミットする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="d3664-172">このため、 **IMessage**の実装では、文字列 "__" で始まる**IStorage**オブジェクト内に作成されるすべてのサブストレージの名前を指定する必要があります。つまり、アンダースコアは2つのアンダースコアで始まります。</span><span class="sxs-lookup"><span data-stu-id="d3664-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="d3664-173">クライアントまたはプロバイダーは、この名前空間のサブクラス名を保持することで、名前の競合を回避できます。</span><span class="sxs-lookup"><span data-stu-id="d3664-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="d3664-174">MAPI では、添付ファイル、ストリーム、埋め込みメッセージなど、メッセージのサブオブジェクトに対して実行される複数の開いている操作の動作は定義されません。</span><span class="sxs-lookup"><span data-stu-id="d3664-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="d3664-175">現在、mapi では、既に開かれているサブオブジェクトをもう一度開くことができますが、mapi は、既存の開いているオブジェクトの参照カウントを増分し、そのオブジェクトを[IMessage:: openattach を呼び出したクライアントまたはプロバイダーに返すことで、open 操作を実行します。](imessage-openattach.md)または[imapiprop:: openproperty](imapiprop-openproperty.md)メソッド。</span><span class="sxs-lookup"><span data-stu-id="d3664-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="d3664-176">これは、サブファイルに対する最初の開いた操作に対して要求されたアクセスが、操作によって要求されたアクセス許可に関係なく、以降のすべてのオープン操作に対して提供されるアクセスであることを意味します。</span><span class="sxs-lookup"><span data-stu-id="d3664-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="d3664-177">添付ファイルにメッセージを配置するための適切な手順は、IID_IMessage のインターフェイス識別子を使用して[imapiprop:: openproperty](imapiprop-openproperty.md)メソッドを呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="d3664-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="d3664-178">**openproperty**は現在、OLE **IStorage**インターフェイスで直接使用できるメッセージの添付ファイルの作成もサポートしています。つまり、IID_IStorage インターフェイス識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="d3664-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="d3664-179">**IStorage** access は、Microsoft Word 文書を OLE **IStream**インターフェイスに変換せずに添付ファイルに簡単に配置できるようにするためにサポートされています。</span><span class="sxs-lookup"><span data-stu-id="d3664-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="d3664-180">ただし、 **OpenIMsgOnIStg**に**IStorage**ポインターを添付ファイルデータに渡した後、オブジェクトが間違った順序で解放された場合、 **IMessage**は予測できない場合があります。</span><span class="sxs-lookup"><span data-stu-id="d3664-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d3664-181">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="d3664-181">MFCMAPI reference</span></span>

<span data-ttu-id="d3664-182">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3664-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d3664-183">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="d3664-183">**File**</span></span>|<span data-ttu-id="d3664-184">**関数**</span><span class="sxs-lookup"><span data-stu-id="d3664-184">**Function**</span></span>|<span data-ttu-id="d3664-185">**コメント**</span><span class="sxs-lookup"><span data-stu-id="d3664-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d3664-186">ファイル .cpp</span><span class="sxs-lookup"><span data-stu-id="d3664-186">File.cpp</span></span>  <br/> |<span data-ttu-id="d3664-187">loadmsgtomessage</span><span class="sxs-lookup"><span data-stu-id="d3664-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="d3664-188">mfcmapi は、 **OpenIMsgOnIStg**メソッドを使用して、の上に IMessage インターフェイスを開きます。MSG ファイルを使用して、ファイルが MAPI で操作されるようにします。</span><span class="sxs-lookup"><span data-stu-id="d3664-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d3664-189">関連項目</span><span class="sxs-lookup"><span data-stu-id="d3664-189">See also</span></span>

- <span data-ttu-id="d3664-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="d3664-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

