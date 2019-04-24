---
title: Project Online の基本
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: アプリケーション開発者は、スタンドアロンアプリケーションまたはプロジェクトアドインを使用して、project Online サイト (SharePoint ホスト型) をカスタマイズできます。プロジェクトに関与する必要のあるニーズに対処することから、次のような PMO サポート機能まで、さまざまなアプリケーションが存在する可能性があります。
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344409"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="5aafb-103">Project Online の基本</span><span class="sxs-lookup"><span data-stu-id="5aafb-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="5aafb-104">アプリケーション開発者は、スタンドアロンアプリケーションまたはプロジェクトアドインを使用して、project Online サイト (SharePoint ホスト型) をカスタマイズできます。プロジェクトに関与する必要のあるニーズに対処することから、次のような PMO サポート機能まで、さまざまなアプリケーションが存在する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5aafb-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="5aafb-105">作業者の合理化されたタイムカードデータ入力</span><span class="sxs-lookup"><span data-stu-id="5aafb-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="5aafb-106">監修者への効率的なタイムカードの承認</span><span class="sxs-lookup"><span data-stu-id="5aafb-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="5aafb-107">プロジェクトに必要な許可 (調達および状態) を監視する</span><span class="sxs-lookup"><span data-stu-id="5aafb-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="5aafb-108">アクティブなプロジェクトの状態/正常性チェック</span><span class="sxs-lookup"><span data-stu-id="5aafb-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="5aafb-109">問題レポート</span><span class="sxs-lookup"><span data-stu-id="5aafb-109">Issues report</span></span>
- <span data-ttu-id="5aafb-110">変更管理の状態レポート</span><span class="sxs-lookup"><span data-stu-id="5aafb-110">Change Management Status report</span></span>
    
<span data-ttu-id="5aafb-111">Project Online には、次のシナリオに対応するための API サポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="5aafb-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="5aafb-112">プロジェクト (SharePoint) ホスト型アドインの場合:</span><span class="sxs-lookup"><span data-stu-id="5aafb-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="5aafb-113">SharePoint Online でホストされているコード (JavaScript、HTML、CSS)</span><span class="sxs-lookup"><span data-stu-id="5aafb-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="5aafb-114">ブラウザーにダウンロードされ、SharePoint Online に対して実行されるアセット。</span><span class="sxs-lookup"><span data-stu-id="5aafb-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="5aafb-115">JavaScript のビジネスロジック</span><span class="sxs-lookup"><span data-stu-id="5aafb-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="5aafb-116">Project Online または SharePoint に格納されているデータにアクセスする (ただし、に制限されることはありません)。</span><span class="sxs-lookup"><span data-stu-id="5aafb-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="5aafb-117">Custom fields</span><span class="sxs-lookup"><span data-stu-id="5aafb-117">Custom fields</span></span>  
  - <span data-ttu-id="5aafb-118">リスト</span><span class="sxs-lookup"><span data-stu-id="5aafb-118">Lists</span></span>
    
