---
title: SharePoint をホストとする Project Server アドインを作成する
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: bb9c3c00-7121-41e1-9db3-75550d040ba8
description: 3 種類のアプリケーションのオンライン プロジェクト (autohosted、プロバイダーによってホストされ、SharePoint でホストされている) を作成することができる SharePoint によってホストされるアプリケーションの作成および展開する最も簡単です。
ms.openlocfilehash: 7a74f5b3b848f3fa238051f5b9f9f563c38417b2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399586"
---
# <a name="create-a-sharepoint-hosted-project-server-add-in"></a>SharePoint をホストとする Project Server アドインを作成する

3 種類のアプリケーションのオンライン プロジェクト (autohosted、プロバイダーによってホストされ、SharePoint でホストされている) を作成することができる SharePoint によってホストされるアプリケーションの作成および展開する最も簡単です。 SharePoint によってホストされるアプリケーションは、OAuth 認証を必要とは Azure を使用して、やではなくプロバイダーでホストされているリソースのローカル サイトのメンテナンスを必要とします。 Visual Studio で**SharePoint 2013 のアプリケーション**テンプレートは、発行し、Office ストアで販売または SharePoint 上のプライベート アプリケーション カタログに配置できるアプリケーションを開発するための便利なフレームワークです。 
  
プロジェクトでは、状態管理とは、チーム メンバーことができますを使用してタスク] ページで、Project Web App で費やされたタスクの作業週の各曜日の就業時間の数など、割り当てられたタスクのステータスを送信するプロセス。 割り当て所有者 (通常はプロジェクト マネージャー) では、承認したり、ステータスを拒否することができます。 ステータスが承認されると、プロジェクトには、スケジュールが再計算されます。 **QuickStatus**アプリケーションでは、割り当てられたタスク、ユーザーは迅速に達成率を更新、承認のための選択した割り当ての状態を送信する場所を表示します。 Project Web App の [タスク] ページには、多くの機能が、 **QuickStatus**アプリケーションは、シンプルなインターフェイスを提供する例です。 
  
