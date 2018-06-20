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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801685"
---
# <a name="openimsgonistg"></a><span data-ttu-id="0c83a-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="0c83a-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="0c83a-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c83a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c83a-105">メッセージ セッション内で使用する、既存の OLE **IStorage**オブジェクトの上に新しい[IMessage](imessageimapiprop.md)オブジェクトを構築します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c83a-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="0c83a-106">Header file:</span></span>  <br/> |<span data-ttu-id="0c83a-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="0c83a-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="0c83a-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0c83a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0c83a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0c83a-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-110">Called by:</span></span>  <br/> |<span data-ttu-id="0c83a-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="0c83a-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="0c83a-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="0c83a-112">Parameters</span></span>

<span data-ttu-id="0c83a-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="0c83a-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="0c83a-114">[in]- **IStorage**オブジェクトの新しい**IMessage**が作成される、メッセージ セッション オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c83a-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="0c83a-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="0c83a-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="0c83a-116">[in]メモリの割り当てに使用する[MAPIAllocateBuffer](mapiallocatebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c83a-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="0c83a-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="0c83a-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="0c83a-118">[in]追加メモリの割り当てに使用する[MAPIAllocateMore](mapiallocatemore.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c83a-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="0c83a-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="0c83a-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="0c83a-120">[in]メモリを解放するために使用する、 [MAPIFreeBuffer](mapifreebuffer.md)関数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c83a-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="0c83a-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="0c83a-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="0c83a-122">[in]OLE **IMalloc**インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c83a-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="0c83a-123">**IMessage**インターフェイスは、 **IStorage**など**IStream**インターフェイスを使用する場合、この割り当てメソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="0c83a-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="0c83a-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="0c83a-125">[in]サービス プロバイダーのメソッドの呼び出しに使用できる MAPI サポート オブジェクトへのポインターを省略可能な[IMAPISupport: IUnknown](imapisupportiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="0c83a-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="0c83a-126">_lpStg_</span></span>
  
> <span data-ttu-id="0c83a-127">[で [チェック アウト]OLE **IStorage**オブジェクトが開いている、読み取り専用または読み取り/書き込みのアクセス許可へのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c83a-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="0c83a-128">**IMessage**が書き込み専用のアクセスをサポートしていないために、 **OpenIMsgOnIStg**は書き込み専用モードで開かれたストレージ オブジェクトを使用できません。</span><span class="sxs-lookup"><span data-stu-id="0c83a-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="0c83a-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="0c83a-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="0c83a-130">[in]-点灯 - **IStorage**オブジェクト**IMessage**の前回のリリースでは、次の呼び出しには、MAPI [MSGCALLRELEASE](msgcallrelease.md)プロトタイプに基づいてコールバック関数へのポインター ポインターです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="0c83a-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="0c83a-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="0c83a-132">[in]-点灯 - **IMessage** **IStorage**オブジェクトには MAPI によって保存され、 **MSGCALLRELEASE**に渡される呼び出し元のデータは、コールバック関数を基づいています。</span><span class="sxs-lookup"><span data-stu-id="0c83a-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="0c83a-133">データでは、リリースされている**IMessage**オブジェクトについてのコンテキストと上に構築された、 **IStorage**オブジェクトを提供します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="0c83a-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c83a-134">_ulFlags_</span></span>
  
> <span data-ttu-id="0c83a-135">[in]クライアント アプリケーションまたはサービス プロバイダーは、 **IMessage::SaveChanges**メソッドを呼び出すと、OLE **IStorage::Commit**メソッドが呼び出されるかどうかは、コントロールに使用するフラグのビットマスクです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="0c83a-136">次のフラグを設定することができます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="0c83a-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="0c83a-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="0c83a-138">OLE メソッド**IStorage::Commit**は、クライアントまたはプロバイダーは、 [SaveChanges](imapiprop-savechanges.md)を呼び出すときに呼び出されるしません。</span><span class="sxs-lookup"><span data-stu-id="0c83a-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="0c83a-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0c83a-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="0c83a-140">Unicode の .msg ファイルを作成をできます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="0c83a-141">[IMessage](imessageimapiprop.md)ファイルでは、その[PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md)に STORE_UNICODE_OK を示しています、Unicode プロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="0c83a-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="0c83a-142">MAPI_UNICODE フラグは、Outlook 2003 またはそれ以降、この関数でのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="0c83a-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="0c83a-143">_lppMsg_</span></span>
  
> <span data-ttu-id="0c83a-144">[out]開かれた**IMessage**オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="0c83a-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0c83a-145">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0c83a-145">Return value</span></span>

<span data-ttu-id="0c83a-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c83a-146">S_OK</span></span> 
  
> <span data-ttu-id="0c83a-147">�ʘb���������A�\�������l�܂��͒l���Ԃ���܂��B</span><span class="sxs-lookup"><span data-stu-id="0c83a-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c83a-148">����</span><span class="sxs-lookup"><span data-stu-id="0c83a-148">Remarks</span></span>

<span data-ttu-id="0c83a-149">プロパティの属性は、プロパティ オブジェクト、つまり、オブジェクトを実装することでのみアクセスできます、 [IMAPIProp: IUnknown](imapipropiunknown.md)インタ フェースです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="0c83a-150">**OpenIMsgOnIStg**ビルドの MAPI プロパティを OLE 構造化ストレージ オブジェクトで使用できるようにするのには、 [IMessage: IMAPIProp](imessageimapiprop.md) OLE **IStorage**オブジェクト上にあるオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="0c83a-151">このようなオブジェクトのプロパティの属性の設定または[SetAttribIMsgOnIStg](setattribimsgonistg.md)に変更し、 [GetAttribIMsgOnIStg](getattribimsgonistg.md)を取得します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0c83a-152">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="0c83a-152">Notes to callers</span></span>

<span data-ttu-id="0c83a-153">**OpenIMsgOnIStg**が呼び出される前に[OpenIMsgSession](openimsgsession.md)でメッセージ セッションを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="0c83a-154">Sures _lpMsgSess_の有効なパラメーターを指定するセッションが閉じられるときが閉じられているようにメッセージのセッション内で新しいメッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="0c83a-155">_LpMsgSess_が NULL の場合は、メッセージの任意のセッションとは別にメッセージが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="0c83a-156">場合、クライアント アプリケーションまたはメッセージを作成するサービス プロバイダーは、それと同様に、すべての添付ファイルを解放されず、テーブルを開き、メモリ リーク、アプリケーションが終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="0c83a-157">MAPI が to で指された_lpAllocateBuffer_、 _lpAllocateMore_、および多くのメモリの割り当てと解放のための_lpFreeBuffer_具体的にはオブジェクトのインターフェイスを呼び出すときにクライアント アプリケーションで使用するメモリの割り当て関数を使用してください。[IMAPIProp::GetProps](imapiprop-getprops.md) 、 [IMAPITable::QueryRows](imapitable-queryrows.md)などです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="0c83a-158">有効な_lpMapiSup_パラメーターを使用して、 **OpenIMsgOnIStg**関数が呼び出されたときに、 _lpAllocateBuffer_、 _lpAllocateMore_、および_lpFreeBuffer_のポインターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="0c83a-159">基になる OLE オブジェクトを扱うにはため、MAPI が OLE メモリの割り当てを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="0c83a-160">OLE 構造化ストレージ オブジェクトと OLE のメモリの割り当ての詳細については、 _OLE プログラマ リファレンス_を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0c83a-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="0c83a-161">**IMessage**が[IMAPIProp::CopyTo](imapiprop-copyto.md)の進行状況のユーザー インターフェイスを提供する[IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md)メソッドを呼び出すことによって、MAPI_DIALOG と ATTACH_DIALOG フラグをサポートする_lpMapiSup_の有効な値を入力する場合[IMessage::DeleteAttach](imessage-deleteattach.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="0c83a-162">また、 [IMessage::ModifyRecipients](imessage-modifyrecipients.md)メソッドは[IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md)メソッドを呼び出すと、結果のアドレス帳オブジェクトに呼び出しを行うことによって、長期のエントリ id を短期的なエントリの識別子を変換しようとします。</span><span class="sxs-lookup"><span data-stu-id="0c83a-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="0c83a-163">_LpMapiSup_に NULL を渡した場合、 **IMessage**は MAPI_DIALOG と ATTACH_DIALOG を無視し、変換せずに短期的なエントリの識別子を格納します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="0c83a-164">_LpStg_パラメーターが指す**IStorage**オブジェクトは、STGM_READ または STGM_READWRITE のいずれかのモードで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="0c83a-165">STGM_READWRITE モードを使用する場合、STGM_TRANSACTED モードも設定しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="0c83a-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="0c83a-166">_LpfMsgCallRelease_パラメーターで指定されたコールバック関数は省略可能です。指定した場合に、 [MSGCALLRELEASE](msgcallrelease.md)関数のプロトタイプに基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="0c83a-167">-点灯 - **IMessage** **IStorage**オブジェクトの参照カウントは、 **Release**メソッドの最後の呼び出しによってゼロに設定されている場合、 **IMessage**インターフェイスを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="0c83a-168">コールバック関数は、基になっている**IStorage**インターフェイスを解放する通常使用されます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="0c83a-169">**IMessage**は、コールバックを行った後、 _lpStg_パラメーターで示される**IStorage**オブジェクトにアクセスするのにはしません。</span><span class="sxs-lookup"><span data-stu-id="0c83a-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="0c83a-170">いくつかのクライアントやプロバイダーは、追加のデータを書き込む可能性があります、 [SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されたときに書き込み自体**IMessage**をどのような**IStorage**オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="0c83a-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="0c83a-171">クライアントまたはプロバイダーは、 **SaveChanges**の呼び出しの処理中に OLE **IStorage::Commit**メソッドを呼び出してから**IMessage**を防ぐために IMSG_NO_ISTG_COMMIT フラグを使用できます。ここでは、クライアントまたはプロバイダー コミットする必要が自体**IStorage**オブジェクト追加のデータが書き込まれるときです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="0c83a-172">これに役立てるため、2 つのアンダー スコアでは、文字列「_ _」から始まる、 **IStorage**オブジェクトに作成し、すべての substorages に名前を付ける**IMessage**の実装を保証します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="0c83a-173">クライアントまたはプロバイダーは、この名前空間からのサブストレージの名前を保持することで名前の衝突を回避できます。</span><span class="sxs-lookup"><span data-stu-id="0c83a-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="0c83a-174">MAPI では、添付ファイル、ストリーム、または埋め込まれたメッセージなどのメッセージの下位で実行される複数の開く操作の動作は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="0c83a-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="0c83a-175">MAPI が現在をもう一度開くオープンされているサブオブジェクトをことができますが、MAPI は、既存の開いているオブジェクトの参照カウントをインクリメントして、クライアント、IMessage::OpenAttach、[と呼ばれるプロバイダーに戻すことによってファイルを開く操作を実行](imessage-openattach.md)または[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドです。</span><span class="sxs-lookup"><span data-stu-id="0c83a-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="0c83a-176">これは、サブオブジェクトの最初の開く操作の要求されたアクセスの操作で要求されたアクセス権に関係なく、その後開く操作のアクセスを意味します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="0c83a-177">添付ファイルにメッセージを配置するための正しい手順では、IID_IMessage のインタ フェース識別子で[IMAPIProp::OpenProperty](imapiprop-openproperty.md)メソッドを呼び出す。</span><span class="sxs-lookup"><span data-stu-id="0c83a-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="0c83a-178">**OpenProperty**現在の作成をサポート メッセージの添付ファイルが利用可能な OLE **IStorage**インターフェイス上で直接は、IID_IStorage インターフェイス識別子を使用します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="0c83a-179">**IStorage**のアクセスをサポートして、簡単に OLE **IStream**インターフェイスとの間に変換せず、添付ファイルを Microsoft Word 文書を配置することを許可します。</span><span class="sxs-lookup"><span data-stu-id="0c83a-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="0c83a-180">ただし、 **OpenIMsgOnIStg**が添付ファイルのデータに、 **IStorage**ポインターを渡され、間違った順序でのオブジェクトの解放し、 **IMessage**が予測可能な動作しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0c83a-181">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="0c83a-181">MFCMAPI reference</span></span>

<span data-ttu-id="0c83a-182">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="0c83a-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0c83a-183">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="0c83a-183">**File**</span></span>|<span data-ttu-id="0c83a-184">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="0c83a-184">**Function**</span></span>|<span data-ttu-id="0c83a-185">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="0c83a-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c83a-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="0c83a-186">File.cpp</span></span>  <br/> |<span data-ttu-id="0c83a-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="0c83a-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="0c83a-188">MFCMAPI を開くには、IMessage インターフェイスの上に**OpenIMsgOnIStg**メソッドを使用して、します。MSG ファイルに MAPI でファイルを操作することがあります。</span><span class="sxs-lookup"><span data-stu-id="0c83a-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c83a-189">関連項目</span><span class="sxs-lookup"><span data-stu-id="0c83a-189">See also</span></span>

- <span data-ttu-id="0c83a-190">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="0c83a-190">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

