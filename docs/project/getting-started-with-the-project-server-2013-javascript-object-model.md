---
title: Project Server 2013 JavaScript オブジェクト モデルの概要
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 30dc3194-7480-4e7c-b731-4a171d652ee0
description: Project Server 2013 では、JavaScript オブジェクト モデルは、プロジェクト オンライン、モバイル、および設置型の開発で使用できます。 このトピックでは、JavaScript オブジェクト モデルの概要について説明し、し、取得し、JavaScript オブジェクト モデルを使用して、プロジェクトを反復処理するアプリケーション ページを作成する方法について説明します。
ms.openlocfilehash: ec8a10e987276807dc4648bd8948b2285f76fd37
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388211"
---
# <a name="getting-started-with-the-project-server-2013-javascript-object-model"></a>Project Server 2013 JavaScript オブジェクト モデルの概要

Project Server 2013 では、JavaScript オブジェクト モデルは、プロジェクト オンライン、モバイル、および設置型の開発で使用できます。 このトピックでは、JavaScript オブジェクト モデルの概要について説明し、し、取得し、JavaScript オブジェクト モデルを使用して、プロジェクトを反復処理するアプリケーション ページを作成する方法について説明します。
  
## <a name="using-the-project-server-javascript-object-model"></a>Project Server JavaScript オブジェクト モデルの使用
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

