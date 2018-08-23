---
title: MAPI トランスポート プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b193e819-749e-4642-8afc-dbc47b17b617
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 11cd1040bb228d789248a89184572b87cd1688ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801482"
---
# <a name="mapi-transport-provider-overview"></a><span data-ttu-id="bb7fc-103">MAPI トランスポート プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="bb7fc-103">MAPI Transport Provider Overview</span></span>

  
  
<span data-ttu-id="bb7fc-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb7fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb7fc-105">トランスポート プロバイダーは、メッセージの送受信を処理し、必要な場合にセキュリティを実装します。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-105">Transport providers handle message transmission and reception and implement security, if necessary.</span></span> <span data-ttu-id="bb7fc-106">注意の必要な前処理および後処理のタスクです。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-106">They also take care of any necessary preprocessing and postprocessing tasks.</span></span> <span data-ttu-id="bb7fc-107">すべてのアクティブなメッセージング システムの通常の 1 つのトランスポート プロバイダーがあります。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-107">There is typically one transport provider for every active messaging system.</span></span>
  
<span data-ttu-id="bb7fc-108">クライアント アプリケーションは、メッセージ ストア プロバイダーを通じてトランスポート プロバイダーと通信します。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-108">Client applications communicate with the transport provider through a message store provider.</span></span> 
  
<span data-ttu-id="bb7fc-109">受信者のエントリの 1 つまたは複数の特定の種類を処理するために MAPI トランスポート プロバイダーに登録します。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-109">Transport providers register with MAPI to handle one or more particular types of recipient entries.</span></span> <span data-ttu-id="bb7fc-110">メッセージを送信する準備ができたら、MAPI がトランスポート プロバイダーは、伝送を処理する必要がありますを決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-110">When a message is ready to be sent, MAPI must determine which transport provider should handle the transmission.</span></span> <span data-ttu-id="bb7fc-111">、受信者の種類によって MAPI でも複数のトランスポート プロバイダーによって呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-111">Depending on the type of recipient, MAPI can even call upon more than one transport provider.</span></span> <span data-ttu-id="bb7fc-112">使用不可のトランスポートプロバイダーが受信者を処理できる 1 つだけの場合は、そのプロバイダーとの接続を再確立することになるまでメッセージの送信が延期されます。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-112">If an unavailable transport provider is the only one that can handle the recipient, the message transmission will be postponed until a connection with that provider can be reestablished.</span></span>
  
<span data-ttu-id="bb7fc-113">いくつかのメッセージング システムは、セキュリティで保護されたシステムです。すべての潜在的なユーザーがアクセスを許可する前に、有効な資格情報のセットを入力する必要です。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-113">Some messaging systems are secure systems; all potential users are required to enter a set of valid credentials before access is permitted.</span></span> <span data-ttu-id="bb7fc-114">MAPI は、トランスポート プロバイダーは、ログオン時に資格情報を検証することによってこのようなセキュリティで保護されたメッセージング システムへの不正アクセスを防止できます。</span><span class="sxs-lookup"><span data-stu-id="bb7fc-114">MAPI prevents unauthorized access to such secure messaging systems by having the transport provider validate credentials at logon time.</span></span> 
  

