---
title: クライアント側オブジェクト モデルを使用してプロジェクトのオンライン アプリケーションを開発
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: この資料では、デスクトップ アプリケーションを.NET Framework 4.0 を使用してプロジェクトをオンラインでマイクロソフトのアプリケーション開発について説明します。 この資料に記載されているアプリケーションは、ホストしているサーバーから情報を取得します。
ms.openlocfilehash: b6e7260fd2337d2b156f97605fdd201f5e0d4edc
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385264"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a>クライアント側オブジェクト モデルを使用してプロジェクトのオンライン アプリケーションを開発

この資料では、デスクトップ アプリケーションを.NET Framework 4.0 を使用してプロジェクトをオンラインでマイクロソフトのアプリケーション開発について説明します。 この資料に記載されているアプリケーションは、ホストしているサーバーから情報を取得します。 
  
## <a name="background"></a>背景

Microsoft Project では、1990 年代初頭にデスクトップ アプリケーションとして起動されます。 今日では、プロジェクトが多く、決まって述べるが、いくつかの種類です。
  
- プロジェクトの標準的なエディションは、スタンドアロン アプリケーションとして実行されるデスクトップ アプリケーションです。
    
- プロフェッショナル エディションのプロジェクトが可能な対話と規模が大きく、サーバーとデータを共有、プロジェクトの標準のエディションの機能を実行するデスクトップ アプリケーションです。
    
- プロジェクト オンラインは、調整し、プロジェクト、プログラム、およびポートフォリオを管理する PMO レベルのソリューションは、企業がマイクロソフトによってホストされるサービスです。 デスクトップのエディションでは、オンラインのプロジェクトよりもさまざまなソリューションでは、管理でき、プロジェクトのライフ サイクル全体にわたってプロジェクトの詳細を追跡することができます。 
    
- Project Server は、エンタープライズでホストされているサービスを企業が管理し、プロジェクト、プログラム、およびポートフォリオ情報を含むサーバーをセキュリティで保護です。 社内でのサーバーをセキュリティで保護するための project Server には、プロジェクト、プログラム、および外部でホストされているプロジェクト、オンラインでのカスタマイズの容量を増やすのポートフォリオの中心の機能が用意されています。
    
オンラインのプロジェクトには、オンラインの 3 つの API セットが含まれて: クライアント側オブジェクト モデル (CSOM)、JavaScript オブジェクト モデル (JSOM)、および主要な状態を転送 (残りの部分)。 
  
- CSOM の .NET の実装は、テナントのプロジェクトをオンラインでやり取りする Windows アプリケーションを開発するときの推奨されるインターフェイスです。 ユーザー中心型のアプリケーションの一般的な環境には、Windows デスクトップおよび Microsoft Surface のデバイスが含まれます。 CSOM を .NET で記述されたバックエンド ・ アプリケーションは、ビジネス ロジックとデータ ソースの外部プロジェクトをオンラインにある他のサーバーに接続できます。 プロジェクトのオンライン検索要求は、基本的な検索機能をいくつかの拡張機能を提供する LINQ のようなクエリ システムを使用します。
    
- JavaScript オブジェクト モデル (JSOM) インターフェイスは、アドイン プロジェクトをオンラインでブラウザー間のサポートを提供します。アドインをプロジェクトのオンラインのテナントに格納されている web アプリケーションです。 ユーザーがアドインを実行しようとすると、アドインのコードがダウンロードされ、ユーザーのマシン上のブラウザーで実行されます。 
    
- 残りの部分と Odata のモデルでは、HTTP ベースの通信を提供するこのインターフェイスは Windows 以外の環境でアプリケーションをお勧めします。 通信のエンドポイントは、プロジェクト Web アプリケーション (PWA) サイト内のオブジェクトです。 結果は、通常の HTTP ステータス コードを提供します。
    
この資料では、CSOM の .NET インターフェイスを使用するアプリケーションについて説明します。
  
## <a name="prerequisites"></a>前提条件

10 を Windows を実行しているベースのシステムで起動し、次の項目を追加します。
  
- .Net framework 4.0 以降--は、完全なフレームワークを使用します。 ダウンロード サイトは、 https://msdn.microsoft.com/vstudio/aa496123.aspx。
    
