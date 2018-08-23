---
title: クライアント側オブジェクト モデルを使用してプロジェクトのオンライン アプリケーションを開発
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: この資料では、デスクトップ アプリケーションを.NET Framework 4.0 を使用してプロジェクトをオンラインでマイクロソフトのアプリケーション開発について説明します。 この資料に記載されているアプリケーションは、ホストしているサーバーから情報を取得します。
ms.openlocfilehash: a65dbbdedb371fae9b8f0b99ea113ae38cbaffb5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572880"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a><span data-ttu-id="72fed-104">クライアント側オブジェクト モデルを使用してプロジェクトのオンライン アプリケーションを開発</span><span class="sxs-lookup"><span data-stu-id="72fed-104">Developing a Project Online application using the client-side object model</span></span>

<span data-ttu-id="72fed-105">この資料では、デスクトップ アプリケーションを.NET Framework 4.0 を使用してプロジェクトをオンラインでマイクロソフトのアプリケーション開発について説明します。</span><span class="sxs-lookup"><span data-stu-id="72fed-105">This article describes Microsoft Project Online application development for desktop applications using the .NET Framework 4.0.</span></span> <span data-ttu-id="72fed-106">この資料に記載されているアプリケーションは、ホストしているサーバーから情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-106">The application described in this article retrieves information from the hosting server.</span></span> 
  
## <a name="background"></a><span data-ttu-id="72fed-107">背景</span><span class="sxs-lookup"><span data-stu-id="72fed-107">Background</span></span>

<span data-ttu-id="72fed-108">Microsoft Project では、1990 年代初頭にデスクトップ アプリケーションとして起動されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-108">Microsoft Project started as desktop application in the early 1990's.</span></span> <span data-ttu-id="72fed-109">今日では、プロジェクトが多く、決まって述べるが、いくつかの種類です。</span><span class="sxs-lookup"><span data-stu-id="72fed-109">Today, Project is much more, as its several varieties attest:</span></span>
  
- <span data-ttu-id="72fed-110">プロジェクトの標準的なエディションは、スタンドアロン アプリケーションとして実行されるデスクトップ アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="72fed-110">Project standard edition is a desktop application that runs as a stand-alone application.</span></span>
    
- <span data-ttu-id="72fed-111">プロフェッショナル エディションのプロジェクトが可能な対話と規模が大きく、サーバーとデータを共有、プロジェクトの標準のエディションの機能を実行するデスクトップ アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="72fed-111">Project professional edition is a desktop application that can interact and share data with a server on a larger scale, as well as perform the functionality found in Project standard edition.</span></span>
    
- <span data-ttu-id="72fed-112">プロジェクト オンラインは、調整し、プロジェクト、プログラム、およびポートフォリオを管理する PMO レベルのソリューションは、企業がマイクロソフトによってホストされるサービスです。</span><span class="sxs-lookup"><span data-stu-id="72fed-112">Project Online is a Microsoft-hosted service that provides companies with a PMO-level solution to coordinate and manage projects, programs, and portfolios.</span></span> <span data-ttu-id="72fed-113">デスクトップのエディションでは、オンラインのプロジェクトよりもさまざまなソリューションでは、管理でき、プロジェクトのライフ サイクル全体にわたってプロジェクトの詳細を追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="72fed-113">A different offering than the desktop editions, Project Online can maintain and track project details throughout the life of a project.</span></span> 
    
- <span data-ttu-id="72fed-114">Project Server は、エンタープライズでホストされているサービスを企業が管理し、プロジェクト、プログラム、およびポートフォリオ情報を含むサーバーをセキュリティで保護です。</span><span class="sxs-lookup"><span data-stu-id="72fed-114">Project Server is an enterprise-hosted service in which the enterprise manages and secures the server containing project, program, and portfolio information.</span></span> <span data-ttu-id="72fed-115">社内でのサーバーをセキュリティで保護するための project Server には、プロジェクト、プログラム、および外部でホストされているプロジェクト、オンラインでのカスタマイズの容量を増やすのポートフォリオの中心の機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="72fed-115">Project Server, by virtue of securing the server in-house, offers the project, program, and portfolio oriented features of externally-hosted Project Online with a greater capacity for customization.</span></span>
    
<span data-ttu-id="72fed-116">オンラインのプロジェクトには、オンラインの 3 つの API セットが含まれて: クライアント側オブジェクト モデル (CSOM)、JavaScript オブジェクト モデル (JSOM)、および主要な状態を転送 (残りの部分)。</span><span class="sxs-lookup"><span data-stu-id="72fed-116">Project Online has three online API sets: Client-side Object Model (CSOM), JavaScript Object Model (JSOM), and Representational State Transfer (REST).</span></span> 
  
- <span data-ttu-id="72fed-117">CSOM の .NET の実装は、テナントのプロジェクトをオンラインでやり取りする Windows アプリケーションを開発するときの推奨されるインターフェイスです。</span><span class="sxs-lookup"><span data-stu-id="72fed-117">The .NET CSOM implementation is the preferred interface when developing Windows applications that interact with Project Online tenants.</span></span> <span data-ttu-id="72fed-118">ユーザー中心型のアプリケーションの一般的な環境には、Windows デスクトップおよび Microsoft Surface のデバイスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="72fed-118">Typical environments for user-centric applications include Windows desktops and Microsoft Surface devices.</span></span> <span data-ttu-id="72fed-119">CSOM を .NET で記述されたバックエンド ・ アプリケーションは、ビジネス ロジックとデータ ソースの外部プロジェクトをオンラインにある他のサーバーに接続できます。</span><span class="sxs-lookup"><span data-stu-id="72fed-119">Back-end applications written with .NET CSOM can connect to other servers for business logic and data sources that are external to Project Online.</span></span> <span data-ttu-id="72fed-120">プロジェクトのオンライン検索要求は、基本的な検索機能をいくつかの拡張機能を提供する LINQ のようなクエリ システムを使用します。</span><span class="sxs-lookup"><span data-stu-id="72fed-120">Retrieval requests to Project Online use a LINQ-like query system that offers several enhancements over basic retrieval functions.</span></span>
    
- <span data-ttu-id="72fed-121">JavaScript オブジェクト モデル (JSOM) インターフェイスは、アドイン プロジェクトをオンラインでブラウザー間のサポートを提供します。アドインをプロジェクトのオンラインのテナントに格納されている web アプリケーションです。</span><span class="sxs-lookup"><span data-stu-id="72fed-121">The JavaScript Object Model (JSOM) interface provides cross-browser support for Project Online Add-ins. An add-in is a web application that is stored in the Project Online tenant.</span></span> <span data-ttu-id="72fed-122">ユーザーがアドインを実行しようとすると、アドインのコードがダウンロードされ、ユーザーのマシン上のブラウザーで実行されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-122">When a user wants to run an add-in, the code for the add-in downloads and runs in the browser on the user machine.</span></span> 
    
