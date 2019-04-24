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
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350919"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="2d7bc-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2d7bc-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="2d7bc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2d7bc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2d7bc-105">通知を処理するためのアドバイズシンクオブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="2d7bc-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="2d7bc-106">アドバイズシンクオブジェクトへのポインターは、サービスプロバイダーの**アドバイズ**メソッドへの呼び出しで渡されます。通知の登録に使用されるメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="2d7bc-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d7bc-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2d7bc-107">Header file:</span></span>  <br/> |<span data-ttu-id="2d7bc-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2d7bc-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2d7bc-109">公開者:</span><span class="sxs-lookup"><span data-stu-id="2d7bc-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="2d7bc-110">アドバイズシンクオブジェクト</span><span class="sxs-lookup"><span data-stu-id="2d7bc-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="2d7bc-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="2d7bc-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="2d7bc-112">クライアントアプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="2d7bc-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="2d7bc-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="2d7bc-113">Called by:</span></span>  <br/> |<span data-ttu-id="2d7bc-114">サービスプロバイダーと MAPI</span><span class="sxs-lookup"><span data-stu-id="2d7bc-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="2d7bc-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="2d7bc-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2d7bc-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="2d7bc-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="2d7bc-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="2d7bc-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="2d7bc-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="2d7bc-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2d7bc-119">v の順序</span><span class="sxs-lookup"><span data-stu-id="2d7bc-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2d7bc-120">onnotify</span><span class="sxs-lookup"><span data-stu-id="2d7bc-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="2d7bc-121">1つまたは複数のタスクを実行して通知に応答します。</span><span class="sxs-lookup"><span data-stu-id="2d7bc-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="2d7bc-122">実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2d7bc-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2d7bc-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="2d7bc-123">See also</span></span>



[<span data-ttu-id="2d7bc-124">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="2d7bc-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

