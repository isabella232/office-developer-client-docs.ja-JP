---
title: Project Server 2013 JavaScript オブジェクト モデルの概要
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: Project Server 2013 では、JavaScript オブジェクト モデルは、プロジェクト オンライン、モバイル、および設置型の開発で使用できます。 このトピックでは、JavaScript オブジェクト モデルの概要について説明し、し、取得し、JavaScript オブジェクト モデルを使用して、プロジェクトを反復処理するアプリケーション ページを作成する方法について説明します。
ms.openlocfilehash: 94c882249474e22328031d55233cfba654dcff83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804554"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a><span data-ttu-id="67fd4-104">Project Server 2013 JavaScript オブジェクト モデルの概要</span><span class="sxs-lookup"><span data-stu-id="67fd4-104">Getting started with the Project Server 2013 JavaScript object model</span></span>

<span data-ttu-id="67fd4-105">Project Server 2013 では、JavaScript オブジェクト モデルは、プロジェクト オンライン、モバイル、および設置型の開発で使用できます。</span><span class="sxs-lookup"><span data-stu-id="67fd4-105">In Project Server 2013, the JavaScript object model can be used in Project Online, mobile, and on-premise development.</span></span> <span data-ttu-id="67fd4-106">このトピックでは、JavaScript オブジェクト モデルの概要について説明し、し、取得し、JavaScript オブジェクト モデルを使用して、プロジェクトを反復処理するアプリケーション ページを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-106">This topic provides a brief overview of the JavaScript object model and then describes how to create an application page that retrieves and iterates through projects by using the JavaScript object model.</span></span>
  
## <a name="using-the-project-server-javascript-object-model"></a><span data-ttu-id="67fd4-107">Project Server JavaScript オブジェクト モデルの使用</span><span class="sxs-lookup"><span data-stu-id="67fd4-107">Using the Project Server JavaScript object model</span></span>
<span data-ttu-id="67fd4-108"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-108"></span></span>

<span data-ttu-id="67fd4-109">JavaScript オブジェクト モデルを使用して、クライアント側ではなく、リモートで実行する必要のあるマネージ クライアント コード) を実行するアプリケーションを作成する優れた方法です。</span><span class="sxs-lookup"><span data-stu-id="67fd4-109">Using the JavaScript object model is a great way to create an app that runs client-side (as opposed to managed client code which needs to run remotely).</span></span> <span data-ttu-id="67fd4-110">アプリケーションでは、取得するか、サーバーへの非同期の呼び出しを送信することによってオブジェクトを変更する JavaScript オブジェクト モデルを使用できます。</span><span class="sxs-lookup"><span data-stu-id="67fd4-110">Apps can use the JavaScript object model to retrieve or change objects by sending asynchronous calls to the server.</span></span> <span data-ttu-id="67fd4-111">JavaScript オブジェクト モデルを使用するアプリケーションは、通常、カスタムの SharePoint アドインの場合、アプリケーション ページ、および Web パーツとして配置されます。</span><span class="sxs-lookup"><span data-stu-id="67fd4-111">Apps that use the JavaScript object model are typically deployed as custom SharePoint Add-ins, application pages, and Web Parts.</span></span> <span data-ttu-id="67fd4-112">詳細については、[ホストの web、web では、追加、](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx)および SharePoint 2013 での SharePoint コンポーネントの種類の SharePoint アプリケーションでは、SharePoint コンポーネント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67fd4-112">For more information, see "Types of SharePoint components that can be in an app for SharePoint" in [Host webs, add-in webs, and SharePoint components in SharePoint 2013](http://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="67fd4-113">JavaScript オブジェクト モデルは、Project Server 2013 では、主要な機能を実装しますが、JavaScript オブジェクト モデル、サーバー オブジェクト モデルでは、一対一のパリティを必要はありません。</span><span class="sxs-lookup"><span data-stu-id="67fd4-113">The JavaScript object model implements the main functionality of Project Server 2013, but the JavaScript object model and the server object model do not have one-to-one parity.</span></span> <span data-ttu-id="67fd4-114">JavaScript オブジェクト モデルへのエントリ ポイントは、Project Server 2013 のクライアント コンテキストを表し、サーバーのコンテンツおよび機能へのアクセスを提供する、 **ProjectContext**オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="67fd4-114">The entry point to the JavaScript object model is the **ProjectContext** object, which represents the client context for Project Server 2013 and provides access to server content and functionality.</span></span> <span data-ttu-id="67fd4-115">Project Server 2013 の JavaScript オブジェクト モデルが既定のパスにある PS.js ファイルで定義されている`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS`のアプリケーション サーバーにします。</span><span class="sxs-lookup"><span data-stu-id="67fd4-115">The JavaScript object model for Project Server 2013 is defined in the PS.js file, which is located in the default path  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS` on the application server.</span></span> <span data-ttu-id="67fd4-116">また、Project Server 2013 にインストールして、PS同じ場所に Debug.js ファイルです。</span><span class="sxs-lookup"><span data-stu-id="67fd4-116">Project Server 2013 also installs the PS.Debug.js file in the same location.</span></span> <span data-ttu-id="67fd4-117">PS.Debug.js は、IntelliSense の情報を提供する PS.js の unminified バージョンです。</span><span class="sxs-lookup"><span data-stu-id="67fd4-117">PS.Debug.js is an unminified version of PS.js that provides IntelliSense information.</span></span> 
  
