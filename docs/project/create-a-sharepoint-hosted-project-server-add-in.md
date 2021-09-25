---
title: SharePoint をホストとする Project Server アドインを作成する
manager: lindalu
ms.date: 08/10/2016
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: Project Online 用に作成できる 3 種類のアプリ (自動ホスト型アプリ、プロバイダー ホスト型アプリ、SharePoint ホスト型アプリ) の中で、SharePoint ホスト型アプリは最も簡単に作成および展開できます。
ms.openlocfilehash: 2afa297fe61f026977277356b8ad63dbf86992ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560271"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>SharePoint をホストとする Project Server アドインを作成する

Project Online 用に作成できる 3 種類のアプリ (自動ホスト型アプリ、プロバイダー ホスト型アプリ、SharePoint ホスト型アプリ) の中で、SharePoint ホスト型アプリは最も簡単に作成および展開できます。 ホストSharePointアプリは、OAuth 認証を必要としないし、Azure を使用しないか、プロバイダーホスト型リソースのローカル サイトのメンテナンスを必要とします。 Visual Studio **の SharePoint 2013** 用アプリ テンプレートは、Office ストアで公開および販売したり、SharePoint のプライベート アプリ カタログに展開したりできるアプリを開発するための便利なフレームワークです。 
  
Project では、ステータスは、チーム メンバーが Project Web App の [タスク] ページを使用して、割り当てられたタスクの状態 (タスクの作業に費やされた 1 週間の毎日の作業時間数など) を送信できるプロセスです。 割り当ての所有者 (通常はプロジェクト マネージャー) は、状態を承認または拒否できます。 状態が承認されると、スケジュールProject再計算されます。 **QuickStatus アプリには割** り当てられたタスクが表示され、ユーザーは選択した割り当ての完了率を迅速に更新し、承認のために状態を送信できます。 [タスク] ページにはProject Web App機能が追加されましたが **、QuickStatus** アプリは簡略化されたインターフェイスを提供する例です。 
  
