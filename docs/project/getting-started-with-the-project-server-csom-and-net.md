---
title: Project Server CSOM および .NET の概要
manager: soliver
ms.date: 08/10/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5ce73baa-dfb6-41d0-918d-b0c3a498815f
description: Project Server 2013 のクライアント側オブジェクト モデル (CSOM) を使用して、.NET Framework 4 でオンライン プロジェクトとオンプレミスのソリューションを開発することができます。 この資料は、CSOM を使用して作成し、プロジェクトを発行するコンソール アプリケーションを作成する方法について説明します。 プロジェクトを発行した後は、アプリケーションは、発行操作を完了するには、プロジェクト サーバー キュー サービスの待機し、発行済みのプロジェクトが一覧表示されています。
ms.openlocfilehash: f4e40cb3165bb2b3caf05b01736d90c21b6ac881
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401743"
---
# <a name="getting-started-with-the-project-server-csom-and-net"></a><span data-ttu-id="08228-105">Project Server CSOM および .NET の概要</span><span class="sxs-lookup"><span data-stu-id="08228-105">Getting started with the Project Server CSOM and .NET</span></span>

<span data-ttu-id="08228-106">Project Server 2013 のクライアント側オブジェクト モデル (CSOM) を使用して、.NET Framework 4 でオンライン プロジェクトとオンプレミスのソリューションを開発することができます。</span><span class="sxs-lookup"><span data-stu-id="08228-106">You can use the Project Server 2013 client-side object model (CSOM) to develop Project Online and on-premises solutions with the .NET Framework 4.</span></span> <span data-ttu-id="08228-107">この資料は、CSOM を使用して作成し、プロジェクトを発行するコンソール アプリケーションを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="08228-107">This article describes how to create a console application that uses the CSOM to create and publish projects.</span></span> <span data-ttu-id="08228-108">プロジェクトを発行した後は、アプリケーションは、発行操作を完了するには、プロジェクト サーバー キュー サービスの待機し、発行済みのプロジェクトが一覧表示されています。</span><span class="sxs-lookup"><span data-stu-id="08228-108">After publishing a project, the application waits for the Project Server Queue Service to finish with the publish action, and then lists the published projects.</span></span>
  
