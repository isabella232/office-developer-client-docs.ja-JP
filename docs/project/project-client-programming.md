---
title: プロジェクト クライアントのプログラミング
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
f1_keywords:
- object model
- Project object model
- Project VBA
- VBA
keywords:
- vba プロジェクト オブジェクト モデルでは、プロジェクト、プログラム、プログラミング、VBA のプロジェクトを Visual Basic for Applications プロジェクト オブジェクト モデルでは、VBA オブジェクト モデル、VBA では、Visual Basic for Applications
localization_priority: Normal
ms.assetid: 0ad49ff6-8dff-4379-a52c-d292c53c2bc0
description: Project 2013 のデスクトップ クライアント アプリケーション-標準 2013 のプロジェクトとプロジェクトの評価のため、カスタマイズし、マクロを作成するのには VBA を使用して拡張できます。 Visual Studio 2012 を使用するにはリボンのユーザー インターフェイスをカスタマイズし、新しい機能拡張モデルの一般的な Office 2013 のプラットフォームに組み込まれているプロジェクトでの作業ウィンドウに Office アドインを有効に複雑なアドインを作成します。 プロジェクト標準 2013 および評価のためのプロジェクトは一般的な Office のアドインを実行し、アドインを使用して作業ウィンドウの SharePoint、他の web サイトや web アプリケーション、および外部のデータと統合するプロジェクト専用に開発されました。
ms.openlocfilehash: e8604b4d479d0c64f8d45ad2363d7391d57408ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804679"
---
# <a name="project-client-programming"></a><span data-ttu-id="64679-106">プロジェクト クライアントのプログラミング</span><span class="sxs-lookup"><span data-stu-id="64679-106">Project client programming</span></span>

<span data-ttu-id="64679-107">Project 2013 のデスクトップ クライアント アプリケーション-標準 2013 のプロジェクトとプロジェクトの評価のため、カスタマイズし、マクロを作成するのには VBA を使用して拡張できます。</span><span class="sxs-lookup"><span data-stu-id="64679-107">The Project 2013 desktop client applications—Project Standard 2013 and Project Professional 2013—can be customized and extended by using VBA to write macros.</span></span> <span data-ttu-id="64679-108">Visual Studio 2012 を使用するにはリボンのユーザー インターフェイスをカスタマイズし、新しい機能拡張モデルの一般的な Office 2013 のプラットフォームに組み込まれているプロジェクトでの作業ウィンドウに Office アドインを有効に複雑なアドインを作成します。</span><span class="sxs-lookup"><span data-stu-id="64679-108">You can use Visual Studio 2012 to customize the ribbon user interface and create complex add-ins. Office Add-ins enables a new extensibility model for task panes in Project that are built on a common Office 2013 platform.</span></span> <span data-ttu-id="64679-109">プロジェクト標準 2013 および評価のためのプロジェクトは一般的な Office のアドインを実行し、アドインを使用して作業ウィンドウの SharePoint、他の web サイトや web アプリケーション、および外部のデータと統合するプロジェクト専用に開発されました。</span><span class="sxs-lookup"><span data-stu-id="64679-109">Project Standard 2013 and Project Professional 2013 can run general Office Add-ins and use task pane add-ins that are developed specifically for Project to integrate with SharePoint, other websites and web applications, and external data.</span></span>
  
 <span data-ttu-id="64679-110">**Visual Studio への移動**VBA では、マクロを記録し、比較的単純なオートメーション ソリューションを開発するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="64679-110">**Moving to Visual Studio** VBA is useful for recording macros and developing relatively simple automation solutions.</span></span> <span data-ttu-id="64679-111">作業ウィンドウ - アドインを開発するには、アドインと複雑なセキュリティで保護された、スケーラブルで、ますます簡単に配置したソリューションをお勧め Visual Studio 2012 を使用することです。</span><span class="sxs-lookup"><span data-stu-id="64679-111">To develop task pane add-ins, add-ins, and more complex, secure, scalable, and easily deployed solutions, we recommend that you use Visual Studio 2012.</span></span> <span data-ttu-id="64679-112">Microsoft.NET Framework 4.0 および Project 2013 のプライマリ相互運用機能アセンブリは、開発および展開を自動化し、Project 2013 のデスクトップ クライアントを統合するソリューションの多くの利点を提供します。</span><span class="sxs-lookup"><span data-stu-id="64679-112">The Microsoft .NET Framework 4.0 and the Project 2013 primary interop assembly provide many advantages for developing and deploying solutions that automate and integrate the Project 2013 desktop clients.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="64679-113">プロジェクトのアドインを開発するのには、Visual Studio 2010 を使用できます。ただし、Visual Studio 2012 には、テンプレートとクライアントの Office アドインを作成するように設計された拡張機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="64679-113">You can use Visual Studio 2010 to develop Project add-ins. However, Visual Studio 2012 includes templates and extensions that are designed to create Office Add-ins clients.</span></span> 
  