**QuickStatus アプリ** は、開発者向けのサンプルです。これは、実稼働環境での使用を目的としていない。 主な目的は、完全に機能する状態アプリを作成するのではなく、Project Onlineのアプリ開発の例を示す方法です。 ステータス設定の優れた方法については、「次の手順」の推奨事項 [を参照してください](#pj15_StatusingApp_NextSteps)。
  
状態の一般的な情報については、「タスクの進行状況 [」を参照してください](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress)。 SharePoint および Project サーバー用のアドインの開発の詳細については、「SharePoint[アドイン」を参照してください](https://msdn.microsoft.com/library/jj163230.aspx)。

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>サーバー 2013 のアプリProject前提条件

Project Online または Project Server 2013 のオンプレミス インストールに展開できる比較的単純なアプリを開発するには、オンラインの開発環境を提供する Napa を使用できます。 より複雑なアプリ、Project Web App リボンの変更、開発中のデバッグの容易さについては、Visual Studio 2012 または Visual Studio 2013。 たとえば、オンプレミスのインストールでは、サーバー データベースの変更について下書きデータテーブルを手動でProjectできます。 この記事では、アプリを使用してアプリ開発を行う方法をVisual Studio。
  
アプリケーションを使用Projectサーバー アプリの開発Visual Studio以下が必要です。
  
- 使用するローカルの開発用コンピューターに最新のサービス パックと Windows 更新プログラムをインストールしてあることを確認します。オペレーティング システムは、Windows 7、Windows 8、Windows Server 2008、Windows Server 2012 のいずれでもかまいません。
    
- SharePoint Server 2013 および Project Server 2013 がインストールされているコンピューターが必要です。このコンピューターはアプリの分離とサイドローディング用に構成されています。 サイドローディングを使用するとVisual Studioアプリを一時的にインストールしてデバッグできます。 サーバーとサーバーのオンプレミス インストールSharePoint使用Projectできます。 詳細については、「アプリのオンプレミスの開発環境をセットアップする」[を](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx)参照SharePoint。
    
   > [!NOTE]
   > 社内インストールの場合は、企業アプリ カタログを作成する前に、  *分離されたアプリ*  ドメインを構成します。 
  
- 開発用コンピューターは、2012 年の開発者Officeインストールされているリモート Visual Studioできます。 最新バージョンがインストールされていることを確認します。ダウンロードの *詳細については*[、「Apps for the Apps for Office」をSharePointしてください](https://msdn.microsoft.com/office/apps/fp123627.aspx)。
    
- 開発およびテストProject Web App使用するインスタンスにブラウザーでアクセス可能なインスタンスを確認します。
    
オンライン ツールの使用の詳細については、「アプリを開発するための環境をセットアップする」を参照SharePoint[をOffice 365。](https://msdn.microsoft.com/library/fp161179.aspx) オンライン ツールを使用する Project Server 用の簡単なアプリを構築する方法のチュートリアルについては、「EPMSource ブログ シリーズ」「Building your first Project [Server app」を参照してください](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/)。

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>サーバー Visual Studioを使用してサーバー アプリProject作成する

Office2012 Visual Studio開発者向けツールには、SharePoint Server 2013 で使用できるアプリProjectが含まれています。 アプリ ソリューションを作成すると、カスタム コード用の次のファイルがソリューションに含まれます。
  
- **AppManifest.xml** には、アプリのタイトル、アクセス許可要求スコープ、その他のプロパティの設定が含まれます。 手順 1 には、マニフェスト デザイナーを使用してプロパティを設定する手順が含まれています。 
    
- **Pages フォルダーの Default.aspx** は、アプリのメイン ページです。 手順 2 は、QuickStatus アプリの HTML5 コンテンツを追加 **する方法を示** しています。 
    
- **App.js** フォルダー内のファイルは、カスタム JavaScript コードのプライマリ ファイルです。 手順 3 では、QuickStatus アプリの **JavaScript コードについて説明** します。 
    
   jQuery ベースのグリッドや日付ピッカーなどの商用コントロールを追加する場合は、Default.aspx ファイルで追加の JavaScript ファイルへの参照を追加できます。
    
- **コンテンツ フォルダーの App.css** は、カスタム CSS3 スタイルのプライマリ ファイルです。 手順 2 と手順 3 には、QuickStatus アプリのカスケード スタイル シート (CSS) スタイル **に関する情報が含** まれています。 Default.aspx ファイルで、追加の CSS ファイルへの参照を追加できます。 
    
- **AppIcon.png** フォルダー内の 96 x 96 アイコンは、アプリが Office ストアまたはアプリ カタログに表示されます。 
    
リボンを変更Project Web App、リボン のカスタム アクションを追加できます。 [[QuickStatus](#pj15_StatusingApp_Example)アプリのコード例] セクションには、変更された Default.aspx、App.js、App.css、Elements.xml、および AppManifest.xml ファイルの完全なコードが含まれています。 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>手順 1. アプリ プロジェクトを作成するには、Visual Studio

1. 管理者Visual Studio 2012 を実行し、[スタート] ページで **[Project]** を選択します。 
    
2. [新しい **Project]** ダイアログ ボックスで、[テンプレート] 、[Visual C#]、および **[Office/SharePoint]** ノードを展開し、[アプリ] を選択 **します**。  中央ウィンドウの.NET Frameworkにあるターゲット フレームワーク ドロップダウン リストの既定の .NET Framework **4.5** を使用し、次に **[SharePoint 2013** のアプリ] を選択します (図 1 を参照)。 
    
3. [名前 **] フィールドに** 「QuickStatus」と入力し、アプリを保存する場所を参照し **、[OK] を選択します**。
    
   **図 1.サーバー 内Projectサーバー アプリを作成Visual Studio**

   ![Visual Studio での Project Server アプリの作成](media/pj15_CreateStatusingApp_NewProject.gif "Visual Studio での Project Server アプリの作成")
  
4. [アプリの **新しいSharePoint]** ダイアログ ボックスで、次の 3 つのフィールドに入力します。 
    
   - 上部のテキスト ボックスに、アプリでアプリに表示する名前を入力Project Web App。 たとえば、「Quick Status Update」と入力します。
    
   - デバッグに使用するサイトの場合は、インスタンスの URL をProject Web Appします。 たとえば  `https://ServerName/ProjectServerName`  _、(ServerName_ と  _ProjectServerName_ を独自の値に置き換える) と入力し、[検証] を **選択します**。 すべてが正常に終了すると、接続Visual Studioが **表示されます**。 エラー メッセージが表示された場合は、Project Web App URL が正しく、Project Server コンピューターがアプリの分離とサイドローディング用に構成されていることを確認します。 詳細については、「サーバー [2013 のアプリを作成するためのProject」を参照](#pj15_StatusingApp_Prerequisites)してください。 
    
   - [アプリ **をホストする方法] ボックス** の一覧SharePoint、[ホストされているアプリSharePoint **選択します**。
    
   > [!CAUTION]
   > プロバイダーホスト型の既定のプロジェクトの種類を誤って選択した場合、Visual Studio はソリューションに QuickStatus プロジェクトと **QuickStatusWeb** プロジェクトの 2 つのプロジェクトを **作成** します。 2 つのプロジェクトが表示される場合は、そのソリューションを削除して、もう一度開始します。 
  
5. **[OK]** を選択して **、QuickStatus** ソリューション **、QuickStatus** プロジェクト、および既定のファイルを作成します。 
    
6. マニフェスト デザイナー ビューを開きます (たとえば、ファイルをダブルクリックAppManifest.xmlします。 [全般 **] タブ** の **[タイトル] テキスト** ボックスに、手順 4 で入力したアプリ名が表示されます。 [アクセス許可 **] タブを** 選択して、アプリの次のアクセス許可要求を追加します (図 2 を参照)。 
    
   - [アクセス許可要求]**リストの** 最初の行の [スコープ]**列で、** ドロップダウン リストの [状態] を選択します。 [アクセス許可 **] 列で****、[SubmitStatus] を選択します**。
    
   - スコープが複数のプロジェクトで **、アクセス****許可** が読み取 **りである行を** 追加 **します**。
    
   **図 2.状態アプリのアクセス許可スコープの設定**

   ![状態管理アプリのアクセス許可の範囲を設定](media/pj15_CreateStatusingApp_PermissionScope.gif "状態管理アプリのアクセス許可の範囲を設定")
  
**QuickStatus アプリを使用** すると、Project Web Appユーザーは、そのユーザーの割り当てを複数のプロジェクトから読み取り、割り当て率の完了率を変更し、更新プログラムを提出できます。 図 2 のドロップダウン リストに示されている他のアクセス許可要求スコープは、このアプリでは必要ありません。 アクセス許可要求スコープは、アプリがユーザーに代わって要求するアクセス許可です。 ユーザーがこれらのアクセス許可を持Project Web App、アプリは実行されません。 アプリには、他のアクセス許可のアクセス許可を含む複数のアクセス許可要求スコープをSharePointできますが、アプリの機能に必要な最小限の権限のみを持つ必要があります。 サーバーに関連するアクセス許可要求スコープをProjectします。 

- **Enterprise : リソース** マネージャーのアクセス許可、他のユーザーに関する情報の読み取りProject Web Appします。
    
- **複数のプロジェクト**: 複数のプロジェクトに対する読み取りまたは書き込み。ユーザーはアクセス許可を要求します。
    
- **Project サーバー**: アプリ ユーザーに管理者のアクセス許可を付与する必要Project Web App。
    
- **レポート**: **ProjectData OData** サービスを読み取り、Project Web App (ユーザーのアクセス許可のみをログオンする必要Project Web App)。 
    
- **単Project**: ユーザーが要求したアクセス許可を持つプロジェクトに対する読み取りまたは書き込み。
    
- **Statusing**: 割り当ての状態 (作業時間、完了率、新しい割り当てなど) の更新プログラムを送信します。
    
- **ワークフロー**: ユーザーがサーバー ワークフローを実行Project場合、アプリはワークフローの管理者特権のアクセス許可を使用して実行されます。
    
Project Server 2013 のアクセス許可要求スコープの詳細については、「Project 2013 の開発者向け更新プログラム」および[「SharePoint 2013](updates-for-developers-in-project-2013.md)のアプリのアクセス許可」の「Project アプリ」セクション[を参照](https://msdn.microsoft.com/library/fp142383.aspx)してください。 


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>QuickStatus アプリの HTML コンテンツの作成

HTML コンテンツのコーディングを開始する前に、QuickStatus アプリのユーザー インターフェイスとユーザー エクスペリエンスを設計します (図 3 は、完成したページの例を示しています)。 デザインには、HTML コードを操作する JavaScript 関数のアウトラインも含めできます。 一般的な情報については[、「2013](https://msdn.microsoft.com/library/fp179934.aspx)年のアプリの UX デザイン」をSharePointしてください。
  
**図 3.QuickStatus アプリ ページのデザイン**

![QuickStatus アプリ ページの設計](media/pj15_CreateStatusingApp_AfterRefresh.gif "QuickStatus アプリ ページの設計")
  
アプリの上部に表示名が表示されます。これは、アプリの **Title** 要素の値AppManifest.xml。 
  
既定では、ページは HTML5 を使用します。 **QuickStatus** アプリがページの本文に含まれている主な UI オブジェクトの標準 HTML 要素を次に示します。 
  
- フォーム **要素** には、他のすべての UI 要素が含まれます。 
    
- fieldset **要素は** 、割り当てのテーブルのコンテナーと罫線を作成します。子凡例 **要素は** 、コンテナーのラベルを提供します。 
    
- **table 要素には**、キャプションとテーブル ヘッダーだけが含まれます。 JavaScript 関数は、テーブルのキャプションを変更し、割り当ての行を追加します。 
    
   > [!NOTE]
   > ページングと並べ替えを簡単に追加するには、実稼働アプリでテーブルの代わりに商用の jQuery ベースのグリッド コントロールを使用する可能性があります。 
  
   このテーブルには、プロジェクト名の列、チェック ボックス付きタスク名、実績作業時間、完了率、残りの作業時間、および割り当ての終了日が含まれます。 JavaScript 関数は、各タスクの完了率のチェック ボックスとテキスト入力フィールドを作成します。
    
- テキスト **ボックスの** 入力要素は、選択した割り当てすべてについて、完了率を設定します。 
    
- **button 要素は**、状態の変更を送信します。 
    
- **button 要素によって** ページが更新されます。 
    
- button **要素** はアプリを終了し、アプリの [タスク] ページにProject Web App。 
    
下部のテキスト ボックスとボタン要素は **div** 要素内にあるので、CSS は UI オブジェクトの位置と外観を簡単に管理できます。 JavaScript 関数は、ページの下部に、状態更新の成功または失敗の結果を含む段落を追加します。 
  
### <a name="procedure-2-to-create-the-html-content"></a>手順 2. HTML コンテンツを作成するには

1. [Visual Studioで、Default.aspx ファイルを開きます。
    
   このファイルには **、2 つの asp:Content** 要素が含まれています。属性を持つ要素はページ ヘッダー内に追加され、属性を持つ要素はページ本文要素  `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"`  `ContentPlaceHolderID="PlaceHolderMain"` 内 **に配置** されます。 
    
2. ページ ヘッダーのコントロールで、サーバー コンピューター上の PS.js `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` ファイルへの参照Projectします。 テストとデバッグでは、次のコマンドをPS.debug.js。 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   アプリ インフラストラクチャは `/_layouts/15/` 、IIS のサイトの仮想ディレクトリSharePoint使用します。 物理ファイルはです  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js` 。
    
   > [!NOTE]
   > 実稼働用にアプリを展開する前に、スクリプト参照から削除  `.debug` してパフォーマンスを向上させます。 
  
3. ページ本文  `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">` のコントロールで、生成された **div** 要素を削除し、UI オブジェクトの HTML コードを追加します。 table **要素** にはヘッダー行だけが含まれます。 [ **タスク名] 列** には、チェック ボックス入力コントロールが含まれます。 caption 要素 **のテキスト** は、ファイル内の getUserInfo 関数の **onGetUserNameSuccess** コールバックに置き換App.jsされます。  
    
    ```HTML
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
        <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
        </div>
    </form>
    ```

4. App.css ファイルで、UI 要素の位置と外観の CSS コードを追加します。 QuickStatus アプリの完全な CSS コードについては **、「QuickStatus** アプリのサンプル [コード」セクションを参照](#pj15_StatusingApp_Example) してください。 
    
手順 3 では、割り当てを読み取り、テーブル行を作成し、割り当ての完了率を変更および更新する JavaScript 関数を追加します。 実際の手順は、HTML コードの一部を交互に作成し、関連するスタイルと JavaScript 関数を追加およびテストし、HTML コードを変更または追加してから、プロセスを繰り返す、アプリの開発におけるより反復的な手順です。

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>QuickStatus アプリの JavaScript 関数の作成

SharePoint アプリの Visual Studio テンプレートには、SharePoint クライアント コンテキストを取得し、アプリ ページの基本的な取得および設定アクションを示す既定の初期化コードを含む App.js ファイルが含まれています。 クライアント側のライブラリライブラリSharePoint JavaScript 名前空間SP.js SP **です**。 Project Server アプリは PS.js ライブラリを使用しますので、アプリは **PS** 名前空間を使用してクライアント コンテキストを取得し、Project Server の JSOM にアクセスします。 
  
QuickStatus アプリの **JavaScript 関数には** 、次のものが含まれます。 
  
- ドキュメント オブジェクト **モデル** (DOM) がインスタンス化されると、ドキュメント準備完了イベント ハンドラーが実行されます。 ready **イベント ハンドラー** は、次の 4 つの手順を実行します。 
    
    1. サーバー JSOM **と pwaWeb** グローバル変数のクライアント コンテキストProject **projContext** グローバル変数を初期化します。 
        
    2. **getUserInfo 関数を呼び** 出して **、projUser グローバル変数を** 初期化します。 
        
    3. **getAssignments 関数を呼び出** し、ユーザーの指定された割り当てデータを取得します。 
        
    4. クリック イベント ハンドラーをテーブル ヘッダー チェック ボックスにバインドし、テーブルの各行のチェック ボックスにバインドします。 Click イベント ハンドラーは、ユーザーがテーブル内のチェック ボックスをオンまたはオフにした場合に、チェック ボックスの check 属性を管理します。 
    
- **getAssignments 関数** が成功すると **、onGetAssignmentsSuccess 関数が呼び出** されます。 この関数は、各割り当てのテーブルに行を挿入し、各行の HTML コントロールを初期化し、下ボタンのプロパティを初期化します。 
    
- [**更新] ボタンの onClick** イベント ハンドラー **は****、updateAssignments 関数を呼び出** します。 この関数は、選択した各割り当てに適用される完全率の値を取得します。または、パーセントの完全なテキスト ボックスが空の場合、関数はテーブル内で選択した各割り当ての完了率を取得します。 **updateAssignments 関数** は、状態の更新を保存して送信し、結果に関するメッセージをページの下部に書き込みます。 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>手順 3. JavaScript 関数を作成するには

1. [Visual Studio] で、App.jsファイルを開き、ファイル内のすべてのコンテンツを削除します。
    
2. グローバル変数とドキュメント準備完了イベント **ハンドラーを** 追加します。 ドキュメント **オブジェクト** にアクセスするには、jQuery 関数を使用します。 
    
   [テーブル ヘッダーのクリック イベント ハンドラー] チェック ボックスは、行チェック ボックスのチェック状態を設定します。 すべての行チェック ボックスがオンまたはすべてクリアされている場合、行チェック ボックスの click イベント ハンドラーは、ヘッダー チェック ボックスのチェック状態を設定します。 click イベント ハンドラーは、ページの下部にある結果メッセージを空の文字列に設定します。
    
   ```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the checked state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
   ```

3. クエリが **成功した場合** に **GetUserNameSuccess** を呼び出す getUserInfo 関数を追加します。 **onGetUserNameSuccess 関数** は、キャプション段落の内容を、ユーザー名を含む表のキャプションに置き換える。 
    
   ```js
        // Get information about the current user.
        function getUserInfo() {
            projUser = pwaWeb.get_currentUser();
            projContext.load(projUser);
            projContext.executeQueryAsync(onGetUserNameSuccess,
                // Anonymous function to execute if getUserInfo fails.
                function (sender, args) {
                    alert('Failed to get user name. Error: ' + args.get_message());
            });
        } 
        // This function is executed if the getUserInfo call is successful.
        function onGetUserNameSuccess() {
            var prefaceInfo = 'Assignments for ' + projUser.get_title();
            $('#tableCaption').text(prefaceInfo);
        }
   ```

4. **getAssignments** 関数を追加します。この関数は、割り当てクエリが成功した場合に **、onGetAssignmentsSuccess** (手順 5 を参照) を呼び出します。 [ **含める** ] オプションは、指定したフィールドのみを返すクエリを制限します。 
    
   ```js
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
   ```

5. 表に **各割り当ての行を追加する onGetAssignmentsSuccess** 関数を追加します。 **prevProjName** 変数を使用して、行が別のプロジェクト用であるかどうかを判断します。 その場合、プロジェクト名は太字で表示されます。指定しない場合、プロジェクト名は空の文字列に設定されます。 
    
   > [!NOTE]
   > JSOM には **、CSOM** に含まれる TimeSpan プロパティ **(ActualWorkTimeSpan** など) は含まれています。 代わりに、JSOM は PS などのミリ秒単位のプロパティを使用 [します。StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx) プロパティ。 そのプロパティを取得するメソッドは **、整数値を返す \_ actualWorkMilliseconds** を取得します。 > メソッドget_actualWork"3h" などの文字列を返します。  どちらの値も **QuickStatus アプリで使用** できますが、表示方法は異なります。 割り当てクエリには両方のプロパティが含まれるので、デバッグ中に値をテストできます。 actualWork 変数 **を削除した** 場合は、割り当てクエリ **で ActualWork** プロパティを削除することもできます。 
  
   最後に **、onGetAssignmentsSuccess** 関数は、[更新] ボタンと[更新] ボタンをクリック イベント ハンドラーで初期化します。 [更新] ボタンの **テキスト値** は、HTML コードでも設定できます。 
    
   ```js
        // Get the enumerator, iterate through the assignment collection, 
        // and add each assignment to the table.
        function onGetAssignmentsSuccess(sender, args) {
            if (assignments.get_count() > 0) {
                var assignmentsEnumerator = assignments.getEnumerator();
                var projName = "";
                var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
                var taskNum = 0;
                var chkTask = "";
                var txtPctComplete = "";
                // Constants for creating input controls in the table.
                var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
                var LBLCHK = '<label for="chk';
                var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
                while (assignmentsEnumerator.moveNext()) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    projName = statusAssignment.get_project().get_name();
                    // Get an integer, such as 3600000.
                    var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds(); 
                    // Get a string, such as "1h". Not used here.
                    var actualWork = statusAssignment.get_actualWork();
                    if (projName === prevProjName) {
                        projName = "";
                    }
                    prevProjName = statusAssignment.get_project().get_name();
                    // Create a row for the assignment information.
                    var row = assignmentsTable.insertRow();
                    taskNum++;
                    // Create an HTML string with a check box and task name label, for example:
                    // <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> <label for="chk1">Task 1</label>
                    chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">' 
                        + statusAssignment.get_name() + '</label>';
                    txtPctComplete = INPUTTXT + taskNum + '" />';
                    // Insert cells for the assignment properties.
                    row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                    row.insertCell().innerHTML = chkTask;
                    row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                    row.insertCell().innerHTML = txtPctComplete;
                    row.insertCell().innerText = statusAssignment.get_remainingWork();
                    row.insertCell().innerText = statusAssignment.get_finish();
                    // Initialize the percent complete cell.
                    $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
                }
            }
            else {
                $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
                $get("message").innerText = projUser.get_title() + ' has no assignments'
            }
            // Initialize the button properties.
            $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
            $get("btnSubmitUpdate").innerText = 'Update';
            $get('btnRefresh').onclick = function () { window.location.reload(true); };
            $get('btnExit').onclick = function () { exitToPwa(); };
        }
   ```

6. Update ボタン **の updateAssignments** click イベント ハンドラーを **追加** します。 ユーザーがタスクの完了率の値を変更したり **、percentComplete** テキスト ボックスに値を追加したりすると、値は "60"、"60%"、"60%" などの複数の形式で入力できます。 **getNumericValue** メソッドは、入力テキストの数値を返します。 
    
   > [!NOTE]
   > 実稼働用に設計されたアプリでは、数値情報の入力値には、フィールドの検証と追加のエラー チェックが含まれる必要があります。 
  
   **updateAssignments** の例には、基本的なエラー チェックが含まれています。ページの下部にあるメッセージ段落に情報が表示されます。更新クエリが成功した場合は緑、入力エラーが発生した場合や更新クエリが失敗した場合は赤を表示します。 
    
   **submitAllStatusUpdates** メソッドを使用する前に、アプリは PS を使用して更新プログラムをサーバーに保存する必要 **があります。StatusAssignmentCollection.update** メソッド。 
    
   ```js
        // Update all checked assignments. If the bottom percent complete field is blank,
        // use the value in the % complete field of each selected row in the table.
        function updateAssignments() {
            // Get percent complete from the bottom text box.
            var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
            var pctComplete = pctCompleteMain;
            var assignmentsEnumerator = assignments.getEnumerator();
            var taskNum = 0;
            var taskRow = "";
            var indexPercent = "";
            var doSubmit = true;
            while (assignmentsEnumerator.moveNext()) {
                var pctCompleteRow = "";
                taskRow = "chk" + ++taskNum;
                if ($get(taskRow).checked) {
                    var statusAssignment = assignmentsEnumerator.get_current();
                    if (pctCompleteMain === "") {
                        // Get percent complete from the text box field in the table row.
                        pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                        pctComplete = pctCompleteRow;
                    }
                    // If both percent complete fields are empty, show an error.
                    if (pctCompleteMain === "" && pctCompleteRow === "") {
                        $('p#message').attr('style', 'color: #e11500');     // Red text.
                        $get("message").innerHTML =
                            '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                            + taskNum
                            + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                            + '<p>Please refresh the page and try again.</p>';
                        doSubmit = false;
                        taskNum = 0;
                        break;
                    }
                    if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
                }
            } 
            // Save and submit the assignment updates.
            if (doSubmit) {
                assignments.update();
                assignments.submitAllStatusUpdates();
                projContext.executeQueryAsync(function (source, args) {
                    $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                    $get("message").innerText = 'Assignments have been updated.';
                }, function (source, args) {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerText = 'Error updating assignments: ' + args.get_message();
                });
            }
        }
        // Get the numeric part for percent complete, from a string. For example, with "20 %", return "20".
        function getNumericValue(pctComplete) {
            pctComplete = pctComplete.trim();
            pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
            indexPercent = pctComplete.indexOf('%', 0);
            if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
            return pctComplete;
        }
   ```

7. サイトのホストの URL に **SPHostUrl** クエリ文字列パラメーターを使用する **exitToPwa** 関数をProject Web Appします。 [タスク] ページに戻る場合は  `"/Tasks.aspx"` 、URL に追加します。 たとえば **、spHostUrl** 変数はに設定されます  `https://ServerName/ProjectServerName/Tasks.aspx` 。
    
   **getQueryStringParameter** 関数は **、QuickStatus** ページの URL を分割して、URL オプションで指定されたパラメーターを抽出して返します。 ドキュメントの例を次に示 **します。QuickStatus** ドキュメント **の URL 値** (すべて 1 行目): 
    
   ```HTML
    https://app-ef98082fa37e3c.servername.officeapps.selfhost.corp.microsoft.com/pwa/
        QuickStatus/Pages/Default.aspx
        ?SPHostUrl=https%3A%2F%2Fsphvm%2D85178%2Fpwa
        &SPLanguage=en%2DUS
        &SPClientTag=1
        &SPProductNumber=15%2E0%2E4420%2E1022
        &SPAppWebUrl=https%3A%2F%2Fapp%2Def98082fa37e3c%2Eservername
            %2Eofficeapps%2Eselfhost%2Ecorp%2Emicrosoft%2Ecom%2Fpwa%2FQuickStatus
   ```

   前の URL では **、getQueryStringParameter** 関数は **SPHostUrl** クエリ文字列値を返します  `https://ServerName/pwa` 。 
    
   ```js
        // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
        function exitToPwa() {
            // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
            var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                            + "/Tasks.aspx";
            // Set the top window for the QuickStatus IFrame to the Tasks page.
            window.top.location.href = spHostUrl;
        }
        // Get a specified query string parameter from the {StandardTokens} URL option string.
        function getQueryStringParameter(urlParameterKey) {
            var docUrl = document.URL;
            var params = docUrl.split('?')[1].split('&');
            for (var i = 0; i < params.length; i++) {
                var theParam = params[i].split('=');
                if (theParam[0] == urlParameterKey)
                    return decodeURIComponent(theParam[1]);
            }
        }
   ```

この時点で **QuickStatus** アプリを発行し、Project Web App に追加した場合、アプリは [サイト コンテンツ] ページから実行できますが、ユーザーが簡単に使用できません。 ユーザーがアプリを見つけて実行するために、[タスク] ページのリボンにボタンを追加できます。 手順 4 は、リボン のカスタム アクションを追加する方法を示しています。 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>リボンのカスタム操作の追加

リボン タブ、グループ、およびコントロールは、Project Web App Server を実行しているコンピューターのディレクトリにインストールされている pwaribbon.xml ファイル `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` でProjectされます。 2013 SDK のダウンロードには、Project Web Appリボンのカスタム アクションを設計Project 2013 SDK のダウンロードには、pwaribbon.xml。 
  
Project Web Appは、Project Web App インスタンスでタイムシートとタスクの状態の両方の値を入力できる単一入力モードを使用するかどうかに応じて、[タスク] ページで異なるリボン定義を使用します。 Project Web App の管理アクセス許可がある場合は、エントリ モードを決定するには、ページの右上隅にあるドロップダウン設定メニューで **[PWA 設定]** を選択します。 [PWA 設定] ページで、[タイムシート] 設定 **と [** 既定値] を選択し、ページの下部にある [単一エントリ モード] チェック ボックスをオンにします。 
  
単一入力モードがオフの場合、[タスク] ページのリボンは、[タスク] ページの [自分の作業] 領域pwaribbon.xml。 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

単一エントリ モードがオンの場合、[タスク] ページリボンは、次の項目の [タイド モード] 領域pwaribbon.xml。 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

各領域のグループとコントロールは似ていますが、タイド モードのコントロールは、非タイド モードの同じコントロールとは異なる関数を呼び出す場合があります。 手順 4 は、シングル エントリ モードがオフのときに **QuickStatus** アプリのボタン コントロールを追加する方法を示しています ([単一エントリ **モード]** チェック ボックスはオフです)。 
  
> [!NOTE]
> リボンまたは SharePoint アプリケーションのメニューにカスタム アクションを追加する方法の一般的な情報については、「カスタム アクションを作成して、SharePoint 用アプリを使用して展開[する」を参照してください](https://msdn.microsoft.com/library/jj163954.aspx)。 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>手順 4. リボン のカスタム アクションを [タスク] ページに追加するには

1. [タスク] ページのリボンを確認Project Web App。 リボンの **[タスク]** タブを選択し、変更方法を計画します。 Submit、Tasks、Period など、7 **つのグループ****があります**。 送信 **グループには** 、[保存] ボタンと **[** 状態の送信] ドロップダウン メニューの **2** つのコントロールがあります。 グループ内の任意の場所にコントロールを追加したり、[ **タスク** ] タブの任意の場所に新しいコントロールを含むグループを追加したり、カスタム グループとコントロールを持つ別のリボン タブを追加することができます。 この例では、Submit グループに 3番目のボタンを追加します。このボタンは QuickStatus アプリの URL **を呼び出** します。 
    
2. [ソリューション **エクスプローラー] ウィンドウ** Visual Studio **QuickStatus** プロジェクトを右クリックし、新しいアイテムを追加します。 [新しい **アイテムの追加] ダイアログ** ボックスで、[リボン カスタム アクション] を **選択します** (図 4 を参照)。 たとえば、カスタム アクションに RibbonQuickStatusAction という名前を付け、[追加] を **選択します**。
    
   **図 4.リボン のカスタム アクションの追加**

   ![リボンのカスタム操作の追加](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "リボンのカスタム操作の追加")
  
3. リボンのカスタム アクションの作成ウィザードの最初のページで、[**ホスト Web]** オプションを選択したままにし、カスタム アクション スコープのドロップダウン リストで [なし] を選択し、[次へ] を選択します **(図** 5 を参照)。 ドロップダウン リスト内のアイテムは、サーバーのSharePointにProjectされます。 カスタム アクションに対して生成された XML のほとんどを置き換え、その XML がサーバーに適用Projectします。 
    
   **図 5.リボン のカスタム アクションのプロパティを指定する**

   ![リボンのカスタム アクションにプロパティを指定](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "リボンのカスタム アクションにプロパティを指定")
  
4. [リボン用カスタム アクションの作成] ウィザードの次のページで、設定のすべての既定値を残し、[完了] を選択します **(図** 6 を参照)。 Visual Studioを含む **RibbonQuickStatusAction** フォルダーをElements.xmlします。 
    
   **図 6.ボタン コントロールの設定を指定する**

   ![ボタン コントロールに設定を指定](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "ボタン コントロールに設定を指定")
  
5. リボン カスタム アクションの既定Elements.xmlコードを変更します。 既定の XML コードを次に示します。
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
        <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon"
                    Sequence="10001"
                    Title="Invoke &apos;RibbonQuickStatusAction&apos; action">
        <CommandUIExtension>
            <!-- 
            Update the UI definitions below with the controls and the command actions
            that you want to enable for the custom action.
            -->
            <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ListItem.Actions.Controls._children">
                <Button Id="Ribbon.ListItem.Actions.RibbonQuickStatusActionButton"
                        Alt="Request RibbonQuickStatusAction"
                        Sequence="100"
                        Command="Invoke_RibbonQuickStatusActionButtonRequest"
                        LabelText="Request RibbonQuickStatusAction"
                        TemplateAlias="o1"
                        Image32by32="_layouts/15/images/placeholder32x32.png"
                        Image16by16="_layouts/15/images/placeholder16x16.png" />
            </CommandUIDefinition>
            </CommandUIDefinitions>
            <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_RibbonQuickStatusActionButtonRequest"
                                CommandAction="~appWebUrl/Pages/Default.aspx"/>
            </CommandUIHandlers>
        </CommandUIExtension >
        </CustomAction>
    </Elements>
   ```

   1. **CustomAction 要素で****、Sequence** 属性と Title 属性を **削除** します。 
    
   2. Submit グループにコントロールを追加するには、コレクション内の最初のグループを pwaribbon.xml ファイル (開始する要素) `Ribbon.ContextualTabs.MyWork.Home.Groups` で検索します `<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"` 。 子コントロールを **Submit** グループに追加するには、次のコードは、コマンド ファイル内の **CommandUIDefinition** 要素の正しい Location 属性Elements.xmlします。 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. 子 Button 要素の属性値を次 **のように** 変更します。 
    
       ```XML
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invoke_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="QuickStatus"
                    ToolTipDescription="Run the QuickStatus app" />
       ```

       - グループ内の 3 番目のコントロールをボタンに設定するには **、Sequence** 属性を既存の [状態の送信] コントロールの値 (pwaribbon.xml の `Sequence="20"` **FlyoutAnchor** 要素) よりも任意の数値にできます。  規則により、グループとコントロールのシーケンス番号は、中間位置に要素を  `10, 20, 30, …` 挿入することができます。
    
       - **Command 属性** は **、CommandUIHandler** 要素で実行するコマンドを指定します (次の手順 5.d を参照)。 コマンド名を簡略化して、次の開発者が簡単に実行できます。 たとえば、  `Command="Invoke_QuickStatus"` より簡単に読み取りが可能です  `Command="Invoke_RibbonQuickStatusActionButtonRequest"` 。
    
       - 画像属性は、ボタン コントロールの 16 x 16 ピクセル アイコンと 32 x 32 ピクセル のアイコンを指定します。 既定の既定のElements.xml、  `Image32by32="_layouts/15/images/placeholder32x32.png"` オレンジ色のドットを指定します。 サーバーを実行しているコンピューターのディレクトリにインストールされているイメージ マップ ファイル (ps16x16.png および ps32x32.png) からアイコンを `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Projectできます。 たとえば、32 x 32 ピクセルのアイコンは、ps32x32.png イメージ マップの上端から左から 10 行目のアイコンの 2 列目に表示されます (アイコンの上部は 9 行目の終わりの後、9 行 x 32 ピクセル/行 = 288 ピクセル)。 
    
       - ボタン コントロールのツール ヒントを表示するには **、ToolTipTitle** 属性と **ToolTipDescription 属性を追加** します。 
    
    4. **CommandUIHandler 要素の属性を変更** します。 たとえば **、Command** 属性が **Button** 要素の **Command** 属性値と一致する必要があります。 **CommandAction 属性** の場合 `~appWebUrl` は **、QuickStatus** Web ページの URL のプレースホルダーです。 リボン ボタンが **QuickStatus** アプリを呼び出すと **、{StandardTokens}** トークンが SPHostUrl、SPLanguage、SPClientTag、SPProductNumber、および **SPAppWebUrl** を含む URL オプションに置き換えられる。    
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. ソリューション **エクスプローラーで****、Feature1.feature** デザイナーを開き **、RibbonQuickStatusAction** アイテムを[ソリューション] ウィンドウの [アイテム] から [機能] ウィンドウの [アイテム]**に移動** します。 その後 **、Package.package** デザイナーを開いた場合 **、RibbonQuickStatusAction** アイテムが [パッケージ] ウィンドウの **[アイテム] に表示** されます。 
    
アプリを開発し、リボン ボタンを追加すると、通常はアプリをテストし、デバッグ用の JavaScript コードにブレークポイントを設定します。 **F5** キーを押してデバッグを開始すると、Visual Studio はアプリをコンパイルし **、QuickStatus** プロジェクトの **Site URL** プロパティで指定されたサイトに展開し、アプリを信頼するかどうかを確認するページを表示します。 **QuickStatus** アプリを続行して終了すると、アプリの [タスク] ページにProject Web App。 

> [!NOTE]
> 図 7 は、リボン **の [タスク** ] タブの [ **クイック** 状態] ボタンが無効になっている状態を示しています。 Visual Studioを使用して多くのデバッグ展開を行った後、発行済みアプリを同じテスト サーバーでデバッグまたは展開し続ける場合、カスタム リボン コントロールをブロックできます。 ボタンを有効にするには、Visual Studio で **RibbonQuickStatusAction** アイテムを削除し、別の名前と ID を持つ新しいリボン アクションを作成します。 それでも問題が解決しない場合は、Project Web App テスト インスタンスからアプリを削除し、別のアプリ ID でアプリを再作成してください。 
  
**図 7.無効にした [クイック状態] ボタンのヒントを表示する**

![無効化されているボタンのツールチップの表示](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "無効化されているボタンのツールチップの表示")
  
手順 5 は、QuickStatus アプリを展開して **インストールする方法を示** しています。 手順 6 では、アプリをインストールした後にアプリをテストする手順を示します。 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>QuickStatus アプリの展開

アプリを web アプリケーションに展開する方法は、SharePointなど、いくつかの方法Project Web App。 使用する展開は、アプリをプライベート SharePoint カタログに発行するか、パブリック Office ストアに発行するか、SharePoint がオンプレミスにインストールされているのか、オンライン テナンシーなのかによって異なっています。 手順 5 は、プライベート アプリ カタログ内のオンプレミス インストールに **QuickStatus** アプリを展開する方法を示しています。 詳細については、「Install [and manage apps for SharePoint 2013」](https://technet.microsoft.com/library/fp161232.aspx)および[「Publish apps for SharePoint](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> アプリをカタログに追加するには、SharePointアクセスSharePoint必要があります。 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>手順 5. QuickStatus アプリを展開するには

1. [Visual Studio、すべてのファイルを保存し、ソリューション エクスプローラーで **QuickStatus** プロジェクトを右クリックし、[**発行]** を **選択します**。
    
2. **QuickStatus アプリは** ホストSharePointので、発行のオプションは非常に少ない (図 8 を参照)。 [アプリの **公開とOfficeとSharePoint]** ダイアログ ボックスで、[完了] を **選択します**。
    
   **図 8.QuickStatus アプリの発行**

   ![公開ウィザードの使用](media/pj15_CreateStatusingApp_PublishWizard.gif "公開ウィザードの使用")
  
3. ディレクトリから QuickStatus.app ファイルをローカル コンピューターの便利なディレクトリ (またはオンプレミス インストール用SharePointコンピューターに `~\QuickStatus\bin\Debug\app.publish\1.0.0.0` コピーします。 
    
4. [SharePoint管理] で、[クイック 起動 **]** で [アプリ] を選択し、[アプリ カタログの管理 **] を選択します**。
    
5. アプリ カタログが存在しない場合は、「SharePoint [2013](https://technet.microsoft.com/library/fp161234.aspx)でアプリ カタログを管理する」の *「Web* アプリケーションのアプリ カタログ サイトを構成する」セクションに従って、アプリ カタログのサイト コレクションを作成します。
    
   アプリ カタログが存在する場合は、[アプリ カタログの管理] ページのサイト URL に移動します。 たとえば、次の手順では、アプリ カタログ サイトは  `https://ServerName/sites/TestApps` です。
    
6. アプリ カタログ ページで、[クイック起動] で [アプリ **SharePoint** を選択します。 [アプリの作成SharePoint] ページで、リボンの **[FILES]** タブで、[ドキュメント]**アップロードします**。
    
7. [ドキュメント **の追加] ダイアログ** ボックスで、QuickStatus.app ファイルを参照し、バージョンのコメントを追加し **、[OK] を選択します**。
    
8. アプリを追加するときに、アプリの説明、アイコン、その他の情報のローカル情報を追加することもできます。 [アプリ **のSharePoint -** QuickStatus.app] ダイアログ ボックスで、アプリに表示する情報をサイト コレクションのSharePointします。 たとえば、次の情報を追加します。 
    
   1. **[短い説明** ] フィールド: 「クイック 状態テスト アプリ」と入力します。
    
   2. **[説明** ] フィールド: 複数のプロジェクトのタスクの完了率を更新するテスト アプリと入力します。
    
   3. **アイコン URL** フィールド: アプリ カタログのサイト アセットにアプリ アイコンの 96 x 96 ピクセルの画像を追加します。 たとえば、[サイトのコンテンツ] ドロップダウン メニューで [サイトコンテンツ] 設定を選択し、[サイトアセット] を選択し、次にquickStatusApp.png `https://ServerName/sites/TestApps` します。    **quickStatusApp アイテムを右クリック** し、[プロパティ]**を選択し**、[プロパティ] ダイアログ ボックスでアドレス **(URL)** の値 **を** コピーします。 たとえば、アイコンの URL Web アドレス フィールドに値を `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png` コピーして貼り付けます。  アイコンの説明 (図 9 のように) を入力し、「QuickStatus アプリ アイコン」と入力します。 URL が有効なテストを行います。
    
      **図 9.QuickStatus アプリのアイコン URL の追加**

      ![SharePoint でのアプリのプロパティの設定](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "SharePoint でのアプリのプロパティの設定")
  
   4. **[カテゴリ** ] フィールド: 既存のカテゴリを選択するか、独自の値を指定します。 たとえば、「Statusing」と入力します。
    
      > [!NOTE]
      > Statusing という **名前のカテゴリ** は、テスト目的のためだけのカテゴリです。 サーバー アプリの一般的なProjectは、[管理 **Projectです**。 
  
   5. **Publisher名フィールド**: 発行元の名前を入力します。 この例では、「SDK」とProjectします。
    
   6. **[有効**] フィールド: アプリをサイト管理者がインストールProject Web App表示するには、[有効] チェック **ボックスを** オンにします。 
    
   7. 追加のフィールドはオプションです。 たとえば、アプリの詳細ページにサポート URL と複数のヘルプ イメージを追加できます。 図 9 では、[ **画像 URL 1]** フィールドには、アプリのスクリーンショットの URL とスクリーンショットの説明が含まれています。 
    
   8. [アプリの **保存SharePoint - QuickStatus.app]** ダイアログ ボックスで、[保存] を **選択します**。 図 9 では、[SharePoint 用アプリ] ライブラリの [クイック状態更新] アイテムが編集用にチェックアウトされているので、ダイアログ ボックス リボンの[**編集**] タブで [チェックイン] を選択してプロセスを完了します (図 10 を参照)。 
    
      **図 10.QuickStatus アプリは、アプリ ライブラリ用アプリにSharePointされます。**

      ![SharePoint への QuickStatus アプリの追加](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "SharePoint への QuickStatus アプリの追加")
  
9. [Project Web App] ドロップダウン **設定で**、[アプリの追加 **] を選択します**。 [アプリ] ページの [クイック起動]で、[組織から] を選択し、[クイック状態更新] アプリの [アプリの詳細 **] を選択** します。 図 11 は、前の手順で追加したアプリ アイコン、スクリーンショット、その他の情報を含む詳細ページを示しています。 
    
   **図 11.クイック ステータス更新の詳細ページを使用Project Web App**

   ![Project Web App への QuickStatus アプリの追加](media/pj15_CreateStatusingApp_AddAppToPWA.gif "Project Web App への QuickStatus アプリの追加")
  
10. [クイック 状態の更新] 詳細ページで、[IT の追加 **] を選択します**。 Project Web App QuickStatus アプリで実行できる操作を一覧表示するダイアログ ボックスが表示されます (図 12 を参照)。 操作の一覧は、アプリケーション ファイル内の **AppPermissionRequest** 要素からAppManifest.xmlされます。 
    
    **図 12.クイック 状態アプリを信頼する確認**

    ![QuickStatus アプリへの信頼の検証](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "QuickStatus アプリへの信頼の検証")
  
11. [クイック 状態 **の更新を信頼する** ] ダイアログ ボックスで、[信頼する] **を選択します**。 アプリが [サイト コンテンツ] ページProject Web App追加されます (図 13 を参照)。
    
    **図 13.[サイト コンテンツ] ページでクイック 状態アプリを表示する**

    ![[サイト コンテンツ] に表示される QuickStatus アプリ](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "[サイト コンテンツ] に表示される QuickStatus アプリ")
  
[サイト コンテンツ] ページで、[クイック状態更新] アイコンを **選択して** アプリを実行できます。

> [!NOTE]
> アプリに関する情報を提供する追加のコマンドについては、[サイト コンテンツ] ページで、クイック状態更新名と省略記号 (...) を含む領域を選択します。アプリの [概要] ページを確認したり、アプリのエラーに関する情報を含む [アプリの詳細] ページを表示したり、アプリのアクセス許可ページを確認したり、アプリをアプリから削除Project Web App。 
  
[タスク] ページProject Web App (図 14 を参照)、リボンで **[QuickStatus]** ボタンを有効にする必要があります。 [クイック **状態] ボタンが** 無効になっている場合は、図 7 のメモに記載されている操作を試してください。 

**図 14.[タスク] タブから QuickStatus アプリを起動する**

![[タスク] タブから QuickStatus アプリを起動](media/pj15_CreateStatusingApp_TasksRibbon.gif "[タスク] タブから QuickStatus アプリを起動")
  
手順 6 は、QuickStatus アプリで行うテストを示しています。

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>QuickStatus アプリのテスト

ユーザーが **QuickStatus** アプリで試す可能性があるすべての操作は、運用サーバーまたは Project Online の運用テナントにアプリを展開する前に、Project Server のテスト インストールでテストする必要があります。 テスト インストールを使用すると、実際のプロジェクトに影響を与えることなく、ユーザーの割り当てを変更および削除できます。 テストには、管理者、プロジェクト マネージャー、チーム メンバーなど、さまざまなアクセス許可セットを持つ複数のユーザーも含まれる必要があります。 完全なテストでは、開発中のテストでは明らかではない、アプリで行う必要がある変更を明らかにできます。 手順 6 では **、QuickStatus** アプリのいくつかのテストを示しますが、網羅的な一連のテストは含めではありません。 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>手順 6. QuickStatus アプリをテストするには

1. ユーザーに **割り当てがない QuickStatus** アプリを実行します。 アプリは、ページの下部に青いメッセージを表示する必要があります 。たとえば、ユーザー名には割り当 **てはありません**。
    
   [ **更新] を** 選択し、緑色の割り当てに対する **メッセージの変更が更新されました**。
    
   > [!NOTE]
   > 割り当てがない場合は、[ **更新** ] ボタンが無効になっていない場合は、アプリの動作を変更する必要があります。 
  
2. ユーザーが複数の異なるプロジェクトに複数の割り当てを持ち、一部の割り当てが完了していないアプリを実行します。 アプリの外観に注意し、次のようにアクションを実行します (図 15 を参照)。
    
   1. **onGetAssignmentsSuccess 関数** は、現在のユーザーの割り当てごとにテーブル内に行を作成します。 プロジェクト名は、各プロジェクトの最初の割り当てに対して、太字のフォントで 1 回だけ表示されます。 
    
   2. [タスク名] 列ヘッダーの **チェック ボックスを** オフにします。 テーブル ヘッダークリック イベント ハンドラーは、タスク行の他のすべてのチェック ボックスをクリアします。 
    
   3. すべてのタスクを選択します。 各行の click イベント ハンドラーは、すべての行を選択するかどうかを決定し、選択した場合は[タスク名] 列ヘッダー **を** 選択します。 
    
   4. もう一度すべてのチェック ボックスをオフにし、残りの作業時間がある割り当てを 1 つ選択します。 たとえば、図 15 は、完了する残りの作業時間が 20% のトップ タスク T1 を示しています。
    
   5. [完了 **率の設定] テキスト** ボックスに「80」と入力し、[更新] を **選択します**。 ページの下部に緑色のメッセージが表示されます。 **割り当てが更新されています**。
    
      **図 15.QuickStatus アプリでの割り当ての更新**

      ![QuickStatus アプリでの割り当ての更新](media/pj15_CreateStatusingApp_Testing1Update.gif "QuickStatus アプリでの割り当ての更新")
  
3. [ **更新] を** 選択します (図 16 を参照)。 すべてのタスクが再度選択され、トップ タスクに 80% 完了が表示されます。 
    
      **図 16.[クイック 状態の更新] ページの更新**

      ![QuickStatus ページの更新](media/pj15_CreateStatusingApp_Testing2Refresh.gif "QuickStatus ページの更新")
  
4. すべてのチェック ボックスをオフにし、別のタスクを選択します。 たとえば、[タスク] から **[新しいタスク] をPWA。** [ **完了率の設定] テキスト** ボックスを空のままにし、選択したタスクの **[** 完了率] 列のすべてのテキストを削除し、[更新] を **選択します**。 両方のテキスト ボックスが空なので、アプリには赤いエラー メッセージが表示されます (図 17 を参照)。
    
      **図 17.エラー メッセージのテスト**

      ![エラー メッセージのテスト](media/pj15_CreateStatusingApp_Testing3Error.gif "エラー メッセージのテスト")
  
5. 前のタスクを 80% 完了に更新し、[終了] を **選択します**。 **exitToPwa** 関数は、ブラウザー ウィンドウの場所を、SharePoint ホスト アプリケーションの [タスク] ページに変更します (つまり、URL はに変更されます https://ServerName/pwa/Tasks.aspx) )。 図 18 は **、T1** タスクと新しいタスクがそれぞれ 80%**完了** PWA示しています。 
    
      **図 18.タスクが更新されるのを確認するには、Project Web App**

      ![Project Web App で更新されたタスクを確認](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Project Web App で更新されたタスクを確認")
  
6. 更新された状態が 2013 年 2013 年Project Professionalに表示される前に、変更を承認のために提出し、プロジェクト マネージャーによって承認する必要があります。
    
テストでは、使いやすさを向上させる目的で **QuickStatus** アプリで行う必要がある他のいくつかの変更が明らかです。 以下に例を示します。

- テキスト ボックス値の追加のエラー チェックと検証が必要です。 現在、ユーザーは完全率に対して数値以外の値または負の値を入力できます。その結果、エラー メッセージが表示されます。 たとえば、負の値を指定すると、エラー メッセージはエラー更新の割り当て **: PJClientCallableException: StatusingSetDataValueInvalid です**。
    
- 空白のテキスト ボックスのエラー メッセージには、行番号に加えて、プロジェクトとタスクが一覧表示される可能性があります。
    
- 成功メッセージには、更新されたタスクの一覧が含まれる場合があります。 **updateAssignments** 関数が成功した場合は、ページの自動更新を実行し、更新されたタスクまたはパーセンテージを別の色と太字のフォントで表示できます。 
    
- 非常に大きなテーブルを回避するには、割り当てのテーブルを 100% 未満のタスクに制限する必要があります。 または、すべてのタスクを表示するオプションを追加します。 この問題は、テーブルの代わりに jQuery ベースのグリッドを使用して解決することもできます。これにより、フィルター処理とグリッド ページングを簡単に実装できます。
    
- **QuickStatus** アプリは状態を送信しないので、リボンの [**タスク**] タブの [クイック状態] アイコンは、送信グループの最後のアイコンではなく、タスク グループの最初のアイコンになります。 
    
- **onGetAssignmentsSuccess** 関数は **btnSubmitUpdate** ボタン テキストを初期化しますが、他のボタンテキスト値は HTML で初期化されます **。getAssignments** 関数の実行中、ページは部分的に初期化された状態で残ります。 テキスト値がすべて HTML で初期化されている場合、ページ上のボタンの一貫性が高く表示されます。 
    
最も重要なのは **、QuickStatus** アプリが使用するアプローチであり、割り当ての完了率が変更される場合は、実稼働アプリで修正する必要があります。 詳細については、「次の手順 [」セクションを参照](#pj15_StatusingApp_NextSteps) してください。 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>QuickStatus アプリのコード例

### <a name="defaultaspx-file"></a>Default.aspx ファイル

次のコードは  `Pages\Default.aspx` **、QuickStatus プロジェクトのファイルに含** まれます。 
  
```HTML
    <%-- The following lines are ASP.NET directives needed when using SharePoint components --%>
    <%@ Page Inherits="Microsoft.SharePoint.WebPartPages.WebPartPage, Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" MasterPageFile="~masterurl/default.master" Language="C#" %>
    <%@ Register TagPrefix="Utilities" Namespace="Microsoft.SharePoint.Utilities" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="WebPartPages" Namespace="Microsoft.SharePoint.WebPartPages" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%@ Register TagPrefix="SharePoint" Namespace="Microsoft.SharePoint.WebControls" Assembly="Microsoft.SharePoint, Version=15.0.0.0, 
    Culture=neutral, PublicKeyToken=71e9bce111e9429c" %>
    <%-- The markup and script in the following Content element will be placed in the <head> of the page.
        For production deployment, change the .debug.js JavaScript references to .js. --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">
    <script type="text/javascript" src="../Scripts/jquery-1.7.1.min.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.runtime.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/sp.debug.js"></script>
    <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
    <!-- CSS styles -->
    <link rel="Stylesheet" type="text/css" href="../Content/App.css" />
    <!-- Add your JavaScript to the following file -->
    <script type="text/javascript" src="../Scripts/App.js"></script>
    </asp:Content>
    <%-- The markup and script in the following Content element will be placed in the <body> of the page --%>
    <asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">
    <form>
        <fieldset>
        <legend>Select assigned tasks</legend>
        <table id="assignmentsTable">
            <caption id="tableCaption">Replace caption</caption>
            <thead>
            <tr id="headerRow">
                <th>Project name</th>
                <th><input type="checkbox" id="headercheckbox" checked="checked" />Task name</th>
                <th>Actual work</th>
                <th>% complete</th>
                <th>Remaining work</th>
                <th>Due date</th>
            </tr>
            </thead>
        </table>
        </fieldset>
        <div id="inputPercentComplete" >
        Set percent complete for all selected assignments, or leave this
        <br /> field blank and set percent complete for individual assignments: 
        <input type="text" name="percentComplete" id="pctComplete" size="4"  maxlength="4" />
        </div>
        <div id="submitResult">
        <p><button id="btnSubmitUpdate" type="button" class="bottomButtons" ></button></p>
        <p id="message"></p>
        </div>
        <div id="refreshPage">
        <p><button id="btnRefresh" type="button" class="bottomButtons" >Refresh</button></p>
        </div>
    <div id="exitPage">
        <p><button id="btnExit" type="button" class="bottomButtons" >Exit</button></p>
    </div>
    </form>
    </asp:Content>
```

<br/>

### <a name="appjs-file"></a>App.js ファイル

次のコードは  `Scripts\App.js` **、QuickStatus プロジェクトのファイルに含** まれます。 
  
```js
    var projContext;
    var pwaWeb;
    var projUser;
    // This code runs when the DOM is ready and creates a ProjectContext object.
    // The ProjectContext object is required to use the JSOM for Project Server.
    $(document).ready(function () {
        projContext = PS.ProjectContext.get_current();
        pwaWeb = projContext.get_web();
        getUserInfo();
        getAssignments();
        // Bind a click event handler to the table header check box, which sets the row check boxes
        // to the selected state of the header check box, and sets the results message to an empty string.
        $('#headercheckbox').live('click', function (event) {
            $('input:checkbox:not(#headercheckbox)').attr('checked', this.checked);
            $get("message").innerText = "";
        });
        // Bind a click event handler to the row check boxes. If any row check box is cleared, clear
        // the header check box. If all of the row check boxes are selected, select the header check box.
        $('input:checkbox:not(#headercheckbox)').live('click', function (event) {
            var isChecked = true;
            $('input:checkbox:not(#headercheckbox)').each(function () {
                if (this.checked == false) isChecked = false;
                $get("message").innerText = "";
            });
            $("#headercheckbox").attr('checked', isChecked);
        });
    });
    // Get information about the current user.
    function getUserInfo() {
        projUser = pwaWeb.get_currentUser();
        projContext.load(projUser);
        projContext.executeQueryAsync(onGetUserNameSuccess,
            // Anonymous function to execute if getUserInfo fails.
            function (sender, args) {
                alert('Failed to get user name. Error: ' + args.get_message());
        });
    }
    // This function is executed if the getUserInfo call is successful.
    // Replace the contents of the 'caption' paragraph with the project user name.
    function onGetUserNameSuccess() {
        var prefaceInfo = 'Assignments for ' + projUser.get_title();
        $('#tableCaption').text(prefaceInfo);
    }
    // Get the collection of assignments for the current user.
    function getAssignments() {
        assignments = PS.EnterpriseResource.getSelf(projContext).get_assignments();
        // Register the request that you want to run on the server. The optional "Include" parameter 
        // requests only the specified properties for each assignment in the collection.
        projContext.load(assignments,
            'Include(Project, Name, ActualWork, ActualWorkMilliseconds, PercentComplete, RemainingWork, Finish, Task)');
        // Run the request on the server.
        projContext.executeQueryAsync(onGetAssignmentsSuccess,
            // Anonymous function to execute if getAssignments fails.
            function (sender, args) {
                alert('Failed to get assignments. Error: ' + args.get_message());
            });
    }
    // Get the enumerator, iterate through the assignment collection, 
    // and add each assignment to the table.
    function onGetAssignmentsSuccess(sender, args) {
        if (assignments.get_count() > 0) {
            var assignmentsEnumerator = assignments.getEnumerator();
            var projName = "";
            var prevProjName = "3D2A8045-4920-4B31-B3E7-9D0C5195FC70"; // Any unique name.
            var taskNum = 0;
            var chkTask = "";
            var txtPctComplete = "";
            // Constants for creating input controls in the table.
            var INPUTCHK = '<input type="checkbox" class="chkTask" checked="checked" id="chk';
            var LBLCHK = '<label for="chk';
            var INPUTTXT = '<input type="text" size="4"  maxlength="4" class="txtPctComplete" id="txt';
            while (assignmentsEnumerator.moveNext()) {
                var statusAssignment = assignmentsEnumerator.get_current();
                projName = statusAssignment.get_project().get_name();
                // Get an integer value for the number of milliseconds of actual work, such as 3600000.
                var actualWorkMilliseconds = statusAssignment.get_actualWorkMilliseconds();
                // Get a string value for the assignment actual work, such as "1h". Not used here.
                var actualWork = statusAssignment.get_actualWork();                         
                if (projName === prevProjName) {
                    projName = "";
                }
                prevProjName = statusAssignment.get_project().get_name();
                // Create a row for the assignment information.
                var row = assignmentsTable.insertRow();
                taskNum++;
                // Create an HTML string with a check box and task name label, for example:
                //     <input type="checkbox" class="chkTask" checked="checked" id="chk1" /> 
                //     <label for="chk1">Task 1</label>
                chkTask = INPUTCHK + taskNum + '" /> ' + LBLCHK + taskNum + '">'
                    + statusAssignment.get_name() + '</label>';
                txtPctComplete = INPUTTXT + taskNum + '" />';
                // Insert cells for the assignment properties.
                row.insertCell().innerHTML = '<strong>' + projName + '</strong>';
                row.insertCell().innerHTML = chkTask;
                row.insertCell().innerText = actualWorkMilliseconds / 3600000 + 'h';
                row.insertCell().innerHTML = txtPctComplete;
                row.insertCell().innerText = statusAssignment.get_remainingWork();
                row.insertCell().innerText = statusAssignment.get_finish();
                // Initialize the percent complete cell.
                $get("txt" + taskNum).innerText = statusAssignment.get_percentComplete() + '%'
            }
        }
        else {
            $('p#message').attr('style', 'color: #0f3fdb');     // Blue text.
            $get("message").innerText = projUser.get_title() + ' has no assignments'
        }
        // Initialize the button properties.
        $get("btnSubmitUpdate").onclick = function() { updateAssignments(); };
        $get("btnSubmitUpdate").innerText = 'Update';
        $get('btnRefresh').onclick = function () { window.location.reload(true); };
        $get('btnExit').onclick = function () { exitToPwa(); };
    }
    // Update all selected assignments. If the bottom percent complete field is blank,
    // use the value in the % complete field of each selected row in the table.
    function updateAssignments() {
        // Get percent complete from the bottom text box.
        var pctCompleteMain = getNumericValue($('#pctComplete').val()).trim();
        var pctComplete = pctCompleteMain;
        var assignmentsEnumerator = assignments.getEnumerator();
        var taskNum = 0;
        var taskRow = "";
        var indexPercent = "";
        var doSubmit = true;
        while (assignmentsEnumerator.moveNext()) {
            var pctCompleteRow = "";
            taskRow = "chk" + ++taskNum;
            if ($get(taskRow).checked) {
                var statusAssignment = assignmentsEnumerator.get_current();
                if (pctCompleteMain === "") {
                    // Get percent complete from the text box field in the table row.
                    pctCompleteRow = getNumericValue($('#txt' + taskNum).val());
                    pctComplete = pctCompleteRow;
                }
                // If both percent complete fields are empty, show an error.
                if (pctCompleteMain === "" && pctCompleteRow === "") {
                    $('p#message').attr('style', 'color: #e11500');     // Red text.
                    $get("message").innerHTML =
                        '<b>Error:</b> Both <i>Percent complete</i> fields are empty, in row '
                        + taskNum
                        + ' and in the bottom textbox.<br/>One of those fields must have a valid percent.'
                        + '<p>Please refresh the page and try again.</p>';
                    doSubmit = false;
                    taskNum = 0;
                    break;
                }
                if (doSubmit) statusAssignment.set_percentComplete(pctComplete);
            }
        } 
        // Save and submit the assignment updates.
        if (doSubmit) {
            assignments.update();
            assignments.submitAllStatusUpdates();
            projContext.executeQueryAsync(function (source, args) {
                $('p#message').attr('style', 'color: #0faa0d');     // Green text.
                $get("message").innerText = 'Assignments have been updated.';
            }, function (source, args) {
                $('p#message').attr('style', 'color: #e11500');     // Red text.
                $get("message").innerText = 'Error updating assignments: ' + args.get_message();
            });
        }
    }
    // Get the numeric part for percent complete, from a string. 
    // For example, with "20 %", return "20".
    function getNumericValue(pctComplete) {
        pctComplete = pctComplete.trim();
        pctComplete = pctComplete.replace(/ /g, "");    // Remove interior spaces.
        indexPercent = pctComplete.indexOf('%', 0);
        if (indexPercent > -1) pctComplete = pctComplete.substring(0, indexPercent);
        return pctComplete;
    }
    // Exit the QuickStatus page and go back to the Tasks page in Project Web App.
    function exitToPwa() {
        // Get the SharePoint host URL, which is the top page of PWA, and add the Tasks page.
        var spHostUrl = decodeURIComponent(getQueryStringParameter('SPHostUrl'))
                        + "/Tasks.aspx";
        // Set the top window for the QuickStatus IFrame to the Tasks page.
        window.top.location.href = spHostUrl;
    }
    // Get a specified query string parameter from the {StandardTokens} URL option string.
    function getQueryStringParameter(urlParameterKey) {
        var docUrl = document.URL;
        var params = docUrl.split('?')[1].split('&');
        for (var i = 0; i < params.length; i++) {
            var theParam = params[i].split('=');
            if (theParam[0] == urlParameterKey)
                return decodeURIComponent(theParam[1]);
        }
    }
```

<br/>

### <a name="appcss-file"></a>App.css ファイル

次の CSS コードは  `Content\App.css` **、QuickStatus プロジェクトのファイルに含** まれます。 
  
```css
    /* Custom styles for the QuickStatus app. */
    /*============= Table elements ========================================*/
    table {
        width: 90%;
    }
    caption {
        font-size: 16px;
        padding-bottom: 5px;
        font-weight: bold;
        color: gray;
    }
    table th {
        background-color: gray;
        color: white;
    }
    table td, th {
        width: auto;
        text-align: left;
        padding: 2px;
        border: solid 1px whitesmoke;
        color: gray;
    }
    /*=== Class for check boxes added to rows 
    */
    .chkTask {
        width: 12px;
        height: 12px;
        color: gray;
    }
    /*========== DIV id for the Percent Complete text box ================*/
    #inputPercentComplete {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 20px;
        margin-left: 30px;
    }
    /*========== DIV id for the Submit Result button ====================*/
    #submitResult {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
    }
    /*========== DIV id for the Refresh Page button ====================*/
    #refreshPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 120px;
    }
    /*========== DIV id for the Exit Page button ====================*/
    #exitPage {
        position: fixed;
        top: auto;
        height: auto;
        padding-top: 60px;
        margin-left: 240px;
    }
    /*========== Class for the buttons at the bottom of the page =======*/
    .bottomButtons {
        color: gray;
        font-weight: bold; 
        font-size: 12px; 
        border-color: darkgreen;
        border-width: thin;
    }
```

<br/>

### <a name="elementsxml-file-for-the-ribbon"></a>Elements.xmlのファイル

リボンの [タスク] タブの追加されたボタンの次の XML 定義は `RibbonQuickStatusAction\Elements.xml` **、QuickStatus プロジェクトのファイルにあります**。 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="http://schemas.microsoft.com/sharepoint/">
    <CustomAction Id="21ea3aaf-79e5-4aac-9479-8eef14b4d9df.RibbonQuickStatusAction"
                    Location="CommandUI.Ribbon">
        <CommandUIExtension>
        <!-- 
        Add a button that invokes the QuickStatus app. The Quick Status button is displayed as  
        the third control in the Page group (the group title is "Submit").
        -->
        <CommandUIDefinitions>
            <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
            <Button Id="Ribbon.ContextualTabs.MyWork.Home.Page.QuickStatus"
                    Alt="Quick Status app"
                    Sequence="30"
                    Command="Invokae_QuickStatus"
                    LabelText="Quick Status"
                    TemplateAlias="o1"
                    Image16by16="_layouts/15/1033/images/ps16x16.png" 
                    Image16by16Left="-80"
                    Image16by16Top="-144"
                    Image32by32="_layouts/15/1033/images/ps32x32.png" 
                    Image32by32Left="-32"
                    Image32by32Top="-288" 
                    ToolTipTitle="Quick Status"
                    ToolTipDescription="Run the QuickStatus app" />
            </CommandUIDefinition>
        </CommandUIDefinitions>
        <CommandUIHandlers>
            <CommandUIHandler Command="Invoke_QuickStatus"
                            CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
        </CommandUIHandlers>
        </CommandUIExtension >
    </CustomAction>
    </Elements>
```

<br/>

### <a name="appmanifestxml-file"></a>AppManifest.xml ファイル

**QuickStatus** プロジェクトのアプリ マニフェストの XML を次に示します。これには、複数のプロジェクトでアプリ ユーザーの割り当て状態を更新するために必要な 2 つのアクセス許可要求スコープが含まれます。 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="http://schemas.microsoft.com/sharepoint/2012/app/manifest"
        Name="QuickStatus"
        ProductID="{bbc497e7-1221-4d7b-a0ae-141a99546008}"
        Version="1.0.0.0"
        SharePointMinVersion="15.0.0.0"
    >
    <Properties>
        <Title>Quick Status Update</Title>
        <StartPage>~appWebUrl/Pages/Default.aspx?{StandardTokens}</StartPage>
    </Properties>
    <AppPrincipal>
        <Internal />
    </AppPrincipal>
    <AppPermissionRequests>
        <AppPermissionRequest Scope="https://sharepoint/projectserver/statusing" Right="SubmitStatus" />
        <AppPermissionRequest Scope="https://sharepoint/projectserver/projects" Right="Read" />
    </AppPermissionRequests>
    </App>
```

<br/>

### <a name="appiconpng-file"></a>AppIcon.png ファイル

**QuickStatus** Visual Studioの完全なソリューションには、カスタム ファイルAppIcon.pngがあります。 ソリューションは、2013 SDK Projectに含まれます。 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>次の手順

**QuickStatus アプリは**、サーバー 2013 およびサーバー 2013 にインストールできるアプリを作成する方法の比較的簡単なProject例Project Online。 [[QuickStatus アプリのテスト] セクション](#pj15_StatusingApp_Testing)には、使いやすさを向上できるいくつかの改善点が示されています。 **QuickStatus アプリは** JavaScript 関数を使用して、ユーザーの割り当て状態を更新Project Web App。 ただし、割り当ての完了率を変更する方法は、推奨されるプロジェクト管理プラクティスではありません。 もう 1 つの方法は、割り当てられたタスクの実際の開始日と残りの期間を更新する方法です。 問題の詳細については、MPUG ニュースレターの [「Update Better」](https://www.mpug.com/articles/update-better) を参照してください。 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>関連項目

- [Project Server のプログラミング タスク](project-programming-tasks.md)
- [SharePoint アドイン](https://msdn.microsoft.com/library/jj163230.aspx)
- [Project Web App でタスク更新を管理する](https://technet.microsoft.com/library/hh767481%28v=office.14%29.aspx)
- [カスタム アクションを作成して SharePoint アドインで展開する](https://msdn.microsoft.com/library/jj163954.aspx)
    