**QuickStatus**アプリケーションは、開発者のためのサンプル実稼働環境で使用するためのものではありません。 主な目的では、プロジェクト オンライン、完全に機能の状態を管理アプリケーションを作成しないようにアプリケーション開発の例を示します。 状態管理により、[次のステップ](#pj15_StatusingApp_NextSteps)の推奨事項を参照してください。
  
状態管理に関する一般的な情報は、[タスクの進捗状況](https://support.office.com/article/Find-information-about-Project-Server-2013-8b08a414-15a7-4076-b2db-c90d0214ea7f?ui=en-US&rs=en-US&ad=US#BKMK_TaskProgress)を参照してください。 Project Server の SharePoint 用のアドインを開発する方法の詳細については、 [SharePoint のアドイン](https://msdn.microsoft.com/library/jj163230.aspx)を参照してください。

<a name="pj15_StatusingApp_Prerequisites"> </a>

## <a name="prerequisites-for-creating-an-app-for-project-server-2013"></a>Project Server 2013 のアプリケーションを作成するための前提条件

オンライン プロジェクトを Project Server 2013 の設置型インストールに展開できる比較的単純なアプリケーションを開発するには、オンラインの開発環境を提供する、Napa 使用できます。 Project Web App のリボンと、開発時のデバッグを容易に変更することのより複雑なアプリケーションは、Visual Studio 2012 のまたは Visual Studio の 2013 を使用することができます。 たとえば、オンプレミスのインストールは、下書きデータ テーブルの変更を Project Server データベース内を手動で確認できます。 この資料では、Visual Studio でアプリケーション開発を行う方法を説明します。
  
Visual Studio でプロジェクトのサーバー アプリケーションの開発には、次の必要があります。
  
- 使用するローカルの開発用コンピューターに最新のサービス パックと Windows 更新プログラムをインストールしてあることを確認します。オペレーティング システムは、Windows 7、Windows 8、Windows Server 2008、Windows Server 2012 のいずれでもかまいません。
    
- SharePoint Server 2013 と Project Server 2013 をインストールすると、アプリケーションの分離とアプリケーションの sideloading のコンピューターに構成されているコンピューターが必要です。 Sideloading は、一時的にデバッグするようにアプリケーションをインストールするのには Visual Studio を使用できます。 Project Server の SharePoint の設置型インストールを使用することができます。 詳細については、 [SharePoint のアプリケーションの設置型開発環境のセットアップ](https://msdn.microsoft.com/library/fp179923%28Office.15%29.aspx)を参照してください。
    
   > [!NOTE]
   > 設置型インストールを分離されたアプリケーション ドメイン*の前に*企業アプリケーションのカタログを作成するを構成します。 
  
- 開発用コンピューターにインストールされている Visual Studio 2012 の Office 開発ツールにはリモート コンピューターができます。 最新のバージョンがインストールされていることを確認します。[Office および SharePoint 用アプリをダウンロード](https://msdn.microsoft.com/office/apps/fp123627.aspx)するは、"*ツール*"を参照してください。
    
- Project Web App インスタンスを使用する開発用のテストは、ブラウザーでアクセスできることを確認します。
    
オンライン ツールを使用する方法の詳細については、 [Office 365 で SharePoint 用アプリの開発環境の設定](https://msdn.microsoft.com/library/fp161179.aspx)を参照してください。 オンライン ツールを使用する Project Server の単純なアプリケーションの構築のチュートリアルは、EPMSource のブログ シリーズは、[最初、プロジェクトのサーバー アプリケーションを構築する](https://epmsource.com/2012/11/20/building-your-first-project-server-app-part-zerothe-introduction/)を参照してください。

<a name="pj15_StatusingApp_UsingVisualStudio"> </a>

## <a name="using-visual-studio-to-create-a-project-server-app"></a>Visual Studio を使用して Project Server アプリケーションを作成するには

Visual Studio 2012 ののための Office 開発ツールには、Project Server 2013 で使用できる SharePoint アプリケーションのテンプレートが含まれています。 アプリケーション ソリューションを作成するときに、ソリューションには、カスタム コードに次のファイルが含まれています。
  
- **AppManifest.xml**には、アプリケーションのタイトル、アクセス許可要求のスコープ、およびその他のプロパティの設定が含まれています。 手順 1 では、マニフェスト デザイナーを使用してプロパティを設定する手順が含まれています。 
    
- ページのフォルダーには、 **Default.aspx**は、アプリケーションのメイン ページです。 手順 2 では、 **QuickStatus**アプリケーションに HTML5 のコンテンツを追加する方法を説明します。 
    
- **App.js**を [スクリプト] フォルダーは、カスタムの JavaScript コードのプライマリ ファイルです。 手順 3 では、 **QuickStatus**アプリケーションの JavaScript コードについて説明します。 
    
   JQuery ベースのグリッドまたは日付の選択などの商用のコントロールを追加する場合は、Default.aspx ファイルに追加の JavaScript ファイルへの参照を追加できます。
    
- コンテンツ フォルダー内の**App.css**は、CSS3 のユーザー設定のスタイルの主要なファイルです。 手順 2 と手順 3 には、 **QuickStatus**アプリケーション用のカスケード スタイル シート (CSS) スタイルに関する情報が含まれます。 Default.aspx ファイルに追加の CSS ファイルへの参照を追加できます。 
    
- [Images] フォルダー内の**AppIcon.png**は、アプリを Office ストアまたはアプリケーションのカタログに表示する 96 x 96 のアイコンです。 
    
Project Web App のリボンを変更するには、リボンのカスタム アクションを追加できます。 [QuickStatus アプリケーションのサンプル コード](#pj15_StatusingApp_Example)のセクションには、更新の Default.aspx、App.js、App.css、Elements.xml を AppManifest.xml ファイルの完全なコードが含まれています。 
  
### <a name="procedure-1-to-create-an-app-project-in-visual-studio"></a>手順 1. Visual Studio でアプリケーション プロジェクトを作成するには

1. 管理者は、Visual Studio 2012 を実行し、[開始] ページで、**新しいプロジェクト**を選択します。 
    
2. **新しいプロジェクト**ダイアログ ボックスで、**テンプレート**、 **Visual C#**、および**Office または SharePoint**ノードを展開し、**アプリケーション**します。 上部 (図 1 を参照してください)、中央のウィンドウと [ **SharePoint 2013 のアプリケーション**のターゲット フレームワーク ドロップダウン リストで既定の **.NET Framework 4.5**を使用します。 
    
3. [**名**] フィールドで、QuickStatus を入力するアプリケーションを保存し、 **[ok]** を選択し、場所を参照します。
    
   **図 1 です。プロジェクトを作成する Visual Studio のサーバー アプリケーション**

   ![プロジェクトを作成するサーバー アプリケーションを Visual Studio で](media/pj15_CreateStatusingApp_NewProject.gif "プロジェクトを作成するサーバー アプリケーションを Visual Studio で")
  
4. **SharePoint の新しいアプリケーション**] ダイアログ ボックスで、次の 3 つのフィールドに入力します。 
    
   - 上部のテキスト ボックスで、Project Web App で表示するアプリケーションの名前を入力します。 簡易ステータスの更新を入力します。
    
   - デバッグに使用するサイトでは、Project Web App インスタンスの URL を入力します。 たとえば、 `https://ServerName/ProjectServerName` (_サーバー名_と置き換える_ProjectServerName_独自の値)、[**検証**] を選択します。 すべてがうまくいけば、Visual Studio では**正常に接続**が表示されます。 エラー メッセージが表示される場合は、Project Web App の URL が正しいことと、アプリケーションの分離とアプリケーションの sideloading のプロジェクトのサーバー コンピューターが構成されているを確認します。 詳細については、 [Project Server 2013 のアプリケーションを作成するための前提条件](#pj15_StatusingApp_Prerequisites)」を参照してください。 
    
   - **SharePoint にアプリケーションをホストする方法**」ドロップ ダウン リスト、 **SharePoint でホストされている**を選択します。
    
   > [!CAUTION]
   > Visual Studio がソリューションの 2 つのプロジェクトを作成する**プロバイダーによってホストされる**既定のプロジェクトの種類を誤って選択した場合: **QuickStatus**プロジェクトと**QuickStatusWeb**プロジェクト。 2 つのプロジェクトを表示する場合は、そのソリューションの削除をやり直します。 
  
5. **QuickStatus**ソリューション、プロジェクトの**QuickStatus** 、および既定のファイルを作成するのには **[ok]** を選択します。 
    
6. マニフェストのデザイナー ビューを開きます (たとえば、AppManifest.xml ファイルをダブルクリックします)。 [**全般**] タブで、**タイトル**] テキスト ボックスは、手順 4 で入力したアプリケーション名を表示する必要があります。 アプリケーションの次のアクセス許可要求を追加するのには [**アクセス許可**] タブを選択 (図 2 を参照してください)。 
    
   - **アクセス許可の要求**] ボックスの一覧で、[**スコープ**] 列の最初の行では、ドロップ ダウン リストで**状態管理**を選択します。 [**アクセス許可**] 列には、 **SubmitStatus**を選択します。
    
   - **スコープ**は、**複数のプロジェクト****アクセス許可**は、**読み取り**の行を追加します。
    
   **図 2 になります。状態管理アプリケーションのアクセス許可のスコープを設定します。**

   ![状態管理アプリケーションのアクセス許可のスコープを設定します。](media/pj15_CreateStatusingApp_PermissionScope.gif "状態管理アプリケーションのアクセス許可のスコープを設定します。")
  
**QuickStatus**アプリケーションは、複数のプロジェクトからそのユーザーの割り当てを読み取り、割り当ての達成率を変更および更新プログラムを送信する Project Web App のユーザーを有効にします。 その他のアクセス許可要求スコープ ボックスの一覧を図 2 に示すようには、このアプリケーションに必要ではありません。 アクセス許可要求のスコープは、アプリケーションがユーザーの代わりに要求されるアクセス許可です。 ユーザーは、Project Web App でこれらのアクセス許可があるない、アプリケーションは実行されません。 アプリケーションなどその他の SharePoint アクセス許可レベルのアクセス許可要求の複数のスコープを持つことができますが、のみ、最低限必要なアプリケーション機能の必要があります。 Project Server に関連付けられているアクセス許可要求の範囲を以下に示します。 

- **エンタープライズ リソース**: リソース マネージャー アクセス許可の [その他の Project Web App のユーザーについての情報を読み書きします。
    
- **複数のプロジェクト**: 読み取りまたは書き込みを複数のプロジェクト、ユーザーが要求するアクセス許可を持っています。
    
- **Project Server**: アプリケーションのユーザーが Project Web App の管理者権限を持っている必要があります。
    
- **レポート**: (Project Web App にのみログオンのアクセス許可が必要です)、Project Web App の**ProjectData**の OData サービスを参照します。 
    
- **1 つのプロジェクト**: 読み取りまたは書き込みをユーザーが要求するアクセス許可を持っているプロジェクト。
    
- **状態管理**: 勤務時間、パーセント完了、および新規の割り当て、割り当ての状態の更新を送信します。
    
- **ワークフロー**: ワークフローのアクセス許可を引き上げてアプリケーションが実行されますユーザーが Project Server のワークフローを実行する権限を持っている場合。
    
Project Server 2013 のためのアクセス許可要求のスコープの詳細については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)と[SharePoint 2013 でのアプリケーションのアクセス許可](https://msdn.microsoft.com/library/fp142383.aspx)で*アプリケーションのプロジェクト*を参照してください。


<a name="pj15_StatusingApp_HTML"> </a>

### <a name="creating-the-html-content-for-the-quickstatus-app"></a>QuickStatus アプリケーションのコンテンツの HTML を作成します。

HTML コンテンツのコーディングを開始する前に、ユーザー インターフェイスと (図 3 では、完成したページの例を示しています)、QuickStatus アプリケーションのユーザー エクスペリエンスをデザインします。 設計では、HTML コードと対話する JavaScript 関数の概要を含めることも。 全般については、 [SharePoint 2013 でのアプリケーションのユーザー エクスペリエンスのデザイン](https://msdn.microsoft.com/library/fp179934.aspx)を参照してください。
  
**図 3 です。QuickStatus アプリケーション ページのデザイン**

![QuickStatus アプリケーション ページのデザイン](media/pj15_CreateStatusingApp_AfterRefresh.gif "QuickStatus アプリケーション ページのデザイン")
  
アプリケーションでは、AppManifest.xml に**Title**要素の値は、一番上に表示名を示しています。 
  
既定では、ページは、HTML5 を使用します。 以下は、 **QuickStatus**アプリケーションがページの本文に含まれているメインの UI オブジェクトの標準的な HTML 要素です。 
  
- **フォーム**要素には、すべての他の UI 要素が含まれています。 
    
- **Fieldset**要素のコンテナーとの割り当てのテーブルの枠線を作成します。**凡例**の子要素では、コンテナーのラベルを提供します。 
    
- **Table**要素には、キャプションとテーブル ヘッダーのみが含まれています。 JavaScript 関数は、テーブルのキャプションを変更し、割り当ての行を追加します。 
    
   > [!NOTE]
   > ページングと並べ替えを簡単に追加するに本番アプリケーションが可能性がありますを使用して、jQuery ベースの商用グリッド コントロール テーブルの代わりにします。 
  
   テーブルには、プロジェクト名、チェック ボックスをオン、実績作業時間、達成完了、残存作業時間のタスク名の列が含まれていて、割り当ての終了日。 JavaScript 関数を作成します] チェック ボックスとテキスト入力フィールド、% の各タスクの完了します。
    
- テキスト ボックスの**入力**要素は、選択されているすべての割り当ての完了率を設定します。 
    
- **ボタン**要素は、状態の変更を送信します。 
    
- **ボタン**要素は、ページを更新します。 
    
- **ボタン**要素は、アプリケーションを終了して、Project Web App の [タスク] ページに戻ります。 
    
下部のテキスト ボックスとボタン要素は、 **div**要素内では CSS 位置と、UI オブジェクトの外観を容易に管理できるようにします。 JavaScript 関数は、成功の結果が含まれるページの下部または状態の更新の失敗時に段落を追加します。 
  
### <a name="procedure-2-to-create-the-html-content"></a>手順 2. HTML のコンテンツを作成するには

1. Visual Studio は、Default.aspx ファイルを開きます。
    
   ファイルには、2 つの**asp: コンテンツ**要素が含まれています。: 要素を、 `ContentPlaceHolderID="PlaceHolderAdditionalPageHead"` 、ページ ヘッダー、および要素内で属性を追加、`ContentPlaceHolderID="PlaceHolderMain"`属性がページの**body**要素内に配置されます。 
    
2. `<asp:Content ContentPlaceHolderID="PlaceHolderAdditionalPageHead" runat="server">` 、ページ ヘッダーの制御、Project Server コンピューター上の PS.js ファイルへの参照を追加します。 テストとデバッグ、PS.debug.js を使用できます。 
    
   ```HTML
     <script type="text/javascript" src="/_layouts/15/ps.debug.js"></script>
   ```

   アプリケーション インフラストラクチャを使用して、`/_layouts/15/`仮想ディレクトリを IIS 内の SharePoint サイトです。 物理ファイルは、 `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\PS.debug.js`。
    
   > [!NOTE]
   > 運用環境で使用するようにアプリケーションを展開する前に削除`.debug`のパフォーマンスを向上させるためにスクリプト参照とします。 
  
3. `<asp:Content ContentPlaceHolderID="PlaceHolderMain" runat="server">`ページ本体の制御、生成された**div**要素を削除して、UI オブジェクトの HTML コードを追加します。 **Table**要素には、ヘッダー行のみが含まれています。 **タスク名**] 列には、チェック ボックスの入力コントロールが含まれています。 **キャプション**要素のテキストは、 **onGetUserNameSuccess**コールバックに**getUserInfo**関数に置き換えられます。 
    
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

4. App.css ファイル内の位置と UI 要素の外観の CSS コードを追加します。 **QuickStatus**アプリケーションの完全な CSS コードは、 [QuickStatus アプリケーションのサンプル コード](#pj15_StatusingApp_Example)を参照してください。 
    
手順 3 では、割り当ての読み取り、およびテーブルの行を作成するを変更して、割り当ての達成率を更新して、JavaScript 関数を追加します。 実際の手順は、アプリケーションの開発により反復的、またはいくつかの HTML コードを作成、追加して関連するスタイルと、JavaScript の関数をテストを変更または、HTML コードを追加、この処理を繰り返します。

<a name="pj15_StatusingApp_JavaScript"> </a>

### <a name="creating-the-javascript-functions-for-the-quickstatus-app"></a>QuickStatus アプリケーションの JavaScript 関数を作成します。

SharePoint アプリケーションの Visual Studio のテンプレートには、SharePoint クライアント コンテキストを取得し、基本を説明する既定の初期化コードを含むファイルを取得し、アプリケーション ページのアクションを設定します App.js が含まれています。 SharePoint クライアント側 SP.js ライブラリの JavaScript の名前空間は、 **SP**です。 Project Server アプリケーションは、PS.js ライブラリを使用するためアプリケーションは、クライアント コンテキストを取得し、JSOM を Project Server にアクセスするのには**PS**の名前空間を使用します。 
  
**QuickStatus**アプリケーションでは、JavaScript 関数を以下に示します。 
  
- ドキュメントの**準備完了**イベント ハンドラーは、ドキュメント オブジェクト モデル (DOM) がインスタンス化されるときに実行されます。 **準備完了**イベント ハンドラーでは、次の 4 つの手順が行われます。 
    
    1. プロジェクトのサーバー JSOM および**pwaWeb**のグローバル変数をクライアント ・ コンテキストを使用して**projContext**のグローバル変数を初期化します。 
        
    2. **ProjUser**のグローバル変数を初期化するために**getUserInfo**関数を呼び出します。 
        
    3. どの取得には、ユーザーの割り当てデータが指定されている、 **getAssignments**関数を呼び出します。 
        
    4. バインドでは、イベント ハンドラーのテーブル ヘッダー] チェック ボックスをオンにし、テーブルの各行のチェック ボックスをクリックします。 Click イベント ハンドラーは、ユーザーを選択するか、テーブル内のすべてのチェック ボックスをオフのチェック ボックスを**オンになって**属性を管理します。 
    
- **GetAssignments**関数が成功した場合は、 **onGetAssignmentsSuccess**関数を呼び出します。 関数は、割り当てごとに、テーブルに行を挿入、各行の HTML コントロールを初期化し、下のボタンのプロパティを初期化し、します。 
    
- **[更新**] ボタンの**onClick**イベント ハンドラーでは、 **updateAssignments**関数を呼び出します。 選択した各割り当てに適用する関数を取得完了率の値またはパーセントの完全なテキスト ボックスが空の場合は、関数、% 選択した各割り当ての完全なテーブルの取得します。 **UpdateAssignments**関数を保存しステータスの更新を送信し、結果について、ページの下部にメッセージを書き込みます。 
    
### <a name="procedure-3-to-create-the-javascript-functions"></a>手順 3。 JavaScript 関数を作成するには

1. Visual Studio で App.js ファイルを開き、ファイル内のすべてのコンテンツを削除し、
    
2. グローバル変数とドキュメントの**準備完了**イベント ハンドラーを追加します。 **ドキュメント**オブジェクトをアクセスするには、jQuery の機能を使用します。 
    
   テーブル ヘッダーのチェック ボックスの click イベント ハンドラーは、行のチェック ボックスのチェック状態を設定します。 すべての行のチェック ボックスが選択されている、またはすべてがオフ、行のチェック ボックスの click イベント ハンドラーは、[ヘッダー] チェック ボックスのチェック状態を設定します。 Click イベント ハンドラーは、空の文字列をページの下部に結果のメッセージを設定します。
    
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

3. **OnGetUserNameSuccess**を呼び出して、クエリが成功した場合、 **getUserInfo**関数を追加します。 **OnGetUserNameSuccess**関数では、ユーザー名を含む表のタイトルに**キャプション**段落の内容を置き換えます。 
    
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

4. **GetAssignments**関数を呼び出す**onGetAssignmentsSuccess**の追加 (手順 5 を参照してください) 割り当てクエリが成功した場合。 [**含める**] オプションは、指定されたフィールドだけを返すクエリを制限します。 
    
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

5. 割り当てごとに行をテーブルに追加する、 **onGetAssignmentsSuccess**関数を追加します。 **PrevProjName**変数を使用すると、別のプロジェクトの行は、かどうかを決定します。 プロジェクト名が太字のフォントで表示されている場合は、ない場合は、プロジェクト名が空の文字列に設定します。 
    
   > [!NOTE]
   > JSOM では、 **ActualWorkTimeSpan**など、CSOM に含まれている**TimeSpan**プロパティは含まれません。 JSOM が[PS. など、時間をミリ秒単位のプロパティを使用する代わりに、StatusAssignment.actualWorkMilliseconds](https://msdn.microsoft.com/library/736bce1e-f734-0efe-6c5f-e0e891ab00ef%28Office.15%29.aspx)プロパティ。 そのプロパティを取得するメソッドは、**を取得\_actualWorkMilliseconds**、整数値が返されます。 > **Get_actualWork**メソッドでは、"3 h"などの文字列を返します。 **QuickStatus**アプリケーションでは、いずれかの値を使用していますが、表示を変える可能性があります。 割り当てクエリには、デバッグ時に値をテストすることができますので、両方のプロパティが含まれます。 **ActualWork**変数を削除する場合は、割り当てクエリで**ActualWork**プロパティを削除することもできます。 
  
   最後に、 **onGetAssignmentsSuccess**関数は、 **[更新**] ボタンを初期化し、 **[更新**] ボタンのクリックしてイベント ハンドラーです。 **[更新**] ボタンのテキスト値は、HTML コードの設定もできました。 
    
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

6. **UpdateAssignments**を追加する [**更新**] ボタンのイベント ハンドラー] をクリックします。 タスクの達成率の値を変更するか、[**達成率**] テキスト ボックスに値を追加、ときに、「60」、「60%」または「60%」などのいくつかの形式で、値を入力する可能性があります。 **GetNumericValue**メソッドは、入力テキストの数値を返します。 
    
   > [!NOTE]
   > 生産用に設計されたアプリケーションで使用して、数値情報の入力値は、フィールドの入力規則およびその他のエラー チェックを含める必要があります。 
  
   **UpdateAssignments**の使用例は、いくつか基本的なエラーのチェックが含まれていて、ページの下部にある**メッセージ**の段落で情報が表示されます: 更新クエリが成功し、入力エラーまたは更新クエリがある場合は赤、緑失敗しました。 
    
   **SubmitAllStatusUpdates**メソッドを使用する前に、アプリケーション必要があります更新をサーバーに保存 PS. の**を使用してStatusAssignmentCollection.update**メソッドです。 
    
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

7. ホストの Project Web App サイトの URL の**SPHostUrl**のクエリ文字列パラメーターを使用して、 **exitToPwa**関数を追加します。 [タスク] ページに移動するには、追加`"/Tasks.aspx"`の URL にします。 **SpHostUrl**変数を設定するとたとえば、 `https://ServerName/ProjectServerName/Tasks.aspx`。
    
   **GetQueryStringParameter**関数は、 **QuickStatus**ページの URL を抽出し、URL のオプションで指定されたパラメーターを返すを分割します。 **文書の例を次に示します。URL** **QuickStatus**ドキュメント (すべて 1 行) の値。 
    
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

   前の URL では、 **getQueryStringParameter**関数を返します**SPHostUrl**クエリ文字列値、 `https://ServerName/pwa`。 
    
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

**QuickStatus**アプリケーションをこの時点で発行すると、Project Web App を追加するからサイト コンテンツ] ページで、アプリケーションを実行することができますが、ないユーザーが簡単に利用できます。 ユーザーを検索してアプリケーションを実行するために、[タスク] ページで、リボンのボタンを追加できます。 手順 4 では、リボンのカスタム アクションを追加する方法を説明します。 

<a name="pj15_StatusingApp_ribbon"> </a>

### <a name="adding-a-ribbon-custom-action"></a>リボンのカスタム操作の追加

リボンのタブ、グループ、および Project Web App ののためのコントロールにインストールされている pwaribbon.xml ファイル内で指定されている、 `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\FEATURES\PWARibbon\listtemplates` Project Server を実行しているコンピューター上のディレクトリです。 Project Web App のリボンのカスタム アクションを設計するために、Project 2013 SDK ダウンロードには、pwaribbon.xml のコピーが含まれています。 
  
Project Web App のタスク] ページの [Project Web App インスタンスが、タイムシートとタスクのステータスの値を入力するユーザーを有効にする 1 つのエントリのモードを使用するかどうかによって、異なるリボン定義を使用します。 Project Web App に対して管理者権限があれば、入力モードの状態を判断するに、ページの右上隅にあるボックスの [設定] メニューで**PWA の設定**を選択します。 PWA の設定] ページで、[**タイムシートの設定と既定の設定**を選択し、ページの下部にある**単一入力モード**] チェック ボックス。 
  
単一入力モードがオフのときは、pwaribbon.xml で自分の作業領域で [タスク] ページで、リボンが定義されています。 
  
```XML
   <!-- REGION My Work Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.MyWork"
      . . .
```

単一入力モードがオンのときは、pwaribbon.xml に関連付けられているモード領域でのタスク] ページのリボンが定義されています。 
  
```XML
   <!-- REGION Tied Mode Ribbon-->
   <CustomAction
      Id="Ribbon.ContextualTabs.TiedMode"
      . . .
```

グループとそれぞれの領域内のコントロールのようながリンク付けされているモードの場合、コントロールの単独モードでは、同じコントロールの別の関数を呼び出すことができます。 手順 4 は、1 つのエントリのモードがオフの場合は、 **QuickStatus**アプリケーションのボタン コントロールを追加する方法を示しています (**単一入力モード**] チェック ボックスがオフ) します。 
  
