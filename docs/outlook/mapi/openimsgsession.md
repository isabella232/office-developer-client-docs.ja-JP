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
ms.openlocfilehash: e7f652e7426792d8b4c878b7f6738439aec65348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801681"
---
# <a name="openimsgsession"></a><span data-ttu-id="15c05-103">OpenIMsgSession</span><span class="sxs-lookup"><span data-stu-id="15c05-103">OpenIMsgSession</span></span>

  
  
<span data-ttu-id="15c05-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="15c05-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="15c05-105">作成し、その中に作成されたメッセージをグループ化するメッセージ セッションを開きます。</span><span class="sxs-lookup"><span data-stu-id="15c05-105">Creates and opens a message session that groups the messages created within it.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15c05-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="15c05-106">Header file:</span></span>  <br/> |<span data-ttu-id="15c05-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="15c05-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="15c05-108">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="15c05-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="15c05-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="15c05-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="15c05-110">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="15c05-110">Called by:</span></span>  <br/> |<span data-ttu-id="15c05-111">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="15c05-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgSession(
  LPMALLOC lpMalloc,
  ULONG ulFlags,
  LPMSGSESS FAR * lppMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="15c05-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="15c05-112">Parameters</span></span>

 <span data-ttu-id="15c05-113">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="15c05-113">_lpMalloc_</span></span>
  
> <span data-ttu-id="15c05-114">[in]OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx)インターフェイスを公開すること、メモリ アロケーター オブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="15c05-114">[in] Pointer to a memory allocator object exposing the OLE [IMalloc](http://msdn.microsoft.com/library/047f281e-2665-4d6d-9a0b-918cd3339447%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="15c05-115">MAPI では、OLE [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx)インターフェイスを使用する場合、この割り当てメソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15c05-115">MAPI needs to use this allocation method when working with the OLE [IStorage](http://msdn.microsoft.com/library/stg.istorage%28Office.15%29.aspx) interface.</span></span> 
    
 <span data-ttu-id="15c05-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="15c05-116">_ulFlags_</span></span>
  
> <span data-ttu-id="15c05-117">[����]�\�񂳂�Ă��܂��B0 �ɂ���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="15c05-117">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="15c05-118">_lppMsgSess_</span><span class="sxs-lookup"><span data-stu-id="15c05-118">_lppMsgSess_</span></span>
  
> <span data-ttu-id="15c05-119">[out]返されるメッセージのセッション オブジェクトへのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="15c05-119">[out] Pointer to a pointer to the returned message session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15c05-120">�߂�l</span><span class="sxs-lookup"><span data-stu-id="15c05-120">Return value</span></span>

<span data-ttu-id="15c05-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="15c05-121">S_OK</span></span>
  
> <span data-ttu-id="15c05-122">セッションが開かれました。</span><span class="sxs-lookup"><span data-stu-id="15c05-122">The session was opened.</span></span>
    
<span data-ttu-id="15c05-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="15c05-123">MAPI_E_INVALID_PARAMETER</span></span>
  
>  <span data-ttu-id="15c05-124">_lpMalloc_または_lppMsgSess_は、NULL です。</span><span class="sxs-lookup"><span data-stu-id="15c05-124">_lpMalloc_ or  _lppMsgSess_ is NULL.</span></span> 
    
<span data-ttu-id="15c05-125">MAPI_E_INVALID_FLAGS</span><span class="sxs-lookup"><span data-stu-id="15c05-125">MAPI_E_INVALID_FLAGS</span></span>
  
> <span data-ttu-id="15c05-126">無効なフラグが渡されました。</span><span class="sxs-lookup"><span data-stu-id="15c05-126">Invalid flags were passed.</span></span>
    
<span data-ttu-id="15c05-127">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="15c05-127">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="15c05-128">この関数を呼び出す場合、クライアントまたはサービス プロバイダーは、Unicode の .msg ファイルを作成するのには MAPI_UNICODE フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="15c05-128">When calling this function, a client or service provider sets the MAPI_UNICODE flag to create Unicode .msg files.</span></span> <span data-ttu-id="15c05-129">[Imessage](imessageimapiprop.md)ファイルでは、その PR_STORE_SUPPORT_MASK に STORE_UNICODE_OK を示しています、Unicode プロパティをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="15c05-129">The resulting [Imessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its PR_STORE_SUPPORT_MASK and supports Unicode properties.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="15c05-130">注釈</span><span class="sxs-lookup"><span data-stu-id="15c05-130">Remarks</span></span>

<span data-ttu-id="15c05-131">メッセージ セッションがクライアント アプリケーションによって使用され、いくつかに対処するために必要なサービス プロバイダーに関連する MAPI [IMessage: IMAPIProp](imessageimapiprop.md)オブジェクトの基になる OLE **IStorage**オブジェクトの上に構築します。</span><span class="sxs-lookup"><span data-stu-id="15c05-131">A message session is used by client applications and service providers that want to deal with several related MAPI [IMessage : IMAPIProp](imessageimapiprop.md) objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="15c05-132">クライアントまたはプロバイダーは、 **OpenIMsgSession**と[CloseIMsgSession](closeimsgsession.md)関数を使用して、メッセージ セッション中には、このようなメッセージの作成をラップします。</span><span class="sxs-lookup"><span data-stu-id="15c05-132">The client or provider uses the **OpenIMsgSession** and [CloseIMsgSession](closeimsgsession.md) functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="15c05-133">メッセージ セッションを開くと、クライアントまたはプロバイダーのポインターに渡します - **IStorage**オブジェクトの新しい**IMessage**を作成する[OpenIMsgOnIStg](openimsgonistg.md)への呼び出しで。</span><span class="sxs-lookup"><span data-stu-id="15c05-133">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="15c05-134">メッセージ セッションの追跡 - 点灯 - **IStorage**オブジェクトのすべての添付ファイルとメッセージの他のプロパティだけでなく、セッションの期間中に作成されたすべての**IMessage**です。</span><span class="sxs-lookup"><span data-stu-id="15c05-134">A message session keeps track of all **IMessage**-on- **IStorage** objects created during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="15c05-135">クライアントまたはプロバイダーを呼び出すと**CloseIMsgSession**、これらすべてのオブジェクトを閉じます。</span><span class="sxs-lookup"><span data-stu-id="15c05-135">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="15c05-136">-点灯 - **IStorage**オブジェクト**IMessage**を終了する唯一の方法は、 **CloseIMsgSession**を呼び出すことです。</span><span class="sxs-lookup"><span data-stu-id="15c05-136">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  
 <span data-ttu-id="15c05-137">**OpenIMsgSession**は、クライアントと OLE **IStorage**オブジェクトに関連するいくつかのメッセージを処理する能力を必要とするプロバイダーが使用されます。</span><span class="sxs-lookup"><span data-stu-id="15c05-137">**OpenIMsgSession** is used by clients and providers that require the ability to handle several related messages as OLE **IStorage** objects.</span></span> <span data-ttu-id="15c05-138">だけこのような 1 つのメッセージを同時に開くことが、複数のメッセージと**OpenIMsgSession**とメッセージ セッションを作成する理由を追跡する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="15c05-138">If only one such message is to be open at a time, there is no need to track multiple messages and no reason to create a message session with **OpenIMsgSession**.</span></span> 
  
<span data-ttu-id="15c05-139">基になる OLE オブジェクトを扱うことはため、MAPI は、OLE のメモリの割り当てを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15c05-139">Because it is dealing with an underlying OLE object, MAPI needs to use OLE memory allocation.</span></span> <span data-ttu-id="15c05-140">OLE 構造化ストレージ オブジェクトと OLE のメモリの割り当ての詳細については、 [OLE アプリケーションとデータの転送](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="15c05-140">For more information about OLE structured storage objects and OLE memory allocation, see [OLE and Data Transfer](http://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx).</span></span> 
  

