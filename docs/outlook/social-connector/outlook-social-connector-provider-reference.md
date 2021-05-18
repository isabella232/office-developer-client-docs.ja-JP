---
title: Outlook Social Connector プロバイダーのリファレンス
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: ソーシャル Outlook 2013 は、個人および専門のコミュニケーションのためのコミュニケーション ハブを提供します。
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359837"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="0fd77-103">Outlook Social Connector プロバイダーのリファレンス</span><span class="sxs-lookup"><span data-stu-id="0fd77-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="0fd77-104">ソーシャル Outlook 2013 は、個人および専門のコミュニケーションのためのコミュニケーション ハブを提供します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="0fd77-105">Outlook ソーシャル コネクタ (OSC) は、SharePoint Server、SharePoint ワークスペース、Lync クライアント、およびプレゼンス情報をサポートするすべての Office クライアント アプリケーションと動作し、連絡先カードは OSC をサポートします。</span><span class="sxs-lookup"><span data-stu-id="0fd77-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="0fd77-106">特に Outlook では、電子メールや会議出席依頼などの Outlook アイテムを選択し、そのアイテムの送信者または受信者をクリックしただけで、Outlook を離れることなく、ユーザーは自分のお気に入りのソーシャル ネットワーク上でこのユーザーのユーザーのアクティビティ、写真、および状態の更新を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0fd77-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="0fd77-107">ユーザーは、このユーザーから受信Outlookメール、添付ファイル、会議のすべての情報を簡単に表示できます。</span><span class="sxs-lookup"><span data-stu-id="0fd77-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="0fd77-108">組織環境では、SharePoint サイト上のユーザーは、ユーザー ウィンドウのドキュメントの更新プログラムや、このユーザーのその他のサイト アクティビティSharePointできます。</span><span class="sxs-lookup"><span data-stu-id="0fd77-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="0fd77-109">ソーシャル ネットワークは、サポート サーバーとアプリケーションでソーシャル ネットワーク更新プログラムを同期および表面化するための OSC のプロバイダーを開発できます。</span><span class="sxs-lookup"><span data-stu-id="0fd77-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="0fd77-110">LinkedIn、Facebook、およびライブなどの人気のあるソーシャル Windows OSC のプロバイダーを提供しています。</span><span class="sxs-lookup"><span data-stu-id="0fd77-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="0fd77-111">ソーシャル Outlook 2013 プロバイダー リファレンスでは、OSC プロバイダーの機能拡張を使用して OSC プロバイダーを開発する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="0fd77-112">Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="0fd77-113">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="0fd77-113">In this section</span></span>

- <span data-ttu-id="0fd77-114">[Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md)の開発の概要 : OSC プロバイダーの役に立つ方法、プロバイダーの開発に関する簡単な手順、技術的要件、プロバイダーを開発するためのベスト プラクティス、このリリースの新機能など、OSC の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="0fd77-115">[OSC サンプル テンプレート](osc-sample-templates.md): プロバイダーを開発するためのVisual Studioテンプレートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="0fd77-116">[OSC の一般的な](osc-typical-calling-sequences.md)呼び出しシーケンス: OSC プロバイダー拡張インターフェイスのメンバーの OSC による一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="0fd77-117">これにより、これらのインターフェイスを実装する方法をよりよく理解できます。</span><span class="sxs-lookup"><span data-stu-id="0fd77-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="0fd77-118">[OSC XML スキーマ](developing-a-provider-with-the-osc-xml-schema.md)を使用してプロバイダーを開発する : OSC プロバイダー拡張インターフェイスと OSC XML スキーマが OSC プロバイダーをサポートするように設計されている方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="0fd77-119">[プロバイダーのデバッグ](debugging-a-provider.md): OSC プロバイダーのデバッグに役立ついくつかの方法を提案します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="0fd77-120">[プロバイダーの展開](deploying-a-provider.md): OSC プロバイダーの登録要件について説明し、プロバイダーをインストールするためのチェックリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="0fd77-121">[OSC プロバイダーをリリースする準備](getting-ready-to-release-an-osc-provider.md): OSC プロバイダーをリリースする前に実行できるテストを提案します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="0fd77-122">[Outlook:OSC](outlook-social-connector-provider-reference-0.md)プロバイダー拡張インターフェイスと OSC XML スキーマの参照情報を提供し、考えられるエラー コードの一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="0fd77-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0fd77-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="0fd77-123">See also</span></span>

- [<span data-ttu-id="0fd77-124">OutlookSocial Connector 2013 プロバイダー参照著作権に関する通知</span><span class="sxs-lookup"><span data-stu-id="0fd77-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="0fd77-125">ドキュメントの表記規則</span><span class="sxs-lookup"><span data-stu-id="0fd77-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="0fd77-126">マイクロソフト製品のアクセシビリティ機能</span><span class="sxs-lookup"><span data-stu-id="0fd77-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- <span data-ttu-id="0fd77-127">[Microsoft �v���C�o�V�[�Ɋւ��鐺��](https://privacy.microsoft.com/en-us/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="0fd77-127">[Microsoft Online Privacy Notice](https://privacy.microsoft.com/en-us/privacystatement)</span></span>
    