- <span data-ttu-id="5aafb-119">プロジェクト (SharePoint) プロバイダー向けのホスト型アドインの場合:</span><span class="sxs-lookup"><span data-stu-id="5aafb-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="5aafb-120">Project Online サイト外のサイトに存在するコード</span><span class="sxs-lookup"><span data-stu-id="5aafb-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="5aafb-121">外部サイト。以下のことができます (ただし、制限はありません)。</span><span class="sxs-lookup"><span data-stu-id="5aafb-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="5aafb-122">別の SharePoint サイト</span><span class="sxs-lookup"><span data-stu-id="5aafb-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="5aafb-123">任意のプラットフォーム上に構築された Web App/サービス</span><span class="sxs-lookup"><span data-stu-id="5aafb-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="5aafb-124">外部サイトにビジネスロジックが含まれている</span><span class="sxs-lookup"><span data-stu-id="5aafb-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="5aafb-125">ブラウザーが project online から外部サイトにリダイレクトされ、access トークンが project online にリダイレクトされます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="5aafb-126">外部サイトは、SharePoint および Project Online を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="5aafb-127">外部/スタンドアロンアドインの場合:</span><span class="sxs-lookup"><span data-stu-id="5aafb-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="5aafb-128">ユーザーがデバイス上でアプリケーションを実行する</span><span class="sxs-lookup"><span data-stu-id="5aafb-128">User executes an application on their device</span></span>
  - <span data-ttu-id="5aafb-129">アプリケーションは、Project Online api を直接認証して呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="5aafb-130">アプリケーションの種類</span><span class="sxs-lookup"><span data-stu-id="5aafb-130">Type of application</span></span>|<span data-ttu-id="5aafb-131">API 実装</span><span class="sxs-lookup"><span data-stu-id="5aafb-131">API implementation</span></span>|<span data-ttu-id="5aafb-132">ターゲット環境</span><span class="sxs-lookup"><span data-stu-id="5aafb-132">Target environment</span></span>|<span data-ttu-id="5aafb-133">アプリケーションの例</span><span class="sxs-lookup"><span data-stu-id="5aafb-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5aafb-134">ホストされるプロジェクト</span><span class="sxs-lookup"><span data-stu-id="5aafb-134">Project hosted</span></span>  <br/> |<span data-ttu-id="5aafb-135">jsom (Java Script オブジェクトモデル)</span><span class="sxs-lookup"><span data-stu-id="5aafb-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="5aafb-136">REST</span><span class="sxs-lookup"><span data-stu-id="5aafb-136">REST</span></span>  <br/> |<span data-ttu-id="5aafb-137">ブラウザー</span><span class="sxs-lookup"><span data-stu-id="5aafb-137">Browser</span></span>  <br/> |<span data-ttu-id="5aafb-138">タイムカードエントリ</span><span class="sxs-lookup"><span data-stu-id="5aafb-138">Timecard entry</span></span>  <br/> <span data-ttu-id="5aafb-139">タイムカードの承認</span><span class="sxs-lookup"><span data-stu-id="5aafb-139">Timecard approval</span></span>  <br/> <span data-ttu-id="5aafb-140">プロジェクトの進捗状況</span><span class="sxs-lookup"><span data-stu-id="5aafb-140">Project Status</span></span>  <br/> <span data-ttu-id="5aafb-141">問題レポート</span><span class="sxs-lookup"><span data-stu-id="5aafb-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="5aafb-142">ホストされているプロジェクトプロバイダー</span><span class="sxs-lookup"><span data-stu-id="5aafb-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="5aafb-143">csom クライアントライブラリ</span><span class="sxs-lookup"><span data-stu-id="5aafb-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="5aafb-144">Azure web サイト/アプリ</span><span class="sxs-lookup"><span data-stu-id="5aafb-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="5aafb-145">Windows 以外の環境 (ランプ等)</span><span class="sxs-lookup"><span data-stu-id="5aafb-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="5aafb-146">外部タイムシートの検証</span><span class="sxs-lookup"><span data-stu-id="5aafb-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="5aafb-147">プロジェクトインポーター</span><span class="sxs-lookup"><span data-stu-id="5aafb-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="5aafb-148">外部/スタンドアロン</span><span class="sxs-lookup"><span data-stu-id="5aafb-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="5aafb-149">REST</span><span class="sxs-lookup"><span data-stu-id="5aafb-149">REST</span></span>  <br/> <span data-ttu-id="5aafb-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="5aafb-150">CSOM</span></span>  <br/> |<span data-ttu-id="5aafb-151">REST-任意のプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="5aafb-151">REST - any platform</span></span>  <br/> <span data-ttu-id="5aafb-152">csom-任意の .net サポートされるプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="5aafb-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="5aafb-153">タイムカードエントリ</span><span class="sxs-lookup"><span data-stu-id="5aafb-153">Timecard entry</span></span>  <br/> <span data-ttu-id="5aafb-154">新しいサイトへのプロジェクトの移行</span><span class="sxs-lookup"><span data-stu-id="5aafb-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="5aafb-155">管理の状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="5aafb-156">Project Online 用のアプリケーションの開発を開始するには、何が必要ですか?</span><span class="sxs-lookup"><span data-stu-id="5aafb-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="5aafb-157">project online アプリケーションの開発に必要な一般的なアイテムは、project online アカウントおよびテストデータ--プロジェクトとプロジェクト関連の情報で、割り当て、タスク、リソース、およびユーザー設定フィールドを含みます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="5aafb-158">開発環境も必要ですが、開発環境の仕様はアプリケーションの種類とアプリケーションに必要な API インターフェイスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="5aafb-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="5aafb-159">次のいくつかのセクションでは、3つの API インターフェイスの開発ニーズについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="5aafb-160">参照ドキュメントでは、3つすべてのインターフェイスに共通のオブジェクトモデルと、オブジェクトモデルコンポーネント間の関係を示すエンティティマップについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="5aafb-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="5aafb-161">プロジェクトでホストされるアドインの開発環境</span><span class="sxs-lookup"><span data-stu-id="5aafb-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="5aafb-162">ホストされるアドインは、サーバー上に存在し、ランタイムの実行のためにブラウザーにダウンロードされるアドインです。</span><span class="sxs-lookup"><span data-stu-id="5aafb-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="5aafb-163">ホストされたアドインは、jsom または REST インターフェイスを使用して、JavaScript で記述できます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="5aafb-164">Project Online では、ランタイムの実行のための jsom ライブラリへの参照が提供されています。</span><span class="sxs-lookup"><span data-stu-id="5aafb-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="5aafb-165">開発が Windows プラットフォームで実行されている場合、必要なリソースは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5aafb-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="5aafb-166">visual studio 2015 (推奨) または visual studio 2013</span><span class="sxs-lookup"><span data-stu-id="5aafb-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="5aafb-167">Office 開発ツール (Visual Studio)</span><span class="sxs-lookup"><span data-stu-id="5aafb-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="5aafb-168">JavaScript 言語</span><span class="sxs-lookup"><span data-stu-id="5aafb-168">JavaScript language</span></span>
    