> [!NOTE]
> リボンまたは SharePoint アプリケーションのメニューにカスタム アクションを追加することに関する一般的な情報は、 [SharePoint のアプリケーションと共に配置するカスタム アクションの作成](https://msdn.microsoft.com/library/jj163954.aspx)を参照してください。 
  
### <a name="procedure-4-to-add-a-ribbon-custom-action-to-the-tasks-page"></a>手順 4 します。 リボンのカスタム アクションを [タスク] ページに追加するのには

1. Project Web App の [タスク] ページのリボンを確認します。 リボンの [**タスク**] タブを選択し、それを変更する方法を計画します。 **送信**、**タスク**の**期間**など、7 つのグループがあります。 **送信**グループは、2 つのコントロール、[**保存**] ボタン、および**送信の状態**」ドロップ ダウン メニューを持っています。 グループ内の任意の場所にコントロールを追加、 **[タスク**] タブで任意の場所に新しいコントロールを持つグループを追加したり、カスタムのグループとコントロールを持つ別のリボン タブを追加できます。 この例では、ボタンが**QuickStatus**アプリケーションの URL を呼び出して、**送信**グループに 3 番目のボタンを追加します。 
    
2. Visual Studio で**ソリューション エクスプ ローラー**ウィンドウで、 **QuickStatus**プロジェクトを右クリックしし、新しい項目を追加します。 **新しい項目の追加**] ダイアログ ボックスで、**リボンのカスタム アクション**を選択します (図 4 を参照してください)。 たとえば、RibbonQuickStatusAction、カスタム アクションの名前を指定し、[**追加**します。
    
   **図 4 です。リボンのカスタム アクションを追加します。**

   ![リボンのカスタム アクションを追加します。](media/pj15_CreateStatusingApp_AddRibbonCustomAction.gif "リボンのカスタム アクションを追加します。")
  
3. **リボンのカスタム アクションの作成**ウィザードの最初のページで選択した**ホストの Web**オプションのままに、カスタム動作のスコープのドロップ ダウン リストで **[なし]** を選択し、[**次**] を選択 (図 5 を参照してください)。 ドロップ ダウン リスト内の項目は、Project Server ではなく、SharePoint に関連します。 Project Server に適用されるため、カスタム動作の生成された XML のほとんどを交換します。 
    
   **図 5。リボンのカスタム アクションのプロパティを指定します。**

   ![リボンのカスタム アクションのプロパティを指定します。](media/pj15_CreateStatusingApp_RibbonCustomAction2.gif "リボンのカスタム アクションのプロパティを指定します。")
  
4. **リボンのカスタム アクションの作成**ウィザードの次のページで、設定のすべての既定値のままにし、[**完了**] を選択 (図 6 を参照してください)。 Visual Studio は、Elements.xml ファイルが含まれる [ **RibbonQuickStatusAction** ] フォルダーを作成します。 
    
   **図 6 です。ボタン コントロールの設定を指定します。**

   ![ボタン コントロールの設定を指定します。](media/pj15_CreateStatusingApp_RibbonCustomAction3.gif "ボタン コントロールの設定を指定します。")
  
5. リボンのカスタム アクションの Elements.xml ファイルで生成された既定のコードを変更します。 以下は、既定の XML コードです。
    
   ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="https://schemas.microsoft.com/sharepoint/">
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

   1. **CustomAction**要素、**シーケンス**属性と**Title**属性を削除します。 
    
   2. **送信**グループにコントロールを追加するのには検索の最初のグループで、`Ribbon.ContextualTabs.MyWork.Home.Groups`を開始する要素では、pwaribbon.xml ファイル内のコレクション`<Group Id="Ribbon.ContextualTabs.MyWork.Home.Page" Command="PageGroup" Sequence="10" Title="$Resources:pwafeatures,PAGE_PDP_CM_SUBMIT"`。 **送信**グループには、子コントロールを追加するには、次のコードは、Elements.xml ファイルに**CommandUIDefinition**要素の適切な**場所**の属性を示します。 
    
      ```XML
        <CommandUIDefinitions>
          <CommandUIDefinition Location="Ribbon.ContextualTabs.MyWork.Home.Page.Controls._children">
             . . .
          </CommandUIDefinition>
        </CommandUIDefinitions>
      ```

   3. **ボタン**の子要素の属性値を次のように変更します。 
    
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

       - **シーケンス**属性は任意の数よりも高い、ボタンを作成する 3 番目のコントロール、グループ内に、 `Sequence="20"` (要素である**FlyoutAnchor** pwaribbon.xml で) 既存の**ステータスの送信**コントロールの値。 規則により、グループ、およびコントロールのシーケンス番号は、 `10, 20, 30, …`、中間の位置に挿入する要素を使用します。
    
       - **コマンド**] 属性には、 **CommandUIHandler**要素で実行するコマンドを指定する (を参照してください次のステップ 5.d)。 次の開発者が容易にできるようにするのにはコマンド名を簡略化できます。 たとえば`Command="Invoke_QuickStatus"`よりも読みやすくするには`Command="Invoke_RibbonQuickStatusActionButtonRequest"`です。
    
       - イメージの属性では、16 x 16 ピクセルのアイコンと、32 x 32 ピクセルのアイコン ボタン コントロールを指定します。 デフォルトの Elements.xml ファイルに`Image32by32="_layouts/15/images/placeholder32x32.png"`オレンジ色の点を指定します。 アイコンを抽出するには、イメージ マップ ファイル (ps16x16.png と ps32x32.png) にインストールされているから、 `[Program Files]\Common Files\Microsoft Shared\Web Server Extensions\15\TEMPLATE\LAYOUTS\1033\IMAGES` Project Server を実行しているコンピューター上のディレクトリです。 32 x 32 ピクセルのアイコンはアイコン、左 10 番目の行からの 2 列目を ps32x32.png のイメージ マップの上から (9 回終了後は、アイコンの上行; 9 行 x 32 ピクセル/行 = 288 ピクセル) です。 
    
       - ボタン コントロールのツール ヒントを表示するには、 **ToolTipTitle**属性と**ToolTipDescription**属性を追加します。 
    
    4. **CommandUIHandler**要素の属性を変更します。 たとえば、**コマンド**の属性が**Button**要素の**コマンド**の属性の値と一致しているを確認します。 **CommandAction**属性では、 `~appWebUrl` **QuickStatus** web ページの URL のプレース ホルダーです。 リボン ボタンは、 **QuickStatus**アプリケーションを起動と、 **SPHostUrl**、 **SPLanguage**、 **SPClientTag**、 **SPProductNumber**、および**SPAppWebUrl は、URL オプションを使用して、 **{StandardTokens}** トークンが置き換えられます。**.
    
        ```XML
            <CommandUIHandlers>
                <CommandUIHandler Command="Invoke_QuickStatus"
                                  CommandAction="~appWebUrl/Pages/Default.aspx?{StandardTokens}"/>
            </CommandUIHandlers>
        ```