- 2013 以降--Visual Studio の任意のエディションは、許容されます。 Visual Studio 2015 の community edition は、サンプル アプリケーションを開発する使用されました。 Community edition は、 https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx。
    
- SDK - オンラインのプロジェクトと Project Server の SharePoint クライアント コンポーネントは、SharePoint、および SharePoint の上にアセンブリを配置できます。 Visual Studio のプロフェッショナルおよびエンタープライズ エディションでは、SharePoint クライアント コンポーネントが含まれます。 コミュニティの Visual Studio エディションを使用すると、Office 開発者ツールの SDK の最新バージョンがあるか、次のサイト: https://www.microsoft.com/en-us/download/details.aspx?id=35585。
    
- プロジェクトのオンライン アカウントの場合は - これは、ホスティング サイトへのアクセスを提供します。 プロジェクトのオンライン アカウントを取得する方法についてを参照してくださいhttps://products.office.com/en-us/Project/project-online-portfolio-management。
    
- 情報が設定されているホスト サイト上のプロジェクト
    
> [!NOTE]
> 標準 (4.0 またはそれ以降) に、.NET Framework は、使用する正しいフレームワークです。 .NET Framework 4 のクライアント プロファイルを使用することはしません。 
  
## <a name="develop-the-application"></a>アプリケーションを開発します。

SharePoint のデスクトップ アプリケーションを開発して、希望のインターフェイスは、プロジェクトのクライアント側オブジェクト モデル (CSOM)。 
  
完全なサンプルをダウンロードすることができますhttps://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks。
  
最初の 2 つのトピックは、基本的な事項を説明します。 適切な名前空間とアセンブリの場合、Visual Studio プロジェクトを作成すると、ホスト サーバーにアクセスします。 残りのトピックと 1 つの多くのオブジェクトから、CSOM を使用して情報を取得する処理です。 
  
クライアント アプリケーションから 2 つのアクションのプロセスは、ホストから情報を取得します。 最初に、アプリケーションは指定し、サーバーに 1 つまたは複数の検索要求を送信します。 第 2 に、アプリケーションは、送信されたクエリを実行するサーバーに通知を発行します。 サーバーは、クエリの結果をクライアントに送信することによって応答します。
  
### <a name="set-up-the-visual-studio-project"></a>Visual Studio プロジェクトを設定します

アプリケーションのセットアップは、新しいプロジェクトを作成する、適切なアセンブリをリンクし、必要な名前空間を宣言することで構成されます。 Visual Studio には、いくつかの種類の開発プロジェクトが表示されます。 
  
#### <a name="select-a-visual-studio-project"></a>Visual Studio プロジェクトを選択します。

1. Visual Studio を起動し、[開始] ページでは、 **A の新しいプロジェクトを開始**] を選択します。 
    
   新しいプロジェクト ダイアログ ボックスでは、利用可能なアプリケーション テンプレート、および選択したテンプレートのデータ フィールドを表示します。 
    
2. このアプリケーションでは、次の項目を指定します。 画面上で発生するキーワードは、太字属性を持ちます。
    
   1. 左側のウィンドウでインストールされたテンプレート] から選択して**C#** => **Windows** => **クラシック デスクトップ**です。 
    
   2. 中央のウィンドウの上部には、 **.NET Framework 4**を選択します。 
    
   3. 中央のウィンドウの種類のアプリケーションから、**コンソール アプリケーション**を選択します。 
    
   4. 下部のセクションで、プロジェクトとソリューション名の場所と名前を指定します。 
    
   5. 下部のセクションで、**ソリューションのディレクトリを作成**チェック ボックスをオンします。 
    
3. 初期プロジェクトを作成するのには **[ok]** をクリックします。 
    
#### <a name="add-assemblies"></a>アセンブリを追加します。

VS ソリューションには、ProjectServerClient アセンブリ プロジェクト 2103 SDK では、アセンブリが SharePoint SDK、および System.Security の.NET Framework アセンブリの 2 つが必要があります。
  
