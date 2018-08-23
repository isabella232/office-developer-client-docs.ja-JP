---
title: OSC と Outlook およびソーシャル ネットワークとの関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook ソーシャル コネクタ (OSC) は、同僚、友人、またはすべてのユーザーに関連付けられている場合の Office の連絡先カードおよび Outlook 人物情報ウィンドウのアクティビティ、状態、または写真の更新プログラムで表示できます。
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804462"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a><span data-ttu-id="92697-103">OSC と Outlook およびソーシャル ネットワークとの関連付け</span><span class="sxs-lookup"><span data-stu-id="92697-103">Relating the OSC with Outlook and social networks</span></span>

<span data-ttu-id="92697-104">Outlook ソーシャル コネクタ (OSC) は、同僚、友人、またはすべてのユーザーに関連付けられている場合の Office の連絡先カードおよび Outlook 人物情報ウィンドウのアクティビティ、状態、または写真の更新プログラムで表示できます。</span><span class="sxs-lookup"><span data-stu-id="92697-104">The Outlook Social Connector (OSC) can display in the Office Contact Card and Outlook People Pane activities, status, or photo updates for a coworker, friend, or any person you are associated with.</span></span> <span data-ttu-id="92697-105">既定では、OSC が Outlook の電子メールの添付ファイルを表示し、選択したユーザーから受信した会議出席依頼します。</span><span class="sxs-lookup"><span data-stu-id="92697-105">By default, the OSC displays the Outlook emails, attachments, and meeting requests received from a selected person.</span></span> <span data-ttu-id="92697-106">選択したユーザーと Office ユーザーは、SharePoint サイトの共同作業する場合、OSC も、ドキュメントの更新とその SharePoint サイトから他のサイトのアクティビティが表示されます。</span><span class="sxs-lookup"><span data-stu-id="92697-106">If the selected person and the Office user collaborate on a SharePoint site, the OSC also displays document updates and other site activities from that SharePoint site.</span></span> <span data-ttu-id="92697-107">Office ユーザーが基幹業務アプリケーション、企業の内部の web サイトまたは LinkedIn などの本格的なソーシャル ネットワーク サイトのさまざまな OSC プロバイダーのインストール時に、Office ユーザーに興味を示している関連のコンテキストに応じてFacebook、および Windows Live をします。</span><span class="sxs-lookup"><span data-stu-id="92697-107">Depending on the contexts of association that the Office user is interested in, the Office user can install OSC providers for line-of-business applications, internal corporate websites, or a variety of professional and social network sites, such as LinkedIn, Facebook, and Windows Live.</span></span>
  
<span data-ttu-id="92697-108">Office クライアント アプリケーション間での機能の共有をサポートする OSC の中核となるエンジンは、Office の共有コンポーネントの一部として実装し、人物情報ウィンドウは、Outlook のアドインとして実装されます。</span><span class="sxs-lookup"><span data-stu-id="92697-108">To support sharing of functionality across Office client applications, the OSC core engine is implemented as part of an Office shared component, and the People Pane is implemented as an Outlook add-in.</span></span> <span data-ttu-id="92697-109">OSC を使用するには、Office ユーザーは、クライアント コンピューターに Outlook がインストールされているし、OSC は、連絡先フォルダーに連絡先をキャッシュできるように、プロファイルを使用して Outlook を構成します。</span><span class="sxs-lookup"><span data-stu-id="92697-109">To use the OSC, an Office user must have installed Outlook on that client computer and configured Outlook with a profile, so that the OSC can cache contacts in a Contacts folder.</span></span> 
  
<span data-ttu-id="92697-110">OSC プロバイダーでは、コンポーネント オブジェクト モデル (COM) DLL の各ソーシャル ネットワークの Api に依存しない方法でデータをソーシャル ネットワークにアクセスする OSC を可能にします。</span><span class="sxs-lookup"><span data-stu-id="92697-110">An OSC provider is a Component Object Model (COM) DLL that allows the OSC to access social network data in a way that is independent of the APIs of each social network.</span></span> <span data-ttu-id="92697-111">OSC プロバイダー DLL は、クライアント コンピューターにローカルにインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="92697-111">An OSC provider DLL must be installed locally on a client computer.</span></span> <span data-ttu-id="92697-112">ソーシャル ネットワークの OSC プロバイダーは、インターネット上のソーシャル ネットワークでの OSC は、Outlook の一部を接続します。</span><span class="sxs-lookup"><span data-stu-id="92697-112">A social network's OSC provider connects the OSC, which is part of Outlook, with the social network on the Internet.</span></span>
  
