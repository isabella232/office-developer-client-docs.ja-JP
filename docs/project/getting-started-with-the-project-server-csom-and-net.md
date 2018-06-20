---
title: Project Server CSOM および .NET の概要
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Project Server 2013 のクライアント側オブジェクト モデル (CSOM) を使用して、.NET Framework 4 でオンライン プロジェクトとオンプレミスのソリューションを開発することができます。 この資料は、CSOM を使用して作成し、プロジェクトを発行するコンソール アプリケーションを作成する方法について説明します。 プロジェクトを発行した後は、アプリケーションは、発行操作を完了するには、プロジェクト サーバー キュー サービスの待機し、発行済みのプロジェクトが一覧表示されています。
ms.openlocfilehash: 1815122ce824fcd2f9b8c9119346ca02c720ae89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804573"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a>Project Server CSOM および .NET の概要

Project Server 2013 のクライアント側オブジェクト モデル (CSOM) を使用して、.NET Framework 4 でオンライン プロジェクトとオンプレミスのソリューションを開発することができます。 この資料は、CSOM を使用して作成し、プロジェクトを発行するコンソール アプリケーションを作成する方法について説明します。 プロジェクトを発行した後は、アプリケーションは、発行操作を完了するには、プロジェクト サーバー キュー サービスの待機し、発行済みのプロジェクトが一覧表示されています。
  
プロジェクトのサーバー CSOM に全般的な概要については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。 CSOM 名前空間のリファレンス トピックでは、 [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)を参照してください。 
  
## <a name="creating-a-csom-project-in-visual-studio"></a>Visual Studio で CSOM プロジェクトを作成する
<a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a>

Visual Studio 2010 または Visual Studio 2012 を使用するには、プロジェクトのサーバー CSOM を使用するソリューションを開発します。 プロジェクトのサーバー CSOM には、.NET Framework 4 を使用して、クライアント アプリケーション、Microsoft Silverlight アプリケーション、および Windows Phone 8 アプリケーションを開発するための 3 つのアセンブリが含まれています。 CSOM には、web アプリケーションを開発するための JavaScript ファイルが含まれています[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)で説明されているようです。 
  
リモート開発用コンピューターに Project Server コンピューターから、または Project 2013 SDK ダウンロードから CSOM アセンブリする必要があることをコピーできます。 このトピックに記載されている**QueueCreateProject**のコンソール アプリケーションは、Silverlight アプリケーションや Windows Phone 8 アプリケーションでは、Microsoft.ProjectServer.Client.dll アセンブリを作成する必要があります。 CSOM は独立の WCF ベースまたは ASMX ベース プロジェクト Server インターフェイス (PSI) であるために、PSI のサービス参照を設定するか、 **Microsoft.Office.Project.Server.Library**名前空間を使用する必要はありません。 
  
**QueueCreateProject**アプリケーションは、キューのタイムアウトの制限を作成するプロジェクトの名前をコマンドライン引数を使用します。 手順 1 で、コマンドラインを解析するルーチンを追加、コマンド ・ ラインにエラーがある場合は、使用法のメッセージを追加する基本的なコンソール アプリケーションを作成します。 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a>手順 1. Visual Studio で CSOM プロジェクトを作成するには

