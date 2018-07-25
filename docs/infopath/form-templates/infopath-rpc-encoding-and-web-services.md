---
title: InfoPath、RPC エンコード、および Web サービス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f8d7b944-a8fd-9c5f-8f66-0f1b628b7c6e
description: Web サービスは、WSDL (Web サービス記述言語) コントラクトの指定で、Web メソッドへのバインドのために 2 つのスタイル (Document または RPC) のどちらかを公開できます。
ms.openlocfilehash: 01b75df42bce97d62ebb5e273588cb522e5e2a09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799137"
---
# <a name="infopath-rpc-encoding-and-web-services"></a>InfoPath、RPC エンコード、および Web サービス

Web サービスは、WSDL (Web サービス記述言語) コントラクトの指定で、Web メソッドへのバインドのために 2 つのスタイル (Document または RPC) のどちらかを公開できます。さらに、バインドのこれらの 2 つのスタイルは、literal または encode のどちらかとして指定できます。各タイプの最も一般的な実装は、document/literal および RPC/encoded です。ただし、Microsoft InfoPath でサポートされるのは、document/literal スタイルを使用する Web サービスへの接続のみです。
  
ほとんどの Web サービス開発ツールには、作成する Web サービスの種類を指定するスイッチが用意されています。InfoPath から接続する Web サービスを開発する場合は、Web サービスのスタイルおよびエンコードとして document/literal を指定する必要があります。
  
ただし、操作する Web サービスを管理せず、RPC/encoded スタイルを使用する Web サービスに接続する必要がある場合は, .NET プロキシ サービスを使用して RPC/encoded Web サービスに接続することができます。
  
## <a name="using-a-net-proxy-service-to-connect-to-a-web-service"></a>.NET プロキシ サービスを使用して Web サービスに接続する

操作する RPC/encoded Web サービスを管理しない場合は、各 Web メソッドのラッパー関数を提供する document/literal プロキシ Microsoft .NET Web サービスを作成し、RPC/encoded Web サービスから呼び出すことができます。これにより、InfoPath からプロキシ document/literal Web サービスを操作できます。
  
.NET Framework コードは、任意の種類の Web サービス (RPC/encoded と document/literal の両方) に対して使用することができ、すべての .NET Web サービスは document/literal スタイルおよびエンコードを使用します。.NET Framework は任意の種類の Web サービスと通信できるので、RPC/encoded Web サービスを呼び出すメソッドが含まれた .NET Web サービスを作成できます。.NET Web サービスは、InfoPath が .NET Web サービスに対する document/literal スタイルの呼び出しを行えるようにするトランスレーターとして機能します。これにより, .NET Web サービスは元の Web サービスに対する RPC/encoded スタイルの呼び出しを行うことができます。
  
このようなプロキシ Microsoft .NET Web サービスを作成するには、Internet Information Services (IIS) を実行していて、ASP.NET がインストールされた、プロキシ サービスを展開するための Microsoft Windows コンピューターまたは Microsoft Windows Server コンピューターが必要です。InfoPath ソリューションを作成するときは、RPC/encoded Web サービスの代わりにプロキシ Web サービスを指定します。これにより、プロキシ Web サービスは RPC/encoded サービスを呼び出すことができます。
  
## <a name="creating-a-proxy-web-service-using-visual-studio"></a>Visual Studio を使用してプロキシ Web サービスを作成する

1. 新しい **ASP.NET Web サービス アプリケーション** プロジェクトを作成します。 
    
2. [ **ソリューション エクスプローラー**] で、新しいプロジェクトの [ **参照**] フォルダーを右クリックし、[ **Web 参照の追加**] をクリックします。 
    
3. [ **Web 参照の追加**] ダイアログ ボックスで、操作する RPC/encoded Web サービスの URL を入力し、[ **移動**] をクリックします。
    
4. [ **参照の追加**] をクリックします。 
    
5. Web サービスの .asmx ファイルを開き、参照する RPC/encoded Web サービスから各 Web サービス メソッドを呼び出す 1 つの Web サービス メソッドを追加します。
    
6. 参照する RPC/encoded Web サーバーのメソッドの一覧を表示するには、[ **クラス ビュー**] ウィンドウを表示します。Web サービス メソッドごとに、3 つのメソッドが表示されます。たとえば、Web サービス メソッドの名前が  `doSearch` である場合、  `doSearch`、 `BegindoSearch`、および  `EnddoSearch` という 3 つのメソッドが表示されます。  `doSearch` メソッド用のラッパー Web サービス メソッドを作成するだけで済みます。メソッド シグネチャと戻り値の型は正確に合わせてください。 
    
7. 次の例に示すように、各ラッパー メソッド内で、参照する RPC/encoded Web サービスを呼び出すコードを書く必要があります。 
    
   ```cs
    [WebMethod] 
    public string[] doSearch(string keyword) 
    { 
        SearchService srch = new SearchService(); 
        return srch.doSearch(keyword); 
    } 
    
   ```

8. RPC/encoded Web サービスで認証を必要とする場合は、プロキシ .NET Web サービスのソース コードに、RPC/encoded Web サービスへの接続に必要な資格情報をハードコードするか、または次の例のようなコードを使用できます。 
    
   ```cs
    myProxy.Credentials = System.Net.CredentialCache.DefaultCredentials; 
    
   ```

詳細については、Microsoft サポート技術情報 (http://support.microsoft.com/ で、現在の資格情報を ASP .NET Web サービスに渡す方法に関する記事 (HOW TO: Pass Current Credentials to an ASP.NET Web Service) を参照してください。
    
## <a name="creating-a-proxy-web-service-without-visual-studio-net"></a>Visual Studio .NET を使用せずにプロキシ Web サービスを作成する

別の方法として, .NET Framework Software Development Kit に用意されているツールを使用してプロキシ Web サービスを作成することができます。これは、MSDN からダウンロードできます。
  
Web サービス記述言語ツール (Wsdl.exe) を使用して、プロキシ Web サービスのコード ファイルを作成します。このコード ファイルは、C# コマンドライン コンパイラ (csc.exe) または Visual Basic .NET コマンドライン コンパイラ (vbc.exe) を使用してコンパイルできます。これらのコンパイラも .NET Framework SDK に用意されています。Web サービス記述言語ツールでコード ファイルを生成したら、ファイル名拡張子を .asmx に変更し、任意のテキスト エディターでファイルを開きます。ドキュメントの最初の行に、次のページ ディレクティブを追加します。
  
```cs
<%@ WebService Language="C#" class="GoogleSearchServiceWrapper" %> 
```

コード ファイルの最後に移動し、RPC/encoded Web サービスで各 Web サービス メソッドの呼び出しを作成します。次のサンプル コードは、RPC/encoded スタイルの開発を使用し、Google Web サービスに接続する .NET Web サービス用のコードを示しています。wsdl.exe で生成されたコードを挿入するためのプレースホルダーがあります。
  
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


