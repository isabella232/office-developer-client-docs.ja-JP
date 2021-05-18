---
title: サーバー JavaScript を使用してプロジェクトを作成、取得、更新Project削除する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 6b690938-05bc-46a3-a40e-30f081403767
description: 現在の ProjectContext インスタンスを取得します。サーバー上の発行済みプロジェクトのコレクションを取得して反復処理します。サーバー JavaScript オブジェクト モデルを使用して、プロジェクトを作成、取得、チェックアウトProject削除します。をクリックし、プロジェクトのプロパティを変更します。
ms.openlocfilehash: 10dac7edfa3e84cebfd0585bc8c4bff1ea22ea44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322667"
---
# <a name="create-retrieve-update-and-delete-projects-using-project-server-javascript"></a>サーバー JavaScript を使用してプロジェクトを作成、取得、更新Project削除する

この記事のシナリオでは、現在の ProjectContext インスタンスを取得 **する方法を示** します。サーバー上の発行済みプロジェクトのコレクションを取得して反復処理します。サーバー JavaScript オブジェクト モデルを使用して、プロジェクトを作成、取得、チェックアウトProject削除します。をクリックし、プロジェクトのプロパティを変更します。 
  
> [!NOTE]
> これらのシナリオでは、SharePoint アプリケーション ページのマークアップでカスタム コードを定義しますが、2012 年に 2012 年に作成されるコード Visual Studio ファイルは使用しません。 
  
## <a name="prerequisites-for-working-with-project-server-2013-projects-in-the-javascript-object-model"></a>JavaScript オブジェクト モデルProject Server 2013 プロジェクトを操作するための前提条件

この記事で説明するシナリオを実行するには、次の製品をインストールおよび構成する必要があります。
  
- SharePoint Server 2013
- Project Server 2013
- Visual Studio 2012
- Office Developer Tools for Visual Studio 2012
    
また、拡張機能をサーバー 2013 に展開し、プロジェクトにSharePointアクセス許可を持っている必要があります。
  
> [!NOTE]
> これらの手順では、サーバー 2013 で実行されているコンピューターで開発Project想定しています。 
  
## <a name="create-the-visual-studio-solution"></a>Visual Studio ソリューションを作成する
<a name="pj15_CRUDProjectsJSOM_Setup"> </a>

次の手順では、Visual Studioとアプリケーション ページを含む 2012 SharePointを作成します。 ページには、プロジェクトを操作するためのロジックが含まれます。
  
### <a name="to-create-the-sharepoint-project-in-visual-studio"></a>Visual Studio で SharePoint を作成するには

1. サーバー 2013 で実行されているProject、管理者として 2012 Visual Studioを実行します。
    
2. メニュー バーで、[ **ファイル**]、[ **新規作成**]、[ **プロジェクト**] の順に選択します。
    
3. [**新しいプロジェクト**] ダイアログ ボックスで、ダイアログ ボックスの上部にあるドロップダウン リストから [**.NET Framework 4.5**] を選択します。 
    
4. [**Office/SharePoint**] テンプレート カテゴリで、[**SharePoint ソリューション**] を選択してから、[**SharePoint 2013 プロジェクト**] テンプレートを選択します。 
    
5. ProjectJSOM に名前を付け **、[OK] ボタンを選択** します。 
    
6. [ **SharePoint カスタマイズ ウィザード**] ダイアログ ボックスで、[ **ファーム ソリューションとして配置する**] を選択して、[ **完了**] をクリックします。 
    
7. **ProjectsJSOM** プロジェクトの **Site URL** プロパティの値を編集して、インスタンスの URL (たとえば、 ) Project Web App一致します `https://ServerName/PWA` 。
    
### <a name="to-create-the-application-page-in-visual-studio"></a>Visual Studio でアプリケーション ページを作成するには

1. **ソリューション エクスプローラー** で、**ProjectsJSOM** プロジェクトのショートカット メニューを開き、SharePoint のマップされた "Layouts" フォルダーを追加します。 
    
2. [レイアウト **] フォルダーで****、ProjectsJSOM** フォルダーのショートカット メニューを開き、ProjectsList.aspx という名前SharePoint新しいアプリケーション ページを追加します。
    
3. [**ProjectsList.aspx**] ページのショートカット メニューを開き、[**スタートアップ アイテムとして設定**] を選択します。
    
4. **ProjectsList.aspx** ページのマークアップで、"Main" **asp:Content** タグ内のユーザー インターフェイス コントロールを次のように定義します。 
    
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
   > これらのコントロールは、すべてのシナリオで使用されるとは限りません。たとえば、"プロジェクトの作成" シナリオでは **textarea** および **button** コントロールを使用しません。 
  
5. **span** タグを閉じた後で、**SharePoint:ScriptLink** タグ、**SharePoint:FormDigest** タグ、および **script** タグを次のように追加します。 
    
   ```HTML
    <SharePoint:ScriptLink id="ScriptLink" name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
    <SharePoint:FormDigest id="FormDigest" runat="server" />
    <script type="text/javascript">
        // Replace this comment with the code for your scenario.
    </script>
   ```

   **SharePoint:ScriptLink** タグは、PS.js Server 2013 の JavaScript オブジェクト モデルを定義する Project ファイルを参照します。 この **SharePoint:FormDigest** タグは、サーバー コンテンツを更新する操作で必要な場合に、セキュリティ検証用のメッセージ ダイジェストを生成します。 
    
