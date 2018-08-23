---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b9244e28337c74487562ec235f246559a49a390d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573804"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="b4699-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4699-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="b4699-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4699-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b4699-105">通知を処理するためのアドバイズ シンク オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="b4699-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="b4699-106">アドバイズ シンク オブジェクトへのポインターは、通知の登録に使用される機構、サービス プロバイダーの**アドバイズ**メソッドへの呼び出しで渡されます。</span><span class="sxs-lookup"><span data-stu-id="b4699-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4699-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="b4699-107">Header file:</span></span>  <br/> |<span data-ttu-id="b4699-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b4699-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="b4699-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="b4699-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="b4699-110">通知シンク オブジェクト</span><span class="sxs-lookup"><span data-stu-id="b4699-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="b4699-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="b4699-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="b4699-112">クライアント アプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="b4699-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="b4699-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="b4699-113">Called by:</span></span>  <br/> |<span data-ttu-id="b4699-114">サービス プロバイダーおよび MAPI</span><span class="sxs-lookup"><span data-stu-id="b4699-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="b4699-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="b4699-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b4699-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="b4699-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="b4699-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="b4699-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="b4699-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="b4699-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b4699-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="b4699-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b4699-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="b4699-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="b4699-121">通知に応答するには、1 つまたは複数のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="b4699-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="b4699-122">実行するタスクは、イベントおよび通知を生成するオブジェクトの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="b4699-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b4699-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="b4699-123">See also</span></span>



[<span data-ttu-id="b4699-124">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="b4699-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

