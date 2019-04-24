---
title: OSC と Outlook およびソーシャル ネットワークとの関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: outlook Social Connector (.osc) は、同僚、友人、または関連付けられている個人の Office 連絡先カードと outlook のユーザーウィンドウの活動、状態、または写真の更新を表示することができます。
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329259"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="3f676-103">OSC と Outlook およびソーシャル ネットワークとの関連付け</span><span class="sxs-lookup"><span data-stu-id="3f676-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="3f676-104">outlook Social Connector (.osc) は、同僚、友人、または関連付けられている個人の Office 連絡先カードと outlook のユーザーウィンドウの活動、状態、または写真の更新を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="3f676-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="3f676-105">既定では、このメッセージには、選択したユーザーから受信した Outlook メール、添付ファイル、会議出席依頼が表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f676-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="3f676-106">選択したユーザーと Office ユーザーが sharepoint サイトで共同作業を行うと、その sharepoint サイトからのドキュメント更新やその他のサイトアクティビティも表示されます。</span><span class="sxs-lookup"><span data-stu-id="3f676-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="3f676-107">office ユーザーは、office ユーザーが関心を持っている関連付けのコンテキストに応じて、基幹業務アプリケーション、社内の web サイト、または LinkedIn などのさまざまな professional およびソーシャルネットワークサイトに対して、.osc プロバイダーをインストールすることができます。Facebook、Windows Live。</span><span class="sxs-lookup"><span data-stu-id="3f676-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="3f676-108">office クライアントアプリケーション間での機能の共有をサポートするために、.osc コアエンジンは office 共有コンポーネントの一部として実装され、People ウィンドウは Outlook アドインとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="3f676-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="3f676-109">.osc を使用するには、Office ユーザーがそのクライアントコンピューターに outlook をインストールし、outlook をプロファイルを使用して構成している必要があります。このため、.osc は連絡先フォルダー内の連絡先をキャッシュできます。</span><span class="sxs-lookup"><span data-stu-id="3f676-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="3f676-110">.osc プロバイダーは、コンポーネントオブジェクトモデル (COM) DLL で、各ソーシャルネットワークの api とは無関係に、.osc がソーシャルネットワークデータにアクセスできるようにします。</span><span class="sxs-lookup"><span data-stu-id="3f676-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="3f676-111">.osc プロバイダ DLL は、クライアントコンピューターにローカルにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f676-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="3f676-112">ソーシャルネットワークの .osc プロバイダーは、Outlook の一部である .osc をインターネット上のソーシャルネットワークに接続します。</span><span class="sxs-lookup"><span data-stu-id="3f676-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="3f676-113">.osc プロバイダーは、.osc と通信するために、.osc プロバイダー拡張機能の一部として定義された一連のインターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f676-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="3f676-114">.osc プロバイダ拡張機能は、オープンプラットフォームとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f676-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="3f676-115">.osc のプロバイダアーキテクチャを使用すると、複数のプロバイダーが .osc コアエンジンと、フレンドやアクティビティなどのソーシャル情報を集約して動作するようになります。</span><span class="sxs-lookup"><span data-stu-id="3f676-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="3f676-116">図1は、.osc プロバイダアーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="3f676-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="3f676-117">**図1。Outlook Social Connector プロバイダーのアーキテクチャ**</span><span class="sxs-lookup"><span data-stu-id="3f676-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![ソーシャル ネットワーク、OSC プロバイダー、OSC、Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="3f676-119">用語</span><span class="sxs-lookup"><span data-stu-id="3f676-119">Terminology</span></span>

<span data-ttu-id="3f676-120">この Outlook social Connector プロバイダーリファレンスでは、ソーシャルネットワークを使用して、次の種類のサイトを参照します。</span><span class="sxs-lookup"><span data-stu-id="3f676-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="3f676-121">SharePoint などのコラボレーションサイト。</span><span class="sxs-lookup"><span data-stu-id="3f676-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="3f676-122">Facebook や Windows Live などのソーシャルネットワークサイト。</span><span class="sxs-lookup"><span data-stu-id="3f676-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="3f676-123">LinkedIn などのプロフェッショナルネットワークサイト。</span><span class="sxs-lookup"><span data-stu-id="3f676-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="3f676-124">ネットワークに使用されるその他の基幹業務アプリケーションまたは企業内部 web サイト。</span><span class="sxs-lookup"><span data-stu-id="3f676-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="3f676-125">friend という用語は、一般に、友人、家族、同僚、接続、および Office ユーザーが SharePoint などのコラボレーションコンテキストで関連付けられている場合や、ユーザーのソーシャルネットワークアカウントに追加されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="3f676-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="3f676-126">友人以外のユーザーは、友人のアクティビティの更新で参照されていますが、Office ユーザーのソーシャルネットワークアカウントに追加されている友人ではありません。</span><span class="sxs-lookup"><span data-stu-id="3f676-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="3f676-127">連絡先は、Outlook の連絡先フォルダー内のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="3f676-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f676-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f676-128">See also</span></span>

- [<span data-ttu-id="3f676-129">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="3f676-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

