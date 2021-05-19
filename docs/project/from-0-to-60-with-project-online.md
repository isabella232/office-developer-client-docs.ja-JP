---
title: Project Online の基本
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: アプリケーション開発者は、スタンドアロン アプリケーションProject OnlineアドインをSharePointして、Project サイト (ホストされている) をカスタマイズできます。プロジェクトに関わるユーザーのニーズへの対応から、次のような PMO サポート機能まで、さまざまなアプリケーションが利用できます。
ms.openlocfilehash: 00f79b05b886bfd2c54c118245e22f10bb5451bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344409"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="98ad0-103">Project Online の基本</span><span class="sxs-lookup"><span data-stu-id="98ad0-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="98ad0-104">アプリケーション開発者は、スタンドアロン アプリケーションProject OnlineアドインをSharePointして、Project サイト (ホストされている) をカスタマイズできます。プロジェクトに関わるユーザーのニーズへの対応から、次のような PMO サポート機能まで、さまざまなアプリケーションが利用できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="98ad0-105">ワーカーのタイムカード データエントリの合理化</span><span class="sxs-lookup"><span data-stu-id="98ad0-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="98ad0-106">監督者の効率的なタイムカード承認</span><span class="sxs-lookup"><span data-stu-id="98ad0-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="98ad0-107">プロジェクトに必要な許可 (調達と状態) の監視</span><span class="sxs-lookup"><span data-stu-id="98ad0-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="98ad0-108">アクティブなプロジェクトの状態/正常性チェック</span><span class="sxs-lookup"><span data-stu-id="98ad0-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="98ad0-109">問題レポート</span><span class="sxs-lookup"><span data-stu-id="98ad0-109">Issues report</span></span>
- <span data-ttu-id="98ad0-110">[管理状態の変更] レポート</span><span class="sxs-lookup"><span data-stu-id="98ad0-110">Change Management Status report</span></span>
    
<span data-ttu-id="98ad0-111">Project Onlineのシナリオに対応する API サポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="98ad0-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="98ad0-112">ホストProject (SharePoint) の場合:</span><span class="sxs-lookup"><span data-stu-id="98ad0-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="98ad0-113">オンラインでホストされているコード (JavaScript、HTML、CSS) SharePointします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="98ad0-114">ブラウザーにダウンロードされ、オンラインに対して実行SharePoint。</span><span class="sxs-lookup"><span data-stu-id="98ad0-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="98ad0-115">JavaScript にあるビジネス ロジック</span><span class="sxs-lookup"><span data-stu-id="98ad0-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="98ad0-116">次に示すデータなど、Project OnlineまたはSharePointに格納されているデータにアクセスします (ただし、これらに限定されません)。</span><span class="sxs-lookup"><span data-stu-id="98ad0-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="98ad0-117">カスタム フィールド</span><span class="sxs-lookup"><span data-stu-id="98ad0-117">Custom fields</span></span>  
  - <span data-ttu-id="98ad0-118">リスト</span><span class="sxs-lookup"><span data-stu-id="98ad0-118">Lists</span></span>
    