<span data-ttu-id="08228-109">プロジェクトのサーバー CSOM に全般的な概要については、 [Project 2013 の開発者用の更新プログラム](updates-for-developers-in-project-2013.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08228-109">For a general introduction to the Project Server CSOM, see [Updates for developers in Project 2013](updates-for-developers-in-project-2013.md).</span></span> <span data-ttu-id="08228-110">CSOM 名前空間のリファレンス トピックでは、 [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08228-110">For reference topics in the CSOM namespace, see [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
## <a name="creating-a-csom-project-in-visual-studio"></a><span data-ttu-id="08228-111">Visual Studio で CSOM プロジェクトを作成する</span><span class="sxs-lookup"><span data-stu-id="08228-111">Creating a CSOM project in Visual Studio</span></span>
<span data-ttu-id="08228-112"><a name="pj15_GettingStartedCSOM_CreatingVSProject"> </a></span><span class="sxs-lookup"><span data-stu-id="08228-112"></span></span>

<span data-ttu-id="08228-113">Visual Studio 2010 または Visual Studio 2012 を使用するには、プロジェクトのサーバー CSOM を使用するソリューションを開発します。</span><span class="sxs-lookup"><span data-stu-id="08228-113">You can use Visual Studio 2010 or Visual Studio 2012 to develop solutions that use the Project Server CSOM.</span></span> <span data-ttu-id="08228-114">プロジェクトのサーバー CSOM には、.NET Framework 4 を使用して、クライアント アプリケーション、Microsoft Silverlight アプリケーション、および Windows Phone 8 アプリケーションを開発するための 3 つのアセンブリが含まれています。</span><span class="sxs-lookup"><span data-stu-id="08228-114">The Project Server CSOM includes three assemblies for development of client applications, Microsoft Silverlight applications, and Windows Phone 8 applications by using the .NET Framework 4.</span></span> <span data-ttu-id="08228-115">CSOM には、web アプリケーションを開発するための JavaScript ファイルが含まれています[Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx)で説明されているようです。</span><span class="sxs-lookup"><span data-stu-id="08228-115">The CSOM also includes a JavaScript file for development of web applications, as described in [Microsoft.ProjectServer.Client](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.aspx) .</span></span> 
  
<span data-ttu-id="08228-116">リモート開発用コンピューターに Project Server コンピューターから、または Project 2013 SDK ダウンロードから CSOM アセンブリする必要があることをコピーできます。</span><span class="sxs-lookup"><span data-stu-id="08228-116">You can copy the CSOM assembly that you need from the Project Server computer or from the Project 2013 SDK download to a remote development computer.</span></span> <span data-ttu-id="08228-117">このトピックに記載されている**QueueCreateProject**のコンソール アプリケーションは、Silverlight アプリケーションや Windows Phone 8 アプリケーションでは、Microsoft.ProjectServer.Client.dll アセンブリを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08228-117">The **QueueCreateProject** console application that is described in this topic is not a Silverlight application or a Windows Phone 8 application, so you need the Microsoft.ProjectServer.Client.dll assembly.</span></span> <span data-ttu-id="08228-118">CSOM は独立の WCF ベースまたは ASMX ベース プロジェクト Server インターフェイス (PSI) であるために、PSI のサービス参照を設定するか、 **Microsoft.Office.Project.Server.Library**名前空間を使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="08228-118">Because the CSOM is independent of the WCF-based or ASMX-based Project Server Interface (PSI), you do not have to set service references for the PSI or use the **Microsoft.Office.Project.Server.Library** namespace.</span></span> 
  
<span data-ttu-id="08228-p106">**QueueCreateProject** アプリケーションでは、作成するプロジェクトの名前とキューのタイムアウト制限をコマンド ライン引数で指定します。手順 1 では、基本的なコンソール アプリケーションを作成し、コマンド ラインを解析するルーチンを追加し、コマンド ラインでエラーが発生した場合に使用方法を説明するメッセージを追加します。</span><span class="sxs-lookup"><span data-stu-id="08228-p106">The **QueueCreateProject** application uses command-line arguments for the name of the project to create and for the queue timeout limit. In Procedure 1, you create the basic console application, add a routine to parse the command line, and add a usage message if there are errors in the command line.</span></span> 
  
### <a name="procedure-1-to-create-a-csom-project-in-visual-studio"></a><span data-ttu-id="08228-p107">手順 1. Visual Studio で CSOM プロジェクトを作成するには</span><span class="sxs-lookup"><span data-stu-id="08228-p107">Procedure 1. To create a CSOM project in Visual Studio</span></span>

1. <span data-ttu-id="08228-123">Microsoft.ProjectServer.Client.dll アセンブリをコピー、`%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\`を開発用コンピューターのフォルダーです。</span><span class="sxs-lookup"><span data-stu-id="08228-123">Copy the Microsoft.ProjectServer.Client.dll assembly from the  `%ProgramFiles%\Common Files\Microsoft Shared\Web Server Extensions\15\ISAPI\` folder to your development computer.</span></span> <span data-ttu-id="08228-124">その他の Project Server および SharePoint の参照アセンブリに使用する、次のように、適当なフォルダーにアセンブリをコピー `C:\Project\Assemblies`。</span><span class="sxs-lookup"><span data-stu-id="08228-124">Copy the assembly to a convenient folder for other Project Server and SharePoint reference assemblies that you will use, such as  `C:\Project\Assemblies`.</span></span>
    
2. <span data-ttu-id="08228-p109">Microsoft.SharePoint.Client.dll アセンブリと Microsoft.SharePoint.Client.Runtime.dll アセンブリを同じソース フォルダーから開発コンピューターにコピーします。Microsoft.ProjectServer.Client.dll アセンブリは関連する SharePoint アセンブリに依存します。</span><span class="sxs-lookup"><span data-stu-id="08228-p109">Copy the Microsoft.SharePoint.Client.dll assembly and the Microsoft.SharePoint.Client.Runtime.dll assembly from the same source folder to your development computer. The Microsoft.ProjectServer.Client.dll assembly has dependencies on the related SharePoint assemblies.</span></span>
    
3. <span data-ttu-id="08228-127">Visual Studio では、Windows コンソール アプリケーションを作成し、ターゲット フレームワークを.NET Framework 4 に設定します。</span><span class="sxs-lookup"><span data-stu-id="08228-127">In Visual Studio, create a Windows console application, and set the target framework to .NET Framework 4.</span></span> <span data-ttu-id="08228-128">たとえば、QueueCreateProject アプリケーションの名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="08228-128">For example, name the application QueueCreateProject.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="08228-p111">適切なターゲットの設定を忘れた場合、Visual Studio でプロジェクトを作成した後で、[**プロジェクト**] メニューの [**QueueCreateProject のプロパティ**] を開きます。[**アプリケーション**] タブの [**対象のフレームワーク**] ドロップダウン リストで、[**.NET Framework 4**] を選択します。[**.NET Framework 4 Client Profile**] は使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="08228-p111">If you forget to set the correct target, after Visual Studio creates the project, open **QueueCreateProject Properties** in the **Project** menu. On the **Application** tab, in the **Target framework** drop-down list, choose **.NET Framework 4**. Do not use the **.NET Framework 4 Client Profile**.</span></span> 
  
4. <span data-ttu-id="08228-132">ソリューション エクスプローラーで、次のアセンブリへの参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="08228-132">In Solution Explorer, set references to the following assemblies:</span></span>
    
   - <span data-ttu-id="08228-133">Microsoft.ProjectServer.Client.dll</span><span class="sxs-lookup"><span data-stu-id="08228-133">Microsoft.ProjectServer.Client.dll</span></span>
   - <span data-ttu-id="08228-134">Microsoft.SharePoint.Client.dll</span><span class="sxs-lookup"><span data-stu-id="08228-134">Microsoft.SharePoint.Client.dll</span></span>
   - <span data-ttu-id="08228-135">Microsoft.SharePoint.Client.Runtime.dll</span><span class="sxs-lookup"><span data-stu-id="08228-135">Microsoft.SharePoint.Client.Runtime.dll</span></span>
    
5. <span data-ttu-id="08228-136">Program.cs ファイルに、編集、`using`ステートメントは、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="08228-136">In the Program.cs file, edit the  `using` statements, as follows.</span></span> 
    
   ```cs
    using System;
    using System.Collections.Generic;
    using System.Linq;
    using System.Text;
    using Microsoft.ProjectServer.Client;
   ```

6. <span data-ttu-id="08228-p112">プロジェクト名とキューのタイムアウト秒数を示すコマンド ライン引数を解析するメソッドを追加し、使用法の情報を表示して、アプリケーションを終了します。Program.cs ファイルのコードの本文を次のコードに置き換えます。</span><span class="sxs-lookup"><span data-stu-id="08228-p112">Add methods to parse the command-line arguments for the project name and the number of seconds for queue timeout, show usage information, and exit the application. Replace the main body of code in the Program.cs file with the following code.</span></span>
    
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

## <a name="getting-the-project-context"></a><span data-ttu-id="08228-139">プロジェクトのコンテキストを取得する</span><span class="sxs-lookup"><span data-stu-id="08228-139">Getting the project context</span></span>
<span data-ttu-id="08228-140"><a name="pj15_GettingStartedCSOM_GettingContext"> </a></span><span class="sxs-lookup"><span data-stu-id="08228-140"></span></span>

<span data-ttu-id="08228-141">CSOM の開発には、Project Web App の URL を使用して初期化する**ProjectContext**オブジェクトが必要です。</span><span class="sxs-lookup"><span data-stu-id="08228-141">CSOM development requires the **ProjectContext** object to be initialized with the Project Web App URL.</span></span> <span data-ttu-id="08228-142">手順 2 のコードは、 **pwaPath**定数を使用します。</span><span class="sxs-lookup"><span data-stu-id="08228-142">The code in Procedure 2 uses the **pwaPath** constant.</span></span> <span data-ttu-id="08228-143">Project Web App の複数のインスタンスのアプリケーションを使用する場合は、変数を**pwaPath**にしてもう 1 つのコマンドライン引数を追加するでした。</span><span class="sxs-lookup"><span data-stu-id="08228-143">If you plan to use the application for multiple instances of Project Web App, you could make **pwaPath** a variable and add another command-line argument.</span></span> 
  
### <a name="procedure-2-to-get-the-project-context"></a><span data-ttu-id="08228-p114">手順 2. プロジェクトのコンテキストを取得するには</span><span class="sxs-lookup"><span data-stu-id="08228-p114">Procedure 2. To get the project context</span></span>

1. <span data-ttu-id="08228-146">クラスの定数を**プログラム**し、 **QueueCreateProject**アプリケーションを使用する変数を追加します。</span><span class="sxs-lookup"><span data-stu-id="08228-146">Add **Program** class constants and variables that the **QueueCreateProject** application will use.</span></span> <span data-ttu-id="08228-147">Project Web App の URL だけでなくアプリケーションを使用して既定のエンタープライズ プロジェクトの種類 (EPT) の名前、名前のプロジェクトを作成して、キューの最大タイムアウト (秒単位)。</span><span class="sxs-lookup"><span data-stu-id="08228-147">In addition to the Project Web App URL, the application uses the name of the default enterprise project type (EPT), the name of the project to create, and a maximum queue timeout in seconds.</span></span> <span data-ttu-id="08228-148">この例では、 **timeoutSeconds**変数を使用すると、タイムアウトの値をさまざまな方法に影響を与えるアプリケーションをテストできます。</span><span class="sxs-lookup"><span data-stu-id="08228-148">In this case, the **timeoutSeconds** variable enables you to test how various values for the timeout affect the application.</span></span> <span data-ttu-id="08228-149">**ProjectContext**オブジェクトは、プライマリ オブジェクト、CSOM にアクセスするためです。</span><span class="sxs-lookup"><span data-stu-id="08228-149">The **ProjectContext** object is the primary object for access to the CSOM.</span></span> 
    
   ```cs
    private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
    private static string basicEpt = "Enterprise Project";   // Basic enterprise project type.
    private static string projName = string.Empty;
    private static int timeoutSeconds = 10;  // The maximum wait time for a queue job, in seconds.
    private static ProjectContext projContext;
   ```

2. <span data-ttu-id="08228-150">交換、`/* Add calls to methods here to get the project context and create a project. */`を次のコードのコメント。</span><span class="sxs-lookup"><span data-stu-id="08228-150">Replace the  `/* Add calls to methods here to get the project context and create a project. */` comment with the following code.</span></span> <span data-ttu-id="08228-151">**Microsoft.ProjectServer.Client.ProjectContext**オブジェクトは Project Web App の URL を使用して初期化します。</span><span class="sxs-lookup"><span data-stu-id="08228-151">The **Microsoft.ProjectServer.Client.ProjectContext** object is initialized with the Project Web App URL.</span></span> <span data-ttu-id="08228-152">手順 4 と手順 5 では、 **CreateTestProject**メソッドと**ListPublishedProjects**メソッドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="08228-152">The **CreateTestProject** method and the **ListPublishedProjects** method are shown in Procedure 4 and Procedure 5.</span></span> 
    
   ```cs
    projContext = new ProjectContext(pwaPath);
    if (CreateTestProject())
        ListPublishedProjects();
    else
        Console.WriteLine("\nProject creation failed: {0}", projName);
   ```

## <a name="getting-an-enterprise-project-type"></a><span data-ttu-id="08228-153">エンタープライズ プロジェクトの種類を取得する</span><span class="sxs-lookup"><span data-stu-id="08228-153">Getting an enterprise project type</span></span>
<span data-ttu-id="08228-154"><a name="pj15_GettingStartedCSOM_GettingEPT"> </a></span><span class="sxs-lookup"><span data-stu-id="08228-154"></span></span>

<span data-ttu-id="08228-p117">**QueueCreateProject** サンプル アプリケーションでは、エンタープライズ プロジェクト テンプレート (EPT) を明示的に選択して、アプリケーションでのプロジェクトの EPT の選択方法を示しています。プロジェクトの作成情報に EPT の GUID が指定されていない場合、アプリケーションは既定の EPT を使用します。**GetEptUid** メソッドは、手順 4 で説明されている **CreateTestProject** メソッドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="08228-p117">The **QueueCreateProject** sample application explicitly selects the Enterprise Project EPT, to show how an application can select the EPT for a project. If the project creation information does not specify the EPT GUID, an application would use the default EPT. The **GetEptUid** method is used by the **CreateTestProject** method that is described in Procedure 4.</span></span> 
  
<span data-ttu-id="08228-p118">**GetEptUid** メソッドは、**EnterpriseProjectTypes** のコレクションに対し、EPT 名が指定した名前と等しい **ProjectContext** オブジェクトに対してクエリを実行します。クエリの実行後、**eptUid** 変数は **eptList** コレクションの最初の **EnterpriseProjectType** オブジェクトの GUID に設定されます。EPT 名は一意であるため、指定した名前を持つ **EnterpriseProjectType** オブジェクトは 1 つのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="08228-p118">The **GetEptUid** method queries the **ProjectContext** object for the collection of **EnterpriseProjectTypes** where the EPT name equals the specified name. After executing the query, the **eptUid** variable is set to the GUID of the first **EnterpriseProjectType** object in the **eptList** collection. Because EPT names are unique, there is only one **EnterpriseProjectType** object that has the specified name.</span></span> 
  
### <a name="procedure-3-to-get-the-guid-of-an-ept-for-a-new-project"></a><span data-ttu-id="08228-p119">手順 3. 新しいプロジェクトの EPT の GUID を取得するには</span><span class="sxs-lookup"><span data-stu-id="08228-p119">Procedure 3. To get the GUID of an EPT for a new project</span></span>

- <span data-ttu-id="08228-163">**GetEptUid** メソッドを **Program** クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="08228-163">Add the **GetEptUid** method to the **Program** class.</span></span> 
    
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

<span data-ttu-id="08228-p120">EPT の GUID の検索方法はいくつかあります。**GetEptUid** メソッドで示されているクエリは、EPT 名と一致する **EnterpriseProjectType** オブジェクトを 1 つだけダウンロードするため、効率的です。次に示す代替ルーチンは、EPT のリスト全体をクライアント アプリケーションにダウンロードしてリストを反復処理するため、効率が低くなります。</span><span class="sxs-lookup"><span data-stu-id="08228-p120">There are several ways to find the EPT GUID. The query shown in the **GetEptUid** method is efficient because it downloads only the one **EnterpriseProjectType** object that matches the EPT name. The following alternate routine is less efficient, because it downloads the complete list of EPTs to the client application and iterates through the list.</span></span> 

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

<span data-ttu-id="08228-167">次のルーチンでは LINQ クエリとラムダ式を使用して EPT オブジェクトを選択しますが、すべての **EnterpriseProjectType** オブジェクトをダウンロードします。</span><span class="sxs-lookup"><span data-stu-id="08228-167">The following routine uses a LINQ query and lambda expression to select the EPT object, but still downloads all of the **EnterpriseProjectType** objects.</span></span> 

```cs
var eptList = projContext.LoadQuery(projContext.EnterpriseProjectTypes);
projContext.ExecuteQuery();
eptUid = eptList.First(ept => ept.Name == eptName).Id;
```

## <a name="setting-the-creation-information-and-publishing-the-project"></a><span data-ttu-id="08228-168">作成情報を設定し、プロジェクトを発行する</span><span class="sxs-lookup"><span data-stu-id="08228-168">Setting the creation information and publishing the project</span></span>
<span data-ttu-id="08228-169"><a name="pj15_GettingStartedCSOM_ProjectCreation"> </a></span><span class="sxs-lookup"><span data-stu-id="08228-169"></span></span>

<span data-ttu-id="08228-p121">**CreateTestProject** メソッドは **ProjectCreationInformation** オブジェクトを作成し、プロジェクトの作成に必要な情報を指定します。プロジェクトの GUID と名前は必須であり、開始日、プロジェクトの説明、EPT の GUID は省略可能です。</span><span class="sxs-lookup"><span data-stu-id="08228-p121">The **CreateTestProject** method creates a **ProjectCreationInformation** object and specifies the information that is required to create a project. The project GUID and name are required; the start date, project description, and EPT GUID are optional.</span></span> 
  
<span data-ttu-id="08228-p122">新しいプロジェクトのプロパティを設定した後、**Projects.Add** メソッドでプロジェクトを **Projects** コレクションに追加します。プロジェクトを保存して発行するには、**Projects.Update** メソッドを呼び出して Project Server キューにメッセージを送信し、プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="08228-p122">After setting the new project properties, the **Projects.Add** method adds the project to the **Projects** collection. To save and publish the project, you must call the **Projects.Update** method to send a message to the Project Server queue and create the project.</span></span> 
  
### <a name="procedure-4-to-set-the-new-project-properties-create-the-project-and-publish-the-project"></a><span data-ttu-id="08228-p123">手順 4. 新しいプロジェクトのプロパティを設定し、プロジェクトを作成して、発行するには</span><span class="sxs-lookup"><span data-stu-id="08228-p123">Procedure 4. To set the new project properties, create the project, and publish the project</span></span>

1. <span data-ttu-id="08228-p124">**CreateTestProject** メソッドを **Program** クラスに追加します。次のコードではプロジェクトを作成して発行しますが、キューのジョブが完了するまで待機しません。</span><span class="sxs-lookup"><span data-stu-id="08228-p124">Add the **CreateTestProject** method to the **Program** class. The following code creates and publishes a project, but does not wait for the queue job to complete.</span></span> 
    
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

2. <span data-ttu-id="08228-178">交換、`/* Add code here to wait for the queue. */`キュー ジョブを待機する次のコードにコメントします。</span><span class="sxs-lookup"><span data-stu-id="08228-178">Replace the  `/* Add code here to wait for the queue. */` comment with the following code to wait for the queue job.</span></span> <span data-ttu-id="08228-179">ルーチンでは、最大秒数を指定した**timeoutSeconds**を待機するか、タイムアウトする前にキューのジョブが終了した場合に行われます。</span><span class="sxs-lookup"><span data-stu-id="08228-179">The routine waits a maximum of the specified **timeoutSeconds** number of seconds, or proceeds if the queue job completes before the timeout.</span></span> <span data-ttu-id="08228-180">キュー ジョブの状態は、 [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08228-180">For possible queue job states, see [Microsoft.ProjectServer.Client.JobState](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.JobState.aspx) .</span></span> 
    
   <span data-ttu-id="08228-p126">**QueueJob** オブジェクトの **Load** メソッドおよび **ExecuteQuery** メソッドの呼び出しは省略可能です。**WaitForQueue** メソッドの呼び出し時に **QueueJob** オブジェクトが未初期化の場合、Project Server で初期化されます。</span><span class="sxs-lookup"><span data-stu-id="08228-p126">Calling the **Load** method and the **ExecuteQuery** method for the **QueueJob** object is optional. If the **QueueJob** object is not initialized when you call the **WaitForQueue** method, Project Server initializes it.</span></span> 
    
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

## <a name="listing-the-published-projects"></a><span data-ttu-id="08228-183">発行されたプロジェクトを一覧表示する</span><span class="sxs-lookup"><span data-stu-id="08228-183">Listing the published projects</span></span>
<span data-ttu-id="08228-184"><a name="pj15_GettingStartedCSOM_ListingPublished"> </a></span><span class="sxs-lookup"><span data-stu-id="08228-184"></span></span>

<span data-ttu-id="08228-185">**ListPublishedProjects**メソッドは、Project Web App で公開されているすべてのプロジェクトのコレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="08228-185">The **ListPublishedProjects** method gets the collection of all projects that are published in Project Web App.</span></span> <span data-ttu-id="08228-186">キューのジョブを作成する場合は手順 4 で、プロジェクトが正常に完了しないか、タイムアウト、新しいプロジェクトが**プロジェクト**コレクションに含まれていません。</span><span class="sxs-lookup"><span data-stu-id="08228-186">If the queue job that creates a project in Procedure 4 does not complete successfully or times out, the new project is not included in the **Projects** collection.</span></span> 
  
### <a name="procedure-5-to-list-the-published-projects"></a><span data-ttu-id="08228-p128">手順 5. 発行したプロジェクトを一覧表示するには</span><span class="sxs-lookup"><span data-stu-id="08228-p128">Procedure 5. To list the published projects</span></span>

1. <span data-ttu-id="08228-189">**ListPublishedProjects** メソッドを **Program** クラスに追加します。</span><span class="sxs-lookup"><span data-stu-id="08228-189">Add the **ListPublishedProjects** method to the **Program** class.</span></span> 
    
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

2. <span data-ttu-id="08228-190">Project Web App の URL の正しい値を設定、 **QueueCreateProject**アプリケーションをコンパイルし、手順 6 のようにアプリケーションをテストします。</span><span class="sxs-lookup"><span data-stu-id="08228-190">Set the correct value for your Project Web App URL, compile the **QueueCreateProject** application, and then test the application as in Procedure 6.</span></span> 
    
## <a name="testing-the-queuecreateproject-application"></a><span data-ttu-id="08228-191">QueueCreateProject アプリケーションをテストする</span><span class="sxs-lookup"><span data-stu-id="08228-191">Testing the QueueCreateProject application</span></span>
<span data-ttu-id="08228-192"><a name="pj15_GettingStartedCSOM_Testing"> </a></span><span class="sxs-lookup"><span data-stu-id="08228-192"></span></span>

<span data-ttu-id="08228-193">とき、最初に、Project Web App のテスト インスタンスの**QueueCreateProject**アプリケーションを実行すると、バーチャル マシンでは、Project Server がインストールされている場合に特に、アプリケーション必要がありますより多くの時間を 10 秒間の既定のキューのタイムアウトよりも実行します。</span><span class="sxs-lookup"><span data-stu-id="08228-193">When you first run the **QueueCreateProject** application on a test instance of Project Web App, especially if Project Server is installed on a virtual machine, the application may require more time to run than the default queue timeout of ten seconds.</span></span> 
  
### <a name="procedure-6-to-test-the-queuecreateproject-application"></a><span data-ttu-id="08228-p129">手順 6. QueueCreateProject アプリケーションをテストするには</span><span class="sxs-lookup"><span data-stu-id="08228-p129">Procedure 6. To test the QueueCreateProject application</span></span>

1. <span data-ttu-id="08228-196">**QueueCreateProject のプロパティ**] ウィンドウを開き、[**デバッグ**] タブを選択し、[**開始オプション**] セクションで、次のコマンドライン引数を追加します。`-n "Test proj 1" -t 20`</span><span class="sxs-lookup"><span data-stu-id="08228-196">Open the **QueueCreateProject Properties** window, select the **Debug** tab, and then add the following command-line arguments in the **Start Options** section:  `-n "Test proj 1" -t 20`</span></span>
    
   <span data-ttu-id="08228-197">アプリケーションを実行 (たとえば、 **f5 キー**を押します)。</span><span class="sxs-lookup"><span data-stu-id="08228-197">Run the application (for example, press **F5**).</span></span> <span data-ttu-id="08228-198">タイムアウト値が十分に長い場合、アプリケーションは、次の出力を示しています (その他の発行済みプロジェクトは、Project Web App インスタンスに存在する場合にも表示されます)。</span><span class="sxs-lookup"><span data-stu-id="08228-198">If the timeout value is long enough, the application shows the following output (if other published projects exist in your Project Web App instance, they will also be shown):</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Project ID : Project name : Created date
            b34d7009-753f-4abb-9191-f4b15a82aac3 :
            Test proj 1 : 9/22/2011 11:27:57 AM
    Press any key to exit...
   ```

2. <span data-ttu-id="08228-199">10 秒あたりのキューのタイムアウトの既定値を使用するのには、以下のコマンドライン引数を持つ別のテストを実行します。`-n "Test proj 1"`</span><span class="sxs-lookup"><span data-stu-id="08228-199">Run another test with the following command-line arguments, to use the default 10-second queue timeout: `-n "Test proj 1"`</span></span>
    
   <span data-ttu-id="08228-200">Test proj 1 は既に存在するため、アプリケーションは次の結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="08228-200">Because Test proj 1 already exists, the application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 1 ...
    Error: PJClientCallableException: ProjectNameAlreadyExists
    ProjectNameAlreadyExists
    projName = Test proj 1
    Project creation failed: Test proj 1
    Press any key to exit...
   ```

3. <span data-ttu-id="08228-201">10 秒あたりのキューのタイムアウトの既定値を使用するのには、以下のコマンドライン引数を持つ別のテストを実行します。`-n "Test proj 2"`</span><span class="sxs-lookup"><span data-stu-id="08228-201">Run another test with the following command-line arguments, to use the default 10-second queue timeout:  `-n "Test proj 2"`</span></span>
    
   <span data-ttu-id="08228-202">**QueueCreateProject** アプリケーションは Test proj 2 という名前のプロジェクトを作成して発行します。</span><span class="sxs-lookup"><span data-stu-id="08228-202">The **QueueCreateProject** application creates and publishes the project named Test proj 2.</span></span> 
    
4. <span data-ttu-id="08228-203">次のコマンドライン引数を指定するには、別のテストを実行し、タイムアウト時間を終了するに対して短すぎるのキュー ジョブを設定します。`-n "Test proj 3" -t 1`</span><span class="sxs-lookup"><span data-stu-id="08228-203">Run another test with the following command-line arguments, and set the timeout to be too short for the queue job to finish:  `-n "Test proj 3" -t 1`</span></span>
    
   <span data-ttu-id="08228-p131">キューのタイムアウトが短すぎるため、プロジェクトは作成されません。アプリケーションは次の結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="08228-p131">Because the queue timeout is too short, the project is not created. The application shows the following output.</span></span>
    
   ```MS-DOS
    Creating project: Test proj 3 ...
    There is a problem in the queue. Timeout is 1 seconds.
            Queue JobState: Unknown
    Project creation failed: Test proj 3
    Press any key to exit...
   ```

5. <span data-ttu-id="08228-206">キュー ジョブのアプリケーションが待機しないようにコードを変更します。</span><span class="sxs-lookup"><span data-stu-id="08228-206">Modify the code so that the application does not wait for the queue job.</span></span> <span data-ttu-id="08228-207">以外のキューに待機するコードをコメントなどの`projCreated = true`行に、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="08228-207">For example, comment out the code that waits for the queue, except for the  `projCreated = true` line, as follows.</span></span> 
    
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

6. <span data-ttu-id="08228-208">アプリケーションを再コンパイルし、次のコマンドライン引数を持つ別のテストを実行します。`-n "Test proj 4"`</span><span class="sxs-lookup"><span data-stu-id="08228-208">Recompile the application and run another test with the following command-line arguments:  `-n "Test proj 4"`</span></span>
    
   <span data-ttu-id="08228-p133">**WaitForQueue** ルーチンがコメント アウトされているため、アプリケーションでは既定のタイムアウト値は使用されません。アプリケーションはキューを待機しませんが、Project Server の発行処理が十分に高速であれば、Test proj 4 が表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="08228-p133">Because the **WaitForQueue** routine is commented out, the application does not use the default timeout value. Even though the application does not wait for the queue, it may show Test proj 4, if the publish action in Project Server is fast enough.</span></span> 
    
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

<span data-ttu-id="08228-211">Project Web App の [プロジェクト センター] ページを更新 (`https://ServerName/ProjectServerName/Projects.aspx`)、発行済みのプロジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="08228-211">Refresh the Project Center page in Project Web App (`https://ServerName/ProjectServerName/Projects.aspx`), to show the published projects.</span></span> <span data-ttu-id="08228-212">次の図は、テスト プロジェクトが発行されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="08228-212">The following figure shows that the test projects are published.</span></span>

<span data-ttu-id="08228-213">**Project Web App で発行済みプロジェクトを確認する**</span><span class="sxs-lookup"><span data-stu-id="08228-213">**Checking the published projects in Project Web App**</span></span>

<span data-ttu-id="08228-214">![Project Web App での発行済みのプロジェクトをチェック](media/pj15_GetStartedCSOMNET_pwa.gif "Project Web App での発行済みのプロジェクトをチェック")</span><span class="sxs-lookup"><span data-stu-id="08228-214">![Checking the published projects in Project Web App](media/pj15_GetStartedCSOMNET_pwa.gif "Checking the published projects in Project Web App")</span></span>
  
<span data-ttu-id="08228-215">**QueueCreateProject**サンプル アプリケーションは、CSOM で**ProjectCreationInformation**クラスを使用して、プロジェクトのエンティティを作成する方法の一般的な例を示しています、公開されているコレクションにプロジェクトを追加する方法でのキュー ジョブを待機する方法**WaitForQueue**メソッド、および発行済みプロジェクトのコレクションを列挙する方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="08228-215">The **QueueCreateProject** sample application shows a typical example of how to create a project entity with the CSOM by using the **ProjectCreationInformation** class, how to add the project to the published collection, how to wait for a queue job by using the **WaitForQueue** method, and how to enumerate the collection of published projects.</span></span> 
  
## <a name="complete-code-example"></a><span data-ttu-id="08228-216">完全なコード例</span><span class="sxs-lookup"><span data-stu-id="08228-216">Complete code example</span></span>
<span data-ttu-id="08228-217"><a name="pj15_GettingStartedCSOM_CompleteCode"> </a></span><span class="sxs-lookup"><span data-stu-id="08228-217"></span></span>

<span data-ttu-id="08228-218">**QueueCreateProject**サンプル アプリケーションの完全なコードを次に示します。</span><span class="sxs-lookup"><span data-stu-id="08228-218">The following is the complete code for the **QueueCreateProject** sample application.</span></span> <span data-ttu-id="08228-219">[Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx)クラスの参照には、このトピックのコードも含まれています。</span><span class="sxs-lookup"><span data-stu-id="08228-219">The [Microsoft.ProjectServer.Client.ProjectCreationInformation](https://msdn.microsoft.com/library/Microsoft.ProjectServer.Client.ProjectCreationInformation.aspx) class reference also includes the code in this topic.</span></span> 
  
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
        private const string pwaPath = "https://ServerName /pwa/"; // Change the path to your Project Web App instance.
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

## <a name="see-also"></a><span data-ttu-id="08228-220">関連項目</span><span class="sxs-lookup"><span data-stu-id="08228-220">See also</span></span>

- [<span data-ttu-id="08228-221">Project 2013 の開発者向けの新機能</span><span class="sxs-lookup"><span data-stu-id="08228-221">Updates for developers in Project 2013</span></span>](updates-for-developers-in-project-2013.md) 
- [<span data-ttu-id="08228-222">Project 2013 のクライアント側オブジェクト モデル (CSOM)</span><span class="sxs-lookup"><span data-stu-id="08228-222">Client-side object model (CSOM) for Project 2013</span></span>](client-side-object-model-csom-for-project-2013.md)
    

