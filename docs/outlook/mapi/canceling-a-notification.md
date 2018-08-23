---
title: 通知の取り消し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 50d1fb451cbfcd07f97c5b12a9c86c03a435faa6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564774"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="ff8a7-103">通知の取り消し</span><span class="sxs-lookup"><span data-stu-id="ff8a7-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="ff8a7-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff8a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff8a7-105">通知をキャンセルするには、クライアントは、アドバイス、ソースの**Unadvise**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="ff8a7-106">アドバイズ シンクへの参照を解放するのにはサービス ・ プロバイダーが発生するため、 **Unadvise**を呼び出すことが重要です。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="ff8a7-107">サービス プロバイダーは、アドバイズ シンクへの参照を管理している限り、アドバイズ シンクは、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)呼び出しの受信を続行できます。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="ff8a7-108">実際には、非同期であるのため、イベントの通知、クライアントが通知成功**Unadvise**の呼び出し後にも。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="ff8a7-109">クライアントは、いつでも通知の受信を処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="ff8a7-110">サービス プロバイダーの実装が異なるため、通知をキャンセルするのには**Unadvise**の呼び出しに失敗したクライアント何も想定できませんに関するプロバイダーは、アドバイズ シンクへの参照を解放するとき。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="ff8a7-111">サービス プロバイダーによっては、アドバイズ ソース バッファーが解放されるときにアドバイズ シンクへの参照をリリースします。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="ff8a7-112">一部のサービス プロバイダーは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-112">Some service providers do not.</span></span> <span data-ttu-id="ff8a7-113">サービス プロバイダーは、アドバイズ シンクへの参照を管理している限り、そのアドバイズ シンクが通知を受信する続行できます。</span><span class="sxs-lookup"><span data-stu-id="ff8a7-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

