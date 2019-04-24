---
title: クライアント側オブジェクト モデルを使用して Project Online アプリケーションを開発する
manager: soliver
ms.date: 11/08/2016
ms.audience: Developer
ms.assetid: 5740d0b2-5d36-40e4-9e83-577cb186359f
description: この記事では、.NET Framework 4.0 を使用して行うデスクトップ アプリケーション用の Microsoft Project Online アプリケーションの開発について説明します。 この記事で説明されているアプリケーションは、ホスト サーバーから情報を取得します。
localization_priority: Priority
ms.openlocfilehash: 3d3c2dd5b896c10dab9a0494288f38610cbc99e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322623"
---
# <a name="developing-a-project-online-application-using-the-client-side-object-model"></a>クライアント側オブジェクト モデルを使用して Project Online アプリケーションを開発する

この記事では、.NET Framework 4.0 を使用して行うデスクトップ アプリケーション用の Microsoft Project Online アプリケーションの開発について説明します。 この記事で説明されているアプリケーションは、ホスト サーバーから情報を取得します。 
  
## <a name="background"></a>背景

Microsoft Project は、1990 年代初期にデスクトップ アプリケーションとして始まりました。 現在、Project には次のような種類があります。
  
- Project Standard エディションは、単体のアプリケーションとして実行されるデスクトップ アプリケーションです。
    
- Project Professional エディションは、大きなスケールでサーバーと対話したりデータを共有したりできるデスクトップ アプリケーションであり、Project Standard エディションの機能も実行できます。
    
- Project Online は、Microsoft でホストされるサービスであり、プロジェクト、プログラム、ポートフォリオを調整および管理するための PMO レベルのソリューションを企業に提供します。 デスクトップ エディションとは異なる製品である Project Online は、プロジェクトの期間全体を通してプロジェクトの詳細を管理および追跡できます。 
    
- Project Server は企業でホストされるサービスであり、プロジェクト、プログラム、ポートフォリオに関する情報が含まれるサーバーの管理とセキュリティ保護は企業において行われます。 社内でサーバーのセキュリティ保護を行うことにより、Project Server では、外部でホストされる Project Online のプロジェクト、プログラム、ポートフォリオ指向の機能と一緒に、優れたカスタマイズ機能も提供されます。
    
Project Online には、クライアント側オブジェクト モデル (CSOM)、JavaScript オブジェクト モデル (JSOM)、Representational State Transfer (REST) という 3 種類のオンライン API セットがあります。 
  
- Project Online テナントとやり取りする Windows アプリケーションを開発するときは、.NET CSOM の実装が推奨されるインターフェイスです。 ユーザー中心アプリケーションの典型的な環境には、Windows デスクトップと Microsoft Surface デバイスが含まれます。 .NET CSOM で記述されたバックエンド アプリケーションは、Project Online の外部にある、ビジネス ロジックおよびデータ ソース用の他のサーバーに接続できます。 Project Online に対する取得要求では、基本的な取得機能よりいくつかの点で強化されている、LINQ に似たクエリ システムを使用します。
    
- JavaScript オブジェクト モデル (JSOM) インターフェイスでは、Project Online アドインに対するクロスブラウザーのサポートが提供されます。アドインは、Project Online テナントに格納されている Web アプリケーションです。 ユーザーがアドインを実行しようとすると、アドインのコードがダウンロードされて、ユーザーのコンピューターのブラウザーで実行されます。 
    
- REST/Odata モデルでは、HTTP ベースの通信が提供されます。このインターフェイスは、Windows 以外の環境でのアプリケーションの場合に推奨されます。 通信エンドポイントは、Project Web アプリケーション (PWA) サイト内のオブジェクトです。 結果では、標準の HTTP 状態コードが提供されます。
    
この記事では、.NET CSOM インターフェイスを使用するアプリケーションについて説明します。
  
## <a name="prerequisites"></a>前提条件

Windows 10 を実行するベース システムから始めて、次の項目を追加します。
  
- .Net framework 4.0 以降 -- 完全なフレームワークを使用します。 ダウンロード サイトは https://msdn.microsoft.com/vstudio/aa496123.aspx です。
    
