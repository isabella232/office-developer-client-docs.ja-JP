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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19800432"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="f734e-103">IMAPIAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f734e-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="f734e-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f734e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f734e-105">通知を処理するためのアドバイズ シンク オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="f734e-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="f734e-106">アドバイズ シンク オブジェクトへのポインターは、通知の登録に使用される機構、サービス プロバイダーの**アドバイズ**メソッドへの呼び出しで渡されます。</span><span class="sxs-lookup"><span data-stu-id="f734e-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f734e-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="f734e-107">Header file:</span></span>  <br/> |<span data-ttu-id="f734e-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f734e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="f734e-109">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="f734e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="f734e-110">通知シンク オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f734e-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="f734e-111">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="f734e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="f734e-112">クライアント アプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="f734e-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="f734e-113">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="f734e-113">Called by:</span></span>  <br/> |<span data-ttu-id="f734e-114">サービス プロバイダーおよび MAPI</span><span class="sxs-lookup"><span data-stu-id="f734e-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="f734e-115">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="f734e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f734e-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="f734e-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="f734e-117">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="f734e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="f734e-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="f734e-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f734e-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="f734e-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f734e-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="f734e-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="f734e-121">通知に応答するには、1 つまたは複数のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="f734e-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="f734e-122">実行するタスクは、イベントおよび通知を生成するオブジェクトの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="f734e-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f734e-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="f734e-123">See also</span></span>



[<span data-ttu-id="f734e-124">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f734e-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

