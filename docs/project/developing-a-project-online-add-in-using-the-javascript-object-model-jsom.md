---
title: JavaScript オブジェクトモデル (jsom) を使用して Project Online アドインを開発する
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: この記事では、project online の利便性を向上させるための Microsoft project online アドイン開発について説明します。 開発プロジェクトは、チュートリアルとして実装されています。 この記事で使用されているアドインでは、project Online アカウントから発行済みプロジェクトのプロジェクト名と id を読み込んで表示することができ、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンすることができます。
ms.openlocfilehash: 0a472a6300f18aaa65649f44d944445642a59e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322691"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>JavaScript オブジェクトモデル (jsom) を使用して Project Online アドインを開発する

この記事では、project online の利便性を向上させるための Microsoft project online アドイン開発について説明します。 開発プロジェクトは、チュートリアルとして実装されています。 この記事で使用されているアドインでは、project Online アカウントから発行済みプロジェクトのプロジェクト名と id を読み込んで表示することができ、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンすることができます。
  
実行時に、アドインの一覧は次の図のようになります。
  
![jsom のプロジェクトとタスクの一覧を示すスクリーンショット](media/766e5914-f048-48f4-9282-291f55e6e90d.png "jsom のプロジェクトとタスクの一覧を示すスクリーンショット")
  
この例の目的は、Project Online との対話と、サービスからの要求ごとにクエリを実行してコンテキストを設定することです。 ユーザーインターフェイス (UI) 要素には、特に注意が払われません。 その代わりに、ソースリストには UI に関するコメントが記載されています。
  
> [!NOTE]
> サンプルアドインのソースファイル (Visual Studio プロジェクト) は、から入手できhttps://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks....ます。 記事を読む際に、ソースファイルを参照できるようにしておきます。 Visual Studio プロジェクトのファイルがビルドされ、最小限の変更で実行可能になります。これは、project Online テナントの URL を PWA フォルダーに置き換えることです。 
  
## <a name="background"></a>背景

project Online は、ポートフォリオ、プログラム、プロジェクトを調整して管理するプロジェクトポートフォリオ管理 (PPM) および project management Office (PMO) ソリューションを企業に提供する Office 365 サービスです。 project Online は、project デスクトップエディションとは異なるオファーリングです。しかし、project Online には、プロジェクトのライフサイクルを通じてプロジェクトの詳細を維持および追跡する機能がまだ含まれています。 Project online は SharePoint online 上に構築されています。
  
Project Online のホスト型アドインは、クライアント側オブジェクトモデル API とやり取りする JavaScript およびリソースファイルで構成されています。 ユーザーがアドインを訪問すると、JavaScript とリソースがダウンロードされ、ブラウザー内で実行されます。 このアドインは、データを作成、取得、更新、削除するかどうかにかかわらず、Project Online への非同期呼び出しを行い、サービスと対話します。 
  
Project Online は、アドインから他のテナントに属する情報を保護するためのもう1つのアクションを実行します。つまり、Project Online は、アドインからの要求を操作する分離されたサイトを作成します。 プロジェクトオンラインホスト上で実行されるカスタムコードはありません。 
  
project Online アドインの開発セットアップでは、Visual Studio SharePoint アドインプロジェクトの種類を使用します。 アドインは javascript で記述され、プロジェクト javascript オブジェクトモデル (jsom) を使用して project Online サービスを操作します。 jsom は、SharePoint jsom から多くの機能を継承します。
  