- Visual Studio 2013 以降 -- どのエディションでもかまいません。 サンプル アプリケーションの開発には、Visual Studio 2015 の Community エディションを使用しました。 Community エディションは https://www.visualstudio.com/en-us/products/visual-studio-community-vs.aspx で入手できます。
    
- SharePoint クライアント コンポーネント SDK -- Project Online と Project Server は、SharePoint および SharePoint アセンブリの上にあります。 SharePoint クライアント コンポーネントは、Visual Studio の Professional エディションと Enterprise エディションに含まれています。 Visual Studio Community エディションを使用する場合は、最新バージョンの Office Developer Tools SDK を https://www.microsoft.com/en-us/download/details.aspx?id=35585 で入手できます。
    
- Project Online アカウント -- ホスティング サイトにアクセスできるようになります。 Project Online アカウントの入手の詳細については、https://products.office.com/en-us/Project/project-online-portfolio-management をご覧ください。
    
- ホスティング サイト上の情報設定済みプロジェクト
    
> [!NOTE]
> 標準の .NET Framework (4.0 以降) が、使用するのに適切なフレームワークです。 .NET Framework 4 Client Profile は使用しないでください。 
  
## <a name="develop-the-application"></a>アプリケーションを開発する

SharePoint 向けデスクトップ アプリケーションの開発で推奨されるインターフェイスは、Project クライアント側オブジェクト モデル (CSOM) です。 
  
完全なサンプルは、https://github.com/OfficeDev/Project-CSOM-List-Projects-Tasks でダウンロードできます。
  
最初の 2 つのトピックでは、基本的な事項、つまり適切な名前空間とアセンブリを使用した Visual Studio プロジェクトの作成と、ホスティング サーバーへのアクセスについて説明します。 残りのトピックでは、1 つのオブジェクトおよび多数のオブジェクトからの、CSOM 経由での情報の取得について説明します。 
  
ホストからの情報の取得は、クライアント アプリケーションからの 2 アクション プロセスです。 最初に、アプリケーションで 1 つまたは複数の取得要求を指定してサーバーに送信します。 次に、アプリケーションでサーバーに通知を発行して、送信されたクエリを実行します。 サーバーは、クエリの結果をクライアントに送信することで応答します。
  
### <a name="set-up-the-visual-studio-project"></a>Visual Studio プロジェクトを設定する

アプリケーションのセットアップは、新しいプロジェクトの作成、適切なアセンブリのリンク、必要な名前空間の宣言で構成されます。 Visual Studio では、複数の種類の開発プロジェクトが提供されています。 
  
#### <a name="select-a-visual-studio-project"></a>Visual Studio プロジェクトを選択する

1. Visual Studio を起動し、開始ページで [**新しいプロジェクトの開始**] を選択します。 
    
   [新しいプロジェクト] ダイアログ ボックスでは、使用可能なアプリケーション テンプレートと、選択したテンプレートのデータ フィールドが表示されます。 
    
