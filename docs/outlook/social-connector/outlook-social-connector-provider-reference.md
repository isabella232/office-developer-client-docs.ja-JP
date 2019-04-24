---
title: Outlook Social Connector プロバイダーのリファレンス
manager: soliver
ms.date: 04/04/2016
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 13661393-adf6-4870-86c4-303262317675
description: Outlook Social Connector 2013 は、個人およびプロフェッショナルコミュニケーションのための通信ハブを提供します。
ms.openlocfilehash: e570fe69cbbe0e8d472e712fb3b8592c97fe43c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359837"
---
# <a name="outlook-social-connector-provider-reference"></a><span data-ttu-id="9ff48-103">Outlook Social Connector プロバイダーのリファレンス</span><span class="sxs-lookup"><span data-stu-id="9ff48-103">Outlook Social Connector provider reference</span></span>

<span data-ttu-id="9ff48-104">Outlook Social Connector 2013 は、個人およびプロフェッショナルコミュニケーションのための通信ハブを提供します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-104">The Outlook Social Connector 2013 provides a communication hub for personal and professional communications.</span></span> <span data-ttu-id="9ff48-105">Outlook Social Connector (.osc) は、sharepoint Server、sharepoint Workspace、Lync クライアント、およびプレゼンス情報をサポートするすべての Office クライアントアプリケーションと連絡先カードが、.osc をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="9ff48-105">The Outlook Social Connector (OSC) works with SharePoint Server, SharePoint Workspace, Lync client, and all Office client applications that support presence information and the Contact Card support the OSC.</span></span> 

<span data-ttu-id="9ff48-106">特に outlook の場合、電子メールや会議出席依頼などの outlook アイテムを選択し、そのアイテムの送信者または受信者をクリックして、outlook を終了せずに、ユーザーは自分の [ユーザー] ウィンドウでこのユーザーのアクティビティ、写真、進捗の更新を閲覧できます。お気に入りのソーシャルネットワーク。</span><span class="sxs-lookup"><span data-stu-id="9ff48-106">In Outlook in particular, just by selecting an Outlook item such as an email or meeting request and clicking the sender or a recipient in that item, without leaving Outlook, users can see in the People Pane activities, photos, and status updates of this person on their favorite social networks.</span></span> <span data-ttu-id="9ff48-107">ユーザーは、このユーザーから受信したすべての Outlook メール、添付ファイル、会議を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="9ff48-107">Users can conveniently see all the Outlook emails, attachments, and meetings received from this person.</span></span> <span data-ttu-id="9ff48-108">組織環境では、sharepoint サイト上のユーザーは、sharepoint サイトでこの人物の [ユーザー] ウィンドウのドキュメントの更新やその他のサイトアクティビティにも表示できます。</span><span class="sxs-lookup"><span data-stu-id="9ff48-108">In an organizational environment, users on a SharePoint site can also see in the People Pane document updates and other site activities of this person on the SharePoint site.</span></span>
  
<span data-ttu-id="9ff48-109">ソーシャルネットワークは、アプリケーションをサポートするためにソーシャルネットワークの更新を同期および表面化するための、.osc のプロバイダーを開発できます。</span><span class="sxs-lookup"><span data-stu-id="9ff48-109">A social network can develop a provider for the OSC to synchronize and surface social network updates in supporting servers and applications.</span></span> <span data-ttu-id="9ff48-110">LinkedIn、Facebook、Windows Live などの一般的なソーシャルネットワークは、.osc のプロバイダーを提供しています。</span><span class="sxs-lookup"><span data-stu-id="9ff48-110">Popular social networks such as LinkedIn, Facebook, and Windows Live are offering providers for the OSC.</span></span> 
  
<span data-ttu-id="9ff48-111">「Outlook Social Connector 2013 プロバイダリファレンス」では、.osc プロバイダ拡張機能を使用して、.osc プロバイダーを開発する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-111">The Outlook Social Connector 2013 Provider Reference describes how to develop an OSC provider using OSC provider extensibility.</span></span> 
  
<span data-ttu-id="9ff48-112">Outlook のソリューションを開発するのが初めての場合は、「[Outlook 用のソリューションを開発するための API またはテクノロジの選択](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md)」を参照し、必要に応じて適切な API とテクノロジを特定します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-112">If you are new to developing solutions for Outlook, see [Selecting an API or technology for developing solutions for Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) to identify the APIs and technologies that are most appropriate for your needs.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="9ff48-113">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="9ff48-113">In this section</span></span>