6. **ソリューション エクスプ ローラー**で**Feature1.feature**デザイナー、開き、**フィーチャー内の項目**] ウィンドウに、**ソリューション内の項目**] ウィンドウから**RibbonQuickStatusAction**項目を移動します。 **Package.package**デザイナーを開く、する場合、**パッケージ内の項目**] ウィンドウで**RibbonQuickStatusAction**項目になります。 
    
アプリケーションを開発するリボン ボタンを追加すると、通常、アプリケーションをテストしてデバッグするための JavaScript コードにブレークポイントを設定します。、 デバッグを開始するのには**f5 キー**を押すと、Visual Studio は、アプリケーションをコンパイル、 **QuickStatus**プロジェクトの [**サイト URL** ] プロパティで指定し、アプリケーションを信頼するかどうかを確認するページが表示されるサイトに配置します。 続行し、 **QuickStatus**アプリケーションを終了すると、Project Web App の [タスク] ページに戻ります。 

> [!NOTE]
> 図 7 は、リボンの [**タスク**] タブで [**クイックのステータス**] ボタンが無効になっているかを示しています。 多くデバッグ、Visual Studio での展開後は、同じテスト サーバーに発行したアプリケーションをデバッグまたは続行すると、カスタム リボンのコントロールをブロックできます。 ボタンを有効にするには、Visual Studio は、 **RibbonQuickStatusAction**アイテムを削除し、作成を別の名前と ID を持つ新しいリボンの操作 Project Web App のテストのインスタンスからアプリケーションを削除してくださいし、別のアプリケーション ID を持つアプリケーションを再作成し、問題が解決しない場合 
  