- <span data-ttu-id="72fed-123">残りの部分と Odata のモデルでは、HTTP ベースの通信を提供するこのインターフェイスは Windows 以外の環境でアプリケーションをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="72fed-123">The REST/Odata model provides HTTP-based communication, This interface is recommended for applications in non-Windows environments.</span></span> <span data-ttu-id="72fed-124">通信のエンドポイントは、プロジェクト Web アプリケーション (PWA) サイト内のオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="72fed-124">Communication endpoints are the objects in the Project Web Application (PWA) site.</span></span> <span data-ttu-id="72fed-125">結果は、通常の HTTP ステータス コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="72fed-125">Results provide normal HTTP status codes.</span></span>
    
<span data-ttu-id="72fed-126">この資料では、CSOM の .NET インターフェイスを使用するアプリケーションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="72fed-126">This article focuses on an application that uses the .NET CSOM interface.</span></span>
  
## <a name="prerequisites"></a><span data-ttu-id="72fed-127">前提条件</span><span class="sxs-lookup"><span data-stu-id="72fed-127">Prerequisites</span></span>

<span data-ttu-id="72fed-128">10 を Windows を実行しているベースのシステムで起動し、次の項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-128">Start with a base system running Windows 10, and add the following items:</span></span>
  
- <span data-ttu-id="72fed-129">.Net framework 4.0 以降--は、完全なフレームワークを使用します。</span><span class="sxs-lookup"><span data-stu-id="72fed-129">.Net Framework 4.0 or later -- Use the complete framework.</span></span> <span data-ttu-id="72fed-130">ダウンロード サイトは、 https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx。</span><span class="sxs-lookup"><span data-stu-id="72fed-130">The download site is https://msdn.microsoft.com/en-us/vstudio/aa496123.aspx.</span></span>
    
- <span data-ttu-id="72fed-131">2013 以降--Visual Studio の任意のエディションは、許容されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-131">Visual Studio 2013 or later -- Any edition is acceptable.</span></span> <span data-ttu-id="72fed-132">Visual Studio 2015 の community edition は、サンプル アプリケーションを開発する使用されました。</span><span class="sxs-lookup"><span data-stu-id="72fed-132">The community edition of Visual Studio 2015 was used to develop the sample application.</span></span> <span data-ttu-id="72fed-133">Community edition は、 https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx。</span><span class="sxs-lookup"><span data-stu-id="72fed-133">The community edition is available at https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx.</span></span>
    
- <span data-ttu-id="72fed-134">SDK - オンラインのプロジェクトと Project Server の SharePoint クライアント コンポーネントは、SharePoint、および SharePoint の上にアセンブリを配置できます。</span><span class="sxs-lookup"><span data-stu-id="72fed-134">SharePoint Client Components SDK -- Project Online and Project Server sit on top of SharePoint, and SharePoint assemblies.</span></span> <span data-ttu-id="72fed-135">Visual Studio のプロフェッショナルおよびエンタープライズ エディションでは、SharePoint クライアント コンポーネントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="72fed-135">The SharePoint Client Components are included in Visual Studio Professional and Enterprise editions.</span></span> <span data-ttu-id="72fed-136">コミュニティの Visual Studio エディションを使用すると、Office 開発者ツールの SDK の最新バージョンがあるか、次のサイト: https://www.microsoft.com/en-us/download/details.aspx?id=35585。</span><span class="sxs-lookup"><span data-stu-id="72fed-136">If you use Visual Studio Community edition, the latest version of the Office Developer Tools SDK is available at the following site: https://www.microsoft.com/en-us/download/details.aspx?id=35585.</span></span>
    
- <span data-ttu-id="72fed-137">プロジェクトのオンライン アカウントの場合は - これは、ホスティング サイトへのアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="72fed-137">A Project Online account -- This provides access to the hosting site.</span></span> <span data-ttu-id="72fed-138">プロジェクトのオンライン アカウントを取得する方法についてを参照してくださいhttps://products.office.com/en-us/Project/project-online-portfolio-management。</span><span class="sxs-lookup"><span data-stu-id="72fed-138">For more information about obtaining a Project Online account, see https://products.office.com/en-us/Project/project-online-portfolio-management.</span></span>
    
- <span data-ttu-id="72fed-139">情報が設定されているホスト サイト上のプロジェクト</span><span class="sxs-lookup"><span data-stu-id="72fed-139">Projects on the hosting site that are populated with information</span></span>
    
> [!NOTE]
> <span data-ttu-id="72fed-140">標準 (4.0 またはそれ以降) に、.NET Framework は、使用する正しいフレームワークです。</span><span class="sxs-lookup"><span data-stu-id="72fed-140">The standard .NET Framework (4.0 or later) is the correct framework to use.</span></span> <span data-ttu-id="72fed-141">.NET Framework 4 のクライアント プロファイルを使用することはしません。</span><span class="sxs-lookup"><span data-stu-id="72fed-141">Do not use the .NET Framework 4 Client Profile.</span></span> 
  
## <a name="develop-the-application"></a><span data-ttu-id="72fed-142">アプリケーションを開発します。</span><span class="sxs-lookup"><span data-stu-id="72fed-142">Develop the application</span></span>

<span data-ttu-id="72fed-143">SharePoint のデスクトップ アプリケーションを開発して、希望のインターフェイスは、プロジェクトのクライアント側オブジェクト モデル (CSOM)。</span><span class="sxs-lookup"><span data-stu-id="72fed-143">In developing a desktop application for SharePoint, the preferred interface is the Project client side object model (CSOM).</span></span> 
  
<span data-ttu-id="72fed-144">完全なサンプルをダウンロードすることができますhttps://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks。</span><span class="sxs-lookup"><span data-stu-id="72fed-144">You can download the complete sample at https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks.</span></span>
  
<span data-ttu-id="72fed-145">最初の 2 つのトピックは、基本的な事項を説明します。 適切な名前空間とアセンブリの場合、Visual Studio プロジェクトを作成すると、ホスト サーバーにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="72fed-145">The first two topics cover basic issues: creating a Visual Studio project with appropriate namespaces and assemblies, and accessing the hosting server.</span></span> <span data-ttu-id="72fed-146">残りのトピックと 1 つの多くのオブジェクトから、CSOM を使用して情報を取得する処理です。</span><span class="sxs-lookup"><span data-stu-id="72fed-146">The remaining topics deal with retrieving information through the CSOM, from one and many objects.</span></span> 
  
<span data-ttu-id="72fed-147">クライアント アプリケーションから 2 つのアクションのプロセスは、ホストから情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-147">Retrieving information from the host is a two-action process from client applications.</span></span> <span data-ttu-id="72fed-148">最初に、アプリケーションは指定し、サーバーに 1 つまたは複数の検索要求を送信します。</span><span class="sxs-lookup"><span data-stu-id="72fed-148">First, the application specifies and sends one or more retrieval requests to the server.</span></span> <span data-ttu-id="72fed-149">第 2 に、アプリケーションは、送信されたクエリを実行するサーバーに通知を発行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-149">Second, the application issues a notification to the server to execute the submitted queries.</span></span> <span data-ttu-id="72fed-150">サーバーは、クエリの結果をクライアントに送信することによって応答します。</span><span class="sxs-lookup"><span data-stu-id="72fed-150">The server responds by sending the query results to the client.</span></span>
  