<span data-ttu-id="64679-114">**MSProject** Project 2013 での VBA オブジェクト モデルは、基本的に 2013 (VSTO とも呼ばれます) を Visual Studio の Office 開発ツールにマネージ コード ソリューションの**Microsoft.Office.Interop.MSProject**オブジェクト モデルと同じです。</span><span class="sxs-lookup"><span data-stu-id="64679-114">The **MSProject** object model for VBA in Project 2013 is essentially the same as the **Microsoft.Office.Interop.MSProject** object model for managed-code solutions with Office Developer Tools for Visual Studio 2013 (also known as VSTO).</span></span> <span data-ttu-id="64679-115">Visual Studio 2012 には、アプリケーション レベルのアドイン プロジェクト 2010年と Project 2013 (標準的なプロジェクトまたはプロジェクトのプロフェッショナル ・ バージョン) を開発するためのテンプレートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="64679-115">Visual Studio 2012 includes templates for developing application-level add-ins for Project 2010 and for Project 2013 (either the Project Standard or Project Professional versions).</span></span> <span data-ttu-id="64679-116">VSTO と Visual Studio 2012 ののための Office 開発ツールが簡単に開発、テスト、および Project デスクトップ クライアントおよびその他の Office 2013 アプリケーションを使用でき、SharePoint サイト、リスト、統合の高度な統合ソリューションを展開してワークフローです。</span><span class="sxs-lookup"><span data-stu-id="64679-116">VSTO and Office Developer Tools for Visual Studio 2012 simplify developing, testing, and deploying advanced integration solutions that can use the Project desktop client and other Office 2013 applications, and integrate with SharePoint sites, lists, and workflows.</span></span> 
  
<span data-ttu-id="64679-117">作業ウィンドウ - アドインおよびその他のアドインを Office および SharePoint は、Office ストアで販売できます (を参照してください[http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) プロジェクトのオンラインと設置型の両方のインストールで使用するためです。</span><span class="sxs-lookup"><span data-stu-id="64679-117">Task pane add-ins and other add-ins for Office and SharePoint can be sold in the Office Store (see [http://office.microsoft.com/store/](http://office.microsoft.com/en-us/store/)) for use with both Project Online and on-premises installations.</span></span> <span data-ttu-id="64679-118">Office ストアには、マクロを VBA と VSTO アドインを配布することはできません。標準的なプロジェクトと Project Professional をローカルで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="64679-118">VBA macros and VSTO add-ins cannot be distributed in the Office Store; they are designed for local use with Project Standard and Project Professional.</span></span> <span data-ttu-id="64679-119">プロジェクト内の VBA マクロを配布することができます。MPP ファイルは、Global.MPT ファイル、お使いのコンピューター上でインストールまたは Project Server 2013 のエンタープライズ グローバル テンプレートの配布。</span><span class="sxs-lookup"><span data-stu-id="64679-119">You can distribute VBA macros within a project .MPP file, install them in the Global.MPT file on your computer, or distribute them in the enterprise global template in Project Server 2013.</span></span> <span data-ttu-id="64679-120">VSTO アドインは、 [ClickOnce](http://msdn.microsoft.com/ja-jp/library/t71a733d.aspx)配置では、簡単に更新プログラムを有効より安全に配布できます。</span><span class="sxs-lookup"><span data-stu-id="64679-120">VSTO add-ins can be distributed more securely through [ClickOnce](http://msdn.microsoft.com/ja-jp/library/t71a733d.aspx) deployment, which enables easy updates.</span></span> 
  
## <a name="reference"></a><span data-ttu-id="64679-121">リファレンス</span><span class="sxs-lookup"><span data-stu-id="64679-121">Reference</span></span>

<span data-ttu-id="64679-122">[プロジェクトの VBA の開発者用リファレンス](http://msdn.microsoft.com/ja-jp/library/ee861523%28office.15%29.aspx)入門が含まれていて、VBA ヘルプの記事です。</span><span class="sxs-lookup"><span data-stu-id="64679-122">[Project VBA developer reference](http://msdn.microsoft.com/ja-jp/library/ee861523%28office.15%29.aspx) Contains introductory and VBA Help articles.</span></span> 
  
## <a name="related-sections"></a><span data-ttu-id="64679-123">関連セクション</span><span class="sxs-lookup"><span data-stu-id="64679-123">Related sections</span></span>

<span data-ttu-id="64679-124">[Project Server 2013 のアーキテクチャ](project-server-2013-architecture.md)クライアント プロジェクトが Project Server とどのようにやり取りする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="64679-124">[Project Server 2013 architecture](project-server-2013-architecture.md) Shows how the Project clients interact with Project Server.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64679-125">関連項目</span><span class="sxs-lookup"><span data-stu-id="64679-125">See also</span></span>



[<span data-ttu-id="64679-126">開発者のためのプロジェクト</span><span class="sxs-lookup"><span data-stu-id="64679-126">Project for developers</span></span>](http://msdn.microsoft.com/ja-jp/office/aa905469)
  
[<span data-ttu-id="64679-127">Office デベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="64679-127">Office developer center</span></span>](https://dev.office.com)
  
[<span data-ttu-id="64679-128">Visual Studio のデベロッパー センター</span><span class="sxs-lookup"><span data-stu-id="64679-128">Visual Studio developer center</span></span>](http://msdn.microsoft.com/en-us/vstudio/aa718325.aspx)
  
[<span data-ttu-id="64679-129">ClickOnce のセキュリティと展開</span><span class="sxs-lookup"><span data-stu-id="64679-129">ClickOnce Security and Deployment</span></span>](http://msdn.microsoft.com/ja-jp/library/t71a733d.aspx)
  
[<span data-ttu-id="64679-130">利用可能なフィールドの参照</span><span class="sxs-lookup"><span data-stu-id="64679-130">Available fields reference</span></span>](http://office.microsoft.com/en-us/project-help/available-fields-reference-HA102749299.aspx?CTT=1)

