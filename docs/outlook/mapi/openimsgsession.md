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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389625"
---
# <a name="openimsgsession"></a><span data-ttu-id="63e42-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="63e42-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="63e42-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="63e42-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="63e42-105">作成し、その中に作成されたメッセージをグループ化するメッセージ セッションを開きます。</span><span class="sxs-lookup"><span data-stu-id="63e42-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="63e42-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="63e42-106">Header file:</span></span>  <br/> |<span data-ttu-id="63e42-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="63e42-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="63e42-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="63e42-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="63e42-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="63e42-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="63e42-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="63e42-110">Called by:</span></span>  <br/> |<span data-ttu-id="63e42-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="63e42-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="63e42-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="63e42-112">Parameters</span></span>

 <span data-ttu-id="63e42-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="63e42-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="63e42-114">[in]OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc)インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="63e42-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-imalloc) interface.</span></span> <span data-ttu-id="63e42-115">MAPI では、OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage)インターフェイスを使用する場合、この割り当てメソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63e42-115">MAPI needs to use this allocation method when working with the OLE [IStorage](https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istorage) interface.</span></span> 
    
 <span data-ttu-id="63e42-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="63e42-116">_ulFlags_</span></span>
  
> <span data-ttu-id="63e42-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="63e42-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="63e42-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="63e42-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="63e42-119">[out]返されるメッセージのセッション オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="63e42-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="63e42-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="63e42-120">Return value</span></span>

<span data-ttu-id="63e42-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="63e42-121">S_OK</span></span>
  
> <span data-ttu-id="63e42-122">セッションが開かれました。</span><span class="sxs-lookup"><span data-stu-id="63e42-122">The session was opened.</span></span>
    
<span data-ttu-id="63e42-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="63e42-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="63e42-124">_lpMalloc_または_lppMsgSess_は、NULL です。</span><span class="sxs-lookup"><span data-stu-id="63e42-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="63e42-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="63e42-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="63e42-126">無効なフラグが渡されました。</span><span class="sxs-lookup"><span data-stu-id="63e42-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="63e42-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="63e42-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="63e42-128">この関数を呼び出す場合、クライアントまたはサービス プロバイダーは、Unicode の .msg ファイルを作成するのには MAPI_UNICODE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="63e42-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="63e42-129">[Imessage](imessageimapiprop.md)ファイルでは、その PR_STORE_SUPPORT_MASK に STORE_UNICODE_OK を示しています、Unicode プロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="63e42-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="63e42-130">備考</span><span class="sxs-lookup"><span data-stu-id="63e42-130">Remarks</span></span>

<span data-ttu-id="63e42-131">メッセージ セッションがクライアント アプリケーションによって使用され、いくつかに対処するために必要なサービス プロバイダーに関連する MAPI [IMessage: IMAPIProp](imessageimapiprop.md)オブジェクトの基になる OLE **IStorage**オブジェクトの上に構築します。</span><span class="sxs-lookup"><span data-stu-id="63e42-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="63e42-132">クライアントまたはプロバイダーは、 **OpenIMsgSession**と[CloseIMsgSession](closeimsgsession.md)関数を使用して、メッセージ セッション中には、このようなメッセージの作成をラップします。</span><span class="sxs-lookup"><span data-stu-id="63e42-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="63e42-133">メッセージ セッションを開くと、クライアントまたはプロバイダーのポインターに渡します - **IStorage**オブジェクトの新しい**IMessage**を作成する[OpenIMsgOnIStg](openimsgonistg.md)への呼び出しで。</span><span class="sxs-lookup"><span data-stu-id="63e42-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="63e42-134">メッセージ セッションの追跡 - 点灯 - **IStorage**オブジェクトのすべての添付ファイルとメッセージの他のプロパティだけでなく、セッションの期間中に作成されたすべての**IMessage**です。</span><span class="sxs-lookup"><span data-stu-id="63e42-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="63e42-135">クライアントまたはプロバイダーを呼び出すと**CloseIMsgSession**、これらすべてのオブジェクトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="63e42-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="63e42-136">-点灯 - **IStorage**オブジェクト**IMessage**を終了する唯一の方法は、 **CloseIMsgSession**を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="63e42-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="63e42-137">**OpenIMsgSession**は、クライアントと OLE **IStorage**オブジェクトに関連するいくつかのメッセージを処理する能力を必要とするプロバイダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="63e42-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="63e42-138">だけこのような 1 つのメッセージを同時に開くことが、複数のメッセージと**OpenIMsgSession**とメッセージ セッションを作成する理由を追跡する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="63e42-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="63e42-139">基になる OLE オブジェクトを扱うことはため、MAPI は、OLE のメモリの割り当てを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63e42-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="63e42-140">OLE 構造化ストレージ オブジェクトと OLE のメモリの割り当ての詳細については、 [OLE アプリケーションとデータの転送](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="63e42-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