<span data-ttu-id="92697-113">OSC プロバイダーは、OSC と通信するのには、OSC のプロバイダーの機能拡張の一部として定義されているインターフェイスのセットを実装しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="92697-113">An OSC provider must implement a set of interfaces, defined as part of the OSC provider extensibility, to communicate with the OSC.</span></span> <span data-ttu-id="92697-114">OSC プロバイダーの拡張機能は、オープン ・ プラットフォームとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="92697-114">OSC provider extensibility is available as an open platform.</span></span>
  
<span data-ttu-id="92697-115">OSC のプロバイダーのアーキテクチャは、OSC の中核となるエンジンと友人や活動などの集計のソーシャル情報を処理する複数のプロバイダーを有効にします。</span><span class="sxs-lookup"><span data-stu-id="92697-115">The provider architecture of the OSC enables multiple providers to work with the OSC core engine and aggregate social information such as friends and activities.</span></span> <span data-ttu-id="92697-116">OSC プロバイダーのアーキテクチャを図 1 に示します。</span><span class="sxs-lookup"><span data-stu-id="92697-116">Figure 1 illustrates the OSC provider architecture.</span></span>
  
<span data-ttu-id="92697-117">**図 1 です。Outlook ソーシャル コネクタ プロバイダー アーキテクチャ**</span><span class="sxs-lookup"><span data-stu-id="92697-117">**Figure 1. Outlook Social Connector provider architecture**</span></span>

![ソーシャル ネットワーク、OSC プロバイダー、OSC、Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a><span data-ttu-id="92697-119">用語集</span><span class="sxs-lookup"><span data-stu-id="92697-119">Terminology</span></span>

<span data-ttu-id="92697-120">この Outlook ソーシャル コネクタ プロバイダー リファレンスで、ソーシャル ネットワークを使用して、次の種類のサイトを参照してください。</span><span class="sxs-lookup"><span data-stu-id="92697-120">In this Outlook Social Connector Provider Reference, a social network is used to refer to the following types of sites:</span></span> 
  
- <span data-ttu-id="92697-121">SharePoint などのコラボレーション サイトです。</span><span class="sxs-lookup"><span data-stu-id="92697-121">Collaborative sites such as SharePoint.</span></span>
    
- <span data-ttu-id="92697-122">Facebook や Windows Live などのソーシャル ネットワーク サイトです。</span><span class="sxs-lookup"><span data-stu-id="92697-122">Social network sites such as Facebook and Windows Live.</span></span>
    
- <span data-ttu-id="92697-123">LinkedIn などのプロのネットワーク サイトです。</span><span class="sxs-lookup"><span data-stu-id="92697-123">Professional network sites such as LinkedIn.</span></span>
    
- <span data-ttu-id="92697-124">他の基幹業務アプリケーションや企業の内部 web サイトがネットワークで利用できます。</span><span class="sxs-lookup"><span data-stu-id="92697-124">Other line-of-business applications or corporate internal websites used for networking.</span></span>
    
<span data-ttu-id="92697-125">用語の友人は、友人、家族、仕事仲間、接続、および他のユーザーが、Office ユーザーは、SharePoint のような共同作業のコンテキストに関連付けられてまたは、ユーザーのソーシャル ネットワークのアカウントに追加するのには一般的に使用されます。</span><span class="sxs-lookup"><span data-stu-id="92697-125">The term friend is used generally to include friends, family, colleagues, connections, and anyone else an Office user is associated with in a collaborative context like SharePoint, or has added to the user's social network account.</span></span> <span data-ttu-id="92697-126">非友人は、友人のアクティビティの更新プログラムで参照されているユーザーが Office ユーザーのソーシャル ネットワークのアカウントに追加されている友人。</span><span class="sxs-lookup"><span data-stu-id="92697-126">Non-friends are people referenced in friends' activity updates but are not friends who have been added to the Office user's social network account.</span></span> <span data-ttu-id="92697-127">連絡先は、Outlook の連絡先フォルダー内のユーザーです。</span><span class="sxs-lookup"><span data-stu-id="92697-127">Contacts are people in an Outlook contact folder.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92697-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="92697-128">See also</span></span>

- [<span data-ttu-id="92697-129">Outlook Social Connector プロバイダーの開発の概要 (英語)(機械翻訳)</span><span class="sxs-lookup"><span data-stu-id="92697-129">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