**図 7 です。無効状態のボタンのツールヒントを表示します。**

![無効なボタンのツールヒントを表示します。](media/pj15_CreateStatusingApp_ButtonToolTipDisabled.gif "無効なボタンのツールヒントを表示します。")
  
手順 5 では、展開して、 **QuickStatus**アプリケーションをインストールする方法を説明します。 手順 6 では、それをインストールした後、アプリケーションのテストでいくつか追加の手順を示しています。 

<a name="pj15_StatusingApp_Deploying"> </a>

## <a name="deploying-the-quickstatus-app"></a>QuickStatus アプリケーションを展開します。

Project Web App などの SharePoint web アプリケーションにアプリケーションを配置するのにはいくつかの方法があります。 SharePoint がインストールされているかどうか、オンプレミスまたはオンラインのテナント機能は、および配置を使用するがプライベートの SharePoint カタログまたは Office のパブリック ストア、アプリケーションを発行するかどうかによって異なります。 手順 5 では、プライベートなアプリ カタログで設置型インストールに**QuickStatus**アプリケーションを配置する方法を示します。 詳細についてを参照してください[をインストールおよび SharePoint 2013 のアプリケーションを管理する](https://technet.microsoft.com/library/fp161232.aspx)と[SharePoint の発行アプリケーション](https://msdn.microsoft.com/library/jj164070.aspx)
  
> [!NOTE]
> SharePoint カタログにアプリケーションを追加するには、SharePoint 管理者のアクセス許可が必要です。 
  
### <a name="procedure-5-to-deploy-the-quickstatus-app"></a>手順 5 です。 QuickStatus アプリケーションを展開するには

1. Visual Studio は、すべてのファイルを保存**ソリューション エクスプ ローラー**で**QuickStatus**プロジェクトを右クリックし、**公開**] をクリックします。
    
