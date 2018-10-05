---
title: Outlook Social Connector プロバイダーのリファレンス
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook の社会的コネクタ 2013 では、個人と専門的な通信の通信ハブを提供します。
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396701"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="1b8fa-103">Outlook Social Connector プロバイダーのリファレンス</span><span class="sxs-lookup"><span data-stu-id="1b8fa-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="1b8fa-104">Outlook の社会的コネクタ 2013 では、個人と専門的な通信の通信ハブを提供します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="1b8fa-105">SharePoint Server、SharePoint ワークスペースでは、Lync クライアントで動作する Outlook ソーシャル コネクタ (OSC) とプレゼンス情報および連絡先カードをサポートするすべての Office クライアント アプリケーションは、OSC をサポートします。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="1b8fa-106">Outlook で特定の電子メールなどの Outlook アイテムを選択すると、会議出席依頼や送信者または受信者に Outlook を終了せず、そのアイテムをクリックするだけで、表示する人物情報ウィンドウの活動、写真、およびその人のステータスの更新の上、お気に入りのソーシャル ネットワークです。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="1b8fa-107">ユーザーは、すべての Outlook 電子メール、添付ファイル、およびその相手から受信した会議に簡単を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="1b8fa-108">組織の環境では、SharePoint サイト上のユーザーが人物情報ウィンドウの [ドキュメントの更新やその他の SharePoint サイトでこの人のサイトのアクティビティの表示もできます。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="1b8fa-109">ソーシャル ネットワークでは、同期し、ソーシャル ネットワークの更新プログラムのサポート サーバーとアプリケーションでのサーフェスに OSC のプロバイダーを開発できます。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="1b8fa-110">LinkedIn、Facebook では、Windows Live などの一般的なソーシャル ネットワークには、OSC のプロバイダーが提供しています。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="1b8fa-111">Outlook ソーシャル コネクタ 2013 プロバイダー リファレンスでは、OSC プロバイダーの拡張機能を使用して、OSC プロバイダーを開発する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="1b8fa-112">Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="1b8fa-113">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="1b8fa-113">In this section</span></span>

- <span data-ttu-id="1b8fa-114">[Outlook ソーシャル コネクタ プロバイダーの開発の概要](getting-started-with-developing-an-outlook-social-connector-provider.md): の OSC は、以下の概要を示します: OSC プロバイダーは、指定できますが、便利な方法、技術的な要件は、プロバイダーを開発する学習のためのクイック操作のベスト プラクティス、プロバイダーは、このリリースの新機能を開発しています。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="1b8fa-115">[OSC サンプル テンプレート](osc-sample-templates.md): プロバイダーを開発するためのいくつかの Visual Studio のテンプレートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="1b8fa-116">[OSC 典型的な呼び出しシーケンス](osc-typical-calling-sequences.md): OSC プロバイダーの機能拡張インターフェイスのメンバーの OSC によって、いくつかの典型的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="1b8fa-117">これらのインタ フェースを実装する方法を理解するようにします。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="1b8fa-118">[OSC の XML スキーマを使用してプロバイダーの開発](developing-a-provider-with-the-osc-xml-schema.md): OSC プロバイダーをサポートするために、OSC プロバイダーの機能拡張インターフェイスと OSC の XML スキーマを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="1b8fa-119">[プロバイダーをデバッグする](debugging-a-provider.md): OSC プロバイダーをデバッグする際に、いくつかの方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="1b8fa-120">[プロバイダーを展開する](deploying-a-provider.md): OSC プロバイダーでは、登録の要件を説明し、プロバイダーをインストールするためのチェックリストを提供します。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="1b8fa-121">[取得する準備ができて OSC プロバイダーを解放する](getting-ready-to-release-an-osc-provider.md): テストは、OSC プロバイダーを解放する前に行うことができますをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="1b8fa-122">[Outlook ソーシャル コネクタ プロバイダーの参照](outlook-social-connector-provider-reference-0.md): 参照は、OSC プロバイダーの機能拡張インターフェイスと OSC の XML スキーマ、および可能性のあるエラー コードの一覧の情報です。</span><span class="sxs-lookup"><span data-stu-id="1b8fa-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1b8fa-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="1b8fa-123">See also</span></span>

- [<span data-ttu-id="1b8fa-124">Outlook ソーシャル コネクタ 2013 プロバイダー リファレンスの著作権情報</span><span class="sxs-lookup"><span data-stu-id="1b8fa-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="1b8fa-125">ドキュメントの表記規則</span><span class="sxs-lookup"><span data-stu-id="1b8fa-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="1b8fa-126">マイクロソフト製品のアクセシビリティ機能</span><span class="sxs-lookup"><span data-stu-id="1b8fa-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- [<span data-ttu-id="1b8fa-127">Microsoft プライバシーに関する声明</span><span class="sxs-lookup"><span data-stu-id="1b8fa-127">Microsoft Online Privacy Notice</span></span>](https://privacy.microsoft.com/en-us/privacystatement)
    

