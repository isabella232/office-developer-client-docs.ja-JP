---
title: OSC と Outlook およびソーシャル ネットワークとの関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook ソーシャル コネクタ (OSC) は、同僚、友人、または関連付けられているユーザーの Office 連絡先カードと Outlook ユーザー ウィンドウのアクティビティ、状態、または写真の更新プログラムに表示できます。
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428012"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="c5a3f-103">OSC と Outlook およびソーシャル ネットワークとの関連付け</span><span class="sxs-lookup"><span data-stu-id="c5a3f-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="c5a3f-104">Outlook ソーシャル コネクタ (OSC) は、同僚、友人、または関連付けられているユーザーの Office 連絡先カードと Outlook ユーザー ウィンドウのアクティビティ、状態、または写真の更新プログラムに表示できます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="c5a3f-105">既定では、OSC には、選択Outlook受信したメール、添付ファイル、および会議出席依頼のリストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="c5a3f-106">選択したユーザーとユーザー Officeが SharePoint サイトで共同作業を行う場合、OSC は、そのサイトからのドキュメント更新プログラムや他のサイト アクティビティSharePointします。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="c5a3f-107">Office ユーザーが関心を持つ関連付けのコンテキストに応じて、Office ユーザーは、業務アプリケーション、社内 Web サイト、または LinkedIn、Facebook、および Windows Live などのさまざまなプロフェッショナルおよびソーシャル ネットワーク サイト用の OSC プロバイダーをインストールできます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="c5a3f-108">Office クライアント アプリケーション間での機能の共有をサポートするために、OSC コア エンジンは Office 共有コンポーネントの一部として実装され、People Pane は Outlook アドインとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="c5a3f-109">OSC を使用するには、Office ユーザーがクライアント コンピューターに Outlook をインストールし、プロファイルを使用して Outlook を構成し、OSC が連絡先フォルダーに連絡先をキャッシュできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="c5a3f-110">OSC プロバイダーはコンポーネント オブジェクト モデル (COM) DLL で、各ソーシャル ネットワークの API とは独立した方法で OSC がソーシャル ネットワーク データにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="c5a3f-111">OSC プロバイダー DLL をクライアント コンピューターにローカルにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="c5a3f-112">ソーシャル ネットワークの OSC プロバイダーは、インターネット上のソーシャル ネットワークOutlookの一部である OSC を接続します。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="c5a3f-113">OSC プロバイダーは、OSC プロバイダーの機能拡張の一部として定義された一連のインターフェイスを実装して、OSC と通信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="c5a3f-114">OSC プロバイダーの機能拡張は、オープン プラットフォームとして利用できます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="c5a3f-115">OSC のプロバイダー アーキテクチャを使用すると、複数のプロバイダーが OSC コア エンジンを操作し、友人やアクティビティなどのソーシャル情報を集約できます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="c5a3f-116">図 1 は、OSC プロバイダーのアーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="c5a3f-117">**図 1.Outlookソーシャル コネクタ プロバイダーのアーキテクチャ**</span><span class="sxs-lookup"><span data-stu-id="c5a3f-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![ソーシャル ネットワーク、OSC プロバイダー、OSC、Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="c5a3f-119">用語</span><span class="sxs-lookup"><span data-stu-id="c5a3f-119">Terminology</span></span>

<span data-ttu-id="c5a3f-120">このページOutlook、ソーシャル ネットワークを使用して、次の種類のサイトを参照します。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="c5a3f-121">コラボレーション サイト (SharePoint)。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="c5a3f-122">Facebook や Live などのソーシャル ネットワーク Windowsサイト。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="c5a3f-123">Professional LinkedIn などのネットワーク サイトを管理します。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="c5a3f-124">ネットワークに使用されるその他の業務用アプリケーションまたは企業の内部 Web サイト。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="c5a3f-125">フレンドという用語は、通常、友人、家族、同僚、接続、および Office ユーザーが SharePoint などの共同作業コンテキストに関連付けられている、またはユーザーのソーシャル ネットワーク アカウントに追加された他のユーザーを含めるのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="c5a3f-126">フレンド以外のユーザーは、フレンドのアクティビティ更新プログラムで参照されますが、ユーザーのソーシャル ネットワーク アカウントに追加されたOfficeではありません。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="c5a3f-127">連絡先は、連絡先フォルダー内Outlookユーザーです。</span><span class="sxs-lookup"><span data-stu-id="c5a3f-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c5a3f-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="c5a3f-128">See also</span></span>

- [<span data-ttu-id="c5a3f-129">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="c5a3f-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