2. このアプリケーションでは、次の項目を指定します。 画面に表示されるキーワードは太字です。
    
   1. 左側のウィンドウのインストール済みテンプレートから、[**C#**]、[**Windows**]、[**従来のデスクトップ**] の順に選択します。 
    
   2. 中央のウィンドウの上部で、[**.NET Framework 4**] を選択します。 
    
   3. 中央のウィンドウのアプリケーションの種類から、[**コンソール アプリケーション**] を選択します。 
    
   4. 下部のセクションで、プロジェクトの名前と場所、ソリューション名を指定します。 
    
   5. また、下部のセクションで、[**ソリューションのディレクトリを作成**] ボックスがオンになっていることを確認します。 
    
3. [**OK**] をクリックして、初期プロジェクトを作成します。 
    
#### <a name="add-assemblies"></a>アセンブリを追加する

VS ソリューションには、Project 2103 SDK の ProjectServerClient アセンブリ、SharePoint SDK のいくつかのアセンブリ、および .NET Framework System.Security アセンブリが必要です。
  
1. VS のソリューション エクスプローラーで、[参照] エントリを右クリックして、[**参照の追加**] を ショートカット メニューから選択します。 
    
2. **Microsoft.ProjectServer.Client.dll** をクリックします。 
    
   必要な場合は、[**参照**] ボタン (ダイアログの下部) をクリックし、Project 2013 SDK のインストール ディレクトリに移動してアセンブリを見つけます。 
    
3. [**OK**] をクリックします。 
    
4. PrjoctServer クライアント名前空間を .cs ファイルに追加します。
    
   ```cs
    using Microsoft.ProjectServer.Client;
   ```

NuGet パッケージ マネージャー コンソールを使用して、SharePoint 2013 SDK アセンブリを追加します。 
  
1. VS の [ツール] メニューから、**[ツール] =\> [NuGet パッケージ マネージャー] =\> [パッケージ マネージャー コンソール]** の順にクリックします。 
    
2. パッケージ マネージャー コンソールで、次のコマンドを入力して \<Enter\> キーを押します。
    
   ```cs
    Install-Package Microsoft.SharePointOnline.CSOM
   ```

   **パッケージ マネージャー コンソール**ではコマンドの結果の説明が提供され、VS ソリューション エクスプローラーではプロジェクト参照内の SharePoint アセンブリが表示されます。 
    
3. .cs ファイルに名前空間を追加します。
    
   ```cs
    using Microsoft.SharePoint.Client;
   ```

System.Security アセンブリは .NET Framework の一部で、フレームワークと共にインストールされています。 サンプル アプリケーションには、認証のため、ホスティング システムに暗号化された文字列を提供する名前空間が 1 つ以上必要です。 認証が済むと、アプリケーションはホスティング システム上のプロジェクトにアクセスできます。 次の方法で、.cs ファイルに System.Security 名前空間を追加します。
  
1. VS のソリューション エクスプローラーで、[参照] エントリを右クリックして、[**参照の追加**] を ショートカット メニューから選択します。 
    
2. [参照マネージャー] ダイアログの左側のウィンドウで **[アセンブリ] =\> [Framework]** を選択し、**System.Security** をオンにします。 
    
3. [**OK**] をクリックします。 
    
4. .cs ファイルに System.Security 名前空間を追加します。
    
   ```cs
    using System.Security;
   ```

.cs ファイルの先頭に、次の名前空間が含まれている必要があります。
  
- System
    
- System.Collections.Generic
    
- System.Linq
    
- System.Test
    
- Microsoft.ProjectServer.Client
    
- Microsoft.SharePoint.Client
    
- System.Security
    
### <a name="connect-to-the-host-system"></a>ホスト システムに接続する

Project Online は SharePoint アプリケーションなので、SharePoint 認証を使用するのが適切なアプローチです。 次のコード フラグメントでは、ホストされている環境へのアクセスの準備をします。
  
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

ホストされている環境へのアクセスの準備には、次の項目が含まれます。
  
1. プロジェクト用のコンテキスト オブジェクトを作成する -- これは、上で示したコード フラグメントの次のコードに含まれます。 
    
   ```cs
    private static ProjectContext projContext;
    
   ```

   コンテキストは他のコンポーネントによって継承されるので、システムで Project オブジェクト モデルのコンテキストを管理できます。
    
2. ホスト サイトを識別する -- これは、上で示したコード フラグメントの次のコードで行われます。
    
   ```cs
    using (ProjectContext projContext = new ProjectContext("https://Contoso.sharepoint.com/sites/pwa"))
   ```

   プロジェクトのコンテキストをインスタンス化する場合、アプリケーションでは Projects サイト コレクションのルートを提供する必要があります。 アプリケーションでは、Projects のルートの URL の部分文字列を使用します。 次の図では、この場所のスナップショットが赤い四角形で強調表示されています。 認証には、文字列の先頭から部分文字列 "pwa" までの部分が必要です。 コードのリストでは、"https://XXXXXXXX.sharepoint.com/sites/pwa" という文字列が使用されています。
        
   ![赤い枠線で囲まれた Projects サイト コレクションの URL のスクリーン ショット。](media/d48c4894-5dba-46b6-886a-3c59bfb83c4d.png "赤い枠線で囲まれた Projects サイト コレクションの URL のスクリーン ショット。")
  
3. セキュリティ保護された文字列にパスワードを配置する -- これは、上で示したコード フラグメントの次のコードで行われます。
    
   ```cs
    SecureString password - new SecureString();
    foreach (char c in "password".ToCharArray()) password.AppendChar(c);
    
   ```

   パスワードとユーザー アカウントは、ホスト サイトにアクセスするための資格情報です。 
    
4. コンテキスト オブジェクトの資格情報の部分にユーザー アカウントとパスワードを追加する -- これは、上で示したコード フラグメントの次のコードで行われます。
    
   ```cs
    projContext.Credentials = new SharePointOnlineCredentials("sarad@Contoso.onmicrosoft.com", password);
   ```

インスタンス化されたプロジェクト コンテキストを使用する準備ができました。
  
### <a name="list-all-published-projects"></a>すべての発行済みプロジェクトの一覧を表示する

Project Online と Project Server は、作成、レポート、更新、削除 (CRUD) の操作のために、プロキシを使用してサーバーと通信します。 ホストとサーバーでは効率的な方法で要求が処理され、クライアントはサーバーとの通信で次の操作を実行します。
  
1. 通信のためのコンテキストを確立します。 
    
   コンテキストは、プロジェクト コレクションによって使用されるだけでなく、継承によってタスク コレクション、割り当てコレクション、ステージ オブジェクト、カスタム フィールドなどの他のオブジェクトとコレクションでも使用されます。 
    
2. オブジェクト モデルを使用して、取得するオブジェクト、コレクション、またはデータを指定します。
    
   このステップでは、クエリまたはメソッドとして LINQ を使用します。 指定によって受け取るものを制御します。 多くの場合、このステップは Load メソッド (ステップ 3) の本文に埋め込まれます。 
    
3. Load() または LoadQuery() メソッドを使用して、前のステップから取得の指定を読み込みます。
    
   コレクションとオブジェクトを読み込むには、Load() を使用します。 "where" や "group" などの句を含むクエリの場合は、LoadQuery() を使用します。 
    
4. ExecuteQuery() メソッドを使用して、要求を実行します。
    
   ExecuteQuery() メソッドにより、クエリを実行する準備ができたことがホストに通知されます。 ホストは、通知を受け取ると、クエリを実行して、結果をクライアントに送信します。 
    
情報がクライアントに届いたら、アプリケーションでそれを使用できます。 次のコード フラグメントでは、発行済みのプロジェクトを反復処理して、ホスト上の各発行済みプロジェクトの ID と名前を出力します。
  
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

出力:
  
```cs
Published Project count:2
1. be80a848-b2ef-e511-80f4-00155dc84e01   A second Project     3/21/2016 10:14:40 PM
2. 9d730a1a-60ed-e511-80f6-00155dc87d01   Ent_Proj_1   3/18/2016 11:21:14 PM

```

### <a name="make-a-request"></a>要求を行う

アプリケーションで、前記のコード フラグメントのアクションを使用して、ホスティング サイト上の指定したアカウントに含まれるプロジェクトの一覧を取得します。 
  
1. プロジェクトで一覧表示する ProjectContext を指定します。 
    
   ```cs
    var projects = projContext.Projects;
   ```

2. 取得する項目を指定します。 
    
   ```cs
    projContext.Load(projects);
   ```

   コレクションのみを指定することで、サーバーではプロジェクトのコレクションが取得されて、既定のプロパティのセットの値が各プロジェクトに設定されます。 既定のプロパティ セットに含まれているプロパティにアクセスすると、正常な結果が得られます。 既定のプロパティ セットに含まれていないプロパティにアクセスすると、結果は "初期化されていません" 例外になります。
    
3. 要求を読み込みます (projContext.Load)。
    
   これは、前のステップの一部です。
    
4. クエリを実行します (ExecuteQuery)。 
    
   ```cs
    projContext.ExecuteQuery();
   ```

### <a name="retrieve-high-level-project-information"></a>上位レベルのプロジェクト情報を取得する

既定のプロパティではないプロパティは、サーバーへの要求で指定する必要があります。 次のコード フラグメントでは、前の例のようにプロジェクト コレクションのコンテキストを読み込みます。 次に、結果に含める既定以外の追加プロパティを要求します。 
  
```cs
var projects = projContext.Projects;
projContext.Load(projects,
    ps => ps.IncludeWithDefaultProperties(
        p => p.StartDate, p => p.Phase, p => p.Stage));
projContext.ExecuteQuery();

```

Load ステートメントでプロジェクト コレクション コンテキストを指定し、StartDate、Phase、Stage をクエリ結果に追加します。 スカラー、オブジェクト、またはコレクションのプロパティを追加できます。 スカラー項目には直接アクセスできます。 オブジェクトとコレクションについては、次のコード フラグメントのように、追加の処理が必要です。
  
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

### <a name="retrieve-all-tasks-in-a-project"></a>プロジェクト内のすべてのタスクを取得する

各プロジェクトには多くのタスクが含まれます。 そのため、1 つのプロジェクトのタスクを取得する手順は次のとおりです。
  
1. プロジェクト コレクションのコンテキストを確立します。
    
   ```cs
    var projects = projContext.Projects;
   ```

2. タスクのプロパティを含む、プロジェクトの情報を取得します。
    
   ```cs
    projContext.Load(projects);
    ProjContext.ExecuteQuery();
    foreach (PublishedProject pubProj in projContext.Projects){
    
   ```

    アプリケーションで発行済みプロジェクトをアドレス指定していることに注意してください。 現在の発行済みプロジェクトのコンテキストは pubProj です。 
    
3. Tasks コレクションのコンテキストを確立します。
    
   ```cs
    PublishedTaskCollection collTask = pubProj.Tasks;
   ```

   `pubProj.Tasks` プロパティでは、現在の発行済みプロジェクトのタスクが参照されています。 
    
4. 既定以外の適切なプロパティを含む、Task コレクションを取得するための指定を読み込みます。
    
   ```cs
    projContext.Load(collTask,
        tsk => tsk.IncludeWithDefaultProperties(
            t => t.Id, t => t.Name, t => t.Start,
            t => t.ScheduledStart, t => t.Completion));
    
   ```

5. クエリを実行して、適切なプロパティを含む Task コレクションを取得します。
    
   ```cs
    projContext.ExecuteQuery();
   ```

情報がローカルに格納されます。 次のコード フラグメントでは、コンソールに情報を出力することによって、発行済みタスクのコレクションを処理します。
  
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

### <a name="access-information-at-multiple-levels"></a>複数のレベルで情報にアクセスする

各タスクには複数の担当者 (通称 リソース) が関わっていることがあります。 Assignments および Resources コレクションには、各タスクについてのこの情報が含まれます。 
  
処理の手順は次のとおりです。
  
1. プロジェクトのタスクのコンテキストを取得します。
    
2. タスクに関連付けられている割り当ての要求を作成して読み込みます。 
    
3. 割り当てに対するクエリを実行します。
    
4. 個々の割り当てに関連付けられているリソースの要求を作成して読み込みます。 
    
5. リソースに対するクエリを実行します。
    
> [!NOTE] 
> - Assignments コレクションは、Tasks コレクションの既定のプロパティではないため、サーバーからの情報で明示的に要求されます。 コレクションであるため、以降のクエリを実行し、サーバーからコレクションを取得します。 
> - Resource はオブジェクトです。 割り当てのクエリには、割り当てに関連付けられているリソース名が含まれます。
    
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

プロジェクトのタスク 52、75、76 に対する出力:
  
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

### <a name="access-custom-enterprise-level-fields"></a>エンタープライズ レベルのカスタム フィールドにアクセスする

Project Online にはカスタム フィールドが存在します。 これらはエンタープライズ レベルのフィールドであり、個々のプロジェクトと関連付けることができます。 このセクションでは、これらのフィールドにアクセスする方法について説明します。 
  
カスタム フィールドは、プロジェクトに関連付けられている既定のプロパティ セットには含まれません。 そのため、取得の指定で明示的に示す必要があります。 プロセスの上位レベルのビューは、次の項目で構成されます。
  
1. 共通名を使用してカスタム フィールドへのトンネル接続を確立します。
    
2. カスタム フィールドの内部名を取得します。
    
3. グローバル コンテキストに戻り、カスタム フィールドの内部名を使用して、システムのクエリを実行します。
    
#### <a name="tunnel-to-the-custom-field-retrieve-its-internal-name-and-used-it-to-query-the-system"></a>カスタム フィールドにトンネル接続して、その内部名を取得し、それを使用してシステムのクエリを実行する

このタスクでは、詳細を 1 つ追加した既定以外のプロパティを使用して取得を指定します。
  
1. この記事の冒頭で説明したように、プロジェクト コンテキストを使用して開始します。
    
   ```cs
    // Get the list of published projects in Project Web App.
    var projects = projContext.Projects;
    
   ```

2. 取得する他の既定以外のプロパティに加えて、2 つの項目をプロジェクト コレクション取得要求に追加します。
    
   ```cs
    projContext.Load(projects,
        ps => ps.IncludeWithDefaultProperties(
            p => p.Phase, p => p.Stage,                  // Other nondefault properties
            p => p.IncludeCustomFields,                  // Gets PublishedProject object 
                                                        // that contains custom fields
            p => p.IncludeCustomFields.CustomFields));   // Populates the custom fields
                    projContext.ExecuteQuery();
    
   ```

   `p => p.IncludeCustomFields` 句は、カスタム フィールドをサポートしているプロジェクト オブジェクトを使用する必要があるかどうかを識別します。 
    
   `p => p.IncludeCustomFields.CustomFields` 句は、クエリ結果にカスタム フィールドのデータを含めることを要求します。 カスタム フィールドの内部名を取得した後で、この情報を使用します。 
    
3. 要求を読み込みます。
    
   これは、前のステップの一部です。
    
4. クエリを実行します。
    
   ```cs
    projContext.ExecuteQuery()
   ```

5. クライアント上のこの情報を使用して、現在のプロジェクトに関連付けられているカスタム フィールドを取得する要求を作成します。
    
   ```cs
    foreach (PublishedProject pubProj in projContext.Projects)
    {
        //Console.WriteLine("\n\t{0}. \t{1} \n\t\t{2} \n\t\t{3} \n", 
                j++, pubProj.Id, pubProj.Name, pubProj.CreatedDate);
        CustomFieldCollection collCustF = pubProj.CustomFields;
                        
        projContext.Load(collCustF);
        projContext.ExecuteQuery();
    
   ```

6. 適切なカスタム フィールドを見つけて、フィールドの内部名を取得します。 
    
   ```cs
        foreach (CustomField oCF in collCustF)
        {
            if (oCF.Name == "Project Health")
            {
                Console.WriteLine("Name: {0}", oCF.Name);
                Console.WriteLine("InternalName: {0}", oCF.InternalName);
    
   ```

   カスタム フィールドの内部名が取得されます。 上位レベルの項目 1 と 2 が完了しました。
    
7. プロジェクトのコンテキストに戻り、カスタム フィールドの値を取得します。
    
   ```cs
    Console.WriteLine("Value: {0}", 
        pubProj.IncludeCustomFields.FieldValues[oCF.InternalName]);
    
   ```

   > [!NOTE]
   > 内部名をインデックスとして使用して、カスタム フィールドの値が取得されます。 
  
プロジェクト ID、プロジェクト名、カスタム フィールド名、カスタム フィールドの内部名、およびカスタム フィールドの値で構成される、3 つのプロジェクトの出力。
  
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

Project Online および CSOM を使用したアプリケーション開発に関するドキュメントとサンプルについては、[Project 開発ポータル](https://developer.microsoft.com/ja-JP/project)をご覧ください。
    