<span data-ttu-id="67fd4-118">JavaScript オブジェクト モデルにより、フォーム認証、およびすべての要求は、現在のユーザーとして認証されます。</span><span class="sxs-lookup"><span data-stu-id="67fd4-118">The JavaScript object model allows Forms authentication, and all requests are authenticated as the current user.</span></span> <span data-ttu-id="67fd4-119">セキュリティおよびカスタム アプリケーションの設計とソリューションの他の考慮事項については、[認証、承認、および SharePoint 2013 のセキュリティ](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx)、SharePoint アドインのアーキテクチャと開発の重要な側面を[を参照してください。横](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)、 [SharePoint のアドインは、SharePoint ソリューションと比較](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx)するとします。</span><span class="sxs-lookup"><span data-stu-id="67fd4-119">For more information about security and other considerations for designing custom apps and solutions, see [Authentication, authorization, and security in SharePoint 2013](http://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx), [Important aspects of the SharePoint Add-in architecture and development landscape](http://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx), and [SharePoint Add-ins compared with SharePoint solutions](http://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx).</span></span>
  
> [!NOTE]
> <span data-ttu-id="67fd4-120">SharePoint サイトからリモートでデータにアクセスするには、SharePoint 2013 は、クロス ドメイン ライブラリをクライアント側のドメイン間呼び出しを行うことができますを提供します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-120">To access data from a SharePoint site remotely, SharePoint 2013 provides a cross-domain library that enables you to make client-side cross-domain calls.</span></span> <span data-ttu-id="67fd4-121">詳細については、[クロス ドメイン ライブラリを使用してアドインからのデータを SharePoint 2013 のアクセス](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67fd4-121">For more information, see [Access SharePoint 2013 data from add-ins using the cross-domain library](http://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx).</span></span> 
  
<span data-ttu-id="67fd4-122">多くの概念とプロセスを Project Server 2013 の JavaScript オブジェクト モデルを使用するため、関連するクライアント オブジェクト モデルのようになります。</span><span class="sxs-lookup"><span data-stu-id="67fd4-122">Many concepts and processes for using the JavaScript object model for Project Server 2013 resemble those in related client object models.</span></span> <span data-ttu-id="67fd4-123">Project Server 2013 のマネージ クライアント オブジェクト モデルの詳細については、 **Microsoft.ProjectServer.Client**を参照してください。</span><span class="sxs-lookup"><span data-stu-id="67fd4-123">For more information about the Project Server 2013 managed client object model, see **Microsoft.ProjectServer.Client**.</span></span> <span data-ttu-id="67fd4-124">SharePoint 2013JavaScript オブジェクト モデルとマネージ クライアント オブジェクト モデルに関する詳細については、 [SharePoint 2013 での JavaScript ライブラリのコードを使用して基本的な操作を完了](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx)し、[基本的な操作を完了 SharePoint 2013 クライアントを使用するを参照してください。ライブラリ コード](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx)。</span><span class="sxs-lookup"><span data-stu-id="67fd4-124">For more information about the SharePoint 2013JavaScript object model and managed client object model, see [Complete basic operations using JavaScript library code in SharePoint 2013](http://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx) and [Complete basic operations using SharePoint 2013 client library code](http://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx).</span></span>
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="67fd4-125">チュートリアル: プロジェクトを取得および反復処理するアプリケーション ページの作成</span><span class="sxs-lookup"><span data-stu-id="67fd4-125">Walkthrough: Creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="67fd4-126"><a name="pj15_GetStartedJSOM_UseJSOM"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-126"></span></span>

<span data-ttu-id="67fd4-127">サイトの各発行済みプロジェクトの ID、名前、および作成日を表示するアプリケーション ページを作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-127">Learn how to create an application page that displays the ID, name, and created date of each published project in a site.</span></span>
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a><span data-ttu-id="67fd4-128">プロジェクトを取得および反復処理するアプリケーション ページの作成の前提条件</span><span class="sxs-lookup"><span data-stu-id="67fd4-128">Prerequisites for creating an application page that retrieves and iterates through projects</span></span>
<span data-ttu-id="67fd4-129"><a name="pj15_GetStartedJSOM_Prereqs"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-129"></span></span>

<span data-ttu-id="67fd4-130">このトピックで説明するアプリケーション ページを開発するには、以下の製品をインストールおよび構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67fd4-130">To develop the application page that is described in this topic, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="67fd4-131">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="67fd4-131">SharePoint Server 2013</span></span>
- <span data-ttu-id="67fd4-132">に少なくとも 1 つの発行されたプロジェクトを Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="67fd4-132">Project Server 2013 with at least one published project</span></span>
- <span data-ttu-id="67fd4-133">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="67fd4-133">Visual Studio 2012</span></span>
- <span data-ttu-id="67fd4-134">Office Developer Tools for Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="67fd4-134">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="67fd4-135">SharePoint Server 2013 に拡張機能を配置し、プロジェクトを取得するためにアクセスを許可する必要があります。</span><span class="sxs-lookup"><span data-stu-id="67fd4-135">You must also have permissions to deploy the extension to SharePoint Server 2013 and to retrieve projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="67fd4-136">次の手順では、Project Server 2013 を実行しているコンピューター上で開発することを前提としています。</span><span class="sxs-lookup"><span data-stu-id="67fd4-136">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a><span data-ttu-id="67fd4-137">Visual Studio 2012 でアプリケーション ページを作成します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-137">Creating the application page in Visual Studio 2012</span></span>
<span data-ttu-id="67fd4-138"><a name="pj15_GetStartedJSOM_CreateVS"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-138"></span></span>

<span data-ttu-id="67fd4-p108">次の手順では、SharePoint プロジェクトと、テーブルとラベルを含むアプリケーション ページを作成します。テーブルにはプロジェクトに関する情報が表示され、ラベルにはエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="67fd4-p108">The following steps create a SharePoint project and an application page that contains a table and label. The table displays information about the projects and the label displays error messages.</span></span>
  
1. <span data-ttu-id="67fd4-141">Project Server 2013 を実行しているコンピューターに管理者として Visual Studio 2012 を実行します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-141">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="67fd4-142">次のように、SharePoint 2013 の空のプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-142">Create an empty SharePoint 2013 project, as follows:</span></span>
    
    1. <span data-ttu-id="67fd4-143">[ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-143">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
        
    2. <span data-ttu-id="67fd4-144">テンプレート カテゴリの一覧では、 **Office SharePoint**カテゴリを選択し、 **SharePoint 2013 のプロジェクト**テンプレートを選択し。</span><span class="sxs-lookup"><span data-stu-id="67fd4-144">In the list of template categories, choose the **Office SharePoint** category, and then choose the **SharePoint 2013 Project** template.</span></span> 
        
    3. <span data-ttu-id="67fd4-145">GetProjectsJSOM、プロジェクトの名前し、 **[OK** ] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="67fd4-145">Name the project GetProjectsJSOM, and then choose the **OK** button.</span></span> 
        
    4. <span data-ttu-id="67fd4-146">**SharePoint カスタマイズ ウィザード**] ダイアログ ボックスで**ファーム ソリューションとして配置する**] を選択し、[ **OK** ] を選択し、します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-146">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **OK** button.</span></span> 
    
3. <span data-ttu-id="67fd4-147">ソリューション エクスプ ローラーで、Project Web App インスタンスの URL と一致する**ProjectsJSOM**プロジェクトの**サイトの URL**プロパティの値を編集します (たとえば、 `http://ServerName/PWA`)。</span><span class="sxs-lookup"><span data-stu-id="67fd4-147">In Solution Explorer, edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `http://ServerName/PWA`).</span></span>
    
4. <span data-ttu-id="67fd4-148">**GetProjectsJSOM**プロジェクトのショートカット メニューを開き、SharePoint を追加し、「レイアウト」フォルダーがマップされています。</span><span class="sxs-lookup"><span data-stu-id="67fd4-148">Open the shortcut menu for the **GetProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
5. <span data-ttu-id="67fd4-149">**レイアウト**フォルダーに**GetProjectsJSOM**フォルダーのショートカット メニューを開くし、ProjectsList.aspx をという名前の新しい SharePoint アプリケーション ページを追加します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-149">In the **Layouts** folder, open the shortcut menu for the **GetProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="67fd4-150">次の使用例は、アプリケーション ページの Visual Studio 2012 を作成する分離コード ファイルを使用しません。</span><span class="sxs-lookup"><span data-stu-id="67fd4-150">This example does not use the code-behind file that Visual Studio 2012 creates for the application page.</span></span> 
  
6. <span data-ttu-id="67fd4-151">**ProjectsList.aspx**ページのショートカット メニューを開き、**スタートアップ アイテムとして設定**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-151">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
7. <span data-ttu-id="67fd4-152">**ProjectsList.aspx**ページのマークアップで次のようにテーブルと、"Main" **asp: コンテンツ**のタグの内部メッセージのプレース ホルダーを定義します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-152">In the markup for the **ProjectsList.aspx** page, define a table and a message placeholder inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
    ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Project name</th>
            <th width="25%" align="left">Created date</th>
            <th width="50%" align="left">Project ID</th>
        </tr>
    </table>
    <div id="divMessage">
        <br/>
        <span id="spanMessage" style="color: #FF0000;"></span>
    </div>
    ```

### <a name="retrieving-the-projects-collection"></a><span data-ttu-id="67fd4-153">プロジェクト コレクションの取得</span><span class="sxs-lookup"><span data-stu-id="67fd4-153">Retrieving the projects collection</span></span>
<span data-ttu-id="67fd4-154"><a name="pj15_GetStartedJSOM_RetrieveProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-154"></span></span>

<span data-ttu-id="67fd4-155">次の手順では、プロジェクト コレクションを取得および初期化します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-155">The following steps retrieve and initialize the projects collection.</span></span>
  
1. <span data-ttu-id="67fd4-156">後終了**div**タグは、ファイルを参照する、PS.js、次のように**SharePoint:ScriptLink**タグを追加します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-156">After the closing **div** tag, add a **SharePoint:ScriptLink** tag that references the PS.js file, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. <span data-ttu-id="67fd4-157">**SharePoint:ScriptLink**タグの下に次のように**スクリプト**タグを追加します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-157">Below the **SharePoint:ScriptLink** tag, add **script** tags, as follows.</span></span> 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. <span data-ttu-id="67fd4-158">次のように、プロジェクト コレクションを格納するためのグローバル変数を宣言します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-158">Declare a global variable to store the projects collection, as follows.</span></span>
    
   ```js
   var projects;
   ```

4. <span data-ttu-id="67fd4-159">**の SP を呼び出すSOD.executeOrDelayUntilScriptLoaded**メソッドにカスタム コードが実行される前に、PS.js ファイルがロードされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-159">Call the **SP.SOD.executeOrDelayUntilScriptLoaded** method to ensure that the PS.js file is loaded before your custom code runs.</span></span> 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. <span data-ttu-id="67fd4-160">次のように、現在のコンテキストに接続してプロジェクト コレクションを取得する関数を追加します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-160">Add a function that connects to the current context and retrieves the projects collection, as follows.</span></span>
    
   ```js
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
   ```

   <span data-ttu-id="67fd4-161">コンテキストを取得するいくつかのクライアント オブジェクトが含まれていないデータが初期化されるまでオブジェクトが初期化されるまでは、オブジェクトのプロパティ値にアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="67fd4-161">Some client objects that you retrieve through the context contain no data until they are initialized; that is, you cannot access the property values of the object until the object is initialized.</span></span> <span data-ttu-id="67fd4-162">さらに、 **ValueObject**の種類のプロパティは、必要があります明示的に要求したプロパティの値にアクセスすることができます前にします。</span><span class="sxs-lookup"><span data-stu-id="67fd4-162">Moreover, for properties of type **ValueObject**, you must explicitly request the property before you can access its value.</span></span> <span data-ttu-id="67fd4-163">(が初期化される前にプロパティにアクセスしようとする場合、 **PropertyOrFieldNotInitializedException**例外表示) されます。</span><span class="sxs-lookup"><span data-stu-id="67fd4-163">(If you try to access a property before it is initialized, you receive a **PropertyOrFieldNotInitializedException** exception.)</span></span> 
    
   <span data-ttu-id="67fd4-164">オブジェクトを初期化するには、 **load**メソッド (または、 **loadQuery**メソッド) を呼び出すと、 **executeQueryAsync**メソッドでは。</span><span class="sxs-lookup"><span data-stu-id="67fd4-164">To initialize an object, you call the **load** method (or the **loadQuery** method) and then the **executeQueryAsync** method.</span></span> 
    
   - <span data-ttu-id="67fd4-165">**読み込み**または**loadQuery**関数を呼び出して、サーバー上で実行する要求を登録します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-165">Calling the **load** function or the **loadQuery** function registers a request that you want to run on the server.</span></span> <span data-ttu-id="67fd4-166">取得するオブジェクトを表すパラメーターを渡します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-166">You pass in a parameter that represents the object that you want to retrieve.</span></span> <span data-ttu-id="67fd4-167">**ValueObject**プロパティを使用して作業している場合、またを要求するパラメーターのプロパティ。</span><span class="sxs-lookup"><span data-stu-id="67fd4-167">If you are working with a **ValueObject** property, then you also request the property in the parameter.</span></span> 
    
   - <span data-ttu-id="67fd4-168">**ExecuteQueryAsync**関数を呼び出すと、サーバーにクエリ要求が非同期的に送信します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-168">Calling the **executeQueryAsync** function sends the query request to the server asynchronously.</span></span> <span data-ttu-id="67fd4-169">成功コールバック関数、およびサーバーの応答が受信されたときに呼び出すの失敗コールバック関数を渡します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-169">You pass in a success callback function and a failure callback function to invoke when the server response is received.</span></span> 
    
   <span data-ttu-id="67fd4-170">ネットワーク トラフィックを減らすためには、**読み込み**関数を呼び出すときに使用するプロパティだけを要求します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-170">To reduce network traffic, request only the properties that you want to work with when you call the **load** function.</span></span> <span data-ttu-id="67fd4-171">さらに、複数のオブジェクトで作業している場合をグループ化**を読み込む**関数を複数回呼び出すことが可能な場合、 **executeQueryAsync**関数を呼び出す前に。</span><span class="sxs-lookup"><span data-stu-id="67fd4-171">In addition, if you are working with multiple objects, group multiple calls to the **load** function before you call the **executeQueryAsync** function when it is possible.</span></span> 
    
### <a name="iterating-through-the-projects-collection"></a><span data-ttu-id="67fd4-172">プロジェクト コレクションの反復処理</span><span class="sxs-lookup"><span data-stu-id="67fd4-172">Iterating through the projects collection</span></span>
<span data-ttu-id="67fd4-173"><a name="pj15_GetStartedJSOM_IterateProjs"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-173"></span></span>

<span data-ttu-id="67fd4-174">次の手順では、プロジェクト コレクションを反復処理 (サーバーの呼び出しが成功の場合)、またはエラー メッセージを表示 (呼び出しが失敗の場合) します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-174">The following steps iterate through the projects collection (if the server call is successful) or render an error message (if the call fails).</span></span>
  
1. <span data-ttu-id="67fd4-175">次のように、プロジェクト コレクションを反復処理する成功のコールバック関数を追加します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-175">Add a success callback function that iterates through the projects collection, as follows.</span></span>
    
   ```js
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
   ```

2. <span data-ttu-id="67fd4-176">次のように、エラー メッセージを表示する失敗のコールバック関数を追加します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-176">Add a failure callback function that renders an error message, as follows.</span></span>
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. <span data-ttu-id="67fd4-177">メニュー バーの [アプリケーション] ページをテストするのには、**デバッグ**、**デバッグの開始**を選択します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-177">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**.</span></span> <span data-ttu-id="67fd4-178">Web.config ファイルを変更するメッセージが表示されたら、 **[ok]** を選択します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-178">If you are prompted to modify the web.config file, choose **OK**.</span></span>

<span data-ttu-id="67fd4-179"><a name="pj15_GetStartedJSOM_CompleteExample"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-179"></span></span>

## <a name="complete-code-example"></a><span data-ttu-id="67fd4-180">完全なコード例</span><span class="sxs-lookup"><span data-stu-id="67fd4-180">Complete code example</span></span>

<span data-ttu-id="67fd4-181">以下は ProjectsList.aspx ファイルの完全なコードです。</span><span class="sxs-lookup"><span data-stu-id="67fd4-181">Following is the complete code from the ProjectsList.aspx file.</span></span>
  
```js
<%@ Assembly Name="$SharePoint.Project.AssemblyFullName$" %>
<%@ Import Namespace="Microsoft.SharePoint.ApplicationPages" %>
<%@ Register Tagprefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Register Tagprefix="asp" Namespace="System.Web.UI" Assembly="System.Web.Extensions, Version=3.5.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35" %>
<%@ Import Namespace="Microsoft.SharePoint" %>
<%@ Assembly Name="Microsoft.Web.CommandUI, Version=15.0.0.0, Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="ProjectsList.aspx.cs" Inherits="GetProjectsJSOM.Layouts.GetProjectsJSOM.ProjectsList" DynamicMasterPageFile="~masterurl/default.master" %>
<asp:Content ID="PageHead" ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
</asp:Content>
<asp:Content ID="Main" ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <table width="100%" id="tblProjects">
    <tr id="headerRow">
        <th width="25%" align="left">Project name</th>
        <th width="25%" align="left">Created date</th>
        <th width="50%" align="left">Project ID</th>
    </tr>
</table>
<div id="divMessage">
    <br/>
    <span id="spanMessage" style="color: #FF0000;"></span>
</div>
<SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
<script type="text/javascript">
    // Declare a variable to store the published projects that exist
    // in the current context.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the
        // Name, CreatedDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, CreatedDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(onQuerySucceeded, onQueryFailed);
    }
    function onQuerySucceeded(sender, args) {
        // Get the enumerator and iterate through the collection.
        var projectEnumerator = projects.getEnumerator();
        while (projectEnumerator.moveNext()) {
            var project = projectEnumerator.get_current();
            // Create the row for the project's information.
            var row = tblProjects.insertRow();
            // Insert cells for the Id, Name, and CreatedDate properties.
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_createdDate();
            row.insertCell().innerText = project.get_id();
        }
    }
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
</script>
</asp:Content>
<asp:Content ID="PageTitle" ContentPlaceHolderID="PlaceHolderPageTitle" runat="server">
Application Page
</asp:Content>
<asp:Content ID="PageTitleInTitleArea" ContentPlaceHolderID="PlaceHolderPageTitleInTitleArea" runat="server" >
My Application Page
</asp:Content>

```

<span data-ttu-id="67fd4-182"><a name="pj15_GetStartedJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="67fd4-182"></span></span>

## <a name="see-also"></a><span data-ttu-id="67fd4-183">関連項目</span><span class="sxs-lookup"><span data-stu-id="67fd4-183">See also</span></span>

- [<span data-ttu-id="67fd4-184">作成、取得、更新、およびプロジェクトのサーバーの JavaScript オブジェクト モデルを使用してプロジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="67fd4-184">Create, retrieve, update, and delete projects by using the Project Server JavaScript object model</span></span>](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [<span data-ttu-id="67fd4-185">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="67fd4-185">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
- [<span data-ttu-id="67fd4-186">プロジェクト サーバー CSOM および .NET の概要</span><span class="sxs-lookup"><span data-stu-id="67fd4-186">Getting started with the Project Server CSOM and .NET</span></span>](getting-started-with-the-project-server-csom-and-net.md)
    

