---
title: InfoPath 2003 オブジェクト モデルを使用してフォーム データにアクセス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- xdocument interface [infopath 2007],InfoPath 2003-compatible form templates, accessing form data,XDocumentsCollection interface [InfoPath 2007]
localization_priority: Normal
ms.assetid: e0731014-f454-4417-9f90-19f3387f5776
description: InfoPath フォームの機能を拡張しようと思うと、多くの場合、フォームの基になる XML ドキュメントに関する情報へのアクセス、XML ドキュメントに記述されているデータへのアクセス、XML ドキュメントに対する何らかの操作の実行などの処理をプログラムで行う必要が出てきます。InfoPath オブジェクト モデルでは、XDocument インターフェイスと XDocumentsCollection インターフェイスを関連させて使用することにより、フォームの基になる XML ドキュメントにアクセスしたり、その XML ドキュメントを操作したりすることができます。
ms.openlocfilehash: 24e9abc8ce7327ab94b3608f1279c0f0d381ea83
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799113"
---
# <a name="access-form-data-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してフォーム データにアクセス

InfoPath フォームの機能を拡張しようと思うと、多くの場合、フォームの基になる XML ドキュメントに関する情報へのアクセス、XML ドキュメントに記述されているデータへのアクセス、XML ドキュメントに対する何らかの操作の実行などの処理をプログラムで行う必要が出てきます。InfoPath オブジェクト モデルでは、[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) インターフェイスと [XDocumentsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocumentsCollection.aspx) インターフェイスを関連させて使用することにより、フォームの基になる XML ドキュメントにアクセスしたり、その XML ドキュメントを操作したりすることができます。 
  
**XDocument** インターフェイスには、実にさまざまなプロパティ、メソッド、およびイベントが用意されており、フォームの基になる XML ドキュメントを扱えるだけではなく、InfoPath のユーザー インターフェイスで行える多数の操作を実行することもできるため、このインターフェイスは InfoPath オブジェクト モデルの中では最も便利な型の 1 つと言えます。InfoPath 2003 互換オブジェクト モデルを使用して作成されたマネージ コード プロジェクトでは、プロジェクトのフォーム コード内にイベント ハンドラーを含む  **** という名前の `thisXDocument` 型の変数が、クラスの  `_StartUp` メソッドの中で自動的に定義されます。フォームのコード内で  `thisXDocument` 変数を使用すると、 **XDocument** インターフェイスとそのメンバーにアクセスできます。 
  
## <a name="overview-of-the-xdocumentscollection-interface"></a>XDocumentsCollection インターフェイスの概要

**XDocumentsCollection** インターフェイスには、次のメソッドおよびプロパティがあります。フォームの開発者は、これらを使用することにより、コレクションに含まれている **XDocument** オブジェクトを管理できます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Close.aspx) メソッド  <br/> |指定したフォームを閉じます。  <br/> |
|[New](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.New.aspx) メソッド  <br/> |既存のフォームに基づいて新しいフォームを作成します。  <br/> |
|[NewFromSolution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolution.aspx) メソッド  <br/> |既存のフォーム テンプレートに基づいて新しいフォームを作成します。  <br/> |
|[NewFromSolutionWithData](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.NewFromSolutionWithData.aspx) メソッド  <br/> |指定した XML データとフォーム テンプレートを使用して、新しい InfoPath フォームを作成します。  <br/> |
|[Open](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Open.aspx) メソッド  <br/> |指定したフォームを開きます。  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Count.aspx) プロパティ  <br/> |コレクションに含まれている **XDocument** オブジェクトの数を返します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocuments2.Item.aspx) プロパティ  <br/> |指定した **XDocument** オブジェクトへの参照を返します。  <br/> |
   
## <a name="overview-of-the-xdocument-interface"></a>XDocument インターフェイスの概要