1. VS ソリューション エクスプ ローラーで参照のエントリを右クリックし、**参照の追加]** を選択 ショートカット メニューの。 
    
2. **Microsoft.ProjectServer.Client.dll**を確認してください。 
    
   必要な場合は、**参照...** ] をクリックします。 ダイアログ ボックスの下部にあるボタンをクリックし、アセンブリを検索するのには Project 2013 SDK のインストール ディレクトリに移動します。 
    
3. **[OK]** をクリックします。 
    
4. .Cs ファイルには、PrjoctServer クライアント名前空間を追加します。
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

NuGet パッケージ マネージャー コンソールを使用して SharePoint 2013 SDK のアセンブリを追加します。 
  
1. VS ツール] メニューから、次のメニューをクリックします:**ツール =\> NuGet パッケージ マネージャー =\>パッケージ マネージャー コンソール**。 
    
2. パッケージ マネージャー コンソールで、次のコマンドとキーを押してを入力してください\<入力\>。
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   **パッケージ マネージャー コンソール**には、コマンドの結果の説明が用意されています。VS のソリューション エクスプ ローラーでは、プロジェクト参照に SharePoint のアセンブリが表示されます。 
    
3. .Cs ファイルに名前空間を追加します。
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

System.Security アセンブリは、.NET Framework の一部であるし、フレームワークを使用してインストールします。 サンプル アプリケーションでは、認証のためにホスト システムに暗号化された文字列を提供する名前空間が 1 つ以上が必要です。 認証されると、アプリケーションはホスト システム上のプロジェクトにアクセスできます。 System.Security 名前空間をこの方法で .cs ファイルに追加します。
  
1. VS ソリューション エクスプ ローラーで参照のエントリを右クリックし、**参照の追加]** を選択 ショートカット メニューの。 
    
2. 選択**アセンブリ =\>フレームワーク**参照マネージャーのダイアログ ボックスの左側のペインで**System.Security**を確認します。 
    
3. **[OK]** をクリックします。 
    
4. .Cs ファイルには、System.Security 名前空間を追加します。
    
   ```cs
    using System.Security;
   ```

.Cs ファイルの先頭には、次の名前空間を含める必要があります。
  
- System/システム
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>ホスト システムへの接続します。

プロジェクト オンラインは、適切なアプローチは、SharePoint の認証を使用するように SharePoint アプリケーションの場合は、です。 ホストされている環境にアクセスするのには次のコードを準備します。
  
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

ホスト環境にアクセスするための準備には、次の項目があります。
  
1. プロジェクトのコンテキスト オブジェクトを作成--上記のコードの次のコードに含まれているこれは。 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   コンテキストは、システムがプロジェクトのオブジェクト モデルのコンテキストを管理できるように、他のコンポーネントによって継承されます。
    
2. ホストのサイトを識別する--これは、次のコードで上記のコードから。
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   プロジェクト コンテキストのインスタンスを作成するには、プロジェクトのサイト コレクションのルートを提供する、アプリケーション必要があります。 アプリケーションでは、プロジェクトのルートの URL の部分文字列を使用します。 この場所のスナップショットは、次の図の赤い四角形で強調表示されます。 認証では、「pwa」の部分文字列で開始からの文字列が必要です。 コードの一覧でアプリケーションを使用して、文字列"https://XXXXXXXX.sharepoint.com/sites/pwa"です。
        
   ![のスクリーン ショットの赤い枠線内でのプロジェクトのサイト コレクションの URL です]。(media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "サイト赤い枠線内のコレクションをプロジェクトの URL のスクリーン ショット")
  
3. パスワードをセキュリティで保護された文字列の配置 - これは、次のコードで上記のコードから。
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   パスワードとユーザー アカウントは、ホスト サイトにアクセスする資格情報です。 
    
4. コンテキスト オブジェクトの資格情報の部分に、ユーザー アカウントとパスワードを追加する--これは、次のコードで上記のコードから。
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

プロジェクトのインスタンスが作成されたコンテキストを使用する準備ができました。
  
### <a name="list-all-published-projects"></a>すべての公開済みのプロジェクトを一覧表示します。

