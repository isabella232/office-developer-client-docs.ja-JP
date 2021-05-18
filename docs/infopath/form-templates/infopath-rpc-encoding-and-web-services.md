---
title: InfoPath、RPC エンコード、および Web サービス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: Web サービスは、WSDL (Web サービス記述言語) コントラクトの指定で、Web メソッドへのバインドのために 2 つのスタイル (Document または RPC) のどちらかを公開できます。
ms.openlocfilehash: 0eacf013c9cdf74f18f3de1d4412ca4ca165a960
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303529"
---
# <a name="infopath-rpc-encoding-and-web-services"></a><span data-ttu-id="83b09-103">InfoPath、RPC エンコード、および Web サービス</span><span class="sxs-lookup"><span data-stu-id="83b09-103">InfoPath, RPC Encoding and Web Services</span></span>

<span data-ttu-id="83b09-p101">Web サービスは、WSDL (Web サービス記述言語) コントラクトの指定で、Web メソッドへのバインドのために 2 つのスタイル (Document または RPC) のどちらかを公開できます。さらに、バインドのこれらの 2 つのスタイルは、literal または encode のどちらかとして指定できます。各タイプの最も一般的な実装は、document/literal および RPC/encoded です。ただし、Microsoft InfoPath でサポートされるのは、document/literal スタイルを使用する Web サービスへの接続のみです。</span><span class="sxs-lookup"><span data-stu-id="83b09-p101">Web services can expose one of two styles for binding to their Web methods in the Web Service Description Language (WSDL) contract that describes them: Document or RPC. Additionally, each of these two styles of binding can be specified as either literal or encoded. The most common implementations for each type are: document/literal and RPC/encoded. However, Microsoft InfoPath only supports connecting to Web services that use the document/literal style.</span></span>
  
<span data-ttu-id="83b09-p102">ほとんどの Web サービス開発ツールには、作成する Web サービスの種類を指定するスイッチが用意されています。InfoPath から接続する Web サービスを開発する場合は、Web サービスのスタイルおよびエンコードとして document/literal を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="83b09-p102">Most Web service development tools provide a switch for specifying what kind of Web service that you want to create. If you are developing a Web service that you will be connecting to from InfoPath, you should specify document/literal as your Web service's style and encoding.</span></span>
  
<span data-ttu-id="83b09-110">ただし、操作する Web サービスを管理せず、RPC/encoded スタイルを使用する Web サービスに接続する必要がある場合は, .NET プロキシ サービスを使用して RPC/encoded Web サービスに接続することができます。</span><span class="sxs-lookup"><span data-stu-id="83b09-110">However, if you do not control the Web service that you want to work with, and you must connect to a Web service uses the RPC/encoded style, you can use a .NET proxy service to connect to an RPC/encoded Web service.</span></span>
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a><span data-ttu-id="83b09-111">.NET プロキシ サービスを使用して Web サービスに接続する</span><span class="sxs-lookup"><span data-stu-id="83b09-111">Using a .NET Proxy Service to Connect to a Web Service</span></span>

<span data-ttu-id="83b09-p103">操作する RPC/encoded Web サービスを管理しない場合は、各 Web メソッドのラッパー関数を提供する document/literal プロキシ Microsoft .NET Web サービスを作成し、RPC/encoded Web サービスから呼び出すことができます。これにより、InfoPath からプロキシ document/literal Web サービスを操作できます。</span><span class="sxs-lookup"><span data-stu-id="83b09-p103">If you do not control the RPC/encoded Web service that you want to work with, you can create a document/literal proxy Microsoft .NET Web service that provides wrapper functions for each of the Web methods, you want to invoke from the RPC/encoded Web service. You can then work with the proxy document/literal Web service from InfoPath.</span></span>
  
<span data-ttu-id="83b09-p104">.NET Framework コードは、任意の種類の Web サービス (RPC/encoded と document/literal の両方) に対して使用することができ、すべての .NET Web サービスは document/literal スタイルおよびエンコードを使用します。.NET Framework は任意の種類の Web サービスと通信できるので、RPC/encoded Web サービスを呼び出すメソッドが含まれた .NET Web サービスを作成できます。.NET Web サービスは、InfoPath が .NET Web サービスに対する document/literal スタイルの呼び出しを行えるようにするトランスレーターとして機能します。これにより, .NET Web サービスは元の Web サービスに対する RPC/encoded スタイルの呼び出しを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="83b09-p104">.NET Framework code can work with any kind of Web service (both RPC/encoded and document/literal), and all .NET Web services use the document/literal style and encoding. Because the .NET Framework can communicate with any kind of Web service, you can create a .NET Web service that has methods that make calls to the RPC/encoded Web service. The .NET Web service will act as a translator that enables InfoPath to make document/literal style calls to the .NET Web service which in turn can make RPC/encoded style calls to the original Web service.</span></span>
  
