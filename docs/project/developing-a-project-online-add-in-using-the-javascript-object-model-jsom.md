---
title: JavaScript オブジェクト Project Online (JSOM) を使用したアドインの開発
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 4a4b1ad2-de46-421d-a698-53c20c90b93a
description: この記事では、Microsoft Project Onlineのエクスペリエンスを向上させるアドイン開発のProject Online。 開発プロジェクトは、チュートリアルとして実装されます。 この記事で使用するアドインは、Project Online アカウントから発行されたプロジェクトのプロジェクト名と ID を読み取って表示し、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンできます。
ms.openlocfilehash: b30350a0d78531e304545e551ff61257e52386e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560222"
---
# <a name="developing-a-project-online-add-in-using-the-javascript-object-model-jsom"></a>JavaScript オブジェクト Project Online (JSOM) を使用したアドインの開発

この記事では、Microsoft Project Onlineのエクスペリエンスを向上させるアドイン開発のProject Online。 開発プロジェクトは、チュートリアルとして実装されます。 この記事で使用するアドインは、Project Online アカウントから発行されたプロジェクトのプロジェクト名と ID を読み取って表示し、個々のプロジェクトに関連付けられたタスクを取得するためにドリルダウンできます。
  
実行時に、アドインの一覧は次の図のようになります。
  
![JSOM のプロジェクトとタスクの一覧を示すスクリーンショット](media/766e5914-f048-48f4-9282-291f55e6e90d.png "JSOM のプロジェクトとタスクの一覧を示すスクリーンショット")
  
この例の焦点は、Project Online要求ごとにクエリを行い、コンテキストを設定する方法です。 ユーザー インターフェイス (UI) 要素は、最小限の注意を受け取る。 代わりに、ソースリストには UI に関するコメントが表示されます。
  