### <a name="set-up-the-visual-studio-project"></a><span data-ttu-id="72fed-151">Visual Studio プロジェクトを設定します</span><span class="sxs-lookup"><span data-stu-id="72fed-151">Set up the Visual Studio project</span></span>

<span data-ttu-id="72fed-152">アプリケーションのセットアップは、新しいプロジェクトを作成する、適切なアセンブリをリンクし、必要な名前空間を宣言することで構成されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-152">The application setup consists of creating a new project, linking the appropriate assemblies and declaring the needed namespaces.</span></span> <span data-ttu-id="72fed-153">Visual Studio には、いくつかの種類の開発プロジェクトが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-153">Visual Studio presents several types of development projects.</span></span> 
  
#### <a name="select-a-visual-studio-project"></a><span data-ttu-id="72fed-154">Visual Studio プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="72fed-154">Select a Visual Studio project</span></span>

1. <span data-ttu-id="72fed-155">Visual Studio を起動し、[開始] ページでは、 **A の新しいプロジェクトを開始**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="72fed-155">Launch Visual Studio and select **Start A New Project** on the Start Page.</span></span> 
    
   <span data-ttu-id="72fed-156">新しいプロジェクト ダイアログ ボックスでは、利用可能なアプリケーション テンプレート、および選択したテンプレートのデータ フィールドを表示します。</span><span class="sxs-lookup"><span data-stu-id="72fed-156">The New Project dialog displays available application templates, and data fields for any selected template.</span></span> 
    
2. <span data-ttu-id="72fed-157">このアプリケーションでは、次の項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="72fed-157">For this application, specify the following items.</span></span> <span data-ttu-id="72fed-158">画面上で発生するキーワードは、太字属性を持ちます。</span><span class="sxs-lookup"><span data-stu-id="72fed-158">Keywords encountered on the screen have a bold attribute:</span></span>
    
   1. <span data-ttu-id="72fed-159">左側のウィンドウでインストールされたテンプレート] から選択して**C#** => **Windows** => **クラシック デスクトップ**です。</span><span class="sxs-lookup"><span data-stu-id="72fed-159">From the Installed templates in the left pane, select **C#** => **Windows** => **Classic desktop**.</span></span> 
    
   2. <span data-ttu-id="72fed-160">中央のウィンドウの上部には、 **.NET Framework 4**を選択します。</span><span class="sxs-lookup"><span data-stu-id="72fed-160">At the top of the central pane, select **.NET Framework 4**.</span></span> 
    
   3. <span data-ttu-id="72fed-161">中央のウィンドウの種類のアプリケーションから、**コンソール アプリケーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="72fed-161">From the application types in the central pane, choose **Console Application**.</span></span> 
    
   4. <span data-ttu-id="72fed-162">下部のセクションで、プロジェクトとソリューション名の場所と名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="72fed-162">In the bottom section, specify a name and location for the project, and a solution name.</span></span> 
    
   5. <span data-ttu-id="72fed-163">下部のセクションで、**ソリューションのディレクトリを作成**チェック ボックスをオンします。</span><span class="sxs-lookup"><span data-stu-id="72fed-163">Also in the bottom section, check the **Create directory for solution** box.</span></span> 
    
3. <span data-ttu-id="72fed-164">初期プロジェクトを作成するのには **[ok]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72fed-164">Click **OK** to create the initial project.</span></span> 
    
#### <a name="add-assemblies"></a><span data-ttu-id="72fed-165">アセンブリを追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-165">Add assemblies</span></span>

<span data-ttu-id="72fed-166">VS ソリューションには、ProjectServerClient アセンブリ プロジェクト 2103 SDK では、アセンブリが SharePoint SDK、および System.Security の.NET Framework アセンブリの 2 つが必要があります。</span><span class="sxs-lookup"><span data-stu-id="72fed-166">The VS solution needs the ProjectServerClient assembly from the Project 2103 SDK, a couple of assemblies from the SharePoint SDK, and the .NET Framework System.Security assembly.</span></span>
  
1. <span data-ttu-id="72fed-167">VS ソリューション エクスプ ローラーで参照のエントリを右クリックし、**参照の追加]** を選択</span><span class="sxs-lookup"><span data-stu-id="72fed-167">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="72fed-168">ショートカット メニューの。</span><span class="sxs-lookup"><span data-stu-id="72fed-168">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="72fed-169">**Microsoft.ProjectServer.Client.dll**を確認してください。</span><span class="sxs-lookup"><span data-stu-id="72fed-169">Check the **Microsoft.ProjectServer.Client.dll**.</span></span> 
    
   <span data-ttu-id="72fed-170">必要な場合は、**参照...** ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72fed-170">If needed, click the **Browse…**</span></span> <span data-ttu-id="72fed-171">ダイアログ ボックスの下部にあるボタンをクリックし、アセンブリを検索するのには Project 2013 SDK のインストール ディレクトリに移動します。</span><span class="sxs-lookup"><span data-stu-id="72fed-171">button at the bottom of the dialog and navigate to the Project 2013 SDK installation directory to locate the assembly.</span></span> 
    
3. <span data-ttu-id="72fed-172">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72fed-172">Click **OK**.</span></span> 
    
4. <span data-ttu-id="72fed-173">.Cs ファイルには、PrjoctServer クライアント名前空間を追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-173">Add the PrjoctServer Client namespace to the .cs file.</span></span>
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

<span data-ttu-id="72fed-174">NuGet パッケージ マネージャー コンソールを使用して SharePoint 2013 SDK のアセンブリを追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-174">Add the SharePoint 2013 SDK assemblies using the NuGet Package Manager Console.</span></span> 
  
1. <span data-ttu-id="72fed-175">VS ツール] メニューから、次のメニューをクリックします:**ツール =\> NuGet パッケージ マネージャー =\>パッケージ マネージャー コンソール**。</span><span class="sxs-lookup"><span data-stu-id="72fed-175">From the VS Tools menu, click the following menus: **Tools =\> NuGet Package Manager =\> Package Manager Console**.</span></span> 
    
2. <span data-ttu-id="72fed-176">パッケージ マネージャー コンソールで、次のコマンドとキーを押してを入力してください\<入力\>。</span><span class="sxs-lookup"><span data-stu-id="72fed-176">In the Package Manager Console, enter the following command and press \<ENTER\>:</span></span>
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   <span data-ttu-id="72fed-177">**パッケージ マネージャー コンソール**には、コマンドの結果の説明が用意されています。VS のソリューション エクスプ ローラーでは、プロジェクト参照に SharePoint のアセンブリが表示されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-177">The **Package Manager Console** provides a description of the command results; and, the VS Solution Explorer displays the SharePoint assemblies in the project references.</span></span> 
    
3. <span data-ttu-id="72fed-178">.Cs ファイルに名前空間を追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-178">Add the namespaces to the .cs file:</span></span>
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