<span data-ttu-id="83b09-p105">このようなプロキシ Microsoft .NET Web サービスを作成するには、Internet Information Services (IIS) を実行していて、ASP.NET がインストールされた、プロキシ サービスを展開するための Microsoft Windows コンピューターまたは Microsoft Windows Server コンピューターが必要です。InfoPath ソリューションを作成するときは、RPC/encoded Web サービスの代わりにプロキシ Web サービスを指定します。これにより、プロキシ Web サービスは RPC/encoded サービスを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="83b09-p105">The prerequisites for creating such a proxy Microsoft .NET Web service are a Microsoft Windows or Microsoft Windows Server computer that is running Internet Information Services (IIS) with ASP.NET installed on which to deploy the proxy Web service. When you create an InfoPath solution, you will point to the proxy Web service instead of the RPC/encoded Web service. The proxy Web service will then make calls to the RPC/encoded service.</span></span>
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a><span data-ttu-id="83b09-120">Visual Studio を使用してプロキシ Web サービスを作成する</span><span class="sxs-lookup"><span data-stu-id="83b09-120">Creating a Proxy Web Service Using Visual Studio</span></span>

1. <span data-ttu-id="83b09-121">新しい **ASP.NET Web サービス アプリケーション** プロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="83b09-121">Create a new **ASP.NET Web Service Application** project.</span></span> 
    
