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
ms.openlocfilehash: dbc56b7334d3966696641a84f23a64ce3802e3e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595273"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="e5147-103">トランスポート プロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="e5147-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="e5147-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e5147-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e5147-105">トランスポート プロバイダーは、MAPI のサブシステムと 1 つまたは複数の基になるメッセージング システムとの間の媒介手段として機能するダイナミック リンク ライブラリ (DLL) です。</span><span class="sxs-lookup"><span data-stu-id="e5147-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="e5147-106">メッセージング システムは、メッセージの送信し、受信はいくつか特定のメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="e5147-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="e5147-107">メッセージング システムのいくつかの例は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e5147-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="e5147-108">トランスポート プロバイダーは、直接にメッセージを書き込み共有ネットワーク ・ ファイル ・ システムです。</span><span class="sxs-lookup"><span data-stu-id="e5147-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="e5147-109">トランスポート プロバイダーを使用して、メッセージング サーバーへの接続に TCP/IP ネットワーク インターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="e5147-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="e5147-110">ユーザーに接続するオンライン サービスです。</span><span class="sxs-lookup"><span data-stu-id="e5147-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="e5147-111">ホスト ・ ベースのメッセージや、office オートメーション システム。</span><span class="sxs-lookup"><span data-stu-id="e5147-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="e5147-112">メッセージング サーバーへのリモート プロシージャ呼び出しのセットです。</span><span class="sxs-lookup"><span data-stu-id="e5147-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="e5147-113">1 台のコンピューター間でデータを転送するに使用できるものです。</span><span class="sxs-lookup"><span data-stu-id="e5147-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="e5147-114">トランスポート プロバイダー DLL は、MAPI によって指定されたインターフェイスに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="e5147-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="e5147-115">トランスポート プロバイダー開発者は、メッセージング システム内の機能には、このインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="e5147-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