<span data-ttu-id="72fed-179">System.Security アセンブリは、.NET Framework の一部であるし、フレームワークを使用してインストールします。</span><span class="sxs-lookup"><span data-stu-id="72fed-179">The System.Security assembly is part of .NET Framework and was installed with the framework.</span></span> <span data-ttu-id="72fed-180">サンプル アプリケーションでは、認証のためにホスト システムに暗号化された文字列を提供する名前空間が 1 つ以上が必要です。</span><span class="sxs-lookup"><span data-stu-id="72fed-180">The sample application needs one more namespace that provides an encrypted string to the hosting system for authentication.</span></span> <span data-ttu-id="72fed-181">認証されると、アプリケーションはホスト システム上のプロジェクトにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="72fed-181">Once authenticated, the application can access projects on the hosting system.</span></span> <span data-ttu-id="72fed-182">System.Security 名前空間をこの方法で .cs ファイルに追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-182">Add the System.Security namespace to the .cs file in this way:</span></span>
  
1. <span data-ttu-id="72fed-183">VS ソリューション エクスプ ローラーで参照のエントリを右クリックし、**参照の追加]** を選択</span><span class="sxs-lookup"><span data-stu-id="72fed-183">In the VS Solution Explorer, right-click the References entry, and select **Add Reference…**</span></span> <span data-ttu-id="72fed-184">ショートカット メニューの。</span><span class="sxs-lookup"><span data-stu-id="72fed-184">from the shortcut menu.</span></span> 
    
2. <span data-ttu-id="72fed-185">選択**アセンブリ =\>フレームワーク**参照マネージャーのダイアログ ボックスの左側のペインで**System.Security**を確認します。</span><span class="sxs-lookup"><span data-stu-id="72fed-185">Select **Assemblies =\> Framework** in the left pane of the References Manager dialog, then check **System.Security**.</span></span> 
    
3. <span data-ttu-id="72fed-186">**[OK]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="72fed-186">Click **OK**.</span></span> 
    
4. <span data-ttu-id="72fed-187">.Cs ファイルには、System.Security 名前空間を追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-187">Add the System.Security namespace to the .cs file:</span></span>
    
   ```cs
    using System.Security;
   ```

<span data-ttu-id="72fed-188">.Cs ファイルの先頭には、次の名前空間を含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="72fed-188">The start of the .cs file should contain the following namespaces:</span></span>
  
- <span data-ttu-id="72fed-189">System/システム</span><span class="sxs-lookup"><span data-stu-id="72fed-189">System</span></span>
    
- <span data-ttu-id="72fed-190">System.Collections.Generic</span><span class="sxs-lookup"><span data-stu-id="72fed-190">System.Collections.Generic</span></span>
    
- <span data-ttu-id="72fed-191">System.Linq</span><span class="sxs-lookup"><span data-stu-id="72fed-191">System.Linq</span></span>
    
- <span data-ttu-id="72fed-192">System.Test</span><span class="sxs-lookup"><span data-stu-id="72fed-192">System.Test</span></span>
    
- <span data-ttu-id="72fed-193">Microsoft.ProjectServer.Client</span><span class="sxs-lookup"><span data-stu-id="72fed-193">Microsoft.ProjectServer.Client</span></span>
    
- <span data-ttu-id="72fed-194">Microsoft.SharePoint.Client</span><span class="sxs-lookup"><span data-stu-id="72fed-194">Microsoft.SharePoint.Client</span></span>
    
- <span data-ttu-id="72fed-195">System.Security</span><span class="sxs-lookup"><span data-stu-id="72fed-195">System.Security</span></span>
    
### <a name="connect-to-the-host-system"></a><span data-ttu-id="72fed-196">ホスト システムへの接続します。</span><span class="sxs-lookup"><span data-stu-id="72fed-196">Connect to the host system</span></span>

<span data-ttu-id="72fed-197">プロジェクト オンラインは、適切なアプローチは、SharePoint の認証を使用するように SharePoint アプリケーションの場合は、です。</span><span class="sxs-lookup"><span data-stu-id="72fed-197">Project Online is a SharePoint application, so using SharePoint authentication is the correct approach.</span></span> <span data-ttu-id="72fed-198">ホストされている環境にアクセスするのには次のコードを準備します。</span><span class="sxs-lookup"><span data-stu-id="72fed-198">The following code fragment prepares to access the hosted environment.</span></span>
  
```cs
    class Program
    {
        private static ProjectContext projContext;
        static void Main (string[] args)
        {
            using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
            {
                SecureString password - new SecureString();
                foreach (char c in "password".ToCharArray()) password.AppendChar(c);
                //Using SharePoint method to load Credentials
                projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);

```

<span data-ttu-id="72fed-199">ホスト環境にアクセスするための準備には、次の項目があります。</span><span class="sxs-lookup"><span data-stu-id="72fed-199">Preparations to access the hosted environment include the following items:</span></span>
  
1. <span data-ttu-id="72fed-200">プロジェクトのコンテキスト オブジェクトを作成--上記のコードの次のコードに含まれているこれは。</span><span class="sxs-lookup"><span data-stu-id="72fed-200">Create a context object for the projects -- this is contained in the following code of the preceding code fragment.</span></span> 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   <span data-ttu-id="72fed-201">コンテキストは、システムがプロジェクトのオブジェクト モデルのコンテキストを管理できるように、他のコンポーネントによって継承されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-201">The context is inherited by other components, allowing the system to manage the context of the Project object model.</span></span>
    
2. <span data-ttu-id="72fed-202">ホストのサイトを識別する--これは、次のコードで上記のコードから。</span><span class="sxs-lookup"><span data-stu-id="72fed-202">Identify the host site -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   <span data-ttu-id="72fed-203">プロジェクト コンテキストのインスタンスを作成するには、プロジェクトのサイト コレクションのルートを提供する、アプリケーション必要があります。</span><span class="sxs-lookup"><span data-stu-id="72fed-203">When instantiating the projects context, the application needs to provide the root of the Projects site collection.</span></span> <span data-ttu-id="72fed-204">アプリケーションでは、プロジェクトのルートの URL の部分文字列を使用します。</span><span class="sxs-lookup"><span data-stu-id="72fed-204">The application uses a substring of the URL of the root of the Projects.</span></span> <span data-ttu-id="72fed-205">この場所のスナップショットは、次の図の赤い四角形で強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-205">A snapshot of this location is highlighted with a red rectangle in the following illustration.</span></span> <span data-ttu-id="72fed-206">認証では、「pwa」の部分文字列で開始からの文字列が必要です。</span><span class="sxs-lookup"><span data-stu-id="72fed-206">The authentication needs the string from its start through the substring "pwa".</span></span> <span data-ttu-id="72fed-207">コードの一覧でアプリケーションを使用して、文字列"https://XXXXXXXX.sharepoint.com/sites/pwa"です。</span><span class="sxs-lookup"><span data-stu-id="72fed-207">In the code listing, the application uses the string "https://XXXXXXXX.sharepoint.com/sites/pwa".</span></span>
        
   <span data-ttu-id="72fed-208">![のスクリーン ショットの赤い枠線内でのプロジェクトのサイト コレクションの URL です]。(media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "サイト赤い枠線内のコレクションをプロジェクトの URL のスクリーン ショット")</span><span class="sxs-lookup"><span data-stu-id="72fed-208">![Screen shot of the URL of the Projects site collection within a red border.](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "Screen shot of the URL of the Projects site collection within a red border")</span></span>
  