2. <span data-ttu-id="83b09-122">[ **ソリューション エクスプローラー**] で、新しいプロジェクトの [ **参照**] フォルダーを右クリックし、[ **Web 参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83b09-122">In the **Solution Explorer**, right-click the **References** folder of your new project, and then click **Add Web Reference**.</span></span> 
    
3. <span data-ttu-id="83b09-123">[ **Web 参照の追加**] ダイアログ ボックスで、操作する RPC/encoded Web サービスの URL を入力し、[ **移動**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83b09-123">In the **Add Web Reference** dialog box, type in the URL of the RPC/encoded Web service that you want to work with, and then click **Go**.</span></span>
    
4. <span data-ttu-id="83b09-124">[ **参照の追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="83b09-124">Click **Add Reference**.</span></span> 
    
5. <span data-ttu-id="83b09-125">Web サービスの .asmx ファイルを開き、参照する RPC/encoded Web サービスから各 Web サービス メソッドを呼び出す 1 つの Web サービス メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="83b09-125">Open the .asmx file for your Web service and add one Web Service method to call each Web Service method from the referenced RPC/encoded Web service.</span></span>
    
6. <span data-ttu-id="83b09-p106">参照する RPC/encoded Web サーバーのメソッドの一覧を表示するには、[ **クラス ビュー**] ウィンドウを表示します。Web サービス メソッドごとに、3 つのメソッドが表示されます。たとえば、Web サービス メソッドの名前が  `doSearch` である場合、  `doSearch`、 `BegindoSearch`、および  `EnddoSearch` という 3 つのメソッドが表示されます。  `doSearch` メソッド用のラッパー Web サービス メソッドを作成するだけで済みます。メソッド シグネチャと戻り値の型は正確に合わせてください。</span><span class="sxs-lookup"><span data-stu-id="83b09-p106">To view a list of the methods in the reference RPC/encoded Web server, display the **Class View** window. For each Web Service method, you will see three methods. For example, if the Web Service method is called  `doSearch`, then you will see three methods called  `doSearch`,  `BegindoSearch`, and  `EnddoSearch`. You only have to create a wrapper Web Service method for the  `doSearch` method. Be sure to match the exact method signature and return type.</span></span> 
    
7. <span data-ttu-id="83b09-131">次の例に示すように、各ラッパー メソッド内で、参照する RPC/encoded Web サービスを呼び出すコードを書く必要があります。</span><span class="sxs-lookup"><span data-stu-id="83b09-131">Within each wrapper method, you have to write code to make a call to the referenced RPC/encoded Web service as shown in the following example.</span></span> 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. <span data-ttu-id="83b09-132">RPC/encoded Web サービスで認証を必要とする場合は、プロキシ .NET Web サービスのソース コードに、RPC/encoded Web サービスへの接続に必要な資格情報をハードコードするか、または次の例のようなコードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="83b09-132">If the RPC/encoded Web service requires authentication, you can hard code the credentials required to connect to the RPC/encoded Web service into the source code for the proxy .NET Web service, or you can use code like the following example.</span></span> 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

<span data-ttu-id="83b09-133">詳細については、Microsoft サポート技術情報 (https://support.microsoft.com/ で、現在の資格情報を ASP .NET Web サービスに渡す方法に関する記事 (HOW TO: Pass Current Credentials to an ASP.NET Web Service) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="83b09-133">For more information, search for the Microsoft Knowledge Base article "HOW TO: Pass Current Credentials to an ASP.NET Web Service" on https://support.microsoft.com/.</span></span>
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a><span data-ttu-id="83b09-134">Visual Studio .NET を使用せずにプロキシ Web サービスを作成する</span><span class="sxs-lookup"><span data-stu-id="83b09-134">Creating a Proxy Web Service Without Visual Studio .NET</span></span>

<span data-ttu-id="83b09-135">別の方法として, .NET Framework Software Development Kit に用意されているツールを使用してプロキシ Web サービスを作成することができます。これは、MSDN からダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="83b09-135">Alternatively, you can create a proxy Web service by using the tools that are provided with the .NET Framework Software Development Kit, which can be downloaded from MSDN.</span></span>
  
<span data-ttu-id="83b09-p107">Web サービス記述言語ツール (Wsdl.exe) を使用して、プロキシ Web サービスのコード ファイルを作成します。このコード ファイルは、C# コマンドライン コンパイラ (csc.exe) または Visual Basic .NET コマンドライン コンパイラ (vbc.exe) を使用してコンパイルできます。これらのコンパイラも .NET Framework SDK に用意されています。Web サービス記述言語ツールでコード ファイルを生成したら、ファイル名拡張子を .asmx に変更し、任意のテキスト エディターでファイルを開きます。ドキュメントの最初の行に、次のページ ディレクティブを追加します。</span><span class="sxs-lookup"><span data-stu-id="83b09-p107">Use the Web Services Description Language Tool (Wsdl.exe) to create the code file for your proxy Web service. This code file can be compiled by using the C# command-line compiler (csc.exe) or the Visual Basic .NET command-line compiler (vbc.exe), which are also included with the .NET Framework SDK. After the Web Services Description Language tool has generated the code file, rename the file name extension to .asmx and open the file in any text editor. On the very first line of the document, add the following page directive:</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

<span data-ttu-id="83b09-p108">コード ファイルの最後に移動し、RPC/encoded Web サービスで各 Web サービス メソッドの呼び出しを作成します。次のサンプル コードは、RPC/encoded スタイルの開発を使用し、Google Web サービスに接続する .NET Web サービス用のコードを示しています。wsdl.exe で生成されたコードを挿入するためのプレースホルダーがあります。</span><span class="sxs-lookup"><span data-stu-id="83b09-p108">Go to the end of the code file and create a call to each Web Service method in the RPC/encoded Web service. The following code sample shows the code for a .NET Web service that connects to the Google Web service, which uses the RPC/encoded style of development. There is a placeholder for where the wsdl.exe generated code should go.</span></span>
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
 
using System; 
using System.Web.Services; 
 
// The auto-generated code from the wsdl.exe tool goes here. 
 
[WebService] 
public class GoogleSearchServiceWrapper : System.Web.Services.WebService  
{ 
    [WebMethod] 
    public System.Byte[] doGetCachedPage(System.String key, System.String url) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doGetCachedPage(key, url); 
    } 
 
    [WebMethod] 
    public System.String doSpellingSuggestion(System.String key, System.String phrase) 
    { 
        GoogleSearchService srch = new GoogleSearchService(); 
        return srch.doSpellingSuggestion(key, phrase); 
    } 
 
    [WebMethod] 
    public GoogleSearchResult doGoogleSearch(System.String key, 
      System.String q, 
      System.Int32 start, 
      System.Int32 maxResults, 
      System.Boolean filter, 
      System.String restrict, 
      System.Boolean safeSearch, 
      System.String lr, 
      System.String ie, 
      System.String oe) 
    {
        GoogleSearchService srch = new GoogleSearchService();
           return srch.doGoogleSearch(key, q, start, maxResults, 
               filter, restrict, safeSearch, lr, ie, oe); 
    } 
}
```