2. **QuickStatus**アプリケーションが SharePoint でホストされているため (図 8 を参照) を発行するための非常にいくつかのオプションがあります。 **Office および SharePoint 用のアプリケーションの発行**] ダイアログ ボックスで [**完了**] を選択します。
    
   **図 8 です。QuickStatus アプリケーションを発行します。**

   ![を使用して、発行ウィザード](media/pj15_CreateStatusingApp_PublishWizard.gif "を使用して、発行ウィザード")
  
3. QuickStatus.app ファイルのコピー、`~\QuickStatus\bin\Debug\app.publish\1.0.0.0`ディレクトリのローカル コンピューター上の適当なディレクトリ (または、設置には、SharePoint コンピューター)。 
    
4. SharePoint サーバーの全体管理で、サイド リンク バーで、**アプリケーション**を選択し、**アプリケーション カタログの管理**します。
    
5. アプリケーションのカタログが存在しない場合は、 [SharePoint 2013 のアプリケーション カタログを管理](https://technet.microsoft.com/library/fp161234.aspx)する*web アプリケーションのアプリケーションのカタログ サイトを構成する*」に従ってアプリケーション カタログのサイト コレクションを作成します。
    
   アプリケーションのカタログが存在する場合は、[アプリケーション カタログの管理] ページで、サイトの URL に移動します。 次の手順でアプリケーションのカタログ サイトは`https://ServerName/sites/TestApps`です。
    
6. アプリケーション カタログ ページで、サイド リンク バーで **、SharePoint のアプリケーション**を選択します。 リボンの [**ファイル**] タブで、SharePoint ページのアプリでは、**ドキュメントのアップロード**を選択します。
    
7. **ドキュメントの追加**] ダイアログ ボックスで QuickStatus.app ファイルを参照する、バージョンについては、コメントを追加し、[ **ok]**。
    
8. アプリケーションを追加すると、アプリケーションの説明、アイコン、およびその他の情報のローカル情報を追加することもできます。 **SharePoint の QuickStatus.app のアプリケーション**] ダイアログ ボックスで、SharePoint サイト コレクション内のアプリケーションに表示する情報を追加します。 たとえば、次の情報を追加します。 
    
   1. フィールドの**簡単な説明**: テスト アプリケーションの状態を入力します。
    
   2. **[説明**] フィールド: 複数のプロジェクトでタスクの達成率を更新するアプリケーションを Test と入力します。
    
   3. **アイコンの URL**フィールド: アプリ カタログのサイトのアセットをアプリケーション アイコンに 96 x 96 ピクセルのイメージを追加します。 移動して、 `https://ServerName/sites/TestApps`、**サイトの内容**を選択して、[**設定**] ドロップ ダウン メニューで、**サイトのアセット**を選択、quickStatusApp.png 画像を追加します。 **QuickStatusApp**の項目を右クリックし、**プロパティ**を選択し、**プロパティ**] ダイアログ ボックスの**アドレス (URL)** の値をコピーします。 たとえば、 `https://ServerName/sites/TestApps/SiteAssets/QuickStatusApp.png`、**アイコンの URL**の web アドレス] フィールドに値を貼り付けるとします。 タイプの例 (図 9) と、アイコンの説明は、QuickStatus アプリケーションのアイコンを入力します。 URL が有効であるかをテストします。
    
      **図 9 です。QuickStatus アプリケーションのアイコンの URL を追加します。**

      ![SharePoint アプリケーションの [プロパティの設定](media/pj15_CreateStatusingApp_AddAppToSharePointSettings.gif "SharePoint アプリケーションの [プロパティの設定")
  
   4. **カテゴリ**フィールド: 既存のカテゴリを選択するか、独自の値を指定します。 たとえば、状態管理を入力します。
    
      > [!NOTE]
      > **状態管理**をという名前のカテゴリは、テストのためだけにします。 Project Server アプリケーションの一般的なカテゴリは、**プロジェクトの管理**です。 
  
   5. **発行元の名前**フィールド: パブリッシャーの名前を入力します。 この例では、プロジェクトの SDK を入力します。
    
   6. **Enabled**フィールド: にアプリをインストールするための Project Web App サイトの管理者に表示するには、 **[有効**] チェック ボックスを選択します。 
    
   7. 追加のフィールドはオプションです。 たとえば、サポート URL とアプリケーションの詳細] ページの複数のヘルプの画像を追加できます。 図 9 は、**イメージの URL の 1**フィールドには、アプリのスクリーン ショットとスクリーン ショットの説明の URL が含まれます。 
    
   8. **SharePoint の QuickStatus.app のアプリケーション**] ダイアログ ボックスで**保存**を選択します。 図 9 アプリケーションで**状態の更新をすばやく**アイテム SharePoint ライブラリをチェック アウト、編集のためのようにダイアログ ボックスのリボンの [**編集**] タブ**チェックインの**プロセスを完了するを選択 (図 10 を参照してください)。 
    
      **図 10 です。QuickStatus アプリケーションは、SharePoint ライブラリをアプリケーションに追加されます。**

      ![「QuickStatus アプリケーション SharePoint に追加](media/pj15_CreateStatusingApp_AddAppToSharePoint.gif "「QuickStatus アプリケーション SharePoint に追加")
  
