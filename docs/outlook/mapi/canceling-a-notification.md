---
title: 通知の取り消し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: decd5d7d-1f47-47c2-b9c4-be0e652c99dd
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fb0972638fdd062c99040694222724566281024f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326405"
---
# <a name="canceling-a-notification"></a><span data-ttu-id="08ed3-103">通知の取り消し</span><span class="sxs-lookup"><span data-stu-id="08ed3-103">Canceling a Notification</span></span>

  
  
<span data-ttu-id="08ed3-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08ed3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08ed3-105">通知を取り消すには、クライアントがアドバイズソースの**アドバイズ**中止メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="08ed3-105">To cancel a notification, clients call an advise source's **Unadvise** method.</span></span> <span data-ttu-id="08ed3-106">**アドバイズ**中止は、サービスプロバイダーがアドバイズシンクへの参照を解放する原因となるため、重要です。</span><span class="sxs-lookup"><span data-stu-id="08ed3-106">Calling **Unadvise** is important because it causes the service provider to release its reference to your advise sink.</span></span> <span data-ttu-id="08ed3-107">サービスプロバイダーがアドバイズシンクへの参照を保持している限り、アドバイズシンクは引き続き[IMAPIAdviseSink:: onnotify](imapiadvisesink-onnotify.md)呼び出しを受信できます。</span><span class="sxs-lookup"><span data-stu-id="08ed3-107">As long as a service provider maintains a reference to an advise sink, the advise sink can continue to receive [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) calls.</span></span> <span data-ttu-id="08ed3-108">実際には、イベント通知の非同期の性質上、**アドバイズ**に成功した後でもクライアントに通知できます。</span><span class="sxs-lookup"><span data-stu-id="08ed3-108">In fact, because of the asynchronous nature of event notification, clients can be notified even after a successful **Unadvise** call.</span></span> <span data-ttu-id="08ed3-109">クライアントは、いつでも通知の受信を処理できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="08ed3-109">Clients must be able to handle the receipt of notifications at any time.</span></span> 
  
<span data-ttu-id="08ed3-110">サービスプロバイダの実装は異なるため、通知を取り消す**アドバイズ**中止の呼び出しに失敗したクライアントは、プロバイダーがアドバイズシンクへの参照を解放したときに何もすることはできません。</span><span class="sxs-lookup"><span data-stu-id="08ed3-110">Because service provider implementations differ, clients that fail to call **Unadvise** to cancel a notification cannot assume anything about when a provider will release its reference to their advise sink.</span></span> <span data-ttu-id="08ed3-111">一部のサービスプロバイダーは、アドバイズソースをリリースするときに、アドバイズシンクへの参照を解放します。</span><span class="sxs-lookup"><span data-stu-id="08ed3-111">Some service providers release their references to advise sinks when they release their advise sources.</span></span> <span data-ttu-id="08ed3-112">一部のサービスプロバイダーではできません。</span><span class="sxs-lookup"><span data-stu-id="08ed3-112">Some service providers do not.</span></span> <span data-ttu-id="08ed3-113">サービスプロバイダーがアドバイズシンクへの参照を保持している限り、アドバイズシンクは通知を引き続き受け取ることができます。</span><span class="sxs-lookup"><span data-stu-id="08ed3-113">As long as a service provider maintains a reference to an advise sink, that advise sink can continue to receive notifications.</span></span> 
  