1. Microsoft.ProjectServer.Client.dll アセンブリをコピー、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\`を開発用コンピューターのフォルダーです。 その他の Project Server および SharePoint の参照アセンブリに使用する、次のように、適当なフォルダーにアセンブリをコピー `C:\Project\Assemblies`。
    
2. Microsoft.SharePoint.Client.dll アセンブリと Microsoft.SharePoint.Client.Runtime.dll アセンブリを同じソース フォルダーから開発コンピューターにコピーします。Microsoft.ProjectServer.Client.dll アセンブリは関連する SharePoint アセンブリに依存します。
    
3. Visual Studio では、Windows コンソール アプリケーションを作成し、ターゲット フレームワークを.NET Framework 4 に設定します。 たとえば、QueueCreateProject アプリケーションの名前を付けます。
    
   > [!NOTE]
   > 忘れた場合は Visual Studio がプロジェクトを作成した後、適切なターゲットを設定するのには、 **[プロジェクト**] メニューの**QueueCreateProject プロパティ**を開きます。 [**アプリケーション**] タブで、**ターゲット フレームワーク**ドロップダウン ボックスの一覧で、 **.NET Framework 4**を選択します。 **.NET Framework 4 のクライアント プロファイル**を使用することはしません。 
  
4. ソリューション エクスプローラーで、次のアセンブリへの参照を設定します。
    
   - Microsoft.ProjectServer.Client.dll
   - Microsoft.SharePoint.Client.dll
   - Microsoft.SharePoint.Client.Runtime.dll
    
5. Program.cs ファイルに、編集、`using`ステートメントは、次のようにします。 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. プロジェクト名とキューのタイムアウト秒数を示すコマンド ライン引数を解析するメソッドを追加し、使用法の情報を表示して、アプリケーションを終了します。Program.cs ファイルのコードの本文を次のコードに置き換えます。
    
   ```cs
    namespace QueueCreateProject
    {
        class Program
        {
            static void Main(string[] args)
            {
                if (!ParseCommandLine(args))
                {
                    Usage();
                    ExitApp();
                }
                /* Add calls to methods here to get the project context and create a project. */
                ExitApp();
            }
            // Parse the command line. Return true if there are no errors.
            private static bool ParseCommandLine(string[] args)
            {
                bool error = false;
                int argsLen = args.Length;
                try
                {
                    for (int i = 0; i < argsLen; i++)
                    {
                        if (error) break;
                        if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                            args[i] = "*" + args[i].Substring(1).ToLower();
                        switch (args[i])
                        {
                            case "*projname":
                            case "*n":
                                if (++i >= argsLen) return false;
                                projName = args[i];
                                break;
                            case "*timeout":
                            case "*t":
                                if (++i >= argsLen) return false;
                                timeoutSeconds = Convert.ToInt32(args[i]);
                                break;
                            case "*?":
                            default:
                                error = true;
                                break;
                        }
                    }
                }
                catch (FormatException)
                {
                    error = true;
                }
                if (string.IsNullOrEmpty(projName)) error = true;
                return !error;
            }
            private static void Usage()
            {
                string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
                example += "\nExample: QueueCreateProject -n \"My new project\"";
                example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
                Console.WriteLine(example);
            }
            private static void ExitApp()
            {
                Console.Write("\nPress any key to exit... ");
                Console.ReadKey(true);
                Environment.Exit(0);
            }
        }
    }
   ```

## <a name="getting-the-project-context"></a>プロジェクトのコンテキストを取得する
<a name="pj15_GettingStartedCSOM_GettingContext"> </a>

CSOM の開発には、Project Web App の URL を使用して初期化する**ProjectContext**オブジェクトが必要です。 手順 2 のコードは、 **pwaPath**定数を使用します。 Project Web App の複数のインスタンスのアプリケーションを使用する場合は、変数を**pwaPath**にしてもう 1 つのコマンドライン引数を追加するでした。 
  
### <a name="procedure-2-to-get-the-project-context"></a>手順 2. プロジェクトのコンテキストを取得するには

1. クラスの定数を**プログラム**し、 **QueueCreateProject**アプリケーションを使用する変数を追加します。 Project Web App の URL だけでなくアプリケーションを使用して既定のエンタープライズ プロジェクトの種類 (EPT) の名前、名前のプロジェクトを作成して、キューの最大タイムアウト (秒単位)。 この例では、 **timeoutSeconds**変数を使用すると、タイムアウトの値をさまざまな方法に影響を与えるアプリケーションをテストできます。 **ProjectContext**オブジェクトは、プライマリ オブジェクト、CSOM にアクセスするためです。 
    
   ```cs
    private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. 交換、`/* Add calls to methods here to get the project context and create a project. */`を次のコードのコメント。 **Microsoft.ProjectServer.Client.ProjectContext**オブジェクトは Project Web App の URL を使用して初期化します。 手順 4 と手順 5 では、 **CreateTestProject**メソッドと**ListPublishedProjects**メソッドが表示されます。 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a>エンタープライズ プロジェクトの種類を取得する
<a name="pj15_GettingStartedCSOM_GettingEPT"> </a>

