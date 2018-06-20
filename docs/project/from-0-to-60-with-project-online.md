---
title: オンライン プロジェクトに 60 を 0 から
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5b48958e-6dab-4121-871f-fb15f58f1b24
description: アプリケーション開発者は、スタンドアロン アプリケーションやプロジェクトのアドインを使用する (SharePoint がホストされている) プロジェクトのオンライン サイトをカスタマイズできます。アプリケーションの豊富なは、範囲の PMO サポート関数では、次のいずれかのようにプロジェクトの関係者のニーズに対応可能です。
ms.openlocfilehash: c50ed12e9f1127f6313a02db4d84a151778e17b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804548"
---
# <a name="from-0-to-60-with-project-online"></a><span data-ttu-id="4b139-103">オンライン プロジェクトに 60 を 0 から</span><span class="sxs-lookup"><span data-stu-id="4b139-103">From 0 to 60 with Project Online</span></span>

<span data-ttu-id="4b139-104">アプリケーション開発者は、スタンドアロン アプリケーションやプロジェクトのアドインを使用する (SharePoint がホストされている) プロジェクトのオンライン サイトをカスタマイズできます。アプリケーションの豊富なは、範囲の PMO サポート関数では、次のいずれかのようにプロジェクトの関係者のニーズに対応可能です。</span><span class="sxs-lookup"><span data-stu-id="4b139-104">An application developer can customize a Project Online site (SharePoint hosted) using standalone applications and/or Project add-ins. A wealth of applications is possible that range from addressing needs of those involved in a project to PMO support functions, such as any of the following:</span></span>
  