<span data-ttu-id="5aafb-169">サンプルhttps://github.com/OfficeDev/Project-JSOM-Copy-Work-Packagesアプリケーションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aafb-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="5aafb-170">簡単な手順でサンプルをダウンロードして実行することができます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="5aafb-171">サンプルアプリケーションをダウンロードして開く</span><span class="sxs-lookup"><span data-stu-id="5aafb-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="5aafb-172">[プロパティ] ウィンドウで SiteURL を更新する</span><span class="sxs-lookup"><span data-stu-id="5aafb-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="5aafb-173">project online は、アドインのアプリケーションスコープとユーザー権限の両方を調べて、project online ホスト上の情報へのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="5aafb-174">どちらか一方または両方の設定で明示的にアクセスが拒否されている場合、Project Online は情報へのアクセスを拒否します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="5aafb-175">それ以外の場合は、アクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="5aafb-176">サイトで[サイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5aafb-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="5aafb-177">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="5aafb-177">Build the project.</span></span>
    
5. <span data-ttu-id="5aafb-178">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="5aafb-179">プロジェクトプロバイダー向けのホスト型アドインの開発環境</span><span class="sxs-lookup"><span data-stu-id="5aafb-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="5aafb-180">プロバイダーホスト型アドインは、どの web プラットフォームにも記述され、常駐するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="5aafb-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="5aafb-181">これらのユーザーは、REST (または csom for Microsoft プラットフォーム) API を使用して接続し、データ操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="5aafb-182">REST インターフェイスをサポートするすべての言語と環境を開発に使用できます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="5aafb-183">この種類のアプリケーションの Windows 開発環境の例には、次の項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5aafb-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="5aafb-184">visual studio 2015 (推奨) または visual studio 2013</span><span class="sxs-lookup"><span data-stu-id="5aafb-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="5aafb-185">Microsoft Office 開発ツール (visual studio 2015 Professional および Enterprise edition で提供されています)</span><span class="sxs-lookup"><span data-stu-id="5aafb-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="5aafb-186">.net Framework 4.0 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="5aafb-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="5aafb-187">[sharepointonline csom パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM)(csom 呼び出しの場合)</span><span class="sxs-lookup"><span data-stu-id="5aafb-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="5aafb-188">プログラミング言語 (C# など)</span><span class="sxs-lookup"><span data-stu-id="5aafb-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="5aafb-189">作業https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations用サンプルスクリプトにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="5aafb-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="5aafb-190">サンプルは、いくつかの手順で実行できます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="5aafb-191">サンプルアプリケーションをダウンロードして開く</span><span class="sxs-lookup"><span data-stu-id="5aafb-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="5aafb-192">[プロパティ] ウィンドウで SiteURL を更新する</span><span class="sxs-lookup"><span data-stu-id="5aafb-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="5aafb-193">project online は、アドインのアプリケーションスコープとユーザー権限の両方を調べて、project online ホスト上の情報へのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="5aafb-194">どちらか一方または両方の設定で明示的にアクセスが拒否されている場合、Project Online は情報へのアクセスを拒否します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="5aafb-195">それ以外の場合は、アクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="5aafb-196">サイトで[サイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins)を有効にします。</span><span class="sxs-lookup"><span data-stu-id="5aafb-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="5aafb-197">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="5aafb-197">Build the project.</span></span>
    
5. <span data-ttu-id="5aafb-198">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="5aafb-199">外部/スタンドアロンアプリケーション開発環境</span><span class="sxs-lookup"><span data-stu-id="5aafb-199">External/standalone application development environment</span></span>

<span data-ttu-id="5aafb-200">スタンドアロンアプリケーションは、クライアント側オブジェクトモデル (csom) を使用して project online を呼び出し、project online と通信して、サーバー上に存在する情報を作成、取得、更新、および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="5aafb-201">これは、ユーザーアクセスレベルによって実行されるスタンドアロンクライアントアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="5aafb-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="5aafb-202">この種類のアプリケーションの Windows 開発環境の例には、次の項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5aafb-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="5aafb-203">visual studio 2015 (推奨) または visual studio 2013</span><span class="sxs-lookup"><span data-stu-id="5aafb-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="5aafb-204">Microsoft Office 開発ツール (visual studio 2015 Professional および Enterprise edition で提供されています)</span><span class="sxs-lookup"><span data-stu-id="5aafb-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="5aafb-205">.net Framework 4.0 またはそれ以降</span><span class="sxs-lookup"><span data-stu-id="5aafb-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="5aafb-206">[sharepointonline csom パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM)(csom 呼び出しの場合)</span><span class="sxs-lookup"><span data-stu-id="5aafb-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="5aafb-207">プログラミング言語 (C# など)</span><span class="sxs-lookup"><span data-stu-id="5aafb-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="5aafb-208">サンプルhttps://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFieldsアプリケーションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5aafb-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="5aafb-209">サンプルは、いくつかの手順で実行できます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="5aafb-210">サンプルアプリケーションをダウンロードする</span><span class="sxs-lookup"><span data-stu-id="5aafb-210">Download the sample application</span></span>
    
2. <span data-ttu-id="5aafb-211">プロジェクトオンラインサイト (サイト名、ユーザーアカウント、パスワード) にアクセスするための、いくつかの変更を行います。</span><span class="sxs-lookup"><span data-stu-id="5aafb-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="5aafb-212">ユーザーがすべてのプロジェクトにアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="5aafb-213">Project Online では、ユーザー権限を使用して、データストア内の情報へのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="5aafb-214">nuget コンソールで次のように入力して、[ツール] メニューから利用できる nuget パッケージマネージャーコンソールを使用して、SharePoint アセンブリを参照に追加します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="5aafb-215">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="5aafb-215">Build the project.</span></span>
    
5. <span data-ttu-id="5aafb-216">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="5aafb-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="5aafb-217">次のステップ</span><span class="sxs-lookup"><span data-stu-id="5aafb-217">Next steps</span></span>

<span data-ttu-id="5aafb-218">各サンプルアプリケーションには、個々のプロジェクト API を使用した作業の概要を説明する記事があります。</span><span class="sxs-lookup"><span data-stu-id="5aafb-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="5aafb-219">この記事は、エンティティの関係、クエリシステムの情報、およびユーザー設定フィールドへのアクセスについて説明するいくつかの記事と共に、次のリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5aafb-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="5aafb-220">クライアント側オブジェクトモデルを使用した Project Online アプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="5aafb-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="5aafb-221">JavaScript オブジェクトモデル (jsom) を使用して Project Online アドインを開発する</span><span class="sxs-lookup"><span data-stu-id="5aafb-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="5aafb-222">Project Online エンタープライズ ユーザー設定フィールドへのアクセス</span><span class="sxs-lookup"><span data-stu-id="5aafb-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="5aafb-223">関連項目</span><span class="sxs-lookup"><span data-stu-id="5aafb-223">See also</span></span>

<span data-ttu-id="5aafb-224">Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="5aafb-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