**QueueCreateProject**サンプル アプリケーションでは、エンタープライズ プロジェクト EPT のアプリケーションがプロジェクトの EPT を選択する方法を表示するのには、明示的に選択します。 プロジェクトの作成については、EPT の GUID を指定しない場合、アプリケーションは、既定の EPT を使用します。 **GetEptUid**メソッドは、手順 4 に記載されている**CreateTestProject**メソッドによって使用されます。 
  
**GetEptUid**メソッドは、EPT の名前が指定された名前に相当する、 **EnterpriseProjectTypes**のコレクションの**ProjectContext**オブジェクトを照会します。 クエリを実行した後は、 **eptUid**変数は、 **eptList**コレクション内の最初の**EnterpriseProjectType**オブジェクトの GUID に設定されます。 EPT の名前は一意であるため、指定された名前を持つ 1 つの**EnterpriseProjectType**オブジェクトがあります。 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a>手順 3. 新しいプロジェクトの EPT の GUID を取得するには

- **プログラム**のクラスに**GetEptUid**メソッドを追加します。 
    
   ```cs
    // Get the GUID of the specified enterprise project type.
    private static Guid GetEptUid(string eptName)
    {
        Guid eptUid = Guid.Empty;
        try
        {
            // Get the list of EPTs that have the specified name. 
            // If the EPT name exists, the list will contain only one EPT.
            var eptList = projContext.LoadQuery(
                projContext.EnterpriseProjectTypes.Where(
                    ept => ept.Name == eptName));
            projContext.ExecuteQuery();
            eptUid = eptList.First().Id;
        }
        catch (Exception ex)
        {
            string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                eptName, ex.GetBaseException().ToString());
            throw new ArgumentException(msg);
        }
        return eptUid;
    }
   ```

EPT の GUID を検索するのにはいくつかの方法があります。 EPT 名に一致する 1 つの**EnterpriseProjectType**オブジェクトのみをダウンロードするため、 **GetEptUid**メソッドに示すようにクエリが効率的です。 次の代替ルーチンは、EPTs の完全な一覧をクライアント アプリケーションにダウンロードし、リストを反復処理するため、効率が低下します。 

```cs
foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
{
    if (ept.Name == eptName)
    {
        eptUid = ept.Id;
        break;
    }
}
```

次のルーチンは EPT オブジェクトを選択するのには、LINQ クエリ式とラムダ式を使用してですが、まだすべての**EnterpriseProjectType**オブジェクトをダウンロードします。 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a>作成情報を設定し、プロジェクトを発行する
<a name="pj15_GettingStartedCSOM_ProjectCreation"> </a>

**CreateTestProject**メソッドでは、 **ProjectCreationInformation**オブジェクトを作成し、プロジェクトを作成するために必要な情報を指定します。 プロジェクト GUID と名前が必要です。開始日、プロジェクトの説明、および GUID の EPT はオプションです。 
  
新しいプロジェクトのプロパティを設定した後は、 **Projects.Add**メソッドは、**プロジェクト**コレクションにプロジェクトを追加します。 保存し、プロジェクトを発行、Project Server キューにメッセージを送信し、プロジェクトを作成するには、 **Projects.Update**メソッドを呼び出す必要があります。 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a>手順 4. 新しいプロジェクトのプロパティを設定し、プロジェクトを作成して、発行するには

1. **プログラム**のクラスに**CreateTestProject**メソッドを追加します。 次のコードは作成されますが、プロジェクトを発行し、キュー ジョブが完了するまで待機しません。 
    
   ```cs
    // Create a project.
    private static bool CreateTestProject()
    {
        bool projCreated = false;
        try
        {
            Console.Write("\nCreating project: {0} ...", projName);
            ProjectCreationInformation newProj = new ProjectCreationInformation();
            newProj.Id = Guid.NewGuid();
            newProj.Name = projName;
            newProj.Description = "Test creating a project with CSOM";
            newProj.Start = DateTime.Today.Date;
            // Setting the EPT GUID is optional. If no EPT is specified, Project Server  
            // uses the default EPT. 
            newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
            PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
            QueueJob qJob = projContext.Projects.Update();
            /* Add code here to wait for the queue. */
        }
        catch(Exception ex)
        {
            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("\nError: {0}", ex.Message);
            Console.ResetColor();
        }
        return projCreated;
    }
   ```

