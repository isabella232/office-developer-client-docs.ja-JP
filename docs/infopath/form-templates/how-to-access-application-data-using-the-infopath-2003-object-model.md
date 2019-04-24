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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303683"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="6e6c7-105">InfoPath 2003 オブジェクト モデルを使用してアプリケーション データにアクセスする</span><span class="sxs-lookup"><span data-stu-id="6e6c7-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="6e6c7-p102">InfoPath 2003 互換オブジェクト モデルには、InfoPath アプリケーションに関する情報 (フォームの基になる XML ドキュメント、フォーム定義ファイル (.xsf) などに関する情報) へのアクセスに使用できるオブジェクトとコレクションがあります。これらのデータには、InfoPath オブジェクト モデルの階層構造の最上位レベルにあるオブジェクトを通じてアクセスします。これらのオブジェクトは、[Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) インターフェイスを通じてインスタンス化されます。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-p102">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file. This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="6e6c7-p103">Visual Studio 2012 を使用して作成した InfoPath 2003 互換マネージ コード フォーム テンプレート プロジェクトでは、フォーム コード クラスの  `thisApplication` メソッドの中で  `_Startup` 変数が初期化されます。この変数を使用すると、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) インターフェイスのメンバーにアクセスできます。次の例では、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) インターフェイスの [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) プロパティと [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) プロパティを使用して、InfoPath の実行中のインスタンスの名前とバージョン番号を取得し、 [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) インターフェイスの [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) メソッドを使用してこの情報をメッセージ ボックスに表示しています。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-p103">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface. In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath. This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="6e6c7-p104">Visual C# の例では、通知メッセージの文字列に  `\n` 文字への参照を入れてありますが、これは InfoPath のアンマネージ コードによって標準の改行として表示されます。このためテキストはそこで分割されて、メッセージ ボックス内で改行されます。現在の環境とプラットフォーム用に定義された改行を明示的に使用するには、次の例のように、代わりに **Environment.NewLine** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-p104">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box. To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="6e6c7-113">フォームの基になる XML ドキュメントからデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="6e6c7-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="6e6c7-114">開発者は、[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスを使用して、フォームの基になる XML ドキュメントに関する情報にアクセスすることができます。アクセスできる情報には、フォームのソース XML データが格納されている XML ドキュメント オブジェクト モデル (DOM) への参照も含まれます。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="6e6c7-p105">次の例では、最初のメッセージ ボックスに [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスから取得できるデータの一部が表示されます。表示されるのは、基となる XML ドキュメントに変更が加えられているかどうか ( [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) プロパティを使用)、およびそれがデジタル署名されているかどうか ( [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) プロパティを使用) という情報です。その次のメッセージ ボックスには、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスの [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) プロパティを使用して、フォームの基になる XML ドキュメントのソース XML を表示しています。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-p105">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property). The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
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

<span data-ttu-id="6e6c7-p106">前の例で使用されている **xml** プロパティは、XML ドキュメント オブジェクト モデル (DOM) のプロパティです。XML DOM の詳細については、MSXML 5.0 SDK のドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-p106">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM). For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="6e6c7-119">フォームのフォーム定義ファイルからデータにアクセスする</span><span class="sxs-lookup"><span data-stu-id="6e6c7-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="6e6c7-p107">フォームの .xsf ファイルに関する情報 (それに含まれるソース XML データへの XML DOM 参照など) には、[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスを使用してアクセスできます。この情報へのアクセスには、 [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) プロパティを使用します。このプロパティは、 [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) インターフェイスへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-p107">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface. This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="6e6c7-p108">次の例では、最初の通知に [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) インターフェイスを通じて取得できるデータのいくつかを表示しています。表示されるのは、URI (Uniform Resource Identifier) での場所 ( [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) プロパティを使用) と、バージョン番号 ( [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) プロパティを使用) です。2 つ目の通知には、 [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) インターフェイスの [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) プロパティを使用して, .xsf ファイルのソース XML を表示しています。</span><span class="sxs-lookup"><span data-stu-id="6e6c7-p108">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property). The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
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