プロジェクト オンライン ProjectServer の作成、レポート、更新プログラム、サーバーと通信するプロキシを使用して削除 (CRUD) 操作します。 ホストまたはサーバーでは、効率的な方法で要求を処理し、クライアントがサーバーとの通信で以下の操作を実行します。
  
1. 通信のコンテキストを確立します。 
    
   によって、プロジェクト コレクションと同様に他のオブジェクトやコレクションのタスクのコレクション、割り当てのコレクション、stage オブジェクトの場合は、ユーザー設定フィールドなど、継承によってコンテキストが使用されます。 
    
2. オブジェクト モデルを使用すると、オブジェクト、コレクション、または取得するのにデータを指定します。
    
   この手順は、クエリ、またはメソッドとして、LINQ を使用します。 仕様では、何が表示を制御します。 多くの場合、この手順は、Load メソッド (手順 3) の本文として埋め込まれます。 
    
3. Load() または LoadQuery() メソッドを使用して前の手順から取得仕様をロードします。
    
   コレクションとオブジェクトをロードするには、Load() を使用します。 「場所」のような句を持つクエリーの LoadQuery() を使用して、[グループ] とします。 
    
4. ExecuteQuery() メソッドを使用して要求を実行します。
    
   ExecuteQuery() メソッドは、クエリまたはクエリは、実行する準備ができましたをホストに通知します。 通知を受信すると、ホスト、クエリを実行し、結果をクライアントに送信します。 
    
クライアントに情報を含む、アプリケーションで使用します。 次のコードは順に発行されたプロジェクトとホストで公開されている各プロジェクトの名前と Id を印刷します。
  
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

出力します。
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>要求を行う

前のコードからアクションを使用するアプリケーションは、ホスト サイトで指定されたアカウント内のプロジェクトのリストを取得します。 
  
1. プロジェクトを一覧表示するため、ProjectContext を指定します。 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. 取得する項目を指定します。 
    
   ```cs
    projContext.Load(projects);
   ```

   コレクションをのみを示すでは、サーバーは、既定のプロパティのセットの値を持つ各プロジェクトを作成、プロジェクト コレクションを取得します。 既定のプロパティ セットの一部であるプロパティにアクセスするには、正常な結果が得られます。 「初期化されていません」の例外の結果を設定する既定値の一部ではないプロパティにアクセスします。
    
3. 要求 (projContext.Load) をロードします。
    
   これは、前の手順の一部です。
    
4. (ExecuteQuery) のクエリを実行します。 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>高度なプロジェクト情報を取得します。

プロパティを既定ではないプロパティは、サーバーへの要求で指定する必要があります。 次のコード フラグメントでは、前の例のように、プロジェクト コレクションのコンテキストを読み込みます。 次に、仕様は、結果に含める追加の既定以外のプロパティを要求します。 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

Load ステートメントは、プロジェクト コレクションのコンテキストを指定し、クエリの結果を開始日、フェーズとステージを追加します。 追加のプロパティは、スカラー、またはオブジェクトのコレクションです。 スカラーのアイテムに直接アクセスできます。 オブジェクトとコレクションの次のコード片に示すように、追加の処理が必要です。
  
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

最初の 3 つのプロジェクトの出力:
  
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

### <a name="retrieve-all-tasks-in-a-project"></a>プロジェクト内のすべてのタスクを取得します。

各プロジェクトには、多くのタスクがあります。 したがって、1 つのプロジェクトのタスクをプルは、以下の。
  
1. プロジェクト コレクションのコンテキストを確立します。
    
   ```cs
    var projects = projContext.Projects;
   ```

2. タスクのプロパティを含む、プロジェクト情報を取得します。
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    アプリケーションが公開されているプロジェクトをアドレス指定するに注意してください。 現在の発行済みプロジェクトのコンテキストとは、pubProj です。 
    
3. Tasks コレクションのコンテキストを確立します。
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   `pubProj.Tasks`プロパティは、現在公開されているプロジェクトのタスクを参照します。 
    
4. 適切な既定以外のプロパティを含め、タスクのコレクションを取得するために仕様をロードします。
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. 適切なプロパティを使用してタスクのコレクションを取得するクエリを実行します。
    
   ```cs
    projContext.ExecuteQuery();
   ```

