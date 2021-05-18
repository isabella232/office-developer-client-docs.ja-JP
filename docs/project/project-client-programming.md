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
- vba、プロジェクト オブジェクト モデル、Project、プログラミング性、Project VBA、Visual Basic for Applications、Project オブジェクト モデル、VBA、オブジェクト モデル、VBA、Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Project 2013 デスクトップ クライアント アプリケーション (Project Standard 2013 および Project Professional 2013) は、VBA を使用してマクロを記述することでカスタマイズおよび拡張できます。 2012 Visual Studioを使用して、リボン のユーザー インターフェイスをカスタマイズし、複雑なアドインを作成できます。Officeアドインを使用すると、2013 年の一般的なプラットフォーム上に構築Project作業ウィンドウの新しい機能拡張モデルをOfficeできます。 Project Standard 2013 および Project Professional 2013 では、一般的な Office アドインを実行し、Project 用に特別に開発された作業ウィンドウ アドインを使用して、SharePoint、他の Web サイトや Web アプリケーション、および外部データと統合できます。
ms.openlocfilehash: cc345f0ff91dfb573dd86c256e89df478edd4924
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301513"
---
# <a name="project-client-programming"></a><span data-ttu-id="51dce-106">Project クライアントのプログラミング</span><span class="sxs-lookup"><span data-stu-id="51dce-106">Project client programming</span></span>

<span data-ttu-id="51dce-107">Project 2013 デスクトップ クライアント アプリケーション (Project Standard 2013 および Project Professional 2013) は、VBA を使用してマクロを記述することでカスタマイズおよび拡張できます。</span><span class="sxs-lookup"><span data-stu-id="51dce-107">The Project 2013 desktop client applications—Project Standard 2013 and Project Professional 2013—can be customized and extended by using VBA to write macros.</span></span> <span data-ttu-id="51dce-108">2012 Visual Studioを使用して、リボン のユーザー インターフェイスをカスタマイズし、複雑なアドインを作成できます。Officeアドインを使用すると、2013 年の一般的なプラットフォーム上に構築Project作業ウィンドウの新しい機能拡張モデルをOfficeできます。</span><span class="sxs-lookup"><span data-stu-id="51dce-108">You can use Visual Studio 2012 to customize the ribbon user interface and create complex add-ins. Office Add-ins enables a new extensibility model for task panes in Project that are built on a common Office 2013 platform.</span></span> <span data-ttu-id="51dce-109">Project Standard 2013 および Project Professional 2013 では、一般的な Office アドインを実行し、Project 用に特別に開発された作業ウィンドウ アドインを使用して、SharePoint、他の Web サイトや Web アプリケーション、および外部データと統合できます。</span><span class="sxs-lookup"><span data-stu-id="51dce-109">Project Standard 2013 and Project Professional 2013 can run general Office Add-ins and use task pane add-ins that are developed specifically for Project to integrate with SharePoint, other websites and web applications, and external data.</span></span>
  
 <span data-ttu-id="51dce-110">**ファイルへのVisual Studio** VBA は、マクロを記録し、比較的単純なオートメーション ソリューションを開発する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="51dce-110">**Moving to Visual Studio** VBA is useful for recording macros and developing relatively simple automation solutions.</span></span> <span data-ttu-id="51dce-111">作業ウィンドウ アドイン、アドイン、およびより複雑で安全で拡張性が高く、展開しやすいソリューションを開発するには、Visual Studio 2012 を使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="51dce-111">To develop task pane add-ins, add-ins, and more complex, secure, scalable, and easily deployed solutions, we recommend that you use Visual Studio 2012.</span></span> <span data-ttu-id="51dce-112">Microsoft .NET Framework 4.0 および Project 2013 プライマリ相互運用機能アセンブリは、Project 2013 デスクトップ クライアントを自動化および統合するソリューションの開発と展開に多くの利点を提供します。</span><span class="sxs-lookup"><span data-stu-id="51dce-112">The Microsoft .NET Framework 4.0 and the Project 2013 primary interop assembly provide many advantages for developing and deploying solutions that automate and integrate the Project 2013 desktop clients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="51dce-113">2010 Visual Studioを使用して、Projectを開発できます。ただし、Visual Studio 2012 には、アドイン クライアントを作成するように設計Office拡張機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="51dce-113">You can use Visual Studio 2010 to develop Project add-ins. However, Visual Studio 2012 includes templates and extensions that are designed to create Office Add-ins clients.</span></span> 
  