3. <span data-ttu-id="72fed-209">パスワードをセキュリティで保護された文字列の配置 - これは、次のコードで上記のコードから。</span><span class="sxs-lookup"><span data-stu-id="72fed-209">Place the password in a secure string -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   <span data-ttu-id="72fed-210">パスワードとユーザー アカウントは、ホスト サイトにアクセスする資格情報です。</span><span class="sxs-lookup"><span data-stu-id="72fed-210">The password and user account are the credentials to access the host site.</span></span> 
    
4. <span data-ttu-id="72fed-211">コンテキスト オブジェクトの資格情報の部分に、ユーザー アカウントとパスワードを追加する--これは、次のコードで上記のコードから。</span><span class="sxs-lookup"><span data-stu-id="72fed-211">Add the user account and password to the credentials portion of the context object -- this is done in the following code from the preceding code fragment.</span></span>
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

<span data-ttu-id="72fed-212">プロジェクトのインスタンスが作成されたコンテキストを使用する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="72fed-212">The instantiated project context is ready to use.</span></span>
  
### <a name="list-all-published-projects"></a><span data-ttu-id="72fed-213">すべての公開済みのプロジェクトを一覧表示します。</span><span class="sxs-lookup"><span data-stu-id="72fed-213">List all published projects</span></span>

<span data-ttu-id="72fed-214">プロジェクト オンライン ProjectServer の作成、レポート、更新プログラム、サーバーと通信するプロキシを使用して削除 (CRUD) 操作します。</span><span class="sxs-lookup"><span data-stu-id="72fed-214">Project Online and ProjectServer use proxies to communicate with the server for create, report, update, and delete (CRUD) operations.</span></span> <span data-ttu-id="72fed-215">ホストまたはサーバーでは、効率的な方法で要求を処理し、クライアントがサーバーとの通信で以下の操作を実行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-215">The host/server handles requests in an efficient manner and has the client perform the following actions in communicating with the server:</span></span>
  
1. <span data-ttu-id="72fed-216">通信のコンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="72fed-216">Establish a context for communication.</span></span> 
    
   <span data-ttu-id="72fed-217">によって、プロジェクト コレクションと同様に他のオブジェクトやコレクションのタスクのコレクション、割り当てのコレクション、stage オブジェクトの場合は、ユーザー設定フィールドなど、継承によってコンテキストが使用されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-217">The context is used by the projects collection, as well as other objects and collections through inheritance, including the tasks collection, assignments collection, the stage object, and custom fields.</span></span> 
    
2. <span data-ttu-id="72fed-218">オブジェクト モデルを使用すると、オブジェクト、コレクション、または取得するのにデータを指定します。</span><span class="sxs-lookup"><span data-stu-id="72fed-218">Use the object model to specify an object, collection, or data to retrieve.</span></span>
    
   <span data-ttu-id="72fed-219">この手順は、クエリ、またはメソッドとして、LINQ を使用します。</span><span class="sxs-lookup"><span data-stu-id="72fed-219">This step uses LINQ as a query or as a method.</span></span> <span data-ttu-id="72fed-220">仕様では、何が表示を制御します。</span><span class="sxs-lookup"><span data-stu-id="72fed-220">The specification controls what you receive.</span></span> <span data-ttu-id="72fed-221">多くの場合、この手順は、Load メソッド (手順 3) の本文として埋め込まれます。</span><span class="sxs-lookup"><span data-stu-id="72fed-221">Often, this step is embedded as the body of the Load method (step 3).</span></span> 
    
3. <span data-ttu-id="72fed-222">Load() または LoadQuery() メソッドを使用して前の手順から取得仕様をロードします。</span><span class="sxs-lookup"><span data-stu-id="72fed-222">Load the retrieval specification from the previous step using the Load() or LoadQuery() method.</span></span>
    
   <span data-ttu-id="72fed-223">コレクションとオブジェクトをロードするには、Load() を使用します。</span><span class="sxs-lookup"><span data-stu-id="72fed-223">For loading collections and objects, use Load().</span></span> <span data-ttu-id="72fed-224">「場所」のような句を持つクエリーの LoadQuery() を使用して、[グループ] とします。</span><span class="sxs-lookup"><span data-stu-id="72fed-224">For queries with clauses such as "where" and "group", use LoadQuery().</span></span> 
    
4. <span data-ttu-id="72fed-225">ExecuteQuery() メソッドを使用して要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-225">Execute the request using the ExecuteQuery() method.</span></span>
    
   <span data-ttu-id="72fed-226">ExecuteQuery() メソッドは、クエリまたはクエリは、実行する準備ができましたをホストに通知します。</span><span class="sxs-lookup"><span data-stu-id="72fed-226">The ExecuteQuery() method notifies the host that the query or queries are ready to execute.</span></span> <span data-ttu-id="72fed-227">通知を受信すると、ホスト、クエリを実行し、結果をクライアントに送信します。</span><span class="sxs-lookup"><span data-stu-id="72fed-227">Once the host receives notification, it executes the queries and sends the results to the client.</span></span> 
    
<span data-ttu-id="72fed-228">クライアントに情報を含む、アプリケーションで使用します。</span><span class="sxs-lookup"><span data-stu-id="72fed-228">With the information at the client, the application can use it.</span></span> <span data-ttu-id="72fed-229">次のコードは順に発行されたプロジェクトとホストで公開されている各プロジェクトの名前と Id を印刷します。</span><span class="sxs-lookup"><span data-stu-id="72fed-229">The following code fragment cycles through the published projects and prints the Id and Name for each published project on the host.</span></span>
  
```cs
// Get the list of projects in Project Web App.
var projects = projContext.Projects;
projContext.Load(projects);
projcontext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
    Console.WriteLine("\n{0}. {1}   {2} \t{3} \n", j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
}

```

<span data-ttu-id="72fed-230">出力します。</span><span class="sxs-lookup"><span data-stu-id="72fed-230">Output:</span></span>
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a><span data-ttu-id="72fed-231">要求を行う</span><span class="sxs-lookup"><span data-stu-id="72fed-231">Make a request</span></span>

<span data-ttu-id="72fed-232">前のコードからアクションを使用するアプリケーションは、ホスト サイトで指定されたアカウント内のプロジェクトのリストを取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-232">Using the actions from the previous code fragment, the application retrieves the list of projects in the specified account on the hosting site.</span></span> 
  
1. <span data-ttu-id="72fed-233">プロジェクトを一覧表示するため、ProjectContext を指定します。</span><span class="sxs-lookup"><span data-stu-id="72fed-233">The ProjectContext is specified for the projects to list.</span></span> 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="72fed-234">取得する項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="72fed-234">Specify the item to retrieve.</span></span> 
    
   ```cs
    projContext.Load(projects);
   ```

   <span data-ttu-id="72fed-235">コレクションをのみを示すでは、サーバーは、既定のプロパティのセットの値を持つ各プロジェクトを作成、プロジェクト コレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-235">By only stating the collection, the server retrieves the project collection, populating each project with values for the default set of properties.</span></span> <span data-ttu-id="72fed-236">既定のプロパティ セットの一部であるプロパティにアクセスするには、正常な結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="72fed-236">Accessing properties that are part of the default property set gives successful results.</span></span> <span data-ttu-id="72fed-237">「初期化されていません」の例外の結果を設定する既定値の一部ではないプロパティにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="72fed-237">Accessing properties that are not part of the default set results in a "Not initialized" exception.</span></span>
    
