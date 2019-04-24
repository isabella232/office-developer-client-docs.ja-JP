---
title: MAPI トランスポートプロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 20b03f7c52ec86d1fb554bf69c53947c3dda4f36
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357345"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="efb75-103">MAPI トランスポートプロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="efb75-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="efb75-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="efb75-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="efb75-105">トランスポートプロバイダーは、必要に応じて、メッセージの転送と受信を処理し、セキュリティを実装します。</span><span class="sxs-lookup"><span data-stu-id="efb75-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="efb75-106">また、必要なプリプロセスおよび後処理タスクを処理します。</span><span class="sxs-lookup"><span data-stu-id="efb75-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="efb75-107">通常、アクティブなメッセージングシステムごとに1つのトランスポートプロバイダーが存在します。</span><span class="sxs-lookup"><span data-stu-id="efb75-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="efb75-108">クライアントアプリケーションは、メッセージストアプロバイダーを経由してトランスポートプロバイダーと通信します。</span><span class="sxs-lookup"><span data-stu-id="efb75-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="efb75-109">トランスポートプロバイダーは、1つ以上の特定の種類の受信者エントリを処理するために MAPI で登録します。</span><span class="sxs-lookup"><span data-stu-id="efb75-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="efb75-110">メッセージを送信する準備ができたら、MAPI は転送を処理する必要があるトランスポートプロバイダーを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efb75-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="efb75-111">受信者の種類に応じて、MAPI は複数のトランスポートプロバイダーで呼び出しを行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="efb75-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="efb75-112">受信者を処理できるトランスポートプロバイダーが利用できない場合は、そのプロバイダーとの接続が再確立されるまで、メッセージの転送が延期されます。</span><span class="sxs-lookup"><span data-stu-id="efb75-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="efb75-113">一部のメッセージングシステムは、セキュリティで保護されたシステムです。アクセスが許可される前に、すべての可能性のあるユーザーに対して有効な資格情報のセットを入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="efb75-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="efb75-114">MAPI は、ログイン時にトランスポートプロバイダーが資格情報を検証することによって、このようなセキュリティで保護されたメッセージングシステムへの権限のないアクセスを防ぎます。</span><span class="sxs-lookup"><span data-stu-id="efb75-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

