---
title: InfoPath 2003 オブジェクト モデルを使用してアプリケーション データにアクセスする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- フォーム テンプレート [infopath 2007],2003 オブジェクト モデルを使用してデータにアクセスする,InfoPath 2003 互換のフォーム テンプレート,アプリケーション データにアクセスする
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: InfoPath 2003 互換オブジェクト モデルには、InfoPath アプリケーションに関する情報 (フォームの基になる XML ドキュメント、フォーム定義ファイル (.xsf) などに関する情報) へのアクセスに使用できるオブジェクトとコレクションがあります。これらのデータには、InfoPath オブジェクト モデルの階層構造の最上位レベルにあるオブジェクトを通じてアクセスします。これらのオブジェクトは、Application インターフェイスを通じてインスタンス化されます。
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437442"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してアプリケーション データにアクセスする

InfoPath 2003 互換オブジェクト モデルには、InfoPath アプリケーションに関する情報 (フォームの基になる XML ドキュメント、フォーム定義ファイル (.xsf) などに関する情報) へのアクセスに使用できるオブジェクトとコレクションがあります。これらのデータには、InfoPath オブジェクト モデルの階層構造の最上位レベルにあるオブジェクトを通じてアクセスします。これらのオブジェクトは、[Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) インターフェイスを通じてインスタンス化されます。 
  
Visual Studio 2012 を使用して作成した InfoPath 2003 互換マネージ コード フォーム テンプレート プロジェクトでは、フォーム コード クラスの  `thisApplication` メソッドの中で  `_Startup` 変数が初期化されます。この変数を使用すると、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) インターフェイスのメンバーにアクセスできます。次の例では、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) インターフェイスの [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) プロパティと [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) プロパティを使用して、InfoPath の実行中のインスタンスの名前とバージョン番号を取得し、 [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) インターフェイスの [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) メソッドを使用してこの情報をメッセージ ボックスに表示しています。 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

Visual C# の例では、通知メッセージの文字列に  `\n` 文字への参照を入れてありますが、これは InfoPath のアンマネージ コードによって標準の改行として表示されます。このためテキストはそこで分割されて、メッセージ ボックス内で改行されます。現在の環境とプラットフォーム用に定義された改行を明示的に使用するには、次の例のように、代わりに **Environment.NewLine** プロパティを使用します。 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a>フォームの基になる XML ドキュメントからデータにアクセスする

開発者は、[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスを使用して、フォームの基になる XML ドキュメントに関する情報にアクセスすることができます。アクセスできる情報には、フォームのソース XML データが格納されている XML ドキュメント オブジェクト モデル (DOM) への参照も含まれます。 
  
次の例では、最初のメッセージ ボックスに [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスから取得できるデータの一部が表示されます。表示されるのは、基となる XML ドキュメントに変更が加えられているかどうか ( [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) プロパティを使用)、およびそれがデジタル署名されているかどうか ( [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) プロパティを使用) という情報です。その次のメッセージ ボックスには、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスの [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) プロパティを使用して、フォームの基になる XML ドキュメントのソース XML を表示しています。 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

前の例で使用されている **xml** プロパティは、XML ドキュメント オブジェクト モデル (DOM) のプロパティです。XML DOM の詳細については、MSXML 5.0 SDK のドキュメントを参照してください。 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a>フォームのフォーム定義ファイルからデータにアクセスする

フォームの .xsf ファイルに関する情報 (それに含まれるソース XML データへの XML DOM 参照など) には、[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスを使用してアクセスできます。この情報へのアクセスには、 [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) プロパティを使用します。このプロパティは、 [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) インターフェイスへの参照を返します。 
  
次の例では、最初の通知に [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) インターフェイスを通じて取得できるデータのいくつかを表示しています。表示されるのは、URI (Uniform Resource Identifier) での場所 ( [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) プロパティを使用) と、バージョン番号 ( [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) プロパティを使用) です。2 つ目の通知には、 [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) インターフェイスの [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) プロパティを使用して, .xsf ファイルのソース XML を表示しています。 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


