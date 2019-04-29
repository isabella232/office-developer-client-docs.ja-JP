---
title: 転送プロバイダーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0fe21cea26c956f8a03a51e2f302b040fc89e751
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416539"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="64f78-103">転送プロバイダーの処理</span><span class="sxs-lookup"><span data-stu-id="64f78-103">Handling a transport provider</span></span>
  
<span data-ttu-id="64f78-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64f78-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64f78-105">クライアントは、トランスポートプロバイダーと MAPI スプーラーで提供される状態オブジェクトを通じて、トランスポートプロバイダーと通信します。</span><span class="sxs-lookup"><span data-stu-id="64f78-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="64f78-106">クライアントは、 [imapisession:: getstatustable](imapisession-getstatustable.md)を呼び出してステータスオブジェクトにアクセスし、状態テーブルを取得します。</span><span class="sxs-lookup"><span data-stu-id="64f78-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="64f78-107">Status オブジェクトは、プロバイダーを構成し、受信および送信メッセージキューをフラッシュする、パスワードを設定する、および状態を検証するための[imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイスを実装しています。</span><span class="sxs-lookup"><span data-stu-id="64f78-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="64f78-108">状態オブジェクトの詳細については、「 [status Table and status objects](status-table-and-status-objects.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="64f78-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="64f78-109">[必要に応じてメッセージを送信または受信](sending-or-receiving-a-message-on-demand.md)する: 必要に応じてメッセージを送信または受信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64f78-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="64f78-110">[トランスポートオーダーの設定](setting-transport-order.md): トランスポート順序を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="64f78-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="64f78-111">[トランスポートプロバイダーの再構成](reconfiguring-a-transport-provider.md): トランスポートプロバイダーを再構成する方法と、設定できるプロパティについて説明します。</span><span class="sxs-lookup"><span data-stu-id="64f78-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

