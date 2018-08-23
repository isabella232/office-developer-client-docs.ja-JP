---
title: トランスポート プロバイダーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 60b3e5f4-4a9b-432f-bad4-4284225ab93f
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 00ae0f4be9818e0e9e4562784b4d5bf44eefe308
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567952"
---
# <a name="handling-a-transport-provider"></a><span data-ttu-id="81713-103">トランスポート プロバイダーの処理</span><span class="sxs-lookup"><span data-stu-id="81713-103">Handling a transport provider</span></span>
  
<span data-ttu-id="81713-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81713-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81713-105">クライアントは、MAPI スプーラーとトランスポート プロバイダーによって提供される状態オブジェクトを介してトランスポート プロバイダーと通信します。</span><span class="sxs-lookup"><span data-stu-id="81713-105">Clients communicate with transport providers through status objects supplied by transport providers and the MAPI spooler.</span></span> <span data-ttu-id="81713-106">クライアントは、状態テーブルを取得するために[IMAPISession::GetStatusTable](imapisession-getstatustable.md)を呼び出すことによって状態オブジェクトをアクセスします。</span><span class="sxs-lookup"><span data-stu-id="81713-106">Clients access status objects by calling [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to retrieve the status table.</span></span> <span data-ttu-id="81713-107">ステータス オブジェクトの実装、 [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースのプロバイダーを構成する、フラッシュの受信および送信メッセージのキュー、パスワードの設定、および状態の検証の方法があります。</span><span class="sxs-lookup"><span data-stu-id="81713-107">Status objects implement the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface, which has methods for configuring providers, flushing incoming and outgoing message queues, setting passwords, and state validation.</span></span> <span data-ttu-id="81713-108">ステータス オブジェクトの詳細については、[状態テーブルおよび状態オブジェクト](status-table-and-status-objects.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="81713-108">For more information about status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>


- <span data-ttu-id="81713-109">[要求時にメッセージを送受信する](sending-or-receiving-a-message-on-demand.md): オン ・ デマンドでメッセージを送受信する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81713-109">[Sending or Receiving a Message on Demand](sending-or-receiving-a-message-on-demand.md): Describes how to send or receive a message on demand.</span></span>
    
- <span data-ttu-id="81713-110">[トランスポート オーダを設定](setting-transport-order.md): トランスポートの順番を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81713-110">[Setting Transport Order](setting-transport-order.md): Describes how to set transport order.</span></span>
    
- <span data-ttu-id="81713-111">[トランスポート プロバイダーを再設定](reconfiguring-a-transport-provider.md): トランスポート プロバイダーを再設定する方法とはどのようなプロパティを設定するのには使用方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="81713-111">[Reconfiguring a Transport Provider](reconfiguring-a-transport-provider.md): Describes how to reconfigure a transport provider and what properties are available to set.</span></span>
    

