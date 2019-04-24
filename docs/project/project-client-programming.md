---
title: Project クライアントのプログラミング
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- vba、project オブジェクトモデル、プロジェクト、プログラミング、プログラミング、プロジェクト VBA、Visual Basic for applications、project オブジェクトモデル、VBA、オブジェクトモデル、VBA、Visual basic for applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: project 2013 デスクトップクライアントアプリケーション (project Standard 2013 および project Professional 2013) は、VBA を使用してマクロを作成することでカスタマイズおよび拡張することができます。 Visual Studio 2012 を使用して、リボンユーザーインターフェイスをカスタマイズしたり、複雑なアドインを作成したりできます。 office アドインでは、共通の office 2013 プラットフォーム上に構築されたプロジェクト内の作業ウィンドウの新しい拡張モデルが有効になります。 project Standard 2013 および project Professional 2013 は、一般的な Office アドインを実行し、project 用に特に開発された作業ウィンドウアドインを使用して SharePoint、他の web アプリケーション、および外部データと統合することができます。
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301513"
---
# <a name="project-client-programming"></a><span data-ttu-id="946a4-106">Project クライアントのプログラミング</span><span class="sxs-lookup"><span data-stu-id="946a4-106">Project client programming</span></span>

<span data-ttu-id="946a4-107">project 2013 デスクトップクライアントアプリケーション (project Standard 2013 および project Professional 2013) は、VBA を使用してマクロを作成することでカスタマイズおよび拡張することができます。</span><span class="sxs-lookup"><span data-stu-id="946a4-107">The Project 2013 desktop client applications—Project Standard 2013 and Project Professional 2013—can be customized and extended by using VBA to write macros.</span></span> <span data-ttu-id="946a4-108">Visual Studio 2012 を使用して、リボンユーザーインターフェイスをカスタマイズしたり、複雑なアドインを作成したりできます。 office アドインでは、共通の office 2013 プラットフォーム上に構築されたプロジェクト内の作業ウィンドウの新しい拡張モデルが有効になります。</span><span class="sxs-lookup"><span data-stu-id="946a4-108">You can use Visual Studio 2012 to customize the ribbon user interface and create complex add-ins. Office Add-ins enables a new extensibility model for task panes in Project that are built on a common Office 2013 platform.</span></span> <span data-ttu-id="946a4-109">project Standard 2013 および project Professional 2013 は、一般的な Office アドインを実行し、project 用に特に開発された作業ウィンドウアドインを使用して SharePoint、他の web アプリケーション、および外部データと統合することができます。</span><span class="sxs-lookup"><span data-stu-id="946a4-109">Project Standard 2013 and Project Professional 2013 can run general Office Add-ins and use task pane add-ins that are developed specifically for Project to integrate with SharePoint, other websites and web applications, and external data.</span></span>
  
 <span data-ttu-id="946a4-110">**Visual Studio への移行**VBA は、マクロを記録し、比較的単純な自動化ソリューションを開発するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="946a4-110">**Moving to Visual Studio** VBA is useful for recording macros and developing relatively simple automation solutions.</span></span> <span data-ttu-id="946a4-111">作業ウィンドウアドイン、アドイン、およびより複雑で安全でスケーラブルなソリューションを開発するには、Visual Studio 2012 を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="946a4-111">To develop task pane add-ins, add-ins, and more complex, secure, scalable, and easily deployed solutions, we recommend that you use Visual Studio 2012.</span></span> <span data-ttu-id="946a4-112">Microsoft .net Framework 4.0 および project 2013 プライマリ相互運用機能アセンブリは、project 2013 デスクトップクライアントを自動化および統合するソリューションを開発および展開するための多くの利点を提供します。</span><span class="sxs-lookup"><span data-stu-id="946a4-112">The Microsoft .NET Framework 4.0 and the Project 2013 primary interop assembly provide many advantages for developing and deploying solutions that automate and integrate the Project 2013 desktop clients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="946a4-113">Visual Studio 2010 を使用して、プロジェクトアドインを開発できます。ただし、Visual Studio 2012 には、Office アドインクライアントを作成するために設計されたテンプレートと拡張機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="946a4-113">You can use Visual Studio 2010 to develop Project add-ins. However, Visual Studio 2012 includes templates and extensions that are designed to create Office Add-ins clients.</span></span> 
  