3. <span data-ttu-id="72fed-238">要求 (projContext.Load) をロードします。</span><span class="sxs-lookup"><span data-stu-id="72fed-238">Load the request (projContext.Load).</span></span>
    
   <span data-ttu-id="72fed-239">これは、前の手順の一部です。</span><span class="sxs-lookup"><span data-stu-id="72fed-239">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="72fed-240">(ExecuteQuery) のクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-240">Execute the query (ExecuteQuery).</span></span> 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a><span data-ttu-id="72fed-241">高度なプロジェクト情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-241">Retrieve high-level project information</span></span>

<span data-ttu-id="72fed-242">プロパティを既定ではないプロパティは、サーバーへの要求で指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="72fed-242">Properties that are not default properties must be specified in the request to the server.</span></span> <span data-ttu-id="72fed-243">次のコード フラグメントでは、前の例のように、プロジェクト コレクションのコンテキストを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="72fed-243">The next code fragment loads the projects collection context as in the previous example.</span></span> <span data-ttu-id="72fed-244">次に、仕様は、結果に含める追加の既定以外のプロパティを要求します。</span><span class="sxs-lookup"><span data-stu-id="72fed-244">Then, the specification requests additional non-default properties to include in the result.</span></span> 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

<span data-ttu-id="72fed-245">Load ステートメントは、プロジェクト コレクションのコンテキストを指定し、クエリの結果を開始日、フェーズとステージを追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-245">The load statement specifies the projects collection context, and adds the StartDate, Phase, and Stage to the query result.</span></span> <span data-ttu-id="72fed-246">追加のプロパティは、スカラー、またはオブジェクトのコレクションです。</span><span class="sxs-lookup"><span data-stu-id="72fed-246">The additional properties can be scalar, objects, or collections.</span></span> <span data-ttu-id="72fed-247">スカラーのアイテムに直接アクセスできます。</span><span class="sxs-lookup"><span data-stu-id="72fed-247">Scalar items can be accessed directly.</span></span> <span data-ttu-id="72fed-248">オブジェクトとコレクションの次のコード片に示すように、追加の処理が必要です。</span><span class="sxs-lookup"><span data-stu-id="72fed-248">Objects and collections require additional processing, as in the following code fragment.</span></span>
  
```cs
// Using the previous definition and Load statement …
projContext.ExecuteQuery();
foreach (PublishedProject pubProj in projContext.Projects)
{
Console.WriteLine("\n\t{0}. \t{1} \n\t{2} \n\t{3} \n", j++, pubProj.Id, pubProj.Name,
    pubProj.CreatedDate);
             // The following statement generates an exception about the object 
             // reference not being set to an instance on the server. 
             // Console.WriteLine("\tCurrent Phase:\t{0}", pubProj.Phase.Name);
             // Phase and Stage are not published with the rest of the data. Need to pull these objects from the server.
             Phase oPhase = pubProj.Phase;
             projContext.Load(oPhase);
             projContext.ExecuteQuery();
             //if-else fails because the else case fails with "Microsoft.SharePoint.Client.ServerObjectNullReferenceException".
             //if (oPhase.ServerObjectIsNull != null)
             //Using try-catch instead
             try
             {
                  Console.WriteLine("\tCurrent Phase:\t{0}", oPhase.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Phase:\t Not available");
             }
             
             Stage oStage = pubProj.Stage;
             projContext.Load(oStage);
             projContext.ExecuteQuery();
             //Again, not using if-else combination for the same reason as above.
             try
             {
                  Console.WriteLine("\tCurrent Stage:\t{0}", oStage.Name);
             }
             
             catch
             {
                  Console.WriteLine("\tCurrent Stage:\t Not available");
    }

```

<span data-ttu-id="72fed-249">最初の 3 つのプロジェクトの出力:</span><span class="sxs-lookup"><span data-stu-id="72fed-249">Output of the first three projects:</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
        CreatedDate:            3/22/2016 5:14:34 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
        CreatedDate:            3/22/2016 5:36:40 PM
        Current Phase:  3. Plan
        Current Stage:  6. Plan
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
        CreatedDate:            3/22/2016 5:02:24 PM
        Current Phase:  2. Select
        Current Stage:  4. Select Gate

```

### <a name="retrieve-all-tasks-in-a-project"></a><span data-ttu-id="72fed-250">プロジェクト内のすべてのタスクを取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-250">Retrieve all tasks in a project</span></span>

<span data-ttu-id="72fed-251">各プロジェクトには、多くのタスクがあります。</span><span class="sxs-lookup"><span data-stu-id="72fed-251">Each project has many tasks.</span></span> <span data-ttu-id="72fed-252">したがって、1 つのプロジェクトのタスクをプルは、以下の。</span><span class="sxs-lookup"><span data-stu-id="72fed-252">So, pulling the tasks for a single project consists of the following:</span></span>
  
1. <span data-ttu-id="72fed-253">プロジェクト コレクションのコンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="72fed-253">Establish the context of the projects collection.</span></span>
    
   ```cs
    var projects = projContext.Projects;
   ```

2. <span data-ttu-id="72fed-254">タスクのプロパティを含む、プロジェクト情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-254">Retrieve the project information, including the Task properties.</span></span>
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    <span data-ttu-id="72fed-255">アプリケーションが公開されているプロジェクトをアドレス指定するに注意してください。</span><span class="sxs-lookup"><span data-stu-id="72fed-255">Note that the application is addressing published projects.</span></span> <span data-ttu-id="72fed-256">現在の発行済みプロジェクトのコンテキストとは、pubProj です。</span><span class="sxs-lookup"><span data-stu-id="72fed-256">The context for the current published project is pubProj.</span></span> 
    
3. <span data-ttu-id="72fed-257">Tasks コレクションのコンテキストを確立します。</span><span class="sxs-lookup"><span data-stu-id="72fed-257">Establish the context for the Tasks collection.</span></span>
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   <span data-ttu-id="72fed-258">`pubProj.Tasks`プロパティは、現在公開されているプロジェクトのタスクを参照します。</span><span class="sxs-lookup"><span data-stu-id="72fed-258">The `pubProj.Tasks` property references the tasks of the current published project.</span></span> 
    
4. <span data-ttu-id="72fed-259">適切な既定以外のプロパティを含め、タスクのコレクションを取得するために仕様をロードします。</span><span class="sxs-lookup"><span data-stu-id="72fed-259">Load the specification to retrieve Task collection, including the appropriate non-default properties.</span></span>
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. <span data-ttu-id="72fed-260">適切なプロパティを使用してタスクのコレクションを取得するクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-260">Execute the query to retrieve the Task collection with the appropriate properties.</span></span>
    
   ```cs
    projContext.ExecuteQuery();
   ```

<span data-ttu-id="72fed-261">情報がローカルではようになりました。</span><span class="sxs-lookup"><span data-stu-id="72fed-261">The information is now local.</span></span> <span data-ttu-id="72fed-262">次のコードは、コンソールに情報を記述することによって公開されているタスクのコレクションを処理します。</span><span class="sxs-lookup"><span data-stu-id="72fed-262">The following code fragment processes the published tasks collection by writing the information to the console.</span></span>
  
```cs
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k++, t.Id, t.Name);
            Console.WriteLine("\t ScheduledStart:{0} \tStart:{1} \tCompletion:{2}", k, t.ScheduledStart, t.Start, t.Completion);
        }
    }