- <span data-ttu-id="9ff48-114">「 [Outlook Social Connector プロバイダーの開発の](getting-started-with-developing-an-outlook-social-connector-provider.md)概要」では、次のような .osc の概要を説明します。 .osc プロバイダーが役に立つ方法、プロバイダーを開発するための簡単な手順、技術要件、ベストプラクティスについて説明します。プロバイダーの開発とこのリリースの新機能</span><span class="sxs-lookup"><span data-stu-id="9ff48-114">[Getting Started with Developing an Outlook Social Connector Provider](getting-started-with-developing-an-outlook-social-connector-provider.md): Provides an overview of the OSC, including the following: how an OSC provider can be useful, quick steps for learning to develop a provider, technical requirements, best practices for developing a provider, and what's new in this release.</span></span>
    
- <span data-ttu-id="9ff48-115">[.osc サンプルテンプレート](osc-sample-templates.md): プロバイダーを開発するためのいくつかの Visual Studio テンプレートについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-115">[OSC Sample Templates](osc-sample-templates.md): Describes several Visual Studio templates for developing a provider.</span></span>
    
- <span data-ttu-id="9ff48-116">[.osc 一般的な呼び出しシーケンス](osc-typical-calling-sequences.md): .osc プロバイダー機能拡張インターフェイスのメンバーの .osc による、いくつかの一般的な呼び出しシーケンスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-116">[OSC Typical Calling Sequences](osc-typical-calling-sequences.md): Describes a few typical calling sequences by the OSC of members in the OSC provider extensibility interfaces.</span></span> <span data-ttu-id="9ff48-117">これにより、これらのインターフェイスを実装する方法をより深く理解できるようになります。</span><span class="sxs-lookup"><span data-stu-id="9ff48-117">This should enable you to better understand how to implement these interfaces.</span></span>
    
- <span data-ttu-id="9ff48-118">[.osc xml スキーマを使用してプロバイダーを開発](developing-a-provider-with-the-osc-xml-schema.md)する: .osc プロバイダ拡張インターフェイスと、.osc xml スキーマが、.osc プロバイダーをサポートするように設計されていることを説明します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-118">[Developing a Provider with the OSC XML Schema](developing-a-provider-with-the-osc-xml-schema.md): Describes how the OSC provider extensibility interfaces and OSC XML schema are designed to support an OSC provider.</span></span>
    
- <span data-ttu-id="9ff48-119">[プロバイダーのデバッグ](debugging-a-provider.md): .osc プロバイダーのデバッグに役立ついくつかの方法が提案されています。</span><span class="sxs-lookup"><span data-stu-id="9ff48-119">[Debugging a Provider](debugging-a-provider.md): Suggests a few ways to help debug an OSC provider.</span></span>
    
- <span data-ttu-id="9ff48-120">[プロバイダーの展開](deploying-a-provider.md): .osc プロバイダーの登録要件について説明し、プロバイダーをインストールするためのチェックリストを示します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-120">[Deploying a Provider](deploying-a-provider.md): Describes registration requirements for an OSC provider, and provides a checklist for installing a provider.</span></span>
    
- <span data-ttu-id="9ff48-121">[.osc プロバイダーをリリースする準備をする](getting-ready-to-release-an-osc-provider.md): .osc プロバイダーを解放する前に実行できるテストを示します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-121">[Getting Ready to Release an OSC Provider](getting-ready-to-release-an-osc-provider.md): Suggests tests you can do before releasing an OSC provider.</span></span>
    
- <span data-ttu-id="9ff48-122">[Outlook Social Connector プロバイダーリファレンス](outlook-social-connector-provider-reference-0.md): .osc プロバイダ拡張インターフェイスと .osc XML スキーマに関するリファレンス情報を提供し、エラーコードを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="9ff48-122">[Outlook Social Connector Provider Reference](outlook-social-connector-provider-reference-0.md): Provides reference information for the OSC provider extensibility interfaces and OSC XML schema, and lists possible error codes.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9ff48-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="9ff48-123">See also</span></span>

- [<span data-ttu-id="9ff48-124">Outlook Social Connector 2013 プロバイダリファレンスの著作権情報</span><span class="sxs-lookup"><span data-stu-id="9ff48-124">Outlook Social Connector 2013 provider reference copyright notice</span></span>](outlook-social-connector-2013-provider-reference-copyright-notice.md) 
- [<span data-ttu-id="9ff48-125">ドキュメントの表記規則</span><span class="sxs-lookup"><span data-stu-id="9ff48-125">Document Conventions</span></span>](https://msdn.microsoft.com/office/aa905365.aspx)   
- [<span data-ttu-id="9ff48-126">マイクロソフト製品のアクセシビリティ機能</span><span class="sxs-lookup"><span data-stu-id="9ff48-126">Accessibility in Microsoft Products</span></span>](https://www.microsoft.com/enable/products/default.aspx)  
- <span data-ttu-id="9ff48-127">[Microsoft �v���C�o�V�[�Ɋւ��鐺��](https://privacy.microsoft.com/en-us/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="9ff48-127">[Microsoft Online Privacy Notice](https://privacy.microsoft.com/en-us/privacystatement)</span></span>
    

