---
title: MAPI プログラミングの概要
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408342"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="41d8b-103">MAPI プログラミングの概要</span><span class="sxs-lookup"><span data-stu-id="41d8b-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="41d8b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="41d8b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="41d8b-105">この Microsoft Outlook Messaging API (MAPI) リファレンスは、C および C++ 開発者がさまざまなニーズに対応し、メッセージングを利用するために作成されています。</span><span class="sxs-lookup"><span data-stu-id="41d8b-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="41d8b-106">MAPI を使用してメッセージング機能を備えたアプリケーションを拡張する開発者にとって、特定の前提条件となる知識は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="41d8b-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="41d8b-107">メッセージングおよびコンポーネントオブジェクトモデル (COM) を使用して MAPI を使用し、専用のメッセージングシステムサービスに対してフルスケールのワークグループアプリケーションまたはドライバーを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41d8b-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="41d8b-108">開発作業を開始する前に、MAPI の使用方法、ログオンプロセス、プロファイルとメッセージサービスの作成および構成方法に関する以下の情報を考慮する必要があります。</span><span class="sxs-lookup"><span data-stu-id="41d8b-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="41d8b-109">メッセージングアプリケーションプログラムインターフェイス (MAPI) は、開発者がメールが有効なアプリケーションを作成するために使用できる豊富な機能セットです。</span><span class="sxs-lookup"><span data-stu-id="41d8b-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="41d8b-110">完全な関数ライブラリは MAPI と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="41d8b-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="41d8b-111">MAPI を使用すると、クライアントコンピューター上のメッセージングシステムを完全に制御し、メッセージの作成と管理、クライアントメールボックスの管理、サービスプロバイダーなどを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="41d8b-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="41d8b-112">拡張 mapi は mapi と同じであり、mapi ドキュメントでは単に mapi と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="41d8b-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="41d8b-113">**簡易 MAPI**</span><span class="sxs-lookup"><span data-stu-id="41d8b-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="41d8b-114">簡易 MAPI には、Microsoft Windows ベースのアプリケーションに対して、基本的なレベルのメッセージング機能を追加できるようにする一連の関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="41d8b-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="41d8b-115">簡易 MAPI 関数 MAPISendMail は、microsoft outlook 2013 および microsoft outlook 2010 でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="41d8b-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="41d8b-116">Windows では、他の簡単な MAPI 機能は廃止されました。</span><span class="sxs-lookup"><span data-stu-id="41d8b-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