<span data-ttu-id="51dce-114">2013 年 2013 年の VBA の Project **MSProject** オブジェクト モデルは、基本的に **Microsoft.Office と同じです。Interop.MSProject** オブジェクト モデルは、Office 開発者向けツール (Visual Studio 2013 とも呼ばれる) を使用したマネージ コード ソリューションVSTO。</span><span class="sxs-lookup"><span data-stu-id="51dce-114">The **MSProject** object model for VBA in Project 2013 is essentially the same as the **Microsoft.Office.Interop.MSProject** object model for managed-code solutions with Office Developer Tools for Visual Studio 2013 (also known as VSTO).</span></span> <span data-ttu-id="51dce-115">Visual Studio 2012 には、Project 2010 および Project 2013 (Project Standard バージョンまたは Project Professional バージョン) 用のアプリケーション レベル アドインを開発するためのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="51dce-115">Visual Studio 2012 includes templates for developing application-level add-ins for Project 2010 and for Project 2013 (either the Project Standard or Project Professional versions).</span></span> <span data-ttu-id="51dce-116">VSTO および Office Developer Tools for Visual Studio 2012 は、Project デスクトップ クライアントおよび他の Office 2013 アプリケーションを使用し、SharePoint サイト、リスト、およびワークフローと統合できる高度な統合ソリューションの開発、テスト、展開を簡素化します。</span><span class="sxs-lookup"><span data-stu-id="51dce-116">VSTO and Office Developer Tools for Visual Studio 2012 simplify developing, testing, and deploying advanced integration solutions that can use the Project desktop client and other Office 2013 applications, and integrate with SharePoint sites, lists, and workflows.</span></span> 
  
<span data-ttu-id="51dce-117">Office と SharePoint の作業ウィンドウ アドインおよび他のアドインは、Project Online とオンプレミスの両方のインストールで使用するために、Office ストア (参照) で販売できます。 [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)</span><span class="sxs-lookup"><span data-stu-id="51dce-117">Task pane add-ins and other add-ins for Office and SharePoint can be sold in the Office Store (see [https://office.microsoft.com/store/](https://office.microsoft.com/en-us/store/)) for use with both Project Online and on-premises installations.</span></span> <span data-ttu-id="51dce-118">VBA マクロVSTOアドインは、Office ストアにOfficeできません。これらは、ローカルで使用するために設計され、Project StandardとProject Professional。</span><span class="sxs-lookup"><span data-stu-id="51dce-118">VBA macros and VSTO add-ins cannot be distributed in the Office Store; they are designed for local use with Project Standard and Project Professional.</span></span> <span data-ttu-id="51dce-119">VBA マクロは、プロジェクト内で配布できます。MPP ファイル、コンピューターの Global.MPT ファイルにインストールするか、またはサーバー 2013 のエンタープライズ グローバル テンプレートに配布Projectします。</span><span class="sxs-lookup"><span data-stu-id="51dce-119">You can distribute VBA macros within a project .MPP file, install them in the Global.MPT file on your computer, or distribute them in the enterprise global template in Project Server 2013.</span></span> <span data-ttu-id="51dce-120">VSTO展開を通じて、より安全にアドインを配布ClickOnce更新が[](https://msdn.microsoft.com/library/t71a733d.aspx)容易になります。</span><span class="sxs-lookup"><span data-stu-id="51dce-120">VSTO add-ins can be distributed more securely through [ClickOnce](https://msdn.microsoft.com/library/t71a733d.aspx) deployment, which enables easy updates.</span></span> 
  
## <a name="reference"></a><span data-ttu-id="51dce-121">参照</span><span class="sxs-lookup"><span data-stu-id="51dce-121">Reference</span></span>

<span data-ttu-id="51dce-122">[Project VBA 開発者向けリファレンス](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx)入門および VBA のヘルプ記事が含まれる。</span><span class="sxs-lookup"><span data-stu-id="51dce-122">[Project VBA developer reference](https://msdn.microsoft.com/library/ee861523%28office.15%29.aspx) Contains introductory and VBA Help articles.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="51dce-123">関連情報</span><span class="sxs-lookup"><span data-stu-id="51dce-123">Related sections</span></span>

<span data-ttu-id="51dce-124">[Project Server 2013 アーキテクチャ](project-server-2013-architecture.md)クライアントがサーバーとProjectする方法をProjectします。</span><span class="sxs-lookup"><span data-stu-id="51dce-124">[Project Server 2013 architecture](project-server-2013-architecture.md) Shows how the Project clients interact with Project Server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51dce-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="51dce-125">See also</span></span>

- [<span data-ttu-id="51dce-126">開発者向け Project</span><span class="sxs-lookup"><span data-stu-id="51dce-126">Project for developers</span></span>](https://msdn.microsoft.com/office/aa905469)
- [<span data-ttu-id="51dce-127">Officeデベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="51dce-127">Office developer center</span></span>](https://dev.office.com)
- [<span data-ttu-id="51dce-128">Visual Studioデベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="51dce-128">Visual Studio developer center</span></span>](https://msdn.microsoft.com/vstudio/aa718325.aspx)
- [<span data-ttu-id="51dce-129">ClickOnceセキュリティと展開</span><span class="sxs-lookup"><span data-stu-id="51dce-129">ClickOnce Security and Deployment</span></span>](https://msdn.microsoft.com/library/t71a733d.aspx)
- [<span data-ttu-id="51dce-130">利用可能なフィールド リファレンス</span><span class="sxs-lookup"><span data-stu-id="51dce-130">Available fields reference</span></span>](https://support.office.com/en-us/article/available-fields-reference-615a4563-1cc3-40f4-b66f-1b17e793a460)