情報がローカルではようになりました。 次のコードは、コンソールに情報を記述することによって公開されているタスクのコレクションを処理します。
  
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

1 つのプロジェクトのタスクの出力:
  
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

### <a name="access-information-at-multiple-levels"></a>複数のレベルでのアクセス情報

各タスク (別名で 1 つまたは複数の担当者を持つことができます。 リソース) は、その終了時に貢献しています。 割り当てとリソースのコレクションには、タスクごとにこの情報が含まれています。 
  
処理は、次ので構成されます。
  
1. プロジェクトのタスクのコンテキストを取得します。
    
2. 要求を作成し、タスクに関連付けられている割り当ての要求をロードします。 
    
3. 割り当てに対してクエリを実行します。
    
4. 要求を作成し、個々 の割り当てに関連付けられているリソースの要求をロードします。 
    
5. リソースのクエリを実行します。
    
> [!NOTE] 
> - Tasks コレクションの既定のプロパティではないために、サーバーからの情報の割り当てのコレクションが明示的に要求します。 コレクションとしては、以降のクエリは、サーバーからコレクションを取得するのには作成されます。 
> - リソースは、オブジェクトです。 割り当てのクエリには、割り当てに関連付けられているリソース名が含まれています。
    
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

52、75、76 のプロジェクトのタスクの出力:
  
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

### <a name="access-custom-enterprise-level-fields"></a>カスタムのエンタープライズ レベルのフィールドのアクセス

オンライン プロジェクトのカスタム フィールドが存在します。 これらは、個々 のプロジェクトに関連付けることができるエンタープライズ ・ レベルのフィールドです。 このセクションでは、これらのフィールドにアクセスする方法について説明します。 
  
ユーザー設定フィールドは、プロジェクトに関連付けられているプロパティの既定のセットには含まれていません。 そのため、取得の仕様で明示的な id が必要です。 プロセスの高度なビューは、次の項目で構成されます。
  
1. 共通名を使用してユーザー設定フィールドにトンネルします。
    
2. ユーザー設定フィールドの内部名を取得します。
    
3. グローバル コンテキストに戻るし、ユーザー設定フィールドの内部名を使用してシステムを照会します。
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>ユーザー設定フィールドにトンネル、その内部の名前を取得およびシステムのクエリを実行するために使用

このタスクは、既定以外のプロパティを使用して詳細を 1 つ追加と取得を指定します。
  
1. この資料の冒頭で説明したように、プロジェクトのコンテキストを使用して開始します。
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. プロジェクト コレクションへの検索要求だけでなく他の既定以外のプロパティを取得するには、2 つの項目を追加します。
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   `p => p.IncludeCustomFields`句は、ユーザー設定フィールドをサポートするプロジェクトのオブジェクトを使用する必要性を識別します。 
    
   `p => p.IncludeCustomFields.CustomFields`句は、クエリ結果内のカスタム フィールドのデータを含めることを要求します。 ユーザー設定フィールドの内部名を取得した後、この情報が使用されます。 
    
3. 要求をロードします。
    
   これは、前の手順の一部です。
    
4. クエリを実行します。
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. クライアント上でこの情報を現在のプロジェクトに関連付けられているユーザー設定フィールドを取得する要求を構築します。
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. 適切なユーザー設定フィールドを検索し、フィールドの内部名を取得します。 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   ユーザー設定フィールドの内部名を取得します。 高レベルの項目 1 と 2 が完了しました。
    
7. プロジェクトのコンテキストに戻るし、ユーザー設定フィールドの値を取得します。
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > インデックスとしての内部名を使用してユーザー設定フィールドの値が取得されます。 
  
プロジェクト ID、プロジェクト名、ユーザー設定フィールド名、ユーザー設定フィールドの内部名、およびユーザー設定フィールドの値で構成される 3 つのプロジェクトの出力をします。
  
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

## <a name="see-also"></a>関連項目

ドキュメントとオンライン プロジェクトと CSOM を使用したアプリケーション開発に関連するサンプルでは、[プロジェクト開発のポータル](https://developer.microsoft.com/en-us/project)を参照してください。
    