```

<span data-ttu-id="72fed-263">1 つのプロジェクトのタスクの出力:</span><span class="sxs-lookup"><span data-stu-id="72fed-263">Output of tasks for one project:</span></span>
  
```cs
Task collection count: 5
1. Id:256fa850-b2ef-e511-80f6-00155dc87d01      Name:Load software onto computer
         ScheduledStart:2       Start:4/4/2016 8:00:00 AM       Completion:4/4/2016 8:00:00 AM
2. Id:266fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load Project Online SDK
         ScheduledStart:3       Start:4/5/2016 8:00:00 AM       Completion:4/5/2016 8:00:00 AM
3. Id:276fa850-b2ef-e511-80f6-00155dc87d01      Name:Locate and load SP SDK
         ScheduledStart:4       Start:4/5/2016 1:00:00 PM       Completion:4/5/2016 1:00:00 PM
4. Id:286fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses Proj Online
         ScheduledStart:5       Start:4/6/2016 8:00:00 AM       Completion:4/6/2016 8:00:00 AM
5. Id:296fa850-b2ef-e511-80f6-00155dc87d01      Name:Build app that accesses task assignments
         ScheduledStart:6       Start:4/7/2016 8:00:00 AM       Completion:4/7/2016 8:00:00 AM

```

### <a name="access-information-at-multiple-levels"></a><span data-ttu-id="72fed-264">複数のレベルでのアクセス情報</span><span class="sxs-lookup"><span data-stu-id="72fed-264">Access information at multiple levels</span></span>

<span data-ttu-id="72fed-265">各タスク (別名で 1 つまたは複数の担当者を持つことができます。</span><span class="sxs-lookup"><span data-stu-id="72fed-265">Each task can have one or more persons (a.k.a.</span></span> <span data-ttu-id="72fed-266">リソース) は、その終了時に貢献しています。</span><span class="sxs-lookup"><span data-stu-id="72fed-266">resource) contributing toward its completion.</span></span> <span data-ttu-id="72fed-267">割り当てとリソースのコレクションには、タスクごとにこの情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="72fed-267">The Assignments and Resources collections contain this information for each task.</span></span> 
  
<span data-ttu-id="72fed-268">処理は、次ので構成されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-268">The processing consists of the following:</span></span>
  
1. <span data-ttu-id="72fed-269">プロジェクトのタスクのコンテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-269">Obtaining a context for the project task.</span></span>
    
2. <span data-ttu-id="72fed-270">要求を作成し、タスクに関連付けられている割り当ての要求をロードします。</span><span class="sxs-lookup"><span data-stu-id="72fed-270">Build a request and load the request for the assignments tied to the task.</span></span> 
    
3. <span data-ttu-id="72fed-271">割り当てに対してクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-271">Execute the query for the assignments.</span></span>
    
4. <span data-ttu-id="72fed-272">要求を作成し、個々 の割り当てに関連付けられているリソースの要求をロードします。</span><span class="sxs-lookup"><span data-stu-id="72fed-272">Build a request and load the request for the resource associated with an individual assignment.</span></span> 
    
5. <span data-ttu-id="72fed-273">リソースのクエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-273">Execute the query for the resource.</span></span>
    
> [!NOTE] 
> - <span data-ttu-id="72fed-274">Tasks コレクションの既定のプロパティではないために、サーバーからの情報の割り当てのコレクションが明示的に要求します。</span><span class="sxs-lookup"><span data-stu-id="72fed-274">The Assignments collection is explicitly requested in the information from the server because it is not a default property of the Tasks collection.</span></span> <span data-ttu-id="72fed-275">コレクションとしては、以降のクエリは、サーバーからコレクションを取得するのには作成されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-275">As a collection, a subsequent query is made to pull the collection from the server.</span></span> 
> - <span data-ttu-id="72fed-276">リソースは、オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="72fed-276">The Resource is an object.</span></span> <span data-ttu-id="72fed-277">割り当てのクエリには、割り当てに関連付けられているリソース名が含まれています。</span><span class="sxs-lookup"><span data-stu-id="72fed-277">The query for an assignment includes the resource name associated with the assignment.</span></span>
    
```cs
PublishedTaskCollection collTask = pubProj.Tasks;
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, 
            t => t.Assignments));
    projContext.Load(collTask);
    projContext.ExecuteQuery();
    Console.WriteLine("Task collection count: {0}", collTask.Count.ToString());
    if (collTask.Count > 0)
    {
        int k = 1;    //Task counter.
        //Processing task list for current project
        foreach (PublishedTask t in collTask)
        {
            Console.WriteLine("{0}. Id:{1} \tName:{2}", k, t.Id, t.Name);
            k++;
            //Define and retrieve Assignments for current task
            PublishedAssignmentCollection collAssgns = t.Assignments;
            projContext.Load(collAssgns);
            projContext.ExecuteQuery();
            Console.WriteLine("    Assignment collection count: {0}", collAssgns.Count);
            if (collAssgns.Count > 0)
            {
                //Output string for resources assigned to task
                StringBuilder output = new StringBuilder();
                output.AppendFormat("\t Assignments: ");
                foreach (PublishedAssignment a in collAssgns)
                {
                    //Define and retrieve resource name for current assignment 
                    //(an object)
                    projContext.Load(a,
                        b => b.Resource.Name);
                    projContext.ExecuteQuery();
                    output.AppendFormat("{0}, ", a.Resource.Name);
                }
                Console.WriteLine(output);
            }
            else
            {
                Console.WriteLine("\t Assignments: None");
            }
        }
    }   // endif

```

<span data-ttu-id="72fed-278">52、75、76 のプロジェクトのタスクの出力:</span><span class="sxs-lookup"><span data-stu-id="72fed-278">Output for tasks 52, 75, and 76 of a project:</span></span>
  
```cs
52. Id:2c729e96-54f0-e511-80c6-000d3a33235f     Name:Develop training materials
    Assignment collection count: 1
         Assignments: Robert Lyon,
75. Id:43729e96-54f0-e511-80c6-000d3a33235f     Name:Determine final deployment strategy
    Assignment collection count: 0
         Assignments: None
76. Id:44729e96-54f0-e511-80c6-000d3a33235f     Name:Develop deployment methodology
    Assignment collection count: 4
         Assignments: Molly Dempsey, Sara Davis, Shammi Mohamed, Zainal Arifin, 

