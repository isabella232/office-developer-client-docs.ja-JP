---
title: トランスポート プロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 22b9da0cfe70cf499cc6f3a699eabe4aaee25b0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804143"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="b03b7-103">トランスポート プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="b03b7-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="b03b7-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b03b7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b03b7-105">トランスポート プロバイダーは、MAPI のサブシステムと 1 つまたは複数の基になるメッセージング システムとの間の媒介手段として機能するダイナミック リンク ライブラリ (DLL) です。</span><span class="sxs-lookup"><span data-stu-id="b03b7-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="b03b7-106">メッセージング システムは、メッセージの送信し、受信はいくつか特定のメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="b03b7-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="b03b7-107">メッセージング システムのいくつかの例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b03b7-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="b03b7-108">トランスポート プロバイダーは、直接にメッセージを書き込み共有ネットワーク ・ ファイル ・ システムです。</span><span class="sxs-lookup"><span data-stu-id="b03b7-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="b03b7-109">トランスポート プロバイダーを使用して、メッセージング サーバーへの接続に TCP/IP ネットワーク インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="b03b7-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="b03b7-110">ユーザーに接続するオンライン サービスです。</span><span class="sxs-lookup"><span data-stu-id="b03b7-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="b03b7-111">ホスト ・ ベースのメッセージや、office オートメーション システム。</span><span class="sxs-lookup"><span data-stu-id="b03b7-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="b03b7-112">メッセージング サーバーへのリモート プロシージャ呼び出しのセットです。</span><span class="sxs-lookup"><span data-stu-id="b03b7-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="b03b7-113">1 台のコンピューター間でデータを転送するに使用できるものです。</span><span class="sxs-lookup"><span data-stu-id="b03b7-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="b03b7-114">トランスポート プロバイダー DLL は、MAPI によって指定されたインターフェイスに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="b03b7-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="b03b7-115">トランスポート プロバイダー開発者は、メッセージング システム内の機能には、このインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="b03b7-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

