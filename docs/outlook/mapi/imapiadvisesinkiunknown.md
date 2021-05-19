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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409567"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="3a752-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3a752-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="3a752-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a752-105">通知を処理するためのアアドバイス シンク オブジェクトを実装します。</span><span class="sxs-lookup"><span data-stu-id="3a752-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="3a752-106">アドバイス シンク オブジェクトへのポインターは、サービス プロバイダーの **Advise** メソッド (通知の登録に使用されるメカニズム) への呼び出しで渡されます。</span><span class="sxs-lookup"><span data-stu-id="3a752-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3a752-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3a752-107">Header file:</span></span>  <br/> |<span data-ttu-id="3a752-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3a752-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3a752-109">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="3a752-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="3a752-110">シンク オブジェクトのアドバイス</span><span class="sxs-lookup"><span data-stu-id="3a752-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="3a752-111">実装元:</span><span class="sxs-lookup"><span data-stu-id="3a752-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a752-112">クライアント アプリケーションと MAPI</span><span class="sxs-lookup"><span data-stu-id="3a752-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="3a752-113">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="3a752-113">Called by:</span></span>  <br/> |<span data-ttu-id="3a752-114">サービス プロバイダーと MAPI</span><span class="sxs-lookup"><span data-stu-id="3a752-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="3a752-115">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="3a752-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3a752-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="3a752-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="3a752-117">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="3a752-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="3a752-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="3a752-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3a752-119">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="3a752-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3a752-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="3a752-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="3a752-121">1 つ以上のタスクを実行して通知に応答します。</span><span class="sxs-lookup"><span data-stu-id="3a752-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="3a752-122">実行されるタスクは、イベントの種類と通知を生成するオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="3a752-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3a752-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="3a752-123">See also</span></span>



[<span data-ttu-id="3a752-124">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="3a752-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

