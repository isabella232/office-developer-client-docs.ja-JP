---
title: MAPI �v���O���~���O�̊T�v
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 177bd84addb001970e52801fd2cddba3a8d81706
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801414"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="e6118-103">MAPI �v���O���~���O�̊T�v</span><span class="sxs-lookup"><span data-stu-id="e6118-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="e6118-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6118-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6118-105">この Microsoft Outlook メッセージング API (MAPI) の参照は、C に書かれてと、C++ 開発者は、さまざまなニーズし、メッセージが発生します。</span><span class="sxs-lookup"><span data-stu-id="e6118-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="e6118-106">開発者にとって、メッセージング機能を持つアプリケーションを拡張するために MAPI を使用する、特定の前提となる知識は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="e6118-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="e6118-107">メッセージの背景と、コンポーネント オブジェクト モデル (COM) 本格的なワークグループ アプリケーション、または特殊なメッセージング システムのサービス用のドライバーを作成するのには MAPI を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e6118-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="e6118-108">開発作業を開始する前に MAPI を使用する方法に関する次の情報を考慮する必要がありますログオン プロセス、およびプロファイルとメッセージ サービスの作成および構成方法。</span><span class="sxs-lookup"><span data-stu-id="e6118-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="e6118-109">メッセージング アプリケーション プログラム インターフェイス (MAPI) は、メールが有効なアプリケーションを作成する開発者が使用できる関数の拡張セットです。</span><span class="sxs-lookup"><span data-stu-id="e6118-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="e6118-110">フル機能のライブラリは、MAPI と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="e6118-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="e6118-111">MAPI は、クライアント コンピューター、作成およびメッセージの管理、クライアントのメールボックス、サービス ・ プロバイダーなどの管理上のメッセージング システムを完全に制御を有効にします。</span><span class="sxs-lookup"><span data-stu-id="e6118-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e6118-112">拡張 MAPI は MAPI と同じは単と呼ばれるに MAPI MAPI ドキュメントで。</span><span class="sxs-lookup"><span data-stu-id="e6118-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="e6118-113">**簡易 MAPI**</span><span class="sxs-lookup"><span data-stu-id="e6118-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="e6118-114">簡易 MAPI は、Microsoft Windows ベースのアプリケーションに機能をメッセージングの基本的なレベルを追加することを可能にする一連の関数を提供します。</span><span class="sxs-lookup"><span data-stu-id="e6118-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e6118-115">MAPISendMail 簡易 MAPI の関数は、Microsoft Outlook 2013 と Microsoft Outlook 2010 でサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e6118-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="e6118-116">シンプル MAPI の関数は他の Windows になりました。</span><span class="sxs-lookup"><span data-stu-id="e6118-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