6. プレースホルダー コメントを、次のいずれかの手順のコードで置換します。
    
   - [JavaScript Projectを使用してサーバー 2013 プロジェクトを作成する](#pj15_CRUDProjectsJSOM_CreateProjects)
    
   - [JavaScript Projectを使用して、Server 2013 プロジェクトを更新する](#pj15_CRUDProjectsJSOM_UpdateProjects)
    
   - [JavaScript Projectを使用して Server 2013 プロジェクトを削除する](#pj15_CRUDProjectsJSOM_DeleteProjects)
    
7. アプリケーション ページをテストするには、メニュー バーの [**デバッグ**] を選択し、[**デバッグの開始**] をクリックします。web.config ファイルの変更を求められたら、[**OK**] を選択します。
    
## <a name="create-project-server-2013-projects-by-using-the-javascript-object-model"></a>JavaScript Projectを使用してサーバー 2013 プロジェクトを作成する
<a name="pj15_CRUDProjectsJSOM_CreateProjects"> </a>

このセクションの手順では、JavaScript オブジェクト モデルを使用してプロジェクトを作成します。 手順には、次の概要手順が含まれます。
  
1. 現在の **ProjectContext** インスタンスを取得します。 
    
2. **ProjectCreationInformation** オブジェクトを作成して、プロジェクトの初期プロパティを指定します。**ProjectCreationInformation.set_name** 関数を使用して、必要な **name** プロパティを指定します。 
    
3. **ProjectContext.get_projects** 関数を使用して、発行済みのプロジェクトをサーバーから取得します。**get_projects** 関数は **ProjectCollection** オブジェクトを返します。 
    
4. **ProjectCollection.add** 関数を使用し、**ProjectCreationInformation** オブジェクトを渡して、コレクションに新しいプロジェクトを追加します。 
    
5. **ProjectCollection.update** 関数および **ProjectContext.waitForQueueAsync** 関数を使用してコレクションを更新します。**update** 関数は、**waitForQueueAsync** に渡す **QueueJob** オブジェクトを返します。この呼び出しは、プロジェクトも発行します。
    
「**Visual Studio でアプリケーション ページを作成するには**」の手順で追加した **script** タグの間に、次に示すコードを貼り付けます。 
  
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

## <a name="update-project-server-2013-projects-by-using-the-javascript-object-model"></a>JavaScript Projectを使用して、Server 2013 プロジェクトを更新する
<a name="pj15_CRUDProjectsJSOM_UpdateProjects"> </a>

このセクションの手順では **、JavaScript** オブジェクト モデルを使用してプロジェクトの startDate プロパティを更新します。 手順には、次の概要手順が含まれます。 
  
1. 現在の **ProjectContext** インスタンスを取得します。 
    
2. **ProjectContext.get_projects** 関数を使用して、発行済みのプロジェクトをサーバーから取得します。**get_projects** 関数は **ProjectCollection** オブジェクトを返します。 
    
3. **ProjectContext.load** 関数と **ProjectContext.executeQueryAsync** 関数を使用して、サーバーで要求を実行します。 
    
4. **ProjectContext.getById** 関数を使用して、**PublishedProject** オブジェクトを取得します。 
    
5. **Project.checkOut** 関数を使用してターゲット プロジェクトをチェックアウトします。**checkOut** 関数は、発行されたプロジェクトのドラフト バージョンを返します。 
    
6. **DraftProject.set_startDate** 関数を使用して、プロジェクトの開始日を変更します。 
    
7. **DraftProject.publish** 関数と **ProjectContext.waitForQueueAsync** 関数を使用してプロジェクトを発行します。**publish** 関数は、**waitForQueueAsync** に渡す **QueueJob** オブジェクトを返します。
    
「**Visual Studio でアプリケーション ページを作成するには**」の手順で追加した **script** タグの間に、次に示すコードを貼り付けます。 
  
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

## <a name="delete-project-server-2013-projects-by-using-the-javascript-object-model"></a>JavaScript Projectを使用して Server 2013 プロジェクトを削除する
<a name="pj15_CRUDProjectsJSOM_DeleteProjects"> </a>

このセクションの手順では、JavaScript オブジェクト モデルを使用してプロジェクトを削除します。 手順には、次の概要手順が含まれます。
  
1. 現在の **ProjectContext** インスタンスを取得します。 
    
2. **ProjectContext.get_projects** 関数を使用して、発行済みのプロジェクトをサーバーから取得します。**get_projects** 関数は **ProjectCollection** オブジェクトを返します。 
    
3. **ProjectContext.load** 関数と **ProjectContext.executeQueryAsync** 関数を使用して、サーバーで要求を実行します。 
    
4. **ProjectCollection.getById** 関数を使用して、**PublishedProject** オブジェクトを取得します。 
    
5. **ProjectCollection.remove** 関数に渡すことでプロジェクトを削除します。 
    
6. **ProjectCollection.update** 関数と **ProjectContext.waitForQueueAsync** 関数を使用してコレクションを更新します。**update** 関数は、**waitForQueueAsync** に渡す **QueueJob** オブジェクトを返します。
    
「**Visual Studio でアプリケーション ページを作成するには**」の手順で追加した **script** タグの間に、次に示すコードを貼り付けます。 
  
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

<a name="pj15_CRUDProjectsJSOM_AR"> </a>

## <a name="see-also"></a>関連項目

- [Project のプログラミング タスク](project-programming-tasks.md)
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
    