<span data-ttu-id="946a4-114">project 2013 の**msproject**オブジェクトモデルは、office Developer Tools for Visual Studio 2013 (VSTO とも呼ばれます) を使用したマネージコードソリューションのための、基本的には、「 **Microsoft office**と同じ」の msproject オブジェクトモデルです。</span><span class="sxs-lookup"><span data-stu-id="946a4-114">The **MSProject** object model for VBA in Project 2013 is essentially the same as the **Microsoft.Office.Interop.MSProject** object model for managed-code solutions with Office Developer Tools for Visual Studio 2013 (also known as VSTO).</span></span> <span data-ttu-id="946a4-115">Visual Studio 2012 には、project 2010 および project 2013 (project Standard または project Professional バージョン) 用のアプリケーションレベルのアドインを開発するためのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="946a4-115">Visual Studio 2012 includes templates for developing application-level add-ins for Project 2010 and for Project 2013 (either the Project Standard or Project Professional versions).</span></span> <span data-ttu-id="946a4-116">VSTO および Office Developer Tools for Visual Studio 2012 は、プロジェクトデスクトップクライアントおよびその他の office 2013 アプリケーションを使用して、SharePoint サイト、リスト、およびを統合できる高度な統合ソリューションの開発、テスト、および展開を簡素化します。ワークフロー.</span><span class="sxs-lookup"><span data-stu-id="946a4-116">VSTO and Office Developer Tools for Visual Studio 2012 simplify developing, testing, and deploying advanced integration solutions that can use the Project desktop client and other Office 2013 applications, and integrate with SharePoint sites, lists, and workflows.</span></span> 
  
<span data-ttu-id="946a4-117">作業ウィンドウアドインと office および SharePoint 用の他のアドインは、office ストアで販売できます (「」 [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)を参照)、Project Online とオンプレミスの両方のインストールで使用できます。</span><span class="sxs-lookup"><span data-stu-id="946a4-117">Task pane add-ins and other add-ins for Office and SharePoint can be sold in the Office Store (see [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)) for use with both Project Online and on-premises installations.</span></span> <span data-ttu-id="946a4-118">VBA マクロと VSTO アドインを Office ストアに配布することはできません。project Standard および project Professional でローカルに使用するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="946a4-118">VBA macros and VSTO add-ins cannot be distributed in the Office Store; they are designed for local use with Project Standard and Project Professional.</span></span> <span data-ttu-id="946a4-119">プロジェクト内で VBA マクロを配布できます。MPP ファイルをコンピューター上の global.mpt ファイルにインストールするか、Project Server 2013 のエンタープライズグローバルテンプレートに配布します。</span><span class="sxs-lookup"><span data-stu-id="946a4-119">You can distribute VBA macros within a project .MPP file, install them in the Global.MPT file on your computer, or distribute them in the enterprise global template in Project Server 2013.</span></span> <span data-ttu-id="946a4-120">VSTO アドインは[ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx)展開により安全に配布できます。これにより、簡単に更新できるようになります。</span><span class="sxs-lookup"><span data-stu-id="946a4-120">VSTO add-ins can be distributed more securely through [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) deployment, which enables easy updates.</span></span> 
  
## <a name="reference"></a><span data-ttu-id="946a4-121">リファレンス</span><span class="sxs-lookup"><span data-stu-id="946a4-121">Reference</span></span>

<span data-ttu-id="946a4-122">[Project VBA 開発者用リファレンス](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx)紹介と VBA のヘルプ記事が含まれています。</span><span class="sxs-lookup"><span data-stu-id="946a4-122">[Project VBA developer reference](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contains introductory and VBA Help articles.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="946a4-123">関連情報</span><span class="sxs-lookup"><span data-stu-id="946a4-123">Related sections</span></span>

<span data-ttu-id="946a4-124">[Project Server 2013 アーキテクチャ](project-server-2013-architecture.md)project クライアントが project Server と対話する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="946a4-124">[Project Server 2013 architecture](project-server-2013-architecture.md) Shows how the Project clients interact with Project Server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="946a4-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="946a4-125">See also</span></span>

- [<span data-ttu-id="946a4-126">開発者向け Project</span><span class="sxs-lookup"><span data-stu-id="946a4-126">Project for developers</span></span>](https://msdn.microsoft.com/office/aa905469)
- [<span data-ttu-id="946a4-127">Office デベロッパーセンター</span><span class="sxs-lookup"><span data-stu-id="946a4-127">Office developer center</span></span>](https://dev.office.com)
- [<span data-ttu-id="946a4-128">Visual Studio デベロッパーセンター</span><span class="sxs-lookup"><span data-stu-id="946a4-128">Visual Studio developer center</span></span>](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [<span data-ttu-id="946a4-129">ClickOnce のセキュリティと展開</span><span class="sxs-lookup"><span data-stu-id="946a4-129">ClickOnce Security and Deployment</span></span>](https://msdn.microsoft.com/library/t71a733d.aspx)
- [<span data-ttu-id="946a4-130">利用可能なフィールド リファレンス</span><span class="sxs-lookup"><span data-stu-id="946a4-130">Available fields reference</span></span>](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

