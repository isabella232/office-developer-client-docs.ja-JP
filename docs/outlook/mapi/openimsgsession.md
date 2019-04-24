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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 607105bd58a14a3510f1ae71246069440a4f05cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326195"
---
# <a name="openimsgsession"></a><span data-ttu-id="474ea-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="474ea-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="474ea-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="474ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="474ea-105">その中で作成されたメッセージをグループ化するメッセージセッションを作成して開きます。</span><span class="sxs-lookup"><span data-stu-id="474ea-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="474ea-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="474ea-106">Header file:</span></span>  <br/> |<span data-ttu-id="474ea-107">Imessage</span><span class="sxs-lookup"><span data-stu-id="474ea-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="474ea-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="474ea-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="474ea-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="474ea-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="474ea-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="474ea-110">Called by:</span></span>  <br/> |<span data-ttu-id="474ea-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="474ea-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="474ea-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="474ea-112">Parameters</span></span>

 <span data-ttu-id="474ea-113">_lpmalloc_</span><span class="sxs-lookup"><span data-stu-id="474ea-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="474ea-114">順番OLE [imalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)インターフェイスを公開するメモリアロケーターオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="474ea-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="474ea-115">MAPI は、OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage)インターフェイスで作業するときに、この割り当て方法を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="474ea-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="474ea-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="474ea-116">_ulFlags_</span></span>
  
> <span data-ttu-id="474ea-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="474ea-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="474ea-118">_lppmsgsess_</span><span class="sxs-lookup"><span data-stu-id="474ea-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="474ea-119">読み上げ返されたメッセージセッションオブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="474ea-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="474ea-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="474ea-120">Return value</span></span>

<span data-ttu-id="474ea-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="474ea-121">S_OK</span></span>
  
> <span data-ttu-id="474ea-122">セッションが開かれました。</span><span class="sxs-lookup"><span data-stu-id="474ea-122">The session was opened.</span></span>
    
<span data-ttu-id="474ea-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="474ea-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="474ea-124">_lpmalloc_または_lppmsgsess_ NULL です。</span><span class="sxs-lookup"><span data-stu-id="474ea-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="474ea-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="474ea-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="474ea-126">無効なフラグが渡されました。</span><span class="sxs-lookup"><span data-stu-id="474ea-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="474ea-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="474ea-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="474ea-128">この関数を呼び出すと、クライアントまたはサービスプロバイダーは、MAPI_UNICODE フラグを設定して、UNICODE の .msg ファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="474ea-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="474ea-129">生成された[Imessage](imessageimapiprop.md)ファイルは、PR_STORE_SUPPORT_MASK に STORE_UNICODE_OK を表示し、UNICODE プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="474ea-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="474ea-130">解説</span><span class="sxs-lookup"><span data-stu-id="474ea-130">Remarks</span></span>

<span data-ttu-id="474ea-131">メッセージセッションは、基になる OLE **IStorage**オブジェクトの上に構築された複数の関連する MAPI [IMessage: imapiprop](imessageimapiprop.md)オブジェクトを処理するクライアントアプリケーションおよびサービスプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="474ea-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="474ea-132">クライアントまたはプロバイダーは、 **OpenIMsgSession**関数と[CloseIMsgSession](closeimsgsession.md)関数を使用して、メッセージセッション内のメッセージの作成をラップします。</span><span class="sxs-lookup"><span data-stu-id="474ea-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="474ea-133">メッセージセッションが開かれると、クライアントまたはプロバイダーは、 [OpenIMsgOnIStg](openimsgonistg.md)への呼び出しによって、新しい**IMessage**オブジェクトを作成するために\*\*\*\* ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="474ea-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="474ea-134">メッセージセッションは、メッセージのすべての添付ファイルと\*\*\*\* その他のプロパティに加えて、セッションの期間中に作成されたすべての**IMessage**オブジェクトを追跡します。</span><span class="sxs-lookup"><span data-stu-id="474ea-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="474ea-135">クライアントまたはプロバイダーが**CloseIMsgSession**を呼び出すと、これらのすべてのオブジェクトが閉じられます。</span><span class="sxs-lookup"><span data-stu-id="474ea-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="474ea-136">**CloseIMsgSession**の呼び出しは、 **IMessage**で、 **IStorage**オブジェクトを閉じる唯一の方法です。</span><span class="sxs-lookup"><span data-stu-id="474ea-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="474ea-137">**OpenIMsgSession**は、複数の関連するメッセージを OLE **IStorage**オブジェクトとして処理する機能を必要とするクライアントとプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="474ea-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="474ea-138">そのようなメッセージを一度に1つだけ開く場合は、複数のメッセージを追跡する必要がなく、 **OpenIMsgSession**を使用してメッセージセッションを作成する理由もありません。</span><span class="sxs-lookup"><span data-stu-id="474ea-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="474ea-139">基になる ole オブジェクトを処理しているため、MAPI は ole メモリ割り当てを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="474ea-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="474ea-140">ole 構造化ストレージオブジェクトと ole メモリ割り当ての詳細については、「 [ole とデータ転送](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="474ea-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

