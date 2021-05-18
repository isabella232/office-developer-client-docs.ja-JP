---
title: OpenIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.OpenIMsgSession
api_type:
- COM
ms.assetid: f75229e3-5f44-4298-8706-9eddf0ef124c
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326195"
---
# <a name="openimsgsession"></a><span data-ttu-id="595b1-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="595b1-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="595b1-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="595b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="595b1-105">作成し、その中に作成されたメッセージをグループ分けするメッセージ セッションを開きます。</span><span class="sxs-lookup"><span data-stu-id="595b1-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="595b1-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="595b1-106">Header file:</span></span>  <br/> |<span data-ttu-id="595b1-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="595b1-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="595b1-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="595b1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="595b1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="595b1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="595b1-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="595b1-110">Called by:</span></span>  <br/> |<span data-ttu-id="595b1-111">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="595b1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="595b1-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="595b1-112">Parameters</span></span>

 <span data-ttu-id="595b1-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="595b1-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="595b1-114">[in]OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) インターフェイスを公開するメモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="595b1-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="595b1-115">MAPI は、OLE IStorage インターフェイスを操作するときにこの割り当 [て方法を使用する必要](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) があります。</span><span class="sxs-lookup"><span data-stu-id="595b1-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="595b1-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="595b1-116">_ulFlags_</span></span>
  
> <span data-ttu-id="595b1-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="595b1-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="595b1-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="595b1-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="595b1-119">[out]返されるメッセージ セッション オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="595b1-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="595b1-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="595b1-120">Return value</span></span>

<span data-ttu-id="595b1-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="595b1-121">S_OK</span></span>
  
> <span data-ttu-id="595b1-122">セッションが開かされました。</span><span class="sxs-lookup"><span data-stu-id="595b1-122">The session was opened.</span></span>
    
<span data-ttu-id="595b1-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="595b1-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="595b1-124">_lpMalloc_ または  _lppMsgSess は_ NULL です。</span><span class="sxs-lookup"><span data-stu-id="595b1-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="595b1-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="595b1-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="595b1-126">無効なフラグが渡された。</span><span class="sxs-lookup"><span data-stu-id="595b1-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="595b1-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="595b1-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="595b1-128">この関数を呼び出す場合、クライアントまたはサービス プロバイダーは、Unicode .msg ファイルMAPI_UNICODEフラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="595b1-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="595b1-129">結果の [Imessage ファイル](imessageimapiprop.md) は、そのSTORE_UNICODE_OKにPR_STORE_SUPPORT_MASK Unicode プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="595b1-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="595b1-130">注釈</span><span class="sxs-lookup"><span data-stu-id="595b1-130">Remarks</span></span>

<span data-ttu-id="595b1-131">メッセージ セッションは、いくつかの関連する MAPI IMessage ( 基になる OLE **IStorage** オブジェクトの上に構築された [IMAPIProp](imessageimapiprop.md)オブジェクト) を処理するクライアント アプリケーションおよびサービス プロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="595b1-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="595b1-132">クライアントまたはプロバイダーは **、OpenIMsgSession** 関数と [CloseIMsgSession](closeimsgsession.md) 関数を使用して、メッセージ セッション内でこのようなメッセージの作成をラップします。</span><span class="sxs-lookup"><span data-stu-id="595b1-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="595b1-133">メッセージ セッションを開いた後、クライアントまたはプロバイダーは [OpenIMsgOnIStg](openimsgonistg.md) への呼び出しでポインターを渡して、新しい **IMessage**-on- **IStorage** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="595b1-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="595b1-134">メッセージ セッションでは、メッセージのすべての添付ファイルと他のプロパティに加えて、セッション中に作成された **すべての IMessage**-on- **IStorage** オブジェクトが追跡されます。</span><span class="sxs-lookup"><span data-stu-id="595b1-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="595b1-135">クライアントまたはプロバイダーが **CloseIMsgSession** を呼び出す場合、これらのオブジェクトはすべて閉じます。</span><span class="sxs-lookup"><span data-stu-id="595b1-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="595b1-136">**CloseIMsgSession** を呼び出す方法は **、IMessage**-on- **IStorage オブジェクトを閉じる唯一の方法** です。</span><span class="sxs-lookup"><span data-stu-id="595b1-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="595b1-137">**OpenIMsgSession** は、OLE **IStorage** オブジェクトとして複数の関連メッセージを処理する機能を必要とするクライアントおよびプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="595b1-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="595b1-138">一度に 1 つのメッセージのみを開く場合は、複数のメッセージを追跡する必要はありません。 **また、OpenIMsgSession** を使用してメッセージ セッションを作成する理由はありません。</span><span class="sxs-lookup"><span data-stu-id="595b1-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="595b1-139">基になる OLE オブジェクトを扱うので、MAPI は OLE メモリ割り当てを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="595b1-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="595b1-140">OLE 構造化ストレージ オブジェクトと OLE メモリ割り当ての詳細については [、「OLE とデータ転送」を参照してください](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)。</span><span class="sxs-lookup"><span data-stu-id="595b1-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