2. 交換、`/* Add code here to wait for the queue. */`キュー ジョブを待機する次のコードにコメントします。 ルーチンでは、最大秒数を指定した**timeoutSeconds**を待機するか、タイムアウトする前にキューのジョブが終了した場合に行われます。 キュー ジョブの状態は、 [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx)を参照してください。 
    
   **QueueJob**オブジェクトの**Load**メソッドと、 **ExecuteQuery**メソッドを呼び出すことは、省略可能です。 **WaitForQueue**メソッドを呼び出すときに、 **QueueJob**オブジェクトが初期化されていない場合は、Project Server によって初期化します。 
    
   ```cs
    // Calling Load and ExecuteQuery for the queue job is optional.
    // projContext.Load(qJob);
    // projContext.ExecuteQuery();
    JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    if (jobState == JobState.Success)
    {
        projCreated = true;
    }
    else
    {
        Console.ForegroundColor = ConsoleColor.Yellow;
        Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
            timeoutSeconds);
        Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
        Console.ResetColor();
    }
    Console.WriteLine();
   ```

## <a name="listing-the-published-projects"></a>発行されたプロジェクトを一覧表示する
<a name="pj15_GettingStartedCSOM_ListingPublished"> </a>

**ListPublishedProjects**メソッドは、Project Web App で公開されているすべてのプロジェクトのコレクションを取得します。 キューのジョブを作成する場合は手順 4 で、プロジェクトが正常に完了しないか、タイムアウト、新しいプロジェクトが**プロジェクト**コレクションに含まれていません。 
  
### <a name="procedure-5-to-list-the-published-projects"></a>手順 5. 発行したプロジェクトを一覧表示するには

1. **プログラム**のクラスに**ListPublishedProjects**メソッドを追加します。 
    
   ```cs
    // List the published projects.
    private static void ListPublishedProjects()
    {
        // Get the list of projects on the server.
        projContext.Load(projContext.Projects);
        projContext.ExecuteQuery();
        Console.WriteLine("\nProject ID : Project name : Created date");
        foreach (PublishedProject pubProj in projContext.Projects)
        {
            Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                pubProj.CreatedDate.ToString());
        }
    }
   ```

2. Project Web App の URL の正しい値を設定、 **QueueCreateProject**アプリケーションをコンパイルし、手順 6 のようにアプリケーションをテストします。 
    
## <a name="testing-the-queuecreateproject-application"></a>QueueCreateProject アプリケーションをテストする
<a name="pj15_GettingStartedCSOM_Testing"> </a>

とき、最初に、Project Web App のテスト インスタンスの**QueueCreateProject**アプリケーションを実行すると、バーチャル マシンでは、Project Server がインストールされている場合に特に、アプリケーション必要がありますより多くの時間を 10 秒間の既定のキューのタイムアウトよりも実行します。 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a>手順 6. QueueCreateProject アプリケーションをテストするには

1. **QueueCreateProject のプロパティ**] ウィンドウを開き、[**デバッグ**] タブを選択し、[**開始オプション**] セクションで、次のコマンドライン引数を追加します。`-n "Test proj 1" -t 20`
    
   アプリケーションを実行 (たとえば、 **f5 キー**を押します)。 タイムアウト値が十分に長い場合、アプリケーションは、次の出力を示しています (その他の発行済みプロジェクトは、Project Web App インスタンスに存在する場合にも表示されます)。
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. 10 秒あたりのキューのタイムアウトの既定値を使用するのには、以下のコマンドライン引数を持つ別のテストを実行します。`-n "Test proj 1"`
    
   Test proj 1 は既に存在するため、アプリケーションは次の結果を表示します。
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. 10 秒あたりのキューのタイムアウトの既定値を使用するのには、以下のコマンドライン引数を持つ別のテストを実行します。`-n "Test proj 2"`
    
   **QueueCreateProject**アプリケーションは、作成し、テスト プロジェクト 2 の名前のプロジェクトを発行します。 
    