- <span data-ttu-id="98ad0-119">プロバイダーホストProject (SharePoint) アドインの場合:</span><span class="sxs-lookup"><span data-stu-id="98ad0-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="98ad0-120">サイトの外部サイトに存在するコードProject Onlineします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="98ad0-121">外部サイトは、次の場合があります (ただし、これらに限定されない)。</span><span class="sxs-lookup"><span data-stu-id="98ad0-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="98ad0-122">別のSharePoint サイト</span><span class="sxs-lookup"><span data-stu-id="98ad0-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="98ad0-123">任意のプラットフォーム上に構築された Web App/Service</span><span class="sxs-lookup"><span data-stu-id="98ad0-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="98ad0-124">外部サイトにはビジネス ロジックが含まれています</span><span class="sxs-lookup"><span data-stu-id="98ad0-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="98ad0-125">ブラウザーは、アクセス トークンを使用Project Online外部サイトから外部サイトにリダイレクトProject Online</span><span class="sxs-lookup"><span data-stu-id="98ad0-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="98ad0-126">外部サイトは、ユーザーとユーザーのSharePointをProject Online</span><span class="sxs-lookup"><span data-stu-id="98ad0-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="98ad0-127">外部アドインまたはスタンドアロン アドインの場合:</span><span class="sxs-lookup"><span data-stu-id="98ad0-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="98ad0-128">ユーザーがデバイス上でアプリケーションを実行する</span><span class="sxs-lookup"><span data-stu-id="98ad0-128">User executes an application on their device</span></span>
  - <span data-ttu-id="98ad0-129">アプリケーションが API を直接認証Project Online呼び出す</span><span class="sxs-lookup"><span data-stu-id="98ad0-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="98ad0-130">アプリケーションの種類</span><span class="sxs-lookup"><span data-stu-id="98ad0-130">Type of application</span></span>|<span data-ttu-id="98ad0-131">API の実装</span><span class="sxs-lookup"><span data-stu-id="98ad0-131">API implementation</span></span>|<span data-ttu-id="98ad0-132">ターゲット環境</span><span class="sxs-lookup"><span data-stu-id="98ad0-132">Target environment</span></span>|<span data-ttu-id="98ad0-133">アプリケーションの例</span><span class="sxs-lookup"><span data-stu-id="98ad0-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="98ad0-134">Projectホスト</span><span class="sxs-lookup"><span data-stu-id="98ad0-134">Project hosted</span></span>  <br/> |<span data-ttu-id="98ad0-135">JSOM (Java スクリプト オブジェクト モデル)</span><span class="sxs-lookup"><span data-stu-id="98ad0-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="98ad0-136">REST</span><span class="sxs-lookup"><span data-stu-id="98ad0-136">REST</span></span>  <br/> |<span data-ttu-id="98ad0-137">ブラウザー</span><span class="sxs-lookup"><span data-stu-id="98ad0-137">Browser</span></span>  <br/> |<span data-ttu-id="98ad0-138">タイムカードエントリ</span><span class="sxs-lookup"><span data-stu-id="98ad0-138">Timecard entry</span></span>  <br/> <span data-ttu-id="98ad0-139">タイムカードの承認</span><span class="sxs-lookup"><span data-stu-id="98ad0-139">Timecard approval</span></span>  <br/> <span data-ttu-id="98ad0-140">プロジェクトの進捗状況</span><span class="sxs-lookup"><span data-stu-id="98ad0-140">Project Status</span></span>  <br/> <span data-ttu-id="98ad0-141">問題レポート</span><span class="sxs-lookup"><span data-stu-id="98ad0-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="98ad0-142">Projectプロバイダーホスト型</span><span class="sxs-lookup"><span data-stu-id="98ad0-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="98ad0-143">CSOM クライアント ライブラリ</span><span class="sxs-lookup"><span data-stu-id="98ad0-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="98ad0-144">Azure Web サイト/アプリ</span><span class="sxs-lookup"><span data-stu-id="98ad0-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="98ad0-145">非Windows環境 (LAMP など)</span><span class="sxs-lookup"><span data-stu-id="98ad0-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="98ad0-146">外部タイムシート検証機能</span><span class="sxs-lookup"><span data-stu-id="98ad0-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="98ad0-147">ProjectImporter</span><span class="sxs-lookup"><span data-stu-id="98ad0-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="98ad0-148">外部/スタンドアロン</span><span class="sxs-lookup"><span data-stu-id="98ad0-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="98ad0-149">REST</span><span class="sxs-lookup"><span data-stu-id="98ad0-149">REST</span></span>  <br/> <span data-ttu-id="98ad0-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="98ad0-150">CSOM</span></span>  <br/> |<span data-ttu-id="98ad0-151">REST - 任意のプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="98ad0-151">REST - any platform</span></span>  <br/> <span data-ttu-id="98ad0-152">CSOM - 任意の .NET でサポートされるプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="98ad0-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="98ad0-153">タイムカードエントリ</span><span class="sxs-lookup"><span data-stu-id="98ad0-153">Timecard entry</span></span>  <br/> <span data-ttu-id="98ad0-154">新しいサイトへのプロジェクトの移行</span><span class="sxs-lookup"><span data-stu-id="98ad0-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="98ad0-155">[管理状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="98ad0-156">アプリケーションの開発を開始するには何が必要Project Online?</span><span class="sxs-lookup"><span data-stu-id="98ad0-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="98ad0-157">Project Online アプリケーションの開発に必要な一般的な項目は、Project Online アカウントとテスト データです。割り当て、タスク、リソース、およびユーザー設定フィールドを含むプロジェクトとプロジェクト関連の情報です。</span><span class="sxs-lookup"><span data-stu-id="98ad0-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="98ad0-158">開発環境も必要ですが、開発環境の詳細は、アプリケーションの種類とアプリケーションに必要な API インターフェイスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="98ad0-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="98ad0-159">次のいくつかのセクションでは、3 つの API インターフェイスの開発ニーズについて説明します。</span><span class="sxs-lookup"><span data-stu-id="98ad0-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="98ad0-160">リファレンス ドキュメントでは、3 つのインターフェイスすべてで一般的なオブジェクト モデルと、オブジェクト モデル コンポーネント間の関係を示すエンティティ マップについて説明します。</span><span class="sxs-lookup"><span data-stu-id="98ad0-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="98ad0-161">Projectホスト型アドインの開発環境</span><span class="sxs-lookup"><span data-stu-id="98ad0-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="98ad0-162">ホスト型アドインは、サーバー上に存在し、実行時に実行するためにブラウザーにダウンロードされるアドインです。</span><span class="sxs-lookup"><span data-stu-id="98ad0-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="98ad0-163">ホストされたアドインは、JSOM または REST インターフェイスを使用し、JavaScript で記述されます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="98ad0-164">Project Online実行時に JSOM ライブラリへの参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="98ad0-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="98ad0-165">開発が新しいプラットフォーム上Windows、必要なリソースは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="98ad0-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="98ad0-166">Visual Studio 2015 (優先) または Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="98ad0-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="98ad0-167">Office開発ツールのVisual Studio</span><span class="sxs-lookup"><span data-stu-id="98ad0-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="98ad0-168">JavaScript 言語</span><span class="sxs-lookup"><span data-stu-id="98ad0-168">JavaScript language</span></span>
    
<span data-ttu-id="98ad0-169">サンプル https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages アプリケーションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="98ad0-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="98ad0-170">サンプルは、次の簡単な手順でダウンロードして実行できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="98ad0-171">サンプル アプリケーションをダウンロードして開く</span><span class="sxs-lookup"><span data-stu-id="98ad0-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="98ad0-172">[プロパティ] ウィンドウで SiteURL を更新する</span><span class="sxs-lookup"><span data-stu-id="98ad0-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="98ad0-173">Project Online、アドインのアプリケーション スコープと、アドイン ホスト上の情報へのアクセスを管理するユーザーアクセス許可の両方をProject Onlineします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="98ad0-174">どちらかまたは両方の設定でアクセスが明示的に拒否された場合、Project Onlineへのアクセスを拒否する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98ad0-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="98ad0-175">それ以外の場合は、アクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="98ad0-176">サイト [でサイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) を有効にする。</span><span class="sxs-lookup"><span data-stu-id="98ad0-176">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span>  
    
4. <span data-ttu-id="98ad0-177">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-177">Build the project.</span></span>
    
5. <span data-ttu-id="98ad0-178">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="98ad0-178">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="98ad0-179">Projectホスト型アドインの開発環境</span><span class="sxs-lookup"><span data-stu-id="98ad0-179">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="98ad0-180">プロバイダーホスト型アドインは、任意の Web プラットフォームで作成および常駐するアプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="98ad0-180">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="98ad0-181">REST (または Microsoft プラットフォーム用 CSOM) API を使用して、データ操作を接続して実行できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-181">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="98ad0-182">REST インターフェイスをサポートする言語と環境は、開発に使用できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-182">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="98ad0-183">この種類のアプリケーションWindows環境の例には、次の項目があります。</span><span class="sxs-lookup"><span data-stu-id="98ad0-183">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="98ad0-184">Visual Studio 2015 (優先) または Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="98ad0-184">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="98ad0-185">Microsoft Office開発ツール for Visual Studio (Visual Studio 2015 Professional および Enterpriseエディション)</span><span class="sxs-lookup"><span data-stu-id="98ad0-185">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="98ad0-186">.NET Framework 4.0 以降</span><span class="sxs-lookup"><span data-stu-id="98ad0-186">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="98ad0-187">[SharePointOnline CSOM パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (CSOM 呼び出しの場合)</span><span class="sxs-lookup"><span data-stu-id="98ad0-187">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="98ad0-188">プログラミング言語 (C など)#</span><span class="sxs-lookup"><span data-stu-id="98ad0-188">A programming language, such as C#</span></span> 
    
<span data-ttu-id="98ad0-189">作業 https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations サンプル スクリプトについては、次のページをご覧ください。</span><span class="sxs-lookup"><span data-stu-id="98ad0-189">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="98ad0-190">このサンプルは、いくつかの手順で実行できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-190">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="98ad0-191">サンプル アプリケーションをダウンロードして開く</span><span class="sxs-lookup"><span data-stu-id="98ad0-191">Download and open the sample application</span></span>
    
2. <span data-ttu-id="98ad0-192">[プロパティ] ウィンドウで SiteURL を更新する</span><span class="sxs-lookup"><span data-stu-id="98ad0-192">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="98ad0-193">Project Online、アドインのアプリケーション スコープと、アドイン ホスト上の情報へのアクセスを管理するユーザーアクセス許可の両方をProject Onlineします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-193">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="98ad0-194">どちらかまたは両方の設定でアクセスが明示的に拒否された場合、Project Onlineへのアクセスを拒否する必要があります。</span><span class="sxs-lookup"><span data-stu-id="98ad0-194">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="98ad0-195">それ以外の場合は、アクセスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-195">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="98ad0-196">サイト [でサイドローディング](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) を有効にする。</span><span class="sxs-lookup"><span data-stu-id="98ad0-196">Enable [sideloading](https://docs.microsoft.com/office/dev/add-ins/testing/create-a-network-shared-folder-catalog-for-task-pane-and-content-add-ins) on your site.</span></span> 
    
4. <span data-ttu-id="98ad0-197">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-197">Build the project.</span></span>
    
5. <span data-ttu-id="98ad0-198">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="98ad0-198">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="98ad0-199">外部/スタンドアロン アプリケーションの開発環境</span><span class="sxs-lookup"><span data-stu-id="98ad0-199">External/standalone application development environment</span></span>

<span data-ttu-id="98ad0-200">スタンドアロン アプリケーションは、クライアント側オブジェクト モデル (CSOM) または REST を使用して Project Online を呼び出して、Project Online と通信して、サーバーに存在する情報を作成、取得、更新、および削除できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-200">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="98ad0-201">これは、実行するユーザー アクセス レベルに依存するスタンドアロン クライアント アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="98ad0-201">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="98ad0-202">この種類のアプリケーションWindows環境の例には、次の項目があります。</span><span class="sxs-lookup"><span data-stu-id="98ad0-202">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="98ad0-203">Visual Studio 2015 (優先) または Visual Studio 2013</span><span class="sxs-lookup"><span data-stu-id="98ad0-203">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="98ad0-204">Microsoft Office開発ツール for Visual Studio (Visual Studio 2015 Professional および Enterpriseエディション)</span><span class="sxs-lookup"><span data-stu-id="98ad0-204">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="98ad0-205">.NET Framework 4.0 以降</span><span class="sxs-lookup"><span data-stu-id="98ad0-205">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="98ad0-206">[SharePointOnline CSOM パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (CSOM 呼び出しの場合)</span><span class="sxs-lookup"><span data-stu-id="98ad0-206">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="98ad0-207">プログラミング言語 (C など)#</span><span class="sxs-lookup"><span data-stu-id="98ad0-207">A programming language, such as C#</span></span> 
    
<span data-ttu-id="98ad0-208">サンプル https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields アプリケーションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="98ad0-208">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="98ad0-209">このサンプルは、いくつかの手順で実行できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-209">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="98ad0-210">サンプル アプリケーションのダウンロード</span><span class="sxs-lookup"><span data-stu-id="98ad0-210">Download the sample application</span></span>
    
2. <span data-ttu-id="98ad0-211">サイト名、ユーザー アカウント、およびパスワードProject Onlineアクセスするために、いくつかの変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-211">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="98ad0-212">ユーザーがすべてのプロジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-212">Ensure the user has access to all projects.</span></span> <span data-ttu-id="98ad0-213">Project Onlineアクセス許可を使用して、データ ストア内の情報へのアクセスを管理します。</span><span class="sxs-lookup"><span data-stu-id="98ad0-213">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="98ad0-214">Nuget コンソールSharePointを使用して、パッケージ マネージャー アセンブリを参照に追加します。Nuget コンソールで次のように入力して、[ツール] メニューから使用できます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-214">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="98ad0-215">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="98ad0-215">Build the project.</span></span>
    
5. <span data-ttu-id="98ad0-216">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="98ad0-216">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="98ad0-217">次の手順</span><span class="sxs-lookup"><span data-stu-id="98ad0-217">Next steps</span></span>

<span data-ttu-id="98ad0-218">各サンプル アプリケーションには、API を使用して個々のアプリケーションを操作するProjectがあります。</span><span class="sxs-lookup"><span data-stu-id="98ad0-218">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="98ad0-219">記事は、エンティティの関係、クエリ システムに関する情報、およびユーザー設定フィールドへのアクセスについて説明する記事と共に、次の一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="98ad0-219">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="98ad0-220">クライアント側Project Onlineモデルを使用したアプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="98ad0-220">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="98ad0-221">JavaScript オブジェクト Project Online (JSOM) を使用したアドインの開発</span><span class="sxs-lookup"><span data-stu-id="98ad0-221">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="98ad0-222">Project Online エンタープライズ ユーザー設定フィールドへのアクセス</span><span class="sxs-lookup"><span data-stu-id="98ad0-222">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="98ad0-223">関連項目</span><span class="sxs-lookup"><span data-stu-id="98ad0-223">See also</span></span>

<span data-ttu-id="98ad0-224">Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="98ad0-224">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

