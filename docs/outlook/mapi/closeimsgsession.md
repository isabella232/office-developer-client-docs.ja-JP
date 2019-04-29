---
title: CloseIMsgSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CloseIMsgSession
api_type:
- COM
ms.assetid: a0a17309-fc59-4822-be9b-b6f623b68bb1
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 877bebf0a156c99907505d815ca8d36a4b398678
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412038"
---
# <a name="closeimsgsession"></a><span data-ttu-id="28c94-103">CloseIMsgSession</span><span class="sxs-lookup"><span data-stu-id="28c94-103">CloseIMsgSession</span></span>

  
  
<span data-ttu-id="28c94-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28c94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28c94-105">メッセージセッションと、そのセッション内で作成されたすべてのメッセージを閉じます。</span><span class="sxs-lookup"><span data-stu-id="28c94-105">Closes a message session and all the messages created within that session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="28c94-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="28c94-106">Header file:</span></span>  <br/> |<span data-ttu-id="28c94-107">Imessage</span><span class="sxs-lookup"><span data-stu-id="28c94-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="28c94-108">実装元:</span><span class="sxs-lookup"><span data-stu-id="28c94-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="28c94-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="28c94-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="28c94-110">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="28c94-110">Called by:</span></span>  <br/> |<span data-ttu-id="28c94-111">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="28c94-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
VOID CloseIMsgSession(
  LPMSGSESS lpMsgSess
);
```

## <a name="parameters"></a><span data-ttu-id="28c94-112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="28c94-112">Parameters</span></span>

 <span data-ttu-id="28c94-113">_lpmsgsess_</span><span class="sxs-lookup"><span data-stu-id="28c94-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="28c94-114">順番メッセージセッションの開始時に[OpenIMsgSession](openimsgsession.md)関数を使用して取得したメッセージセッションオブジェクトへのポインター。</span><span class="sxs-lookup"><span data-stu-id="28c94-114">[in] Pointer to the message session object obtained using the [OpenIMsgSession](openimsgsession.md) function at the start of the message session.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="28c94-115">Return value</span><span class="sxs-lookup"><span data-stu-id="28c94-115">Return value</span></span>

<span data-ttu-id="28c94-116">なし。</span><span class="sxs-lookup"><span data-stu-id="28c94-116">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28c94-117">注釈</span><span class="sxs-lookup"><span data-stu-id="28c94-117">Remarks</span></span>

<span data-ttu-id="28c94-118">メッセージセッションは、基になる OLE **IStorage**オブジェクトの上に構築された複数の関連する MAPI **IMessage**オブジェクトを処理するクライアントアプリケーションおよびサービスプロバイダーによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="28c94-118">A message session is used by client applications and service providers that want to deal with several related MAPI **IMessage** objects built on top of underlying OLE **IStorage** objects.</span></span> <span data-ttu-id="28c94-119">クライアントまたはプロバイダーは、 [OpenIMsgSession](openimsgsession.md)関数と**CloseIMsgSession**関数を使用して、メッセージセッション内のメッセージの作成をラップします。</span><span class="sxs-lookup"><span data-stu-id="28c94-119">The client or provider uses the [OpenIMsgSession](openimsgsession.md) and **CloseIMsgSession** functions to wrap the creation of such messages inside a message session.</span></span> <span data-ttu-id="28c94-120">メッセージセッションが開かれると、クライアントまたはプロバイダーは、 [OpenIMsgOnIStg](openimsgonistg.md)への呼び出しによって、新しい**IMessage**オブジェクトを作成するために\*\*\*\* ポインターを渡します。</span><span class="sxs-lookup"><span data-stu-id="28c94-120">Once the message session is opened, the client or provider passes a pointer to it in a call to [OpenIMsgOnIStg](openimsgonistg.md) to create a new **IMessage**-on- **IStorage** object.</span></span> 
  
<span data-ttu-id="28c94-121">メッセージセッションは、メッセージのすべての添付ファイルと\*\*\*\* その他のプロパティに加えて、セッションの間に開かれたすべての**IMessage**オブジェクトを追跡します。</span><span class="sxs-lookup"><span data-stu-id="28c94-121">A message session keeps track of all **IMessage**-on- **IStorage** objects opened during the duration of the session, in addition to all the attachments and other properties of the messages.</span></span> <span data-ttu-id="28c94-122">クライアントまたはプロバイダーが**CloseIMsgSession**を呼び出すと、これらのすべてのオブジェクトが閉じられます。</span><span class="sxs-lookup"><span data-stu-id="28c94-122">When a client or provider calls **CloseIMsgSession**, it closes all these objects.</span></span> <span data-ttu-id="28c94-123">**CloseIMsgSession**の呼び出しは、 **IMessage**で、 **IStorage**オブジェクトを閉じる唯一の方法です。</span><span class="sxs-lookup"><span data-stu-id="28c94-123">Calling **CloseIMsgSession** is the only way to close **IMessage**-on- **IStorage** objects.</span></span> 
  

