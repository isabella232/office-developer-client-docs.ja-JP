---
title: トランスポートプロバイダーの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a51547e6-8f0e-45f4-a341-3cfa735112c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 53bdba624ba759debba25bae78fb45b0f9d5247e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433158"
---
# <a name="transport-provider-overview"></a><span data-ttu-id="4a1ce-103">トランスポートプロバイダーの概要</span><span class="sxs-lookup"><span data-stu-id="4a1ce-103">Transport Provider Overview</span></span>

  
  
<span data-ttu-id="4a1ce-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4a1ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4a1ce-105">トランスポートプロバイダーは、MAPI サブシステムと1つ以上の基礎となるメッセージングシステムとの間の仲介として機能するダイナミックリンクライブラリ (DLL) です。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-105">A transport provider is a dynamic-link library (DLL) which acts as an intermediary between the MAPI subsystem and one or more underlying messaging systems.</span></span> <span data-ttu-id="4a1ce-106">メッセージングシステムは、メッセージを送受信するための特定のメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-106">A messaging system is some specific mechanism by which messages are sent and received.</span></span> <span data-ttu-id="4a1ce-107">メッセージングシステムの例として、次のようなものがあります。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-107">Some examples of messaging systems are:</span></span>
  
- <span data-ttu-id="4a1ce-108">トランスポートプロバイダーがメッセージを直接書き込む共有ネットワークファイルシステム。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-108">A shared network file system that the transport provider writes messages to directly.</span></span>
    
- <span data-ttu-id="4a1ce-109">トランスポートプロバイダーがメッセージングサーバーに接続するために使用する tcp/ip ネットワークインターフェイス。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-109">A TCP/IP network interface that the transport provider uses to connect to a messaging server.</span></span>
    
- <span data-ttu-id="4a1ce-110">ユーザーが接続するオンラインサービス。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-110">An online service that users connect to.</span></span>
    
- <span data-ttu-id="4a1ce-111">ホストベースのメッセージングまたは office automation システム。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-111">A host-based messaging or office automation system.</span></span>
    
- <span data-ttu-id="4a1ce-112">メッセージングサーバーへのリモートプロシージャ呼び出しのセット。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-112">A set of remote procedure calls to a messaging server.</span></span>
    
- <span data-ttu-id="4a1ce-113">あるコンピューターから別のコンピューターにデータを転送するために使用できるすべてのもの。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-113">Anything that can be used to transfer data from one computer to another.</span></span>
    
<span data-ttu-id="4a1ce-114">トランスポートプロバイダー DLL は、MAPI で指定されているインターフェイスに準拠している必要があります。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-114">A transport provider DLL must conform to the interface specified by MAPI.</span></span> <span data-ttu-id="4a1ce-115">トランスポートプロバイダーの開発者は、メッセージングシステムに存在する機能の観点から、このインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="4a1ce-115">As a transport provider developer, you will implement this interface in terms of the functionality present in the messaging system.</span></span>
  

