---
title: MAPI トランスポート プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404576"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="3897b-103">MAPI トランスポート プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="3897b-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="3897b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3897b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3897b-105">トランスポート プロバイダーは、メッセージの送受信を処理し、必要に応じてセキュリティを実装します。</span><span class="sxs-lookup"><span data-stu-id="3897b-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="3897b-106">また、必要な前処理タスクと後処理タスクも処理します。</span><span class="sxs-lookup"><span data-stu-id="3897b-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="3897b-107">通常、アクティブなメッセージング システムごとに 1 つのトランスポート プロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="3897b-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="3897b-108">クライアント アプリケーションは、メッセージ ストア プロバイダーを介してトランスポート プロバイダーと通信します。</span><span class="sxs-lookup"><span data-stu-id="3897b-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="3897b-109">トランスポート プロバイダーは、1 つ以上の特定の種類の受信者エントリを処理するために MAPI に登録します。</span><span class="sxs-lookup"><span data-stu-id="3897b-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="3897b-110">メッセージを送信する準備ができたら、MAPI は送信を処理するトランスポート プロバイダーを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3897b-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="3897b-111">受信者の種類に応じて、MAPI は複数のトランスポート プロバイダーを呼び出す場合があります。</span><span class="sxs-lookup"><span data-stu-id="3897b-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="3897b-112">使用できないトランスポート プロバイダーだけが受信者を処理できる場合、そのプロバイダーとの接続が再確立されるまで、メッセージ送信は延期されます。</span><span class="sxs-lookup"><span data-stu-id="3897b-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="3897b-113">一部のメッセージング システムはセキュリティで保護されたシステムです。すべての潜在的なユーザーは、アクセスが許可される前に、一連の有効な資格情報を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3897b-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="3897b-114">MAPI は、トランスポート プロバイダーがログオン時に資格情報を検証することで、このようなセキュリティで保護されたメッセージング システムへの不正アクセスを防止します。</span><span class="sxs-lookup"><span data-stu-id="3897b-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