9. Project Web App では、[**設定**] ドロップ ダウン メニューで、**アプリケーションの追加**を選択します。 [アプリ] ページの [サイド リンク バーで、[は**の組織**を選択し、**クイックのステータスの更新プログラム**のアプリケーションの**アプリケーションの詳細**を選択します。 図 11 は、アプリケーションのアイコン、スクリーン ショットは、前の手順で追加したその他の情報と詳細のページを示しています。 
    
   **図 11。Project Web App でクイックのステータスの更新プログラムの詳細] ページを使用します。**

   ![QuickStatus アプリケーションは、Project Web App を追加します。](media/pj15_CreateStatusingApp_AddAppToPWA.gif "QuickStatus アプリケーションは、Project Web App を追加します。")
  
10. 簡易ステータスの更新プログラムの詳細ページで、 **IT の追加**を選択します。 Project Web App には、(図 12 を参照してください)、QuickStatus アプリケーションを実行できる操作の一覧が表示されるダイアログ ボックスが表示されます。 操作の一覧は、AppManifest.xml ファイル内の**AppPermissionRequest**要素から取得されます。 
    
    **図 12 です。状態をアプリケーションが信頼できることを確認します。**

    ![QuickStatus アプリケーションの信頼性を確認](media/pj15_CreateStatusingApp_AddAppToPWA2Trust.gif "QuickStatus アプリケーションの信頼性を確認")
  
11. **簡易ステータスの更新プログラムを信頼する**] ダイアログ ボックスで、**信頼する**を選択します。 アプリケーションは、Project Web App サイトのコンテンツ ページに追加されます (図 13 を参照してください)。
    
    **図 13。[サイト コンテンツ] ページで、状態のアプリケーションを表示します。**

    ![QuickStatus アプリケーションでは、サイトの内容を表示します。](media/pj15_CreateStatusingApp_AddAppToPWA3.gif "QuickStatus アプリケーションでは、サイトの内容を表示します。")
  
[サイト コンテンツ] ページで、アプリケーションを実行するのには**クイックのステータスの更新**] アイコンを選択します。

> [!NOTE]
> サイト コンテンツ] ページで、アプリケーションに関する情報を提供するその他のコマンドでは、**簡易ステータスの更新プログラム**の名前と、省略記号 (...) を含む領域を選択します。アプリケーションの [バージョン情報] ページを確認してアプリケーション エラーに関する情報を含むアプリケーションの詳細ページを表示、アプリケーションのアクセス許可] ページを確認するか、または Project Web App からアプリケーションを削除することができます。 
  
[Project Web App の [タスク] ページ (図 14 を参照)、 **QuickStatus**ボタンは、リボンで有効にする必要があります。 **クイック ステータス**] ボタンが無効の場合は、図 7 では、ノートに記載されている操作をしてみてください。 

**図 14。[タスク] タブから QuickStatus アプリケーションを起動します。**

![[タスク] タブから QuickStatus アプリケーションを起動します。](media/pj15_CreateStatusingApp_TasksRibbon.gif "[タスク] タブから QuickStatus アプリケーションを起動します。")
  
手順 6 では、QuickStatus アプリケーションのテストをいくつか示しています。

<a name="pj15_StatusingApp_Testing"> </a>

## <a name="testing-the-quickstatus-app"></a>QuickStatus アプリケーションのテスト

**QuickStatus**アプリケーションでは、ユーザーが試みる場合がありますすべての操作は、運用サーバーに、またはオンラインのプロジェクトの生産のテナントには、アプリケーションを展開する前に Project Server のテスト環境でテストしてください。 テスト インストールを使用すると、変更して、実際のプロジェクトに影響を与えずに、ユーザーの割り当てを削除できます。 テストすると、管理者、プロジェクト マネージャー、チーム メンバーなど、アクセス許可セットを持つユーザーは、いくつか必要がありますもあります。 徹底的なテストの開発時にテストでは検出されなかったアプリケーションで行う必要のある変更を明らかにできます。 手順 6 は、 **QuickStatus**アプリケーションのいくつかのテストを一覧表示が、すべてを網羅した、一連テストにはが含まれていません。 
  
### <a name="procedure-6-to-test-the-quickstatus-app"></a>手順 6。 QuickStatus アプリケーションをテストするのには

1. ユーザーに割り当てがない**QuickStatus**アプリケーションを実行します。 アプリケーションは、たとえば、**ユーザー名には、割り当て**、ページの下部にある青色のメッセージに表示されます。
    
   **更新プログラム**、および**割り当てが更新されて**の緑のメッセージの変更を選択します。
    
   > [!NOTE]
   > 割り当てがない場合、 **[更新**] ボタンが無効になっているように、アプリケーションの動作を変更してください。 
  
2. ユーザーが複数の異なるプロジェクトで複数の割り当てを持っているアプリケーションを実行し、一部の割り当ては完全ではありません。 アプリケーションの外観と操作を次のように実行 (されています図 15 を参照してください)。
    
   1. **OnGetAssignmentsSuccess**関数は、現在のユーザーの割り当てごとにテーブルに行を作成します。 プロジェクト名は、各プロジェクトの最初の割り当てのための太字のフォントで、1 回だけ表示されます。 
    
   2. [**タスク名**] 列のヘッダーのチェック ボックスをオフにします。 テーブルのヘッダーでは、イベント ハンドラーは、タスクの行のすべての他のチェック ボックスをクリア] をクリックします。 
    
   3. すべてのタスクを選択します。 Click イベント ハンドラーとそれぞれの行のすべての行を選択したかどうかを決定する場合は、 **[タスク名**] 列のヘッダーを選択します。 
    
   4. すべてのチェック ボックスをオフにもう一度とをいくつかの残存作業時間を持つ 1 つの割り当てを選択します。 たとえば、図 15 を示しています上のタスク T1 20% の残存作業を完了するには。
    
   5. **達成率を設定する**テキスト ボックスで、80 と入力し、**更新プログラム**を選択します。 ページの一番下**の割り当てが更新されて**、緑色のメッセージが表示されます。
    
      **図 15 です。QuickStatus アプリケーションでは、割り当ての更新**

      ![QuickStatus アプリケーションでは、割り当ての更新](media/pj15_CreateStatusingApp_Testing1Update.gif "QuickStatus アプリケーションでは、割り当ての更新")
  
