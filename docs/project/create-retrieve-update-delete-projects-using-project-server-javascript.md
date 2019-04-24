---
title: Project Server JavaScript を使用してプロジェクトを作成、取得、更新、および削除する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: 現在の projectcontext インスタンスを取得します。サーバー上の発行済みプロジェクトのコレクションを取得し、反復処理を行います。project Server JavaScript オブジェクトモデルを使用して、プロジェクトの作成、取得、チェックアウト、削除を行うことができます。プロジェクトのプロパティを変更します。
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322667"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a><span data-ttu-id="36aa5-103">Project Server JavaScript を使用してプロジェクトを作成、取得、更新、および削除する</span><span class="sxs-lookup"><span data-stu-id="36aa5-103">Create, retrieve, update, and delete projects using Project Server JavaScript</span></span>

<span data-ttu-id="36aa5-104">この記事のシナリオでは、現在の**projectcontext**インスタンスを取得する方法について説明します。サーバー上の発行済みプロジェクトのコレクションを取得し、反復処理を行います。project Server JavaScript オブジェクトモデルを使用して、プロジェクトの作成、取得、チェックアウト、削除を行うことができます。プロジェクトのプロパティを変更します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-104">The scenarios in this article show how to get the current **ProjectContext** instance; retrieve and iterate through the collection of published projects on the server; create, retrieve, check out, and delete a project by using the Project Server JavaScript object model; and change a project's properties.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="36aa5-105">これらのシナリオでは、SharePoint アプリケーションページのマークアップにカスタムコードを定義していますが、ページ用に Visual Studio 2012 が作成する分離コードファイルは使用しません。</span><span class="sxs-lookup"><span data-stu-id="36aa5-105">These scenarios define custom code in the markup of a SharePoint application page but do not use the code-behind file that Visual Studio 2012 creates for the page.</span></span> 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a><span data-ttu-id="36aa5-106">JavaScript オブジェクトモデルで Project Server 2013 プロジェクトを使用するための前提条件</span><span class="sxs-lookup"><span data-stu-id="36aa5-106">Prerequisites for working with Project Server 2013 projects in the JavaScript object model</span></span>

<span data-ttu-id="36aa5-107">この記事で説明するシナリオを実行するには、次の製品をインストールおよび構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="36aa5-107">To perform the scenarios that are described in this article, you must install and configure the following products:</span></span>
  
- <span data-ttu-id="36aa5-108">SharePoint Server 2013</span><span class="sxs-lookup"><span data-stu-id="36aa5-108">SharePoint Server 2013</span></span>
- <span data-ttu-id="36aa5-109">Project Server 2013</span><span class="sxs-lookup"><span data-stu-id="36aa5-109">Project Server 2013</span></span>
- <span data-ttu-id="36aa5-110">Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="36aa5-110">Visual Studio 2012</span></span>
- <span data-ttu-id="36aa5-111">Office Developer Tools for Visual Studio 2012</span><span class="sxs-lookup"><span data-stu-id="36aa5-111">Office Developer Tools for Visual Studio 2012</span></span>
    
<span data-ttu-id="36aa5-112">また、SharePoint Server 2013 に拡張機能を展開し、プロジェクトに投稿する権限も必要です。</span><span class="sxs-lookup"><span data-stu-id="36aa5-112">You must also have permissions to deploy the extension to SharePoint Server 2013 and to contribute to projects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="36aa5-113">これらの手順は、Project Server 2013 を実行しているコンピューター上で開発していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="36aa5-113">These instructions assume that you are developing on the computer that is running Project Server 2013.</span></span> 
  
## <a name="create-the-visual-studio-solution"></a><span data-ttu-id="36aa5-114">Visual Studio ソリューションを作成する</span><span class="sxs-lookup"><span data-stu-id="36aa5-114">Create the Visual Studio solution</span></span>
<span data-ttu-id="36aa5-115"><a name="pj15_CRUDProjectsJSOM_Setup"> </a></span><span class="sxs-lookup"><span data-stu-id="36aa5-115"></span></span>