4. 次のコマンドライン引数を指定するには、別のテストを実行し、タイムアウト時間を終了するに対して短すぎるのキュー ジョブを設定します。`-n "Test proj 3" -t 1`
    
   キューのタイムアウトが短すぎるため、プロジェクトは作成されません。アプリケーションは次の結果を表示します。
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. キュー ジョブのアプリケーションが待機しないようにコードを変更します。 以外のキューに待機するコードをコメントなどの`projCreated = true`行に、次のようにします。 
    
   ```cs
    //JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
    //if (jobState == JobState.Success)
    //{
    projCreated = true;
    //}
    //else
    //{
    //    Console.ForegroundColor = ConsoleColor.Yellow;
    //    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.",
    //        timeoutSeconds);
    //    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
    //    Console.ResetColor();
    //}
    
   ```

6. アプリケーションを再コンパイルし、次のコマンドライン引数を持つ別のテストを実行します。`-n "Test proj 4"`
    
   **WaitForQueue**ルーチンがコメント アウトされているため、アプリケーションは既定のタイムアウト値を使用しません。 アプリケーションがキューを待っていない場合でも、Project Server に発行操作が十分に高速の場合、テスト プロジェクト 4 を表示ことがあります。 
    
   ```MS-DOS
    Creating project: Test proj 4 ...
    Project ID : Project name : Created date
            cdd54103-082f-425c-b075-9ff52ac7d4e6 :
            Test proj 2 : 9/25/2011 4:28:55 PM
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
            5c0c73f2-f5dd-499b-8bd8-ebb74bf8c122 :
            Test proj 4 : 9/25/2011 4:39:21 PM
    Press any key to exit...
   ```

Project Web App の [プロジェクト センター] ページを更新 (`http://ServerName/ProjectServerName/Projects.aspx`)、発行済みのプロジェクトを表示します。 次の図は、テスト プロジェクトが発行されたことを示します。

**Project Web App での発行済みのプロジェクトをチェック**

![Project Web App での発行済みのプロジェクトをチェック](media/pj15_GetStartedCSOMNET_pwa.gif "Project Web App での発行済みのプロジェクトをチェック")
  
**QueueCreateProject**サンプル アプリケーションは、CSOM で**ProjectCreationInformation**クラスを使用して、プロジェクトのエンティティを作成する方法の一般的な例を示しています、公開されているコレクションにプロジェクトを追加する方法でのキュー ジョブを待機する方法**WaitForQueue**メソッド、および発行済みプロジェクトのコレクションを列挙する方法を使用します。 
  
## <a name="complete-code-example"></a>完全なコード例
<a name="pj15_GettingStartedCSOM_CompleteCode"> </a>