JavaScript オブジェクト モデルを使用して、クライアント側ではなく、リモートで実行する必要のあるマネージ クライアント コード) を実行するアプリケーションを作成する優れた方法です。 アプリケーションでは、取得するか、サーバーへの非同期の呼び出しを送信することによってオブジェクトを変更する JavaScript オブジェクト モデルを使用できます。 JavaScript オブジェクト モデルを使用するアプリケーションは、通常、カスタムの SharePoint アドインの場合、アプリケーション ページ、および Web パーツとして配置されます。 詳細については、[ホストの web、web では、追加、](https://msdn.microsoft.com/library/b791cdf5-8aa2-47fa-bc4c-aee437354759%28Office.15%29.aspx)および SharePoint 2013 での SharePoint コンポーネントの種類の SharePoint アプリケーションでは、SharePoint コンポーネント」を参照してください。
  
JavaScript オブジェクト モデルは、Project Server 2013 では、主要な機能を実装しますが、JavaScript オブジェクト モデル、サーバー オブジェクト モデルでは、一対一のパリティを必要はありません。 JavaScript オブジェクト モデルへのエントリ ポイントは、Project Server 2013 のクライアント コンテキストを表し、サーバーのコンテンツおよび機能へのアクセスを提供する、 **ProjectContext**オブジェクトです。 Project Server 2013 の JavaScript オブジェクト モデルが既定のパスにある PS.js ファイルで定義されている`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS`のアプリケーション サーバーにします。 また、Project Server 2013 にインストールして、PS同じ場所に Debug.js ファイルです。 PS.Debug.js は、IntelliSense の情報を提供する PS.js の unminified バージョンです。 
  
JavaScript オブジェクト モデルにより、フォーム認証、およびすべての要求は、現在のユーザーとして認証されます。 セキュリティおよびカスタム アプリケーションの設計とソリューションの他の考慮事項については、[認証、承認、および SharePoint 2013 のセキュリティ](https://msdn.microsoft.com/library/8734790c-eb75-4d78-9604-7cc23b33b693%28Office.15%29.aspx)、SharePoint アドインのアーキテクチャと開発の重要な側面を[を参照してください。横](https://msdn.microsoft.com/library/ae96572b-8f06-4fd3-854f-fc312f7f2d88%28Office.15%29.aspx)、 [SharePoint のアドインは、SharePoint ソリューションと比較](https://msdn.microsoft.com/library/0e9efadb-aaf2-4c0d-afd5-d6cf25c4e7a8%28Office.15%29.aspx)するとします。
  
> [!NOTE]
> SharePoint サイトからリモートでデータにアクセスするには、SharePoint 2013 は、クロス ドメイン ライブラリをクライアント側のドメイン間呼び出しを行うことができますを提供します。 詳細については、[クロス ドメイン ライブラリを使用してアドインからのデータを SharePoint 2013 のアクセス](https://msdn.microsoft.com/library/bc37ff5c-1285-40af-98ae-01286696242d%28Office.15%29.aspx)を参照してください。 
  
多くの概念とプロセスを Project Server 2013 の JavaScript オブジェクト モデルを使用するため、関連するクライアント オブジェクト モデルのようになります。 Project Server 2013 のマネージ クライアント オブジェクト モデルの詳細については、 **Microsoft.ProjectServer.Client**を参照してください。 SharePoint 2013JavaScript オブジェクト モデルとマネージ クライアント オブジェクト モデルに関する詳細については、 [SharePoint 2013 での JavaScript ライブラリのコードを使用して基本的な操作を完了](https://msdn.microsoft.com/library/29089af8-dbc0-49b7-a1a0-9e311f49c826%28Office.15%29.aspx)し、[基本的な操作を完了 SharePoint 2013 クライアントを使用するを参照してください。ライブラリ コード](https://msdn.microsoft.com/library/5a69c9e3-73bf-4ed5-bc19-182056bdb394%28Office.15%29.aspx)。
  
## <a name="walkthrough-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>チュートリアル: プロジェクトを取得および反復処理するアプリケーション ページの作成
<a name="pj15_GetStartedJSOM_UseJSOM"> </a>

サイトの各発行済みプロジェクトの ID、名前、および作成日を表示するアプリケーション ページを作成する方法を説明します。
  
### <a name="prerequisites-for-creating-an-application-page-that-retrieves-and-iterates-through-projects"></a>プロジェクトを取得および反復処理するアプリケーション ページの作成の前提条件
<a name="pj15_GetStartedJSOM_Prereqs"> </a>

このトピックで説明するアプリケーション ページを開発するには、以下の製品をインストールおよび構成する必要があります。
  
- SharePoint Server 2013
- に少なくとも 1 つの発行されたプロジェクトを Project Server 2013
- Visual Studio 2012
- Office Developer Tools for Visual Studio 2012
    
SharePoint Server 2013 に拡張機能を配置し、プロジェクトを取得するためにアクセスを許可する必要があります。
  
> [!NOTE]
> 次の手順では、Project Server 2013 を実行しているコンピューター上で開発することを前提としています。 
  
### <a name="creating-the-application-page-in-visual-studio-2012"></a>Visual Studio 2012 でアプリケーション ページを作成します。
<a name="pj15_GetStartedJSOM_CreateVS"> </a>

次の手順では、SharePoint プロジェクトと、テーブルとラベルを含むアプリケーション ページを作成します。テーブルにはプロジェクトに関する情報が表示され、ラベルにはエラー メッセージが表示されます。
  
1. Project Server 2013 を実行しているコンピューターに管理者として Visual Studio 2012 を実行します。
    
2. 次のように、SharePoint 2013 の空のプロジェクトを作成します。
    
    1. [ **新しいプロジェクト**] ダイアログ ボックスで、上部のドロップダウン リストから [ **.NET Framework 4.5**] を選択します。 
        
    2. テンプレート カテゴリの一覧で、[**Office SharePoint**] カテゴリを選択し、[**SharePoint 2013 Project**] テンプレートを選択します。 
        
    3. GetProjectsJSOM、プロジェクトの名前し、 **[OK** ] ボタンをクリックします。 
        
    4. [**SharePoint カスタマイズ ウィザード**] ダイアログ ボックスで、[**ファーム ソリューションとして配置する**] を選択し、[**OK**] ボタンを選択します。 
    
3. ソリューション エクスプ ローラーで、Project Web App インスタンスの URL と一致する**ProjectsJSOM**プロジェクトの**サイトの URL**プロパティの値を編集します (たとえば、 `https://ServerName/PWA`)。
    
4. [**GetProjectsJSOM**] プロジェクトのショートカット メニューを開き、SharePoint "レイアウト" のマップされたフォルダーを追加します。 
    
5. **レイアウト**フォルダーに**GetProjectsJSOM**フォルダーのショートカット メニューを開くし、ProjectsList.aspx をという名前の新しい SharePoint アプリケーション ページを追加します。
    
   > [!NOTE]
   > 次の使用例は、アプリケーション ページの Visual Studio 2012 を作成する分離コード ファイルを使用しません。 
  
6. **ProjectsList.aspx** ページのショートカット メニューを開き、[**スタートアップ アイテムとして設定**] を選択します。
    
7. 次のように、[**ProjectsList.aspx**] ページのマークアップで、"Main" の **asp:Content** タグ内にテーブルとメッセージ プレースホルダーを定義します。 
    
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

### <a name="retrieving-the-projects-collection"></a>プロジェクト コレクションの取得
<a name="pj15_GetStartedJSOM_RetrieveProjs"> </a>

次の手順では、プロジェクト コレクションを取得および初期化します。
  
1. 次のように、**div** 終了タグの後ろに、PS.js ファイルを参照する **SharePoint:ScriptLink** タグを追加します。 
    
   ```HTML
    <SharePoint:ScriptLink name="PS.js" runat="server" ondemand="false" localizable="false" loadafterui="true" />
   ```

2. 次のように、**SharePoint:ScriptLink** タグの下に **script** タグを追加します。 
    
   ```HTML
    <script type="text/javascript">
        // Paste the remaining code snippets here, in the order that they are presented.
    </script>
   ```

3. 次のように、プロジェクト コレクションを格納するためのグローバル変数を宣言します。
    
   ```js
   var projects;
   ```

4. ユーザー設定コードの実行前に PS.js ファイルが確実に読み込まれるようにするための **SP.SOD.executeOrDelayUntilScriptLoaded** メソッドを呼び出します。 
    
   ```js
   SP.SOD.executeOrDelayUntilScriptLoaded(GetProjects, "PS.js");
   ```

5. 次のように、現在のコンテキストに接続してプロジェクト コレクションを取得する関数を追加します。
    
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

   このコンテキストで取得されるいくつかのクライアント オブジェクトは、初期化されるまでデータが格納されません。つまり、オブジェクトを初期化するまでオブジェクトのプロパティ値にアクセスできません。また、**ValueObject** 型のプロパティの場合、値にアクセスするには明示的にプロパティを要求する必要があります (初期化する前にプロパティにアクセスしようとすると、**PropertyOrFieldNotInitializedException** 例外が発生します)。 
    
   オブジェクトを初期化するには、**load** メソッド (または **loadQuery** メソッド) を呼び出し、次に **executeQueryAsync** メソッドを呼び出します。 
    
   - **load** 関数または **loadQuery** 関数を呼び出すと、サーバー上で実行する要求が登録されます。取得するオブジェクトを表すパラメーターを渡します。**ValueObject** プロパティを操作する場合は、そのプロパティもパラメーターで要求します。 
    
   - **executeQueryAsync** 関数を呼び出すと、クエリ要求がサーバーに非同期に送信されます。サーバーから応答を受け取ったときに呼び出す成功のコールバック関数と失敗のコールバック関数を渡します。 
    
   ネットワーク トラフィックを減らすには、**load** 関数を呼び出すときに、操作するプロパティのみを要求します。また、複数のオブジェクトを操作する場合、可能であれば **load** 関数の複数の呼び出しをまとめてから、**executeQueryAsync** 関数を呼び出します。 
    
### <a name="iterating-through-the-projects-collection"></a>プロジェクト コレクションの反復処理
<a name="pj15_GetStartedJSOM_IterateProjs"> </a>

次の手順では、プロジェクト コレクションを反復処理 (サーバーの呼び出しが成功の場合)、またはエラー メッセージを表示 (呼び出しが失敗の場合) します。
  
1. 次のように、プロジェクト コレクションを反復処理する成功のコールバック関数を追加します。
    
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

2. 次のように、エラー メッセージを表示する失敗のコールバック関数を追加します。
    
    ```js
    function onQueryFailed(sender, args) {
        $get("spanMessage").innerText = 'Request failed: ' + args.get_message();
    }
    ```

3. アプリケーション ページをテストするには、メニュー バーの [**デバッグ**] を選択し、[**デバッグの開始**] をクリックします。web.config ファイルの変更を求められたら、[**OK**] を選択します。

<a name="pj15_GetStartedJSOM_CompleteExample"> </a>

## <a name="complete-code-example"></a>完全なコード例

以下は ProjectsList.aspx ファイルの完全なコードです。
  
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

<a name="pj15_GetStartedJSOM_AR"> </a>

## <a name="see-also"></a>関連項目

- [作成、取得、更新、およびプロジェクトのサーバーの JavaScript オブジェクト モデルを使用してプロジェクトを削除します。](create-retrieve-update-delete-projects-using-project-server-javascript.md)  
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
- [Project Server CSOM および .NET の概要](getting-started-with-the-project-server-csom-and-net.md)
    