```

### <a name="access-custom-enterprise-level-fields"></a><span data-ttu-id="72fed-279">カスタムのエンタープライズ レベルのフィールドのアクセス</span><span class="sxs-lookup"><span data-stu-id="72fed-279">Access custom enterprise-level fields</span></span>

<span data-ttu-id="72fed-280">オンライン プロジェクトのカスタム フィールドが存在します。</span><span class="sxs-lookup"><span data-stu-id="72fed-280">Custom fields exist for Project Online.</span></span> <span data-ttu-id="72fed-281">これらは、個々 のプロジェクトに関連付けることができるエンタープライズ ・ レベルのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="72fed-281">These are enterprise-level fields that can be associated with individual project.</span></span> <span data-ttu-id="72fed-282">このセクションでは、これらのフィールドにアクセスする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="72fed-282">This section describes how to access these fields.</span></span> 
  
<span data-ttu-id="72fed-283">ユーザー設定フィールドは、プロジェクトに関連付けられているプロパティの既定のセットには含まれていません。</span><span class="sxs-lookup"><span data-stu-id="72fed-283">Custom fields are not included in the default set of properties associated with a project.</span></span> <span data-ttu-id="72fed-284">そのため、取得の仕様で明示的な id が必要です。</span><span class="sxs-lookup"><span data-stu-id="72fed-284">So, they need explicit identification in the retrieval specification.</span></span> <span data-ttu-id="72fed-285">プロセスの高度なビューは、次の項目で構成されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-285">The high-level view of the process consists of the following items:</span></span>
  
1. <span data-ttu-id="72fed-286">共通名を使用してユーザー設定フィールドにトンネルします。</span><span class="sxs-lookup"><span data-stu-id="72fed-286">Tunnel to the custom field using its common name.</span></span>
    
2. <span data-ttu-id="72fed-287">ユーザー設定フィールドの内部名を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-287">Retrieve the internal name of the custom field.</span></span>
    
3. <span data-ttu-id="72fed-288">グローバル コンテキストに戻るし、ユーザー設定フィールドの内部名を使用してシステムを照会します。</span><span class="sxs-lookup"><span data-stu-id="72fed-288">Return to the global context and query the system using the internal name of the custom field.</span></span>
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a><span data-ttu-id="72fed-289">ユーザー設定フィールドにトンネル、その内部の名前を取得およびシステムのクエリを実行するために使用</span><span class="sxs-lookup"><span data-stu-id="72fed-289">Tunnel to the custom field, retrieve its internal name, and used it to query the system</span></span>

<span data-ttu-id="72fed-290">このタスクは、既定以外のプロパティを使用して詳細を 1 つ追加と取得を指定します。</span><span class="sxs-lookup"><span data-stu-id="72fed-290">This task specifies a retrieval that uses a non-default property with one added detail.</span></span>
  
1. <span data-ttu-id="72fed-291">この資料の冒頭で説明したように、プロジェクトのコンテキストを使用して開始します。</span><span class="sxs-lookup"><span data-stu-id="72fed-291">Begin by using the projects context, as described at the beginning of this article.</span></span>
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. <span data-ttu-id="72fed-292">プロジェクト コレクションへの検索要求だけでなく他の既定以外のプロパティを取得するには、2 つの項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="72fed-292">Add two items to the projects collection retrieval request in addition to any other non-default properties to retrieve:</span></span>
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   <span data-ttu-id="72fed-293">`p => p.IncludeCustomFields`句は、ユーザー設定フィールドをサポートするプロジェクトのオブジェクトを使用する必要性を識別します。</span><span class="sxs-lookup"><span data-stu-id="72fed-293">The  `p => p.IncludeCustomFields` clause identifies the need to use a project object that supports custom fields.</span></span> 
    
   <span data-ttu-id="72fed-294">`p => p.IncludeCustomFields.CustomFields`句は、クエリ結果内のカスタム フィールドのデータを含めることを要求します。</span><span class="sxs-lookup"><span data-stu-id="72fed-294">The  `p => p.IncludeCustomFields.CustomFields` clause requests the inclusion of custom field data in the query result.</span></span> <span data-ttu-id="72fed-295">ユーザー設定フィールドの内部名を取得した後、この情報が使用されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-295">This information is used after the custom field internal name is retrieved.</span></span> 
    
3. <span data-ttu-id="72fed-296">要求をロードします。</span><span class="sxs-lookup"><span data-stu-id="72fed-296">Load the request.</span></span>
    
   <span data-ttu-id="72fed-297">これは、前の手順の一部です。</span><span class="sxs-lookup"><span data-stu-id="72fed-297">This is part of the previous step.</span></span>
    
4. <span data-ttu-id="72fed-298">クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="72fed-298">Execute the Query.</span></span>
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. <span data-ttu-id="72fed-299">クライアント上でこの情報を現在のプロジェクトに関連付けられているユーザー設定フィールドを取得する要求を構築します。</span><span class="sxs-lookup"><span data-stu-id="72fed-299">With this information on the client, build a request to retrieve the custom fields associated with the current project.</span></span>
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. <span data-ttu-id="72fed-300">適切なユーザー設定フィールドを検索し、フィールドの内部名を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-300">Locate the appropriate custom field and retrieve the internal name of the field.</span></span> 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   <span data-ttu-id="72fed-301">ユーザー設定フィールドの内部名を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-301">The internal name of the custom field is retrieved.</span></span> <span data-ttu-id="72fed-302">高レベルの項目 1 と 2 が完了しました。</span><span class="sxs-lookup"><span data-stu-id="72fed-302">High-level items 1 and 2 are now complete.</span></span>
    
7. <span data-ttu-id="72fed-303">プロジェクトのコンテキストに戻るし、ユーザー設定フィールドの値を取得します。</span><span class="sxs-lookup"><span data-stu-id="72fed-303">Return to the project context and retrieve the value of the custom field.</span></span>
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > <span data-ttu-id="72fed-304">インデックスとしての内部名を使用してユーザー設定フィールドの値が取得されます。</span><span class="sxs-lookup"><span data-stu-id="72fed-304">The value of the custom field is retrieved using the internal name as an index.</span></span> 
  
<span data-ttu-id="72fed-305">プロジェクト ID、プロジェクト名、ユーザー設定フィールド名、ユーザー設定フィールドの内部名、およびユーザー設定フィールドの値で構成される 3 つのプロジェクトの出力をします。</span><span class="sxs-lookup"><span data-stu-id="72fed-305">Output of three projects consisting of project ID, project Name, custom field name, custom field internal name, and custom field value.</span></span>
  
```cs
Project counts:31
1. Project ID:  957d5fcd-5cbf-e111-9f1e-00155d022681
        Name:           Acquisition Target Analysis
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
2. Project ID:  16905202-5fbf-e111-9f1e-00155d022681
        Name:           Apparel ERP Upgrade
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Green
3. Project ID:  dce23152-63bf-e111-9f1e-00155d022681
        Name:           Audit Tracking Solution
Name: Project Health
InternalName: Custom_745de6dfcfb4e11195dc00155d02c97f
Value: Red

```

## <a name="see-also"></a><span data-ttu-id="72fed-306">関連項目</span><span class="sxs-lookup"><span data-stu-id="72fed-306">See also</span></span>

<span data-ttu-id="72fed-307">ドキュメントとオンライン プロジェクトと CSOM を使用したアプリケーション開発に関連するサンプルでは、[プロジェクト開発のポータル](https://developer.microsoft.com/en-us/project)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="72fed-307">For documentation and samples related to Project Online and application development using CSOM, see the [Project Development Portal](https://developer.microsoft.com/en-us/project).</span></span>
    