**QueueCreateProject**サンプル アプリケーションの完全なコードを次に示します。 [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx)クラスの参照には、このトピックのコードも含まれています。 
  
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Microsoft.ProjectServer.Client;
namespace QueueCreateProject
{
    class Program
    {
        private const string pwaPath = "http://ServerName /pwa/"; // Change the path to your Project Web App instance.
        private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
        private static string projName = string.Empty;
        private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
        private static ProjectContext projContext;
        static void Main(string[] args)
        {
            if (!ParseCommandLine(args))
            {
                Usage();
                ExitApp();
            }
            projContext = new ProjectContext(pwaPath);
            if (CreateTestProject())
                ListPublishedProjects();
            else
                Console.WriteLine("\nProject creation failed: {0}", projName);
            ExitApp();
        }
        // Create a project.
        private static bool CreateTestProject()
        {
            bool projCreated = false;
            try
            {
                Console.Write("\nCreating project: {0} ...", projName);
                ProjectCreationInformation newProj = new ProjectCreationInformation();
                newProj.Id = Guid.NewGuid();
                newProj.Name = projName;
                newProj.Description = "Test creating a project with CSOM";
                newProj.Start = DateTime.Today.Date;
                // Setting the EPT GUID is optional. If no EPT is specified, Project Server uses 
                // the default EPT. 
                newProj.EnterpriseProjectTypeId = GetEptUid(basicEpt);
                PublishedProject newPublishedProj = projContext.Projects.Add(newProj);
                QueueJob qJob = projContext.Projects.Update();
                // Calling Load and ExecuteQuery for the queue job is optional. If qJob is 
                // not initialized when you call WaitForQueue, Project Server initializes it.
                // projContext.Load(qJob);
                // projContext.ExecuteQuery();
                JobState jobState = projContext.WaitForQueue(qJob, timeoutSeconds);
                if (jobState == JobState.Success)
                {
                    projCreated = true;
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.Yellow;
                    Console.WriteLine("\nThere is a problem in the queue. Timeout is {0} seconds.", 
                        timeoutSeconds);
                    Console.WriteLine("\tQueue JobState: {0}", jobState.ToString());
                    Console.ResetColor();
                }
                Console.WriteLine();
            }
            catch(Exception ex)
            {
                Console.ForegroundColor = ConsoleColor.Red;
                Console.WriteLine("\nError: {0}", ex.Message);
                Console.ResetColor();
            }
            return projCreated;
        }
        // Get the GUID of the specified enterprise project type.
        private static Guid GetEptUid(string eptName)
        {
            Guid eptUid = Guid.Empty;
            try
            {
                // Get the list of EPTs that have the specified name. 
                // If the EPT name exists, the list will contain only one EPT.
                var eptList = projContext.LoadQuery(
                    projContext.EnterpriseProjectTypes.Where(
                        ept => ept.Name == eptName));
                projContext.ExecuteQuery();
                eptUid = eptList.First().Id;
                // Alternate routines to find the EPT GUID. Both (a) and (b) download the entire list of EPTs.
                // (a) Using a foreach block:
                //foreach (EnterpriseProjectType ept in projSvr.EnterpriseProjectTypes)
                //{
                //    if (ept.Name == eptName)
                //    {
                //        eptUid = ept.Id;
                //        break;
                //    }
                //}
                // (b) Querying for the EPT list, and then using a lambda expression to select the EPT:
                //var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
                //projContext.ExecuteQuery();
                //eptUid = eptList.First(ept => ept.Name == eptName).Id;
            }
            catch (Exception ex)
            {
                string msg = string.Format("GetEptUid: eptName = \"{0}\"\n\n{1}",
                    eptName, ex.GetBaseException().ToString());
                throw new ArgumentException(msg);
            }
            return eptUid;
        }
        // List the published projects.
        private static void ListPublishedProjects()
        {
            // Get the list of projects on the server.
            projContext.Load(projContext.Projects);
            projContext.ExecuteQuery();
            Console.WriteLine("\nProject ID : Project name : Created date");
            foreach (PublishedProject pubProj in projContext.Projects)
            {
                Console.WriteLine("\n\t{0} :\n\t{1} : {2}", pubProj.Id.ToString(), pubProj.Name,
                    pubProj.CreatedDate.ToString());
            }
        }
        // Parse the command line. Return true if there are no errors.
        private static bool ParseCommandLine(string[] args)
        {
            bool error = false;
            int argsLen = args.Length;
            try
            {
                for (int i = 0; i < argsLen; i++)
                {
                    if (error) break;
                    if (args[i].StartsWith("-") || args[i].StartsWith("/"))
                        args[i] = "*" + args[i].Substring(1).ToLower();
                    switch (args[i])
                    {
                        case "*projname":
                        case "*n":
                            if (++i >= argsLen) return false;
                            projName = args[i];
                            break;
                        case "*timeout":
                        case "*t":
                            if (++i >= argsLen) return false;
                            timeoutSeconds = Convert.ToInt32(args[i]);
                            break;
                        case "*?":
                        default:
                            error = true;
                            break;
                    }
                }
            }
            catch (FormatException)
            {
                error = true;
            }
            if (string.IsNullOrEmpty(projName)) error = true;
            return !error;
        }
        private static void Usage()
        {
            string example = "Usage: QueueCreateProject -projName | -n \"New project name\" [-timeout | -t sec]";
            example += "\nExample: QueueCreateProject -n \"My new project\"";
            example += "\nDefault timeout seconds = " + timeoutSeconds.ToString();
            Console.WriteLine(example);
        }
        private static void ExitApp()
        {
            Console.Write("\nPress any key to exit... ");
            Console.ReadKey(true);
            Environment.Exit(0);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md) 
- [Project 2013 のクライアント側オブジェクト モデル (CSOM)](client-side-object-model-csom-for-project-2013.md)
    