> [!NOTE]
> アドインは、Office ストアで発行して販売したり、SharePoint 上のプライベートアプリカタログに展開したりできます。 詳細については、「 [Office アドインを展開して発行する](https://docs.microsoft.com/office/dev/add-ins/publish/publish)」を参照してください。
> 
> この記事で使用されているアドインは、開発者向けのサンプルです。これは、運用環境での使用を目的としたものではありません。 主な目的は、Project Online のアプリ開発の例を示すことです。 
  
## <a name="prerequisites"></a>前提条件

サポートされている Windows 環境に以下の項目を追加します。
  
- **.net Framework 4.0**以降: バージョン4.0 のフレームワークの完全なバージョンは互換性があります。 ダウンロード サイトは https://msdn.microsoft.com/vstudio/aa496123.aspx です。
    
- **Visual Studio 2013 以降**:  
    
   - Visual Studio 2015 のプロフェッショナルエディションは、すぐにご利用いただけhttps://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspxます。また、から入手できます。
    
   - Visual Studio 2015 のコミュニティエディションは、でhttps://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx入手できます。 このエディションでは、Microsoft Office Developer Tools for Visual Studio を手動でインストールする必要があります。
    
   Microsoft Office Developer Tools for Visual Studio は、からhttps://www.visualstudio.com/en-us/features/office-tools-vs.aspx入手できます。
    
- **Project Online アカウント**: これにより、ホスティングサービスへのアクセスが可能になります。 Project Online アカウントの入手の詳細については、https://products.office.com/en-us/Project/project-online-portfolio-management をご覧ください。
    
   アドインユーザーに、Project Online テナントの一部のプロジェクトにアクセスするための十分な権限があることを確認します。 
    
- 情報が格納されている**ホストサイト上のプロジェクト**。
    
> [!NOTE]
> 標準の .net framework は、適切なフレームワークを使用します。 ".net Framework 4 クライアントプロファイル" は使用しないでください。 
  
### <a name="set-up-the-visual-studio-project"></a>Visual Studio プロジェクトを設定する

アプリケーションのセットアップでは、新しいプロジェクトを作成し、適切なライブラリをリンクし、必要な名前空間を宣言します。 Visual Studio では、複数の種類の開発プロジェクトが提供されています。 このセクションは短時間で、非常に基本的なものです。 この値は、情報が1つの場所に結合されていることを示します。
  
#### <a name="select-a-visual-studio-project"></a>Visual Studio プロジェクトを選択する

アドインに適した種類のプロジェクトを作成するには、次の手順を実行する必要があります。 画面に表示されたキーワードには、**太字**の属性があります。 
  
1. [ファイル] メニューの [ **** > **新しい** > **プロジェクト**] を選択します。 
    
2. インストールされているテンプレートの左側のウィンドウで、[ **C#** > **Office/SharePoint** > **Web アドイン**] を選択します。 
    
3. 中央のウィンドウの上部で、[ **.net Framework 4**以降] を選択します。現在のバージョンは4.6 です。 
    
4. 中央のウィンドウの [アプリケーションの種類] で、[ **SharePoint アドイン**] を選択します。 
    
5. 下部のセクションで、プロジェクトの名前と場所、ソリューション名を指定します。 
    
6. また、下部のセクションで、[**ソリューションのディレクトリを作成**] ボックスがオンになっていることを確認します。 
    
7. [**OK**] をクリックして、初期プロジェクトを作成します。 
    
Visual Studio ウィザードは、次の2つのダイアログボックスで、Project Online 設定サイト (ダイアログ内の SharePoint 設定と呼ばれます) についてのいくつかの質問を行います。 質問は次のとおりです。
  
1. アドインのデバッグに使用する SharePoint サイトを指定します。 のような PWA サイトの URL を指定しhttps://contoso.sharepoint.com/sites/pwaます。
    
2. SharePoint アドインをどのようにホストしますか? [X] **SharePoint ホスト型**を選択します。
    
   ホスティングオプションを含む sharepoint アドインの詳細については、「 [sharepoint アドイン](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)」を参照してください。
    
3. **[次へ]** をクリックします。 
    
2番目の追加のダイアログで、アドインの SharePoint Online バージョンを指定するよう求められます。 
  
1. アドインの対象となる SharePoint の最も古いバージョンは何ですか。 [X] S **harePoint-Online**を選択します。 
    
2. **[完了]** をクリックします。 
    
Visual Studio によってプロジェクトが作成され、project Online サイトにアクセスします。 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>Project Online サイトでサイドローディングを有効にする

サイドローディングは、Project Online アドインをテストおよびデバッグするためのメカニズムです。サイドローディングには2つのスクリプトが必要です。1つは、Project Online サイトでサイドローディングを有効にする方法と、アドインのテストとデバッグを完了した後にサイドローディングを無効にするためのスクリプトです。
  
サイドローディングのセットアップの詳細については、「[開発者以外のサイトコレクションでアプリのサイドローディングを有効にする](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)」を参照してください。
  
> [!NOTE]
> サイドローディングアプリは開発/テストの機能です。 これは、**運用環境での使用を目的**としたものではありません。 アプリを定期的にサイドロードさせないでください。または、アプリのサイドロードは、この機能を使用している時間よりも長く有効にしておきます。 
  
## <a name="add-content-to-the-add-in-project"></a>アドインプロジェクトにコンテンツを追加する

プロジェクトを作成し、デバッグ機構を設定した後、アプリにコンテンツを追加すると、次のタスクが実行されます。
  
- アプリケーションスコープの設定
    
- jsom ライブラリのリンク
    
- UI 要素をアドインに追加する
    
- Project Online サービスを初期化して接続する
    
- プロジェクトと詳細/プロパティを取得する
    
- プロジェクトの表示
    
- プロジェクトのタスクを表示する
    
アドインプロジェクトは、多くのファイルで構成されています。 この例では、次のファイルを編集する必要があります。 
  
- appmanifest.xml
    
- default.aspx
    
- アプリケーション .js
    
- app.xaml-省略可能。アドイン用に開発されたスタイル定義が含まれています。
    
試用版からサブスクリプションサイトへの移動など、project Online テナントの変更によっては、[プロパティ] ウィンドウ**** > を使用して、サーバー接続やサイトの URL など、プロジェクトのプロパティを更新できます。**Window**コマンド 
  
プロジェクトにファイルを追加することもできます。 その場合は、同じグループ (コンテンツ、画像、ページ、またはスクリプト) にある要素の .xml ファイルを更新して、新しいファイルを含める必要があります。 プロジェクトファイルの詳細については、「 [SharePoint アドインのアプリマニフェスト構造とパッケージを調査](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)する」を参照してください。
  
### <a name="set-application-scope"></a>アプリケーションスコープの設定

このアドインには、サービスがクエリ結果に情報を返す前に定義されたスコープまたはアクセス許可レベルが必要です。 このアドインでは、Visual Studio プロジェクトに対して次のスコープを使用します。 この変更は、[アクセス許可] タブの appmanifest.xml ファイルに対して行われます。

|Scope|アクセス許可|
|:-----|:-----|
|複数のプロジェクト (Project Server)  <br/> |読み取り  <br/> |
   
アプリケーションスコープを設定した後、ファイルを保存します。 それ以外の場合、サービスからデータは返されません。 
  
### <a name="link-the-jsom-library"></a>jsom ライブラリをリンクする

実行時の project online ライブラリ (js および .ps) は project online で提供されており、常に最新のバージョンです。 jsom を使用する JavaScript アドインは、これらのライブラリのいずれかとリンクする必要があります。 リンク定義が default.aspx ファイルに追加されます。 .js または pcl を使用するためのコマンドは、app.config ファイルにあるコードに含まれています。
  
次のコマンドを、node.js の「SharePoint: scriptlink」の後にある`<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"`要素に追加して、次のコマンドを実行します。 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> この場合、-js または-.js の**OnDemand**属性は**false**に設定されます。 
  
### <a name="add-ui-elements-to-the-add-in"></a>UI 要素をアドインに追加する

サンプルアドインは、いくつかのコンポーネントで構成されています。 静的要素の説明は、default.aspx ファイルにあります。 すべてのコンポーネントの動的な要素の記述とコードは、アプリケーション .js ファイルにあります。 コンポーネントに関するコメントについては、ソースコードの一覧を参照してください。 次に、アドインの UI コンポーネントの一覧を示します。
  
- タイトル
    
- 導入の説明
    
- テーブルからタスクを削除するボタン
    
- プロジェクト ID と名前、およびタスク情報を一覧表示する表。
    
- [タスク] ボタン (プロジェクトごとに1回複製されます)。タスクデータをテーブルにインポートします。
    
ユーザーインターフェイスの詳細 (プロジェクトテーブルのタイトル、ヘッダー部分など) については、default.aspx プロジェクトファイルを参照してください。
  
### <a name="initialize-and-connect-to-the-host-system"></a>ホストシステムを初期化して接続する

app.config ファイルには、JavaScript コードが含まれています。 アドインはブラウザーで .ps を読み込み、initializepage 関数を呼び出します。 initializepage は、Project Online エンドポイントへのコンテキストを取得し、loadprojects 関数を開始します。
  
```js
    'use strict';
    SP.SOD.executeOrDelayUntilScriptLoaded(initializePage, "PS.js");
    //Project PWA Context and published projects in PWA
    var projContext;
    var projects;
    function initializePage() {
        //Get the Project context for this web
        projContext = PS.ProjectContext.get_current();
        loadProjects();
    }
    //General CSOM failure event handler
    //Invoked when ExecuteQueryAsync returns unsuccessfully
    function onRequestFailed(sender, args) {
        alert("Failed to execute: " + args.get_message());
        return;
    };

```

### <a name="retrieve-the-projects"></a>プロジェクトを取得する

loadprojects 関数は、プロジェクト名と id のサービスを照会します。 
  
アプリケーションは、プロジェクト名とプロジェクト Id を取得します。プロジェクトに関するその他の情報は、使用可能で、load メソッドを変更して、取得するプロパティを明示的に特定することによってアクセスできます。 この例は、コメントとしてコードで提供されています。 
  
クエリが成功した場合、アドインは displayprojects を呼び出すことによって続行されます。 
  
```js
    //Query CSOM and get the list of projects in PWA
    function loadProjects() {
        projects = projContext.get_projects();
    //Request to server - identifies what to retrieve
        projContext.load(projects, 'Include(Name, Id)');
        //Notice to server to execute query
        projContext.executeQueryAsync(displayProjects, onRequestFailed);
        // Syntax for requesting more fields to pull down from server
        // projContext.load(projects, 'Include(Name, Description, StartDate, 
        // Id, IsCheckedOut)');
    }

```

### <a name="display-the-projects"></a>プロジェクトを表示する

displayprojects 関数は、テーブル、プロジェクトごとに1行、および特定のプロジェクトのタスクを表示するボタンを作成します。 
  
```js
    //Display the projects with names and ids in a table
    function displayProjects() {
        //Current published project and ID
        var p, projId;
        //Project table rows to publish collectively
        var pTable = []; 
        var pEnum = projects.getEnumerator();
        //Build a 3-column table, with one project per row.
        while (pEnum.moveNext()) {
            p = pEnum.get_current();
        
            //Items used in getting information for table rows:
            //Current published project object, and ID and name
            // var project = p;
            // var projId = p.get_id();
            // var projName = p.get_name();
        
            //Continue processing/working with project object as needed.
        }
    }

```

> [!NOTE]
> while ループは、ID プロパティと name プロパティにアクセスします。 これは、同じプロパティにアクセスする関数を呼び出すソースコードプロジェクトとはわずかに異なります。 
  
### <a name="display-the-tasks-for-a-project"></a>プロジェクトのタスクを表示する

アドインの一部であるタスクは、最初の読み込みの一部ではありません。 ユーザーがプロジェクトに関連付けられているタスクに関心を持っている場合は、[タスクの表示] ボタンをクリックすると、btnloadtasks イベントハンドラーを使用してタスクが一覧に表示されます。 
  
btnloadtasks イベントハンドラーは、適切なプロジェクト ID を使用して、サーバーから指定したプロジェクトのタスクを要求します。 取得した btnloadtasks は、タスクリストを表示タスクに渡して、タスクを画面に表示します。
  
```js
    //Query CSOM and get the list of tasks for a specific project
    function btnLoadTasks(pid) {
        //Event handler for the "Show tasks" buttons. 
        //
        //The project ID is the sole argument and is used to get the appropriate task 
        //info from the service.
        //The project ID is also the button name, and is used to identify where to place
        //the task information in the table.
        //
        //Project ID to pass to the event handler
        var projId = pid;
        //
        //Get the project reference
        var pProj = projects.getById(projId);
        //
        //Get the tasks collection reference associated with the project.
        var tasks = pProj.get_tasks();
        //
        projContext.load(tasks, 'Include(Id, Name, Start, ScheduledStart, Completion)');
        //
        //If the query succeeds, displayTasks presents the tasks to the user.
        projContext.executeQueryAsync(function () { displayTasks(tasks, projId) }, onRequestFailed);
    }

```

displaytasks 関数は、指定したプロジェクトに関連付けられているタスクをプロジェクトエントリのすぐ下に表示します。
  
```js
    //Insert tasks for the specified project immediately underneath the project entry 
    //in the table.
    function displayTasks(tasks, projId) {
        //selected project ID
        var pId = projId;
        //individual task
        var t;
        //Task table rows to publish collectively
        var tTable = [];
        var tEnum = tasks.getEnumerator();
        //Build table one task per row.
        while (tEnum.moveNext()) {
            t = tEnum.get_current();
            //
            //Items used in getting information for table rows:
            //Current task object, and ID and name
            // var task = t;
            // var taskId = t.get_id();
            // var taskName = t.get_name();
            
            //Continue processing/working with task object as needed.
        }
    }

```

> [!NOTE]
> while ループは、タスク ID と名前のプロパティにアクセスします。 これは、同じプロパティにアクセスする関数を呼び出すソースコードプロジェクトとはわずかに異なります。 
  
1つのプロジェクトのタスクの出力例を次に示します。
  
![プロジェクトタスクの出力を示すスクリーンショット](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "プロジェクトタスクの出力を示すスクリーンショット")
  
## <a name="see-also"></a>関連項目

Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。
    