**XDocument** インターフェイスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、フォームの基になる XML ドキュメントと相互作用したり、その XML ドキュメントに対して操作を実行したりできます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[GetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDataVariable.aspx) メソッド  <br/> |指定したデータ変数の文字列値を返します。  <br/> |
|[GetDOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.GetDOM.aspx) メソッド  <br/> |指定した **DataObject** オブジェクトに関連付けられている XML ドキュメント オブジェクト モデル (DOM) への参照を返します。  <br/> |
|[ImportFile](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ImportFile.aspx) メソッド  <br/> |指定したフォームを現在開いているフォームにインポート (マージ) します。  <br/> |
|[PrintOut](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.PrintOut.aspx) メソッド  <br/> |フォームの現在のビューを印刷します。  <br/> |
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Query.aspx) メソッド  <br/> |フォームに関連付けられているデータ アダプターからデータを取得します。  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Save.aspx) メソッド  <br/> |現在開いているフォームを保存します。  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SaveAs.aspx) メソッド  <br/> |現在開いているフォームを指定された名前で保存します。  <br/> |
|[SetDataVariable](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.SetDataVariable.aspx) メソッド  <br/> |指定したデータ変数の値を設定します。  <br/> |
|[Submit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Submit.aspx) メソッド  <br/> |デザイン モードで確立された送信操作に従ってフォームを送信します。  <br/> |
|[DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) プロパティ  <br/> |**DataObjects** コレクションへの参照を返します。  <br/> |
|[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) プロパティ  <br/> |フォームのソース XML データが格納されている XML DOM への参照を返します。  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Errors.aspx) プロパティ  <br/> |**Errors** コレクションへの参照を返します。  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Extension.aspx) プロパティ  <br/> |フォーム コード ファイルに含まれているすべての関数と変数を表すオブジェクトへの参照を返します。  <br/> |
|[IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) プロパティ  <br/> |フォーム内のデータが変更されているかどうかを示す **Boolean** 値を返します。  <br/> |
|[IsDOMReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDOMReadOnly.aspx) プロパティ  <br/> |XML DOM が読み取り専用に設定されているかどうかを示す **Boolean** 値を返します。  <br/> |
|[IsNew](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsNew.aspx) プロパティ  <br/> |変更された後にフォームが保存されたかどうかを示す **Boolean** 値を返します。  <br/> |
|[IsReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsReadOnly.aspx) プロパティ  <br/> |フォームが読み取り専用モードかどうかを示す **Boolean** 値を返します。  <br/> |
|[IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) プロパティ  <br/> |フォームがデジタル署名されているかどうかを示す **Boolean** 値を返します。  <br/> |
|[Language](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Language.aspx) プロパティ  <br/> |フォームに使用される言語の文字列値を指定または取得します。  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.QueryAdapter.aspx) プロパティ  <br/> |データ アダプター オブジェクトへの参照を返します。  <br/> |
|[Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) プロパティ  <br/> |**Solution** オブジェクトへの参照を返します。  <br/> |
|[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) プロパティ  <br/> |**UI** オブジェクトへの参照を返します。  <br/> |
|[URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.URI.aspx) プロパティ  <br/> |フォームの URI (Uniform Resource Identifier) が格納された文字列値を返します。  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) プロパティ  <br/> |**View** オブジェクトへの参照を返します。  <br/> |
|[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.ViewInfos.aspx) プロパティ  <br/> |**ViewInfos** コレクションへの参照を返します。  <br/> |
   
## <a name="using-the-xdocuments-collection-and-the-xdocument-interfaces"></a>XDocuments コレクションと XDocument インターフェイスを使用する

**XDocumentsCollection** インターフェイスには、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.XDocuments.aspx) インターフェイスの [XDocuments](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) プロパティを通じてアクセスできます。InfoPath 2003 互換オブジェクト モデルを使用して作成されたマネージ コード プロジェクトでは、プロジェクトのフォーム コードの  **** メソッド内でインスタンス化される  `thisApplication` 変数を使用して `_StartUp` インターフェイスにアクセスできます。次に示すコードは、現在のプロジェクトの **XDocumentsCollection** インターフェイスを参照する変数を作成します。 
  
```cs
XDocumentsCollection xdocs;
xdocs = thisApplication.XDocuments;
// Write code here to work with the XDocumentsCollection.
```

```vb
Dim xdocs As XDocumentsCollection
xdocs = thisApplication.XDocuments
' Write code here to work with the XDocumentsCollection.
```

InfoPath 2003 互換オブジェクト モデルを使用して作成されたマネージ コード プロジェクトでは、プロジェクトのフォーム コードの  **** メソッド内でインスタンス化される  `thisXDocument` 変数を使用して `StartUp` インターフェイスにアクセスできます。次に示すコードは、  `thisXDocument` 変数を使用して現在のプロジェクトの **XDocument** インターフェイスにアクセスし、現在開いているフォームの URI を通知メッセージで表示します。 
  
```cs
thisXDocument.UI.Alert(thisXDocument.URI);
```

```vb
thisXDocument.UI.Alert(thisXDocument.URI)
```

> [!NOTE]
> [!メモ] **XDocument** インターフェイスを使用してフォームの基になる XML ドキュメントにアクセスすると、現在開いているフォームに関連付けられている XML ドキュメントにアクセスできます。 
  
**XDocument** インターフェイスのキー プロパティは **DOM** プロパティです。このプロパティは、フォームのソース XML データが格納された XML DOM への参照を返します。 **DOM** プロパティを使用すると、XML DOM でサポートされている任意のプロパティとメソッドを使用できます。たとえば、次に示すコードは、XML DOM の **xml** プロパティを使用して、フォームの基になる XML ドキュメントのすべての内容を取得し、表示しています。 
  
```cs
string xmldoc;
xmldoc = thisXDocument.DOM.xml;
// Display xml.
thisXDocument.UI.Alert(xmldoc);
```

```vb
Dim xmldoc As String
xmldoc = thisXDocument.DOM.xml
' Display xml.
thisXDocument.UI.Alert(xmldoc)
```

> [!NOTE]
> XML DOM の詳細とそのすべてのプロパティとそれをサポートするメソッドについては、MSDN の MSXML SDK を参照してください。 
  