> [!NOTE]
> アドインの例のソース ファイル (プロジェクトVisual Studio次の場所で使用できます https://github.com/OfficeDev/Project-JSOM-List-Projects-Tasks.... 。 ソース ファイルは、記事の読み取り中に参照として便利な状態に保ちます。それぞれが他のファイルを補完します。 Visual Studio プロジェクト ビルド内のファイルは、最小限の変更で実行可能です。Project Online テナントの URL を PWA フォルダーに置き換えます。 
  
## <a name="background"></a>背景

Project Onlineは、Office 365 ポートフォリオ管理 (PPM) およびプロジェクト管理オフィス (PMO) ソリューションを企業に提供し、ポートフォリオ、プログラム、プロジェクトを調整および管理する Office 365 サービスです。 Project Onlineデスクトップ エディションとは異なるProjectです。しかし、Project Onlineプロジェクトの一生を通じてプロジェクトの詳細を維持および追跡する機能がまだ含まれている場合があります。 Project OnlineはオンラインでSharePointされます。
  
ホストProject Onlineは、クライアント側オブジェクト モデル API と対話する JavaScript ファイルとリソース ファイルで構成されます。 ユーザーがアドインにアクセスすると、JavaScript とリソースがダウンロードされ、ブラウザー内で実行されます。 アドインは、データの作成、取得、更新、または削除Project Online、サービスを操作するための非同期呼び出しを行います。 
  
Project Online、アドインから他のテナントに属する情報を保護するためのもう 1 つのアクションを実行します。つまり、Project Onlineアドインからの要求を操作するための分離サイトを作成します。 カスタム コードは、カスタム ホストProject Online実行します。 
  
アドインの開発Project Onlineは、アドイン のプロジェクトVisual Studio SharePointを使用します。 アドインは JavaScript で記述され、Project JavaScript オブジェクト モデル (JSOM) を使用して、Project Online サービスを操作します。 JSOM は、その機能の多くを JSOM のSharePointします。
  
> [!NOTE]
> アドインは、Office ストアで公開および販売するか、SharePoint のプライベート アプリ カタログに展開できます。 詳細については、「Deploy [and publish your Office アドイン」を参照してください](https://docs.microsoft.com/office/dev/add-ins/publish/publish)。
> 
> この記事で使用するアドインは、開発者向けのサンプルです。これは、実稼働環境での使用を目的としていない。 主な目的は、アプリ開発の例を示Project Online。 
  
## <a name="prerequisites"></a>前提条件

サポートされている環境に次のWindowsします。
  
- **.NET Framework 4.0 以降**: バージョン 4.0 のフレームワークの完全なバージョンは互換性があります。 ダウンロード サイトは https://msdn.microsoft.com/vstudio/aa496123.aspx です。
    
- **Visual Studio 2013以降**:  
    
   - 2015 年 2015 Visual Studioのプロフェッショナル エディションは、すぐに使用できる状態で利用可能です https://www.visualstudio.com/en-us/products/visual-studio-professional-with-msdn-vs.aspx 。
    
   - 2015 年 2015 Visual Studioのコミュニティ エディションはで利用できます https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx 。 このエディションでは、開発者向けツールを手動Microsoft Officeインストールする必要Visual Studio。
    
   [Microsoft Office開発者ツール] は、Visual Studioで利用できます https://www.visualstudio.com/en-us/features/office-tools-vs.aspx 。
    
- **アカウントProject Online:** ホスティング サービスへのアクセスを提供します。 Project Online アカウントの入手の詳細については、https://products.office.com/en-us/Project/project-online-portfolio-management をご覧ください。
    
   アドイン ユーザーが、テナント内の一部のプロジェクトにアクセスするための十分なProject Onlineします。 
    
- **情報が設定されたホスティング** サイト上のプロジェクト。
    
> [!NOTE]
> 標準の.NET Framework使用する正しいフレームワークです。 ".NET Framework 4 クライアント プロファイル" を使用しない。 
  
### <a name="set-up-the-visual-studio-project"></a>Visual Studio プロジェクトを設定する

アプリケーションのセットアップは、新しいプロジェクトを作成し、適切なライブラリをリンクし、必要な名前空間を宣言します。 Visual Studio では、複数の種類の開発プロジェクトが提供されています。 このセクションは簡潔で非常に基本的なセクションです。 この値は、情報が 1 か所に合体している場合です。
  
#### <a name="select-a-visual-studio-project"></a>Visual Studio プロジェクトを選択する

アドインに適切な種類のプロジェクトを作成するには、次の手順を実行する必要があります。 画面で検出されたキーワードには、 **太字の属性** があります。 
  
1. [ファイル] メニューの[ファイルの新  >  **しいファイル] を**  >  **Project。** 
    
2. 左側のウィンドウの [インストール済みテンプレート]で、[Web アドイン  >  **C#Office/SharePoint**  >  **を選択します**。 
    
3. 中央のウィンドウの上部で **、[4 .NET Framework]** を選択します。現在のバージョンは 4.6 です。 
    
4. 中央ウィンドウのアプリケーションの種類から、[アドイン] **SharePoint選択します**。 
    
5. 下部のセクションで、プロジェクトの名前と場所、ソリューション名を指定します。 
    
6. また、下部のセクションで、[**ソリューションのディレクトリを作成**] ボックスがオンになっていることを確認します。 
    
7. [**OK**] をクリックして、初期プロジェクトを作成します。 
    
Visual Studio ウィザードでは、Project Online 設定サイト (ダイアログの SharePoint 設定と呼ばれる) に関するいくつかのフォローアップ質問を、その後に続くいくつかのダイアログで確認します。 質問は次のとおりです。
  
1. アドインSharePointデバッグに使用するサイトは何ですか? サイトの URL をPWAします https://contoso.sharepoint.com/sites/pwa 。
    
2. アドインをホストするSharePoint方法 [X] を選択SharePoint **ホストされます**。
    
   ホスティング オプションを含むSharePointアドインの詳細については[、「SharePoint」を参照してください](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/sharepoint-add-ins)。
    
3. [**次へ**] をクリックします。 
    
2 番目の追加ダイアログでは、アドインSharePointオンライン バージョンを指定する必要があります。 
  
1. アドインにターゲットを設定するSharePointの最も古いバージョンは何ですか? [X] S **harePoint-Online を選択します**。 
    
2. [**完了**] をクリックします。 
    
Visual Studio作成し、プロジェクト サイトにProject Onlineします。 
  
### <a name="enable-sideloading-on-the-project-online-site"></a>サイトでサイドローディングをProject Onlineする

サイドローディングは、アドインのテストとデバッグProject Onlineメカニズムです。サイドローディングには、Project Online サイトでサイドローディングを有効にするスクリプトと、アドインのテストとデバッグが完了したらサイドローディングを無効にするスクリプトの 2 つが必要です。
  
サイドローディングの設定の詳細については、「開発者以外のサイト コレクションでアプリのサイドローディングを有効にする [」を参照してください](https://blogs.msdn.microsoft.com/officeapps/2013/12/10/enable-app-sideloading-in-your-non-developer-site-collection/)。
  
> [!NOTE]
> サイドローディング アプリは開発者/テスト機能です。 これは、 **実稼働環境での使用を目的としたものではありません**。 アプリを定期的にサイドロードしたり、アプリのサイドローディングをアクティブに使用しているよりも長く有効にしたりしません。 
  
## <a name="add-content-to-the-add-in-project"></a>アドイン プロジェクトにコンテンツを追加する

プロジェクトを作成し、デバッグ メカニズムを設定した後、アプリにコンテンツを追加するには、次のタスクが含まれます。
  
- アプリケーション スコープの設定
    
- JSOM ライブラリのリンク
    
- アドインへの UI 要素の追加
    
- サービスの初期化と接続Project Onlineする
    
- プロジェクトと詳細/プロパティの取得
    
- プロジェクトの表示
    
- ユーザーのタスクを表示Project
    
アドイン プロジェクトは、多数のファイルで構成されます。 この例では、次のファイルを編集する必要があります。 
  
- AppManifest.xml
    
- Default.aspx
    
- App.js
    
- App.css - 省略可能。アドイン用に開発されたスタイル定義が含まれている
    
試用版からサブスクリプション サイトへの移行など、Project Online テナントが変更された場合は、[プロパティ ウィンドウの表示] コマンドで使用できる [プロパティ] ウィンドウを使用して、サーバー接続やサイト URL などのプロジェクト プロパティを更新できます。  >   
  
プロジェクトにファイルを追加することもできます。 その場合は、同じグループ (コンテンツ、イメージ、ページ、またはスクリプト) にある Elements.xml ファイルを更新して、新しいファイルを含める必要があります。 プロジェクト ファイルの詳細については、「アプリ マニフェスト構造の探索」および「アドインのパッケージSharePoint[参照してください](https://docs.microsoft.com/sharepoint/dev/sp-add-ins/explore-the-app-manifest-structure-and-the-package-of-a-sharepoint-add-in)。
  
### <a name="set-application-scope"></a>アプリケーション スコープの設定

サービスがクエリ結果に情報を返す前に、アドインにはスコープまたはアクセス許可レベルが定義されている必要があります。 このアドインでは、次のスコープを使用してプロジェクトのVisual Studioします。 この変更は、[アクセス許可] タブAppManifest.xmlファイルに対して行います。

|範囲|アクセス許可|
|:-----|:-----|
|複数のプロジェクト (Project サーバー)  <br/> |読み取り  <br/> |
   
アプリケーションスコープを設定した後にファイルを保存します。 それ以外の場合、サービスからデータは返されません。 
  
### <a name="link-the-jsom-library"></a>JSOM ライブラリのリンク

ランタイム ライブラリProject Online、PS.jsおよびPS.debug.jsは、Project Onlineによって提供され、常に最新のバージョンです。 JSOM を使用する JavaScript アドインは、これらのライブラリの 1 つとリンクする必要があります。 リンク定義は Default.aspx ファイルに追加されます。 このコマンドを使用PS.js、PS.debug.jsファイルにあるコードの一部App.jsします。
  
"PS.js:ScriptLink" PS.js SharePoint:ScriptLink" にPS.debug.jsの要素に、次のコマンドを追加 `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` sp.js。 
  
```js
<SharePoint:ScriptLink name="PS.js" runat="server" OnDemand="false" LoadAfterUI="true" Localizable="false" />
```

> [!NOTE]
> ユーザー **またはユーザーの OnDemand** 属性PS.js false にPS.debug.js設定 **されます**。 
  
### <a name="add-ui-elements-to-the-add-in"></a>アドインに UI 要素を追加する

アドインの例は、いくつかのコンポーネントで構成されています。 静的要素の説明は、Default.aspx ファイルに保存されます。 すべてのコンポーネントの動的要素の説明とコードは、App.jsファイルに保存されます。 コンポーネントに関するコメントについては、ソース コードの一覧を参照してください。 アドインの UI コンポーネントの一覧を次に示します。
  
- Title
    
- 入門動詞
    
- テーブルからタスクを削除するボタン
    
- プロジェクト ID と名前、およびタスク情報を一覧表示するテーブル。
    
- タスク データをテーブルにインポートするタスク ボタン (プロジェクトごとに 1 回複製)。
    
プロジェクト テーブルのタイトルやヘッダー部分など、ユーザー インターフェイスの詳細については、「Default.aspx プロジェクト ファイル」を参照してください。
  
### <a name="initialize-and-connect-to-the-host-system"></a>ホスト システムの初期化と接続

このApp.jsには JavaScript コードが含まれている。 アドインはブラウザーでPS.js読み込み、initializePage 関数を呼び出します。 InitializePage は、エンドポイントのコンテキストを取得Project Online loadProjects 関数を開始します。
  
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

loadProjects 関数は、プロジェクト名と ID をサービスに照会します。 
  
アプリケーションは、プロジェクト名とプロジェクト ID を取得します。プロジェクトに関するその他の情報は使用可能であり、取得するプロパティを明示的に識別するために load メソッドを変更することでアクセスできます。 例は、コード内でコメントとして提供されます。 
  
クエリが成功すると、アドインは displayProjects を呼び出して続行されます。 
  
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

displayProjects 関数は、表、プロジェクトごとに 1 行、および特定のプロジェクトのタスクを表示するボタンを作成します。 
  
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
> while ループは ID と名前のプロパティにアクセスします。 これは、同じプロパティにアクセスする関数を呼び出すソース コード プロジェクトとは若干異なります。 
  
### <a name="display-the-tasks-for-a-project"></a>プロジェクトのタスクを表示する

アドインの一部であるタスクは、最初の読み込みの一部ではありません。 ユーザーがプロジェクトに関連付けられているタスクに関心がある場合は、[タスクの表示] ボタンをクリックすると、タスクが btnLoadTasks イベント ハンドラーを使用してリストに表示されます。 
  
btnLoadTasks イベント ハンドラーは、適切なプロジェクト ID を持ち、指定したプロジェクトのタスクをサーバーから要求します。 取得されると、btnLoadTasks はタスク リストを displayTasks に渡し、タスクを画面上に表示します。
  
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

displayTasks 関数は、指定したプロジェクトに関連付けられたタスクを、プロジェクト エントリの直下に表示します。
  
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
> while ループは、タスク ID と名前のプロパティにアクセスします。 これは、同じプロパティにアクセスする関数を呼び出すソース コード プロジェクトとは若干異なります。 
  
1 つのプロジェクトのタスクの出力例を次に示します。
  
![プロジェクト タスクの出力を示すスクリーンショット](media/f6500a3f-000b-4f3e-9be6-9a74d0bea15e.png "プロジェクト タスクの出力を示すスクリーンショット")
  
## <a name="see-also"></a>関連項目

Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/en-us/project)をご覧ください。
    