<span data-ttu-id="36aa5-116">次の手順では、SharePoint プロジェクトとアプリケーションページを含む Visual Studio 2012 ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-116">The following steps create a Visual Studio 2012 solution that contains a SharePoint project and an application page.</span></span> <span data-ttu-id="36aa5-117">ページには、プロジェクトを操作するためのロジックが含まれます。</span><span class="sxs-lookup"><span data-stu-id="36aa5-117">The page contains the logic for working with projects.</span></span>
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a><span data-ttu-id="36aa5-118">Visual Studio で SharePoint を作成するには</span><span class="sxs-lookup"><span data-stu-id="36aa5-118">To create the SharePoint project in Visual Studio</span></span>

1. <span data-ttu-id="36aa5-119">Project Server 2013 を実行しているコンピューターで、Visual Studio 2012 を管理者として実行します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-119">On the computer that is running Project Server 2013, run Visual Studio 2012 as an administrator.</span></span>
    
2. <span data-ttu-id="36aa5-120">メニュー バーで、[ **ファイル**]、[ **新規作成**]、[ **プロジェクト**] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-120">On the menu bar, choose **File**, **New**, **Project**.</span></span>
    
3. <span data-ttu-id="36aa5-121">[**新しいプロジェクト**] ダイアログ ボックスで、ダイアログ ボックスの上部にあるドロップダウン リストから [**.NET Framework 4.5**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-121">In the **New Project** dialog box, choose **.NET Framework 4.5** from the drop-down list at the top of the dialog box.</span></span> 
    
4. <span data-ttu-id="36aa5-122">[**Office/SharePoint**] テンプレート カテゴリで、[**SharePoint ソリューション**] を選択してから、[**SharePoint 2013 プロジェクト**] テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-122">In the **Office/SharePoint** template category, choose **SharePoint Solutions**, and then choose the **SharePoint 2013 Project** template.</span></span> 
    
5. <span data-ttu-id="36aa5-123">プロジェクトに「プロジェクト名」という名前を指定し、[ **OK** ] ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-123">Name the project ProjectsJSOM, and then choose the **OK** button.</span></span> 
    
6. <span data-ttu-id="36aa5-124">[ **SharePoint カスタマイズ ウィザード**] ダイアログ ボックスで、[ **ファーム ソリューションとして配置する**] を選択して、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="36aa5-124">In the **SharePoint Customization Wizard** dialog box, choose **Deploy as a farm solution**, and then choose the **Finish** button.</span></span> 
    
7. <span data-ttu-id="36aa5-125">project Web App インスタンスの url と一致するよう\*\*\*\* に、プロジェクトの**サイト url**プロパティの値を編集します (例: `https://ServerName/PWA`)。</span><span class="sxs-lookup"><span data-stu-id="36aa5-125">Edit the value of the **Site URL** property for the **ProjectsJSOM** project to match the URL of the Project Web App instance (for example,  `https://ServerName/PWA`).</span></span>
    
### <a name="to-create-the-application-page-in-visual-studio"></a><span data-ttu-id="36aa5-126">Visual Studio でアプリケーション ページを作成するには</span><span class="sxs-lookup"><span data-stu-id="36aa5-126">To create the application page in Visual Studio</span></span>

1. <span data-ttu-id="36aa5-127">**ソリューション エクスプローラー**で、**ProjectsJSOM** プロジェクトのショートカット メニューを開き、SharePoint のマップされた "Layouts" フォルダーを追加します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-127">In **Solution Explorer**, open the shortcut menu for the **ProjectsJSOM** project, and then add a SharePoint "Layouts" mapped folder.</span></span> 
    
2. <span data-ttu-id="36aa5-128">**Layouts**フォルダーで、**プロジェクトプロジェクト**のショートカットメニューを開き、新しい SharePoint アプリケーションページを「プロジェクトリスト .aspx」という名前で追加します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-128">In the **Layouts** folder, open the shortcut menu for the **ProjectsJSOM** folder, and then add a new SharePoint application page named ProjectsList.aspx.</span></span>
    
3. <span data-ttu-id="36aa5-129">[**ProjectsList.aspx**] ページのショートカット メニューを開き、[**スタートアップ アイテムとして設定**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-129">Open the shortcut menu for the **ProjectsList.aspx** page and choose **Set as Startup Item**.</span></span>
    
4. <span data-ttu-id="36aa5-130">**ProjectsList.aspx** ページのマークアップで、"Main" **asp:Content** タグ内のユーザー インターフェイス コントロールを次のように定義します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-130">In the markup for the **ProjectsList.aspx** page, define user interface controls inside the "Main" **asp:Content** tags, as follows.</span></span> 
    
   ```HTML
    <table width="100%" id="tblProjects">
        <tr id="headerRow">
            <th width="25%" align="left">Name</th>
            <th width="25%" align="left">Description</th>
            <th width="25%" align="left">Start Date</th>
            <th width="25%" align="left">ID</th>
        </tr>
    </table>
    <textarea id="txtGuid" rows="1" cols="35">Paste the project GUID here.</textarea>
    <button id="btnSend" type="button"></button><br />
    <span id="spanMessage" style="color: #FF0000;"></span>
   ```

   > [!NOTE]
   > <span data-ttu-id="36aa5-131">これらのコントロールは、すべてのシナリオで使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="36aa5-131">These controls may not be used in every scenario.</span></span> <span data-ttu-id="36aa5-132">たとえば、"プロジェクトの作成" シナリオでは **textarea** および **button**コントロールを使用しません。</span><span class="sxs-lookup"><span data-stu-id="36aa5-132">For example, the "Create projects" scenario does not use the **textarea** and **button** controls.</span></span> 
  
5. <span data-ttu-id="36aa5-133">**span** タグを閉じた後で、**SharePoint:ScriptLink** タグ、**SharePoint:FormDigest** タグ、および **script** タグを次のように追加します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-133">After the closing **span** tag, add a **SharePoint:ScriptLink** tag, a **SharePoint:FormDigest** tag, and **script** tags, as follows.</span></span> 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   <span data-ttu-id="36aa5-134">**SharePoint: scriptlink**タグは、プロジェクトサーバー2013の JavaScript オブジェクトモデルを定義する、.ps ファイルを参照します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-134">The **SharePoint:ScriptLink** tag references the PS.js file, which defines the JavaScript object model for Project Server 2013.</span></span> <span data-ttu-id="36aa5-135">**SharePoint: formdigest**タグは、サーバーのコンテンツを更新する操作で必要とされる場合に、セキュリティ検証のためにメッセージダイジェストを生成します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-135">The **SharePoint:FormDigest** tag generates a message digest for security validation when required by operations that update server content.</span></span> 
    
6. <span data-ttu-id="36aa5-136">プレースホルダー コメントを、次のいずれかの手順のコードで置換します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-136">Replace the placeholder comment with the code from one of the following procedures:</span></span>
    
   - [<span data-ttu-id="36aa5-137">JavaScript オブジェクトモデルを使用して Project Server 2013 プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="36aa5-137">Create Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [<span data-ttu-id="36aa5-138">JavaScript オブジェクトモデルを使用して Project Server 2013 プロジェクトを更新する</span><span class="sxs-lookup"><span data-stu-id="36aa5-138">Update Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [<span data-ttu-id="36aa5-139">JavaScript オブジェクトモデルを使用して Project Server 2013 プロジェクトを削除する</span><span class="sxs-lookup"><span data-stu-id="36aa5-139">Delete Project Server 2013 projects by using the JavaScript object model</span></span>](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. <span data-ttu-id="36aa5-p104">アプリケーション ページをテストするには、メニュー バーの [**デバッグ**] を選択し、[**デバッグの開始**] をクリックします。web.config ファイルの変更を求められたら、[**OK**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-p104">To test the application page, on the menu bar, choose **Debug**, **Start Debugging**. If you are prompted to modify the web.config file, choose **OK**.</span></span>
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="36aa5-142">JavaScript オブジェクトモデルを使用して Project Server 2013 プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="36aa5-142">Create Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="36aa5-143"><a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="36aa5-143"></span></span>

<span data-ttu-id="36aa5-144">このセクションの手順では、JavaScript オブジェクトモデルを使用してプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-144">The procedure in this section creates projects by using the JavaScript object model.</span></span> <span data-ttu-id="36aa5-145">手順には、次の概要手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="36aa5-145">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="36aa5-146">現在の **ProjectContext** インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-146">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="36aa5-147">**ProjectCreationInformation** オブジェクトを作成して、プロジェクトの初期プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-147">Create a **ProjectCreationInformation** object to specify initial properties for your project.</span></span> <span data-ttu-id="36aa5-148">**ProjectCreationInformation.set_name** 関数を使用して、必要な **name** プロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-148">Specify the required **name** property by using the **ProjectCreationInformation.set_name** function.</span></span> 
    
3. <span data-ttu-id="36aa5-149">**ProjectContext.get_projects** 関数を使用して、発行済みのプロジェクトをサーバーから取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-149">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="36aa5-150">**get_projects** 関数は **ProjectCollection** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-150">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
4. <span data-ttu-id="36aa5-151">**ProjectCollection.add** 関数を使用し、**ProjectCreationInformation** オブジェクトを渡して、コレクションに新しいプロジェクトを追加します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-151">Add the new project to the collection by using the **ProjectCollection.add** function and passing in the **ProjectCreationInformation** object.</span></span> 
    
5. <span data-ttu-id="36aa5-152">**ProjectCollection.update** 関数と **ProjectContext.waitForQueueAsync** 関数を使用してコレクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-152">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="36aa5-153">**update** 関数は、**waitForQueueAsync** に渡す **QueueJob** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-153">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span> <span data-ttu-id="36aa5-154">この呼び出しは、プロジェクトも発行します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-154">This call also publishes the project.</span></span>
    
<span data-ttu-id="36aa5-155">「**Visual Studio でアプリケーション ページを作成するには**」の手順で追加した **script** タグの間に、次に示すコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="36aa5-155">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare a global variable to store the project collection.
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(CreateProject, "PS.js");
    // Add a project the projects collection.
    function CreateProject() {
        
        // Initialize the current client context.
        var projContext = PS.ProjectContext.get_current();
        // Initialize a ProjectCreationInformation object and specify properties
        // for the new project.
        // The Name property is required and must be unique.
        var creationInfo = new PS.ProjectCreationInformation();
        creationInfo.set_name("Test Project 1");
        // Specify optional properties for the new project.
        // If not specified, the Start property uses the current date and the
        // EnterpriseProjectTypeId property uses the default EPT.
        creationInfo.set_description("Created through the JSOM.");
        creationInfo.set_start("2013-10-01 09:00:00.000");
        // Get the projects collection.
        projects = projContext.get_projects();
        // Add the new project to the projects collection.
        projects.add(creationInfo);
        // Add a second project to use in the deleting projects procedure.
        creationInfo.set_name("Test Project 2");
        projects.add(creationInfo);
        // Submit the request to update the collection on the server
        var updateJob = projects.update();
        projContext.waitForQueueAsync(updateJob, 10, GetProjects);
    }
    // Get the projects collection.
    function GetProjects(response) {
        // This call demonstrates that you can get the context from the 
        // ProjectCollection object.
        var projContext = projects.get_context();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // This scenario does not use the textarea or button controls.
        $get("txtGuid").disabled = true;
        $get("btnSend").disabled = true;
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="36aa5-156">JavaScript オブジェクトモデルを使用して Project Server 2013 プロジェクトを更新する</span><span class="sxs-lookup"><span data-stu-id="36aa5-156">Update Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="36aa5-157"><a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="36aa5-157"></span></span>

<span data-ttu-id="36aa5-158">このセクションの手順では、JavaScript オブジェクトモデルを使用してプロジェクトの**startDate**プロパティを更新します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-158">The procedure in this section updates the **startDate** property of a project by using the JavaScript object model.</span></span> <span data-ttu-id="36aa5-159">手順には、次の概要手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="36aa5-159">The procedure includes the following high-level steps:</span></span> 
  
1. <span data-ttu-id="36aa5-160">現在の **ProjectContext** インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-160">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="36aa5-161">**ProjectContext.get_projects** 関数を使用して、発行済みのプロジェクトをサーバーから取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-161">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="36aa5-162">**get_projects** 関数は **ProjectCollection** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-162">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="36aa5-163">**ProjectContext.load** 関数と **ProjectContext.executeQueryAsync** 関数を使用して、サーバーで要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-163">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="36aa5-164">**ProjectContext.getById** 関数を使用して、**PublishedProject** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-164">Retrieve a **PublishedProject** object by using the **ProjectContext.getById** function.</span></span> 
    
5. <span data-ttu-id="36aa5-165">**Project.checkOut** 関数を使用してターゲット プロジェクトをチェックアウトします。</span><span class="sxs-lookup"><span data-stu-id="36aa5-165">Check out the target project by using the **Project.checkOut** function.</span></span> <span data-ttu-id="36aa5-166">**checkOut** 関数は、発行されたプロジェクトのドラフト バージョンを返します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-166">The **checkOut** function returns the draft version of the published project.</span></span> 
    
6. <span data-ttu-id="36aa5-167">**DraftProject.set_startDate** 関数を使用して、プロジェクトの開始日を変更します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-167">Change the project's start date by using the **DraftProject.set_startDate** function.</span></span> 
    
7. <span data-ttu-id="36aa5-168">**DraftProject.publish** 関数と **ProjectContext.waitForQueueAsync** 関数を使用してプロジェクトを発行します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-168">Publish the project by using the **DraftProject.publish** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="36aa5-169">**publish** 関数は、**waitForQueueAsync** に渡す **QueueJob** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-169">The **publish** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="36aa5-170">「**Visual Studio でアプリケーション ページを作成するには**」の手順で追加した **script** タグの間に、次に示すコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="36aa5-170">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { ChangeProject(); };
        $get("btnSend").innerText = "Update";
    }
    // Change the project's start date.
    function ChangeProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then check it out. The checkOut function
        // returns the draft version of the project.
        var project = projects.getById(targetGuid);
        var draftProject = project.checkOut();
        // Set the new property value and then publish the project.
        // Specify "true" to also check the project in.
        draftProject.set_startDate("2013-12-31 09:00:00.000");
        var publishJob = draftProject.publish(true);
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(publishJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a><span data-ttu-id="36aa5-171">JavaScript オブジェクトモデルを使用して Project Server 2013 プロジェクトを削除する</span><span class="sxs-lookup"><span data-stu-id="36aa5-171">Delete Project Server 2013 projects by using the JavaScript object model</span></span>
<span data-ttu-id="36aa5-172"><a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a></span><span class="sxs-lookup"><span data-stu-id="36aa5-172"></span></span>

<span data-ttu-id="36aa5-173">このセクションの手順では、JavaScript オブジェクトモデルを使用してプロジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-173">The procedure in this section deletes a project by using the JavaScript object model.</span></span> <span data-ttu-id="36aa5-174">手順には、次の概要手順が含まれます。</span><span class="sxs-lookup"><span data-stu-id="36aa5-174">The procedure includes the following high-level steps:</span></span>
  
1. <span data-ttu-id="36aa5-175">現在の **ProjectContext** インスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-175">Get the current **ProjectContext** instance.</span></span> 
    
2. <span data-ttu-id="36aa5-176">**ProjectContext.get_projects** 関数を使用して、発行済みのプロジェクトをサーバーから取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-176">Retrieve the published projects from the server by using the **ProjectContext.get_projects** function.</span></span> <span data-ttu-id="36aa5-177">**get_projects** 関数は **ProjectCollection** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-177">The **get_projects** function returns a **ProjectCollection** object.</span></span> 
    
3. <span data-ttu-id="36aa5-178">**ProjectContext.load** 関数と **ProjectContext.executeQueryAsync** 関数を使用して、サーバーで要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-178">Run the request on the server by using the **ProjectContext.load** function and the **ProjectContext.executeQueryAsync** function.</span></span> 
    
4. <span data-ttu-id="36aa5-179">**ProjectCollection.getById** 関数を使用して、**PublishedProject** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-179">Retrieve a **PublishedProject** object by using the **ProjectCollection.getById** function.</span></span> 
    
5. <span data-ttu-id="36aa5-180">**ProjectCollection.remove** 関数に渡すことでプロジェクトを削除します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-180">Delete the project by passing it to the **ProjectCollection.remove** function.</span></span> 
    
6. <span data-ttu-id="36aa5-181">**ProjectCollection.update** 関数と **ProjectContext.waitForQueueAsync** 関数を使用してコレクションを更新します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-181">Update the collection by using the **ProjectCollection.update** function and the **ProjectContext.waitForQueueAsync** function.</span></span> <span data-ttu-id="36aa5-182">**update** 関数は、**waitForQueueAsync** に渡す **QueueJob** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="36aa5-182">The **update** function returns a **QueueJob** object that you pass to **waitForQueueAsync**.</span></span>
    
<span data-ttu-id="36aa5-183">「**Visual Studio でアプリケーション ページを作成するには**」の手順で追加した **script** タグの間に、次に示すコードを貼り付けます。</span><span class="sxs-lookup"><span data-stu-id="36aa5-183">Paste the following code between the **script** tags that you added in the **To create the application page in Visual Studio** procedure.</span></span> 
  
```js
    // Declare global variables.
    var projContext;
    var projects;
    // Ensure that the PS.js file is loaded before your custom code runs.
    SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
    // Get the projects collection.
    function GetProjects() {
        // Initialize the current client context.
        projContext = PS.ProjectContext.get_current();
        // Get the projects collection.
        projects = projContext.get_projects();
        // Register the request for information that you want to run on the server.
        // This call includes an optional "Include" parameter to request only the Name, Description,
        // StartDate, and Id properties of the projects in the collection.
        projContext.load(projects, 'Include(Name, Description, StartDate, Id)');
        // Run the request on the server.
        projContext.executeQueryAsync(IterateThroughProjects, QueryFailed);
    }
    // Iterate through the projects collection.
    function IterateThroughProjects(response) {
        // Get the enumerator and iterate through the collection.
        var enumerator = projects.getEnumerator();
        while (enumerator.moveNext()) {
            var project = enumerator.get_current();
            // Create and populate a row with the values for the project's Name, Description,
            // StartDate, and Id properties.
            var row = tblProjects.insertRow();
            row.insertCell().innerText = project.get_name();
            row.insertCell().innerText = project.get_description();
            row.insertCell().innerText = project.get_startDate();
            row.insertCell().innerText = project.get_id();
        }
        // Initialize button properties.
        $get("btnSend").onclick = function () { DeleteProject(); };
        $get("btnSend").innerText = "Delete";
    }
    // Delete the project.
    function DeleteProject() {
        // Get the identifier of the target project.
        var targetGuid = $get("txtGuid").innerText;
        // Get the target project and then remove it from the collection.
        var project = projects.getById(targetGuid);
        projects.remove(project);
        var removeJob = projects.update();
        // Register the job that you want to run on the server and specify the
        // timeout duration and callback function.
        projContext.waitForQueueAsync(removeJob, 10, QueueJobSent);
    }
    // Print the JobState return code, which gives the status of the queue job.
    function QueueJobSent(response) {
        $get("spanMessage").innerText = 'JobState = ' + response + '. Wait a few seconds, then refresh the page to see your changes.';
    }
    function QueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
```

<span data-ttu-id="36aa5-184"><a name="pj15_CRUDProjectsJSOM_AR"> </a></span><span class="sxs-lookup"><span data-stu-id="36aa5-184"></span></span>

## <a name="see-also"></a><span data-ttu-id="36aa5-185">関連項目</span><span class="sxs-lookup"><span data-stu-id="36aa5-185">See also</span></span>

- [<span data-ttu-id="36aa5-186">Project のプログラミング タスク</span><span class="sxs-lookup"><span data-stu-id="36aa5-186">Project programming tasks</span></span>](project-programming-tasks.md)
- [<span data-ttu-id="36aa5-187">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="36aa5-187">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