3. **更新**を選択 (図 16 参照)。 、もう一度すべてのタスクの選択し、最上位のタスクは 80% が完了します。 
    
      **図 16。簡易ステータスの更新ページを更新します。**

      ![QuickStatus ページを更新します。](media/pj15_CreateStatusingApp_Testing2Refresh.gif "QuickStatus ページを更新します。")
  
4. すべてのチェック ボックスをオフにし、別のタスクを選択します。 たとえば、 **PWA から新しいタスク**を選択します。 **達成率を設定する**テキスト ボックスを空のままにして、選択したタスクの**達成率**の列のすべてのテキストを削除し、**更新**します。 両方のテキスト ボックスは空であるため、アプリケーションは、赤のエラーを示しています (図 17 を参照してください) のメッセージです。
    
      **図 17 です。エラー メッセージをテストします。**

      ![エラー メッセージをテストします。](media/pj15_CreateStatusingApp_Testing3Error.gif "エラー メッセージをテストします。")
  
5. 80% が完了すると、前のタスクを更新して**終了**] をクリックします。 **ExitToPwa**関数は、SharePoint のホスト アプリケーションの [タスク] ページにブラウザー ウィンドウの位置を変更 (つまり、URL に変更https://ServerName/pwa/Tasks.aspx)。 図 18 は、 **T1**のタスクと、**新しい PWA から**タスクを表示する 80% 完了を示します。 
    
      **図 18。Project Web App の更新タスクを確認します。**

      ![Project Web App で更新されたタスクを確認します。](media/pj15_CreateStatusingApp_TasksUpdatedInPWA.gif "Project Web App で更新されたタスクを確認します。")
  
6. 評価のためのプロジェクトで、最新の状態が表示されている前に、変更を承認のため送信し、プロジェクト管理者によって承認する必要があります。
    
テストには、利便性が向上するように**QuickStatus**アプリケーションで行う必要のある他のいくつかの変更が表示されます。 例:

- 追加のエラー チェックやテキスト ボックスの値の検証の必要があります。 現時点では、ユーザーには、数値以外の値または悪意のあるエラー メッセージの結果の達成率は、負の値を入力できます。 たとえば、負の値、エラー メッセージは、**の割り当てを更新中のエラー: PJClientCallableException: StatusingSetDataValueInvalid**。
    
- プロジェクトとタスクの行番号だけでなく、空のテキスト ボックスは、エラー メッセージを一覧表示でした。
    
- 成功時のメッセージは、更新するタスクの一覧を含めることがまたは**updateAssignments**関数が成功した場合は、可能性があります、ページの自動更新を実行して更新されたタスクまたはパーセンテージを表示する別の色とフォントを太字にします。 
    
- 非常に大きなテーブルを避けるためには、割り当てのテーブルという制限があります 100% 未満が完了するタスクにします。 または、すべてのタスクを表示するオプションを追加します。 簡単に実装できるフィルタ リングし、グリッド、テーブルの代わりに jQuery ベースのグリッドを使用して、この問題を解決も可能性がありますページングします。
    
- **QuickStatus**アプリケーションは、ステータスを送信していない、ため、リボンの [**タスク**] タブの**状態**をアイコンより論理的になります**送信**グループ内の最後のアイコンではなく、[**タスク**] で、最初のアイコン。 
    
- ページは、の**getAssignments**の中に部分的に初期化された状態のままに**onGetAssignmentsSuccess**関数が、[ **btnSubmitUpdate** ] ボタンのテキストを初期化しますが、他のボタンのテキスト値は、html 形式で初期化されます、ため関数を実行します。 Html 形式でテキストの値すべて初期化された場合より一貫性のあるページ上のボタンが表示されます。 
    
最も重要なは、運用アプリケーションでは、割り当ての割合を変更して、 **QuickStatus**アプリケーションの使用を完了する方法を改訂する必要があります。 詳細については、[次の手順](#pj15_StatusingApp_NextSteps)を参照してください。 

<a name="pj15_StatusingApp_Example"> </a>

## <a name="example-code-for-the-quickstatus-app"></a>QuickStatus アプリケーションのコードの例

### <a name="defaultaspx-file"></a>Default.aspx ファイル

次のコードに、 `Pages\Default.aspx` 、 **QuickStatus**プロジェクトのファイル。 
  
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

次のコードに、 `Scripts\App.js` 、 **QuickStatus**プロジェクトのファイル。 
  
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

次の CSS コードに、 `Content\App.css` 、 **QuickStatus**プロジェクトのファイル。 
  
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

### <a name="elementsxml-file-for-the-ribbon"></a>リボンの Elements.xml ファイル

リボンの [**タスク**] タブで追加したボタンを次の XML 定義では、 `RibbonQuickStatusAction\Elements.xml` 、 **QuickStatus**プロジェクトのファイル。 
  
```XML
    <?xml version="1.0" encoding="utf-8"?>
    <Elements xmlns="https://schemas.microsoft.com/sharepoint/">
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

以下は、複数のプロジェクトで、アプリケーションのユーザーの割り当ての状態を更新するために必要な 2 つのアクセス許可要求のスコープが含まれている**QuickStatus**プロジェクトのアプリケーション マニフェストの XML です。 
  
```XML
    <?xml version="1.0" encoding="utf-8" ?>
    <!--Created:cb85b80c-f585-40ff-8bfc-12ff4d0e34a9-->
    <App xmlns="https://schemas.microsoft.com/sharepoint/2012/app/manifest"
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

**QuickStatus**アプリケーションの完全な Visual Studio のソリューションには、独自の AppIcon.png ファイルが含まれています。 ソリューションが含まれます。 Project 2013 SDK ダウンロードにします。 

<a name="pj15_StatusingApp_NextSteps"> </a>

## <a name="next-steps"></a>次の手順

**QuickStatus**アプリケーションは、Project Server 2013 とプロジェクトをオンラインでインストールできるアプリケーションを記述する方法の比較的単純な例です。 [QuickStatus アプリケーションをテストする](#pj15_StatusingApp_Testing)セクションには、可能な使いやすさのいくつかの機能強化が一覧表示されます。 **QuickStatus**アプリケーションは、Project Web App の割り当ての状態を更新するのに JavaScript 関数を使用します。 割り当ての達成率を変更することは推奨されるプロジェクト管理手法ではありません。 実績開始日と割り当てられているタスクの残存期間を更新する別の方法があります。 問題についてを参照してください[更新プログラムより優れた](https://www.mpug.com/articles/update-better)MPUG ニュースレターです。 

<a name="pj15_StatusingApp_AdditionalResources"> </a>

## <a name="see-also"></a>関連項目

- [Project Server のプログラミング タスク](project-programming-tasks.md)
- [SharePoint アドイン](https://msdn.microsoft.com/library/jj163230.aspx)
- [Project Web App の [タスクの更新を管理します。](https://technet.microsoft.com/en-us/library/hh767481%28v=office.14%29.aspx)
- [カスタム アクションを作成して SharePoint アドインで展開する](https://msdn.microsoft.com/library/jj163954.aspx)
    