- <span data-ttu-id="4b139-105">作業者の効率化されたタイムカード データの入力</span><span class="sxs-lookup"><span data-stu-id="4b139-105">Streamlined timecard data entry for workers</span></span>
- <span data-ttu-id="4b139-106">監督者の効率的なタイムカードの承認</span><span class="sxs-lookup"><span data-stu-id="4b139-106">Efficient timecard approval for supervisors</span></span>
- <span data-ttu-id="4b139-107">プロジェクトに必要な許可 (調達などの状態の監視</span><span class="sxs-lookup"><span data-stu-id="4b139-107">Oversight of permits (procurement and status) needed for a project</span></span>
- <span data-ttu-id="4b139-108">アクティブなプロジェクトのステータスと稼働状態のチェック</span><span class="sxs-lookup"><span data-stu-id="4b139-108">Status/Health check of active projects</span></span>
- <span data-ttu-id="4b139-109">問題に関するレポート</span><span class="sxs-lookup"><span data-stu-id="4b139-109">Issues report</span></span>
- <span data-ttu-id="4b139-110">管理ステータス レポートを変更します。</span><span class="sxs-lookup"><span data-stu-id="4b139-110">Change Management Status report</span></span>
    
<span data-ttu-id="4b139-111">オンライン プロジェクトにはには、次のシナリオに対応するための API のサポートが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b139-111">Project Online includes API support to accommodate the following scenarios:</span></span>
  
- <span data-ttu-id="4b139-112">プロジェクト (SharePoint) ホストを追加で。</span><span class="sxs-lookup"><span data-stu-id="4b139-112">For a Project (SharePoint) hosted add-in:</span></span>
    
  - <span data-ttu-id="4b139-113">SharePoint Online でホストされているコード (JavaScript、HTML、CSS など)</span><span class="sxs-lookup"><span data-stu-id="4b139-113">Code (JavaScript, HTML, CSS) that is hosted in SharePoint Online</span></span>
  - <span data-ttu-id="4b139-114">ブラウザーにダウンロードして、SharePoint Online に対して実行される資産です。</span><span class="sxs-lookup"><span data-stu-id="4b139-114">Assets that are downloaded to the browser and executed against SharePoint Online.</span></span>  
  - <span data-ttu-id="4b139-115">JavaScript では、ビジネス ロジック</span><span class="sxs-lookup"><span data-stu-id="4b139-115">Business logic that is in JavaScript</span></span>   
  - <span data-ttu-id="4b139-116">/保存と SharePoint のプロジェクトをオンラインでは次のように、(ただしに制限されていません) をデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4b139-116">Access data that is in/stored in Project Online or SharePoint such as (but is not limited to):</span></span>  
  - <span data-ttu-id="4b139-117">ユーザー設定フィールド</span><span class="sxs-lookup"><span data-stu-id="4b139-117">Custom fields</span></span>  
  - <span data-ttu-id="4b139-118">リスト</span><span class="sxs-lookup"><span data-stu-id="4b139-118">Lists</span></span>
    
- <span data-ttu-id="4b139-119">プロジェクト (SharePoint) プロバイダーがホストを追加で。</span><span class="sxs-lookup"><span data-stu-id="4b139-119">For a Project (SharePoint) provider-hosted add-in:</span></span>
    
  - <span data-ttu-id="4b139-120">プロジェクトのオンライン サイトに外部のサイト上に存在するコード</span><span class="sxs-lookup"><span data-stu-id="4b139-120">Code that exists on a site external to the Project Online site</span></span> 
  - <span data-ttu-id="4b139-121">外部のサイトをすることができます (ただしに制限されていません)。</span><span class="sxs-lookup"><span data-stu-id="4b139-121">An external site, which can be (but is not limited to):</span></span>  
  - <span data-ttu-id="4b139-122">別の SharePoint サイト</span><span class="sxs-lookup"><span data-stu-id="4b139-122">Another SharePoint site</span></span>  
  - <span data-ttu-id="4b139-123">任意のプラットフォーム上に構築された web アプリケーションとサービス</span><span class="sxs-lookup"><span data-stu-id="4b139-123">Web App/Service built on any platform</span></span>  
  - <span data-ttu-id="4b139-124">外部のサイトには、ビジネス ロジックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b139-124">The external site contains business logic</span></span>  
  - <span data-ttu-id="4b139-125">プロジェクト オンラインへのアクセス トークンを持つ外部のサイトにブラウザーがリダイレクトからプロジェクト オンライン</span><span class="sxs-lookup"><span data-stu-id="4b139-125">The browser is redirected from Project Online to external site with access tokens to Project Online</span></span>  
  - <span data-ttu-id="4b139-126">外部のサイトは、SharePoint とオンライン プロジェクトへの呼び出しを行うことが</span><span class="sxs-lookup"><span data-stu-id="4b139-126">The external site can make calls to SharePoint and Project Online</span></span>
    
- <span data-ttu-id="4b139-127">外部またはスタンドアロンのアドインの場合。</span><span class="sxs-lookup"><span data-stu-id="4b139-127">For an external/standalone add-in:</span></span>
    
  - <span data-ttu-id="4b139-128">ユーザーがそのデバイスでアプリケーションを実行します。</span><span class="sxs-lookup"><span data-stu-id="4b139-128">User executes an application on their device</span></span>
  - <span data-ttu-id="4b139-129">アプリケーションを認証し、プロジェクトのオンライン Api を直接呼び出す</span><span class="sxs-lookup"><span data-stu-id="4b139-129">Application authenticates and calls Project Online APIs directly</span></span>
    

|<span data-ttu-id="4b139-130">アプリケーションの種類</span><span class="sxs-lookup"><span data-stu-id="4b139-130">Type of application</span></span>|<span data-ttu-id="4b139-131">API の実装</span><span class="sxs-lookup"><span data-stu-id="4b139-131">API implementation</span></span>|<span data-ttu-id="4b139-132">ターゲット環境</span><span class="sxs-lookup"><span data-stu-id="4b139-132">Target environment</span></span>|<span data-ttu-id="4b139-133">アプリケーションの例</span><span class="sxs-lookup"><span data-stu-id="4b139-133">Application examples</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="4b139-134">ホストされているプロジェクト</span><span class="sxs-lookup"><span data-stu-id="4b139-134">Project hosted</span></span>  <br/> |<span data-ttu-id="4b139-135">JSOM (Java スクリプト オブジェクト モデル)</span><span class="sxs-lookup"><span data-stu-id="4b139-135">JSOM (Java Script Object Model)</span></span>  <br/> <span data-ttu-id="4b139-136">REST</span><span class="sxs-lookup"><span data-stu-id="4b139-136">REST</span></span>  <br/> |<span data-ttu-id="4b139-137">ブラウザー</span><span class="sxs-lookup"><span data-stu-id="4b139-137">Browser</span></span>  <br/> |<span data-ttu-id="4b139-138">タイムカードの入力</span><span class="sxs-lookup"><span data-stu-id="4b139-138">Timecard entry</span></span>  <br/> <span data-ttu-id="4b139-139">タイムカードの承認</span><span class="sxs-lookup"><span data-stu-id="4b139-139">Timecard approval</span></span>  <br/> <span data-ttu-id="4b139-140">プロジェクトの進捗状況</span><span class="sxs-lookup"><span data-stu-id="4b139-140">Project Status</span></span>  <br/> <span data-ttu-id="4b139-141">問題に関するレポート</span><span class="sxs-lookup"><span data-stu-id="4b139-141">Issues Report</span></span>  <br/> |
|<span data-ttu-id="4b139-142">ホストされるプロバイダーのプロジェクト</span><span class="sxs-lookup"><span data-stu-id="4b139-142">Project Provider Hosted</span></span>  <br/> |<span data-ttu-id="4b139-143">CSOM クライアント ライブラリ</span><span class="sxs-lookup"><span data-stu-id="4b139-143">CSOM client library</span></span>  <br/> |<span data-ttu-id="4b139-144">Azure の web サイト/アプリケーション</span><span class="sxs-lookup"><span data-stu-id="4b139-144">Azure Website/App</span></span>  <br/> <span data-ttu-id="4b139-145">Windows 以外の環境 (照明器具など)</span><span class="sxs-lookup"><span data-stu-id="4b139-145">Non-Windows environment (LAMP, etc.)</span></span>  <br/> |<span data-ttu-id="4b139-146">外部タイムシートの検証</span><span class="sxs-lookup"><span data-stu-id="4b139-146">External timesheet validator</span></span>  <br/> <span data-ttu-id="4b139-147">プロジェクト インポート機能</span><span class="sxs-lookup"><span data-stu-id="4b139-147">Project Importer</span></span>  <br/> |
|<span data-ttu-id="4b139-148">外部/スタンドアロン</span><span class="sxs-lookup"><span data-stu-id="4b139-148">External/Standalone</span></span>  <br/> |<span data-ttu-id="4b139-149">REST</span><span class="sxs-lookup"><span data-stu-id="4b139-149">REST</span></span>  <br/> <span data-ttu-id="4b139-150">CSOM</span><span class="sxs-lookup"><span data-stu-id="4b139-150">CSOM</span></span>  <br/> |<span data-ttu-id="4b139-151">残りのすべてのプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="4b139-151">REST - any platform</span></span>  <br/> <span data-ttu-id="4b139-152">CSOM の任意の .NET がサポートされているプラットフォーム</span><span class="sxs-lookup"><span data-stu-id="4b139-152">CSOM - any .NET supported platform</span></span>  <br/> |<span data-ttu-id="4b139-153">タイムカードの入力</span><span class="sxs-lookup"><span data-stu-id="4b139-153">Timecard entry</span></span>  <br/> <span data-ttu-id="4b139-154">新しいサイトへのプロジェクトの移行</span><span class="sxs-lookup"><span data-stu-id="4b139-154">Migration of projects to a new site</span></span>  <br/> <span data-ttu-id="4b139-155">管理のステータスを変更します。</span><span class="sxs-lookup"><span data-stu-id="4b139-155">Change Management Status.</span></span>  <br/> |
   
## <a name="what-does-it-take-to-start-developing-applications-for-project-online"></a><span data-ttu-id="4b139-156">オンライン プロジェクトのアプリケーションの開発を開始するのには何が必要でしょうか。</span><span class="sxs-lookup"><span data-stu-id="4b139-156">What does it take to start developing applications for Project Online?</span></span>

<span data-ttu-id="4b139-157">プロジェクトのオンライン アプリケーションを開発するために必要な一般的な項目では、プロジェクトのオンライン アカウントには、プロジェクトおよびプロジェクトに関連する情報の割り当て、タスク、リソース、およびユーザー設定フィールドを含むデータをテストします。</span><span class="sxs-lookup"><span data-stu-id="4b139-157">The common items needed for developing Project Online applications are a Project Online account and test data--projects and project-related information that include assignments, tasks, resources, and custom fields.</span></span> <span data-ttu-id="4b139-158">同様に、開発環境が必要ですが、開発環境の詳細については、アプリケーションとアプリケーションに必要な API インターフェイスの種類によって異なります。</span><span class="sxs-lookup"><span data-stu-id="4b139-158">A development environment is needed as well, but specifics of the development environment depend on the type of application and the API interface needed for the application.</span></span> <span data-ttu-id="4b139-159">次のセクションでは、次の 3 つの API インタ フェースの開発のニーズについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b139-159">The next few sections describe development needs for the three API interfaces.</span></span>
  
<span data-ttu-id="4b139-160">リファレンス ドキュメントでは、すべての 3 つのインターフェイスとオブジェクト モデルのコンポーネント間の関係を示すエンティティ マップの一般的なオブジェクト モデルについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b139-160">The reference documentation describes the object model that is common for all three interfaces, as well as an entity map that shows relations among the object model components.</span></span>
  
## <a name="project-hosted-add-in-development-environment"></a><span data-ttu-id="4b139-161">プロジェクトのアドインの開発環境をホストします。</span><span class="sxs-lookup"><span data-stu-id="4b139-161">Project hosted add-in development environment</span></span>

<span data-ttu-id="4b139-162">ホストされているアドインには、サーバー上に存在すると、ランタイムの実行のためのブラウザーにダウンロードするアドインが。</span><span class="sxs-lookup"><span data-stu-id="4b139-162">A hosted add-in is an add-in that resides on the server and is downloaded to a browser for runtime execution.</span></span> <span data-ttu-id="4b139-163">ホストのアドインでは、JSOM またはそれ以外のインターフェイスを使用することができ、JavaScript で書かれています。</span><span class="sxs-lookup"><span data-stu-id="4b139-163">Hosted add-ins can use the JSOM or REST interfaces and are written in JavaScript.</span></span> <span data-ttu-id="4b139-164">プロジェクトのオンラインでは、ランタイムの実行の JSOM ライブラリへの参照を提供します。</span><span class="sxs-lookup"><span data-stu-id="4b139-164">Project Online provides references to the JSOM library for runtime execution.</span></span> <span data-ttu-id="4b139-165">前提とすると開発は、Windows プラットフォームで必要なリソースには。</span><span class="sxs-lookup"><span data-stu-id="4b139-165">Assuming development is on a Windows platform, the needed resources follow:</span></span>
  
- <span data-ttu-id="4b139-166">Visual Studio の 2015 (推奨) または Visual Studio の 2013</span><span class="sxs-lookup"><span data-stu-id="4b139-166">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span>
    
- <span data-ttu-id="4b139-167">Visual Studio の Office 開発ツール</span><span class="sxs-lookup"><span data-stu-id="4b139-167">Office development tools for Visual Studio</span></span>
    
- <span data-ttu-id="4b139-168">JavaScript 言語</span><span class="sxs-lookup"><span data-stu-id="4b139-168">JavaScript language</span></span>
    
<span data-ttu-id="4b139-169">参照してくださいhttps://github.com/OfficeDev/Project-JSOM-Copy-Work-Packagesサンプル アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="4b139-169">Visit https://github.com/OfficeDev/Project-JSOM-Copy-Work-Packages for a sample application.</span></span> 
  
<span data-ttu-id="4b139-170">ダウンロードして、いくつかの簡単な手順でサンプルを実行します。</span><span class="sxs-lookup"><span data-stu-id="4b139-170">You can download and run the sample in a few easy steps:</span></span>
  
1. <span data-ttu-id="4b139-171">ダウンロードしてサンプル アプリケーションを開く</span><span class="sxs-lookup"><span data-stu-id="4b139-171">Download and open the sample application</span></span>
    
2. <span data-ttu-id="4b139-172">[SiteURL プロパティ] ウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="4b139-172">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="4b139-173">プロジェクトのオンラインでは、アドインとホストでプロジェクトのオンライン情報へのアクセスを管理するユーザーのアクセス許可の両方のアプリケーションのスコープについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b139-173">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="4b139-174">設定のいずれかまたは両方のアクセスを明示的に拒否すると、オンライン プロジェクトを拒否、情報へのアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4b139-174">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="4b139-175">それ以外の場合、アクセスが与えられます。</span><span class="sxs-lookup"><span data-stu-id="4b139-175">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="4b139-176">サイト上の sideloading を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4b139-176">Enable sideloading on your site.</span></span> <span data-ttu-id="4b139-177">[アプリケーション開発のプロジェクトのオンラインを構成する](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)詳細についてを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b139-177">See the [Configuring Project Online for App Development ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)article for more information.</span></span> 
    
4. <span data-ttu-id="4b139-178">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="4b139-178">Build the project.</span></span>
    
5. <span data-ttu-id="4b139-179">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="4b139-179">Run the project.</span></span>
    
## <a name="project-provider-hosted-add-in-development-environment"></a><span data-ttu-id="4b139-180">プロジェクトのプロバイダーでホストされているアドインの開発環境</span><span class="sxs-lookup"><span data-stu-id="4b139-180">Project provider-hosted add-in development environment</span></span>

<span data-ttu-id="4b139-181">プロバイダーがホストされているアドインは、作成されたアプリケーションおよび web プラットフォーム上に存在します。</span><span class="sxs-lookup"><span data-stu-id="4b139-181">Provider hosted add-ins are applications written and residing on any web platform.</span></span> <span data-ttu-id="4b139-182">接続でき、残りの部分 (またはマイクロソフトのプラットフォームの CSOM) を使用してデータ操作を実行する API です。</span><span class="sxs-lookup"><span data-stu-id="4b139-182">They can connect and perform data operations using the REST (or CSOM for Microsoft platforms) API.</span></span> <span data-ttu-id="4b139-183">任意の言語と REST インターフェイスをサポートする環境は、開発に使用できます。</span><span class="sxs-lookup"><span data-stu-id="4b139-183">Any language and environment that supports the REST interface can be used for development.</span></span> 
  
<span data-ttu-id="4b139-184">この種のアプリケーションに対して Windows 開発環境の例には、次の項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b139-184">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
-  <span data-ttu-id="4b139-185">Visual Studio の 2015 (推奨) または Visual Studio の 2013</span><span class="sxs-lookup"><span data-stu-id="4b139-185">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="4b139-186">(Visual Studio の 2015 プロフェッショナルおよびエンタープライズ エディションに付属している)、Visual Studio 用の Microsoft Office の開発ツール</span><span class="sxs-lookup"><span data-stu-id="4b139-186">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="4b139-187">4.0 またはそれ以降の.NET Framework</span><span class="sxs-lookup"><span data-stu-id="4b139-187">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="4b139-188">[SharePointOnline CSOM パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx)(CSOM 呼び出し) の</span><span class="sxs-lookup"><span data-stu-id="4b139-188">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="4b139-189">C# などのプログラミング言語</span><span class="sxs-lookup"><span data-stu-id="4b139-189">A programming language, such as C#</span></span> 
    
<span data-ttu-id="4b139-190">参照してくださいhttps://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperationsのサンプル スクリプトを使用します。</span><span class="sxs-lookup"><span data-stu-id="4b139-190">Visit https://github.com/OfficeDev/Project-Add-in-REST-BasicDataOperations for working sample scripts.</span></span> 
  
<span data-ttu-id="4b139-191">いくつかの手順でサンプルを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="4b139-191">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="4b139-192">ダウンロードしてサンプル アプリケーションを開く</span><span class="sxs-lookup"><span data-stu-id="4b139-192">Download and open the sample application</span></span>
    
2. <span data-ttu-id="4b139-193">[SiteURL プロパティ] ウィンドウを更新します。</span><span class="sxs-lookup"><span data-stu-id="4b139-193">Update the SiteURL in the Properties window</span></span>
    
   <span data-ttu-id="4b139-194">プロジェクトのオンラインでは、アドインとホストでプロジェクトのオンライン情報へのアクセスを管理するユーザーのアクセス許可の両方のアプリケーションのスコープについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4b139-194">Project Online examines both the application scope of the add-in and the user permissions to govern access to information on the Project Online host.</span></span> <span data-ttu-id="4b139-195">設定のいずれかまたは両方のアクセスを明示的に拒否すると、オンライン プロジェクトを拒否、情報へのアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4b139-195">If access is explicitly denied in either or both settings, Project Online denies access to the information.</span></span> <span data-ttu-id="4b139-196">それ以外の場合、アクセスが与えられます。</span><span class="sxs-lookup"><span data-stu-id="4b139-196">Otherwise, access is granted.</span></span>
    
3. <span data-ttu-id="4b139-197">サイト上の sideloading を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4b139-197">Enable sideloading on your site.</span></span> <span data-ttu-id="4b139-198">[アプリケーション開発のプロジェクトのオンラインを構成する](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)詳細についてを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b139-198">See the [Configuring Project Online for App Development ](http://nearbaseline.com/2013/12/configuring-project-online-for-app-development/.aspx)article for more information.</span></span> 
    
4. <span data-ttu-id="4b139-199">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="4b139-199">Build the project.</span></span>
    
5. <span data-ttu-id="4b139-200">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="4b139-200">Run the project.</span></span>
    
## <a name="externalstandalone-application-development-environment"></a><span data-ttu-id="4b139-201">外部とスタンドアロン アプリケーションの開発環境</span><span class="sxs-lookup"><span data-stu-id="4b139-201">External/standalone application development environment</span></span>

<span data-ttu-id="4b139-202">スタンドアロン アプリケーションでは、呼び出しを作成、取得、更新、オンライン プロジェクトと通信するクライアント側オブジェクト モデル (CSOM) または他の部分を使用してプロジェクト オンラインでき、サーバー上に存在する情報を削除することができます。</span><span class="sxs-lookup"><span data-stu-id="4b139-202">A standalone application can call Project Online using the Client Side Object Model (CSOM) or REST to communicate with Project Online to create, retrieve, update, and delete information residing on the server.</span></span> <span data-ttu-id="4b139-203">これは、スタンドアロンのクライアント アプリケーションを実行するユーザーのアクセス レベルに依存しています。</span><span class="sxs-lookup"><span data-stu-id="4b139-203">This is a standalone client application that depends on the user access level to run.</span></span> 
  
<span data-ttu-id="4b139-204">この種のアプリケーションに対して Windows 開発環境の例には、次の項目が含まれています。</span><span class="sxs-lookup"><span data-stu-id="4b139-204">An example of the Windows development environment for this type of application includes the following items:</span></span>
  
- <span data-ttu-id="4b139-205">Visual Studio の 2015 (推奨) または Visual Studio の 2013</span><span class="sxs-lookup"><span data-stu-id="4b139-205">Visual Studio 2015 (preferred) or Visual Studio 2013</span></span> 
    
- <span data-ttu-id="4b139-206">(Visual Studio の 2015 プロフェッショナルおよびエンタープライズ エディションに付属している)、Visual Studio 用の Microsoft Office の開発ツール</span><span class="sxs-lookup"><span data-stu-id="4b139-206">Microsoft Office Development Tools for Visual Studio (supplied with Visual Studio 2015 Professional and Enterprise editions)</span></span>
    
- <span data-ttu-id="4b139-207">4.0 またはそれ以降の.NET Framework</span><span class="sxs-lookup"><span data-stu-id="4b139-207">.NET Framework 4.0 or newer</span></span>
    
- <span data-ttu-id="4b139-208">[SharePointOnline CSOM パッケージ](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx)(CSOM 呼び出し) の</span><span class="sxs-lookup"><span data-stu-id="4b139-208">[SharePointOnline CSOM package](https://www.nuget.org/packages/Microsoft.SharePointOnline.CSOM/.aspx) (for CSOM calls)</span></span> 
    
- <span data-ttu-id="4b139-209">C# などのプログラミング言語</span><span class="sxs-lookup"><span data-stu-id="4b139-209">A programming language, such as C#</span></span> 
    
<span data-ttu-id="4b139-210">参照してくださいhttps://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFieldsサンプル アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="4b139-210">Visit https://github.com/OfficeDev/Project-CSOM-Read-Enterprise-CustomFields for a sample application.</span></span> 
  
<span data-ttu-id="4b139-211">いくつかの手順でサンプルを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="4b139-211">You can run the sample in a few steps:</span></span>
  
1. <span data-ttu-id="4b139-212">サンプル アプリケーションをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="4b139-212">Download the sample application</span></span>
    
2. <span data-ttu-id="4b139-213">いくつかのプロジェクトのオンライン サイトにアクセスして変更を加えるなど、サイト名、ユーザー アカウント、およびパスワード。</span><span class="sxs-lookup"><span data-stu-id="4b139-213">Make a couple of changes to access your Project Online site—the site name, user account, and password.</span></span>
    
   <span data-ttu-id="4b139-214">ユーザーがすべてのプロジェクトへのアクセス権を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="4b139-214">Ensure the user has access to all projects.</span></span> <span data-ttu-id="4b139-215">プロジェクトのオンラインでは、データ ストア内の情報へのアクセスを管理するのにユーザーのアクセス許可を使用します。</span><span class="sxs-lookup"><span data-stu-id="4b139-215">Project Online uses user permissions to govern access to information in the data store.</span></span>
    
3. <span data-ttu-id="4b139-216">Nuget パッケージ マネージャー コンソールでは、Nuget のコンソールで、次を入力して [ツール] メニューから利用可能なを使用して参照するには、SharePoint アセンブリを追加します。</span><span class="sxs-lookup"><span data-stu-id="4b139-216">Add the SharePoint assembly to the references using the Nuget Package Manager Console, available from the Tools menu by typing the following in the Nuget console:</span></span> 
    
   `Install-Package Microsoft.SharePointOnline.CSOM`

4. <span data-ttu-id="4b139-217">プロジェクトをビルドします。</span><span class="sxs-lookup"><span data-stu-id="4b139-217">Build the project.</span></span>
    
5. <span data-ttu-id="4b139-218">プロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="4b139-218">Run the project.</span></span>
    
## <a name="next-steps"></a><span data-ttu-id="4b139-219">次の手順</span><span class="sxs-lookup"><span data-stu-id="4b139-219">Next steps</span></span>

<span data-ttu-id="4b139-220">各サンプル アプリケーションでは、プロジェクトの個々 の API の使用の主な特徴を説明する記事があります。</span><span class="sxs-lookup"><span data-stu-id="4b139-220">Each sample application has an article to explain the highlights of working with the individual Project API.</span></span> <span data-ttu-id="4b139-221">記事は、次の一覧とは、エンティティの関連付けを記述するいくつかの記事については、クエリ システム、およびユーザー設定フィールドへのアクセスに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4b139-221">The articles appear in the following list, along with a few articles that describe the entity relationships, information on the query system, and accessing Custom Fields.</span></span> 
  
- [<span data-ttu-id="4b139-222">クライアント側オブジェクト モデルを使用してプロジェクトのオンライン アプリケーションの開発</span><span class="sxs-lookup"><span data-stu-id="4b139-222">Developing a Project Online Application Using the Client-side Object Model</span></span>](developing-a-project-online-application-using-the-client-side-object-model.md)
    
- [<span data-ttu-id="4b139-223">プロジェクトのオンライン追加の JavaScript オブジェクト モデル (JSOM) を使用して開発</span><span class="sxs-lookup"><span data-stu-id="4b139-223">Developing a Project Online add-in using the JavaScript Object Model (JSOM)</span></span>](developing-a-project-online-add-in-using-the-javascript-object-model-jsom.md)
    
- [<span data-ttu-id="4b139-224">オンライン プロジェクトのエンタープライズ ユーザー設定フィールドにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="4b139-224">Accessing Project Online enterprise custom fields</span></span>](accessing-project-online-enterprise-custom-fields.md)
    
## <a name="see-also"></a><span data-ttu-id="4b139-225">関連項目</span><span class="sxs-lookup"><span data-stu-id="4b139-225">See also</span></span>

<span data-ttu-id="4b139-226">ドキュメントとオンライン プロジェクトと CSOM を使用したアプリケーション開発に関連するサンプルでは、[プロジェクト開発のポータル](http://dev.office.com/project.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4b139-226">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](http://dev.office.com/project.aspx).</span></span>
    

