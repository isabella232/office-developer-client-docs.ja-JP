---
title: 通知をキャンセルします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 8cd96dd22daeb98646a62672bd17f7de4d2f7dab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799756"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="a569f-103">通知をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="a569f-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="a569f-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a569f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a569f-105">通知をキャンセルするには、クライアントは、アドバイス、ソースの**Unadvise**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="a569f-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="a569f-106">アドバイズ シンクへの参照を解放するのにはサービス ・ プロバイダーが発生するため、 **Unadvise**を呼び出すことが重要です。</span><span class="sxs-lookup"><span data-stu-id="a569f-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="a569f-107">サービス プロバイダーは、アドバイズ シンクへの参照を管理している限り、アドバイズ シンクは、 [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)呼び出しの受信を続行できます。</span><span class="sxs-lookup"><span data-stu-id="a569f-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="a569f-108">実際には、非同期であるのため、イベントの通知、クライアントが通知成功**Unadvise**の呼び出し後にも。</span><span class="sxs-lookup"><span data-stu-id="a569f-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="a569f-109">クライアントは、いつでも通知の受信を処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a569f-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="a569f-110">サービス プロバイダーの実装が異なるため、通知をキャンセルするのには**Unadvise**の呼び出しに失敗したクライアント何も想定できませんに関するプロバイダーは、アドバイズ シンクへの参照を解放するとき。</span><span class="sxs-lookup"><span data-stu-id="a569f-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="a569f-111">サービス プロバイダーによっては、アドバイズ ソース バッファーが解放されるときにアドバイズ シンクへの参照をリリースします。</span><span class="sxs-lookup"><span data-stu-id="a569f-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="a569f-112">一部のサービス プロバイダーは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a569f-112">Some service providers do not.</span></span> <span data-ttu-id="a569f-113">サービス プロバイダーは、アドバイズ シンクへの参照を管理している限り、そのアドバイズ シンクが通知を受信する続行できます。</span><span class="sxs-lookup"><span data-stu-id="a569f-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

