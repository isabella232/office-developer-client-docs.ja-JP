---
title: InfoPath 2003 オブジェクト モデルを使用してエラーを処理する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, handling errors,InfoPath 2003-compatible form templates, error handling,form templates [InfoPath 2007], error handling,error handling [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: eeb05205-d6f4-4931-b9a9-55a663bb1a25
description: カスタム アプリケーションを作成する際、開発者はしばしばエラー ハンドリングを行わなければなりません。これには、アプリケーションで発生したエラーをチェックするプログラム コードや、カスタム エラーを作成して発生させるプログラム コードの記述などの作業が伴います。InfoPath 2003 互換オブジェクト モデルでは、ErrorObject オブジェクトと ErrorsCollection コレクションを組み合わせて使用することによるエラー ハンドリングがサポートされています。
ms.openlocfilehash: 93991e33d8867f89454bec08b41ba83e98ab0a17
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439479"
---
# <a name="handle-errors-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してエラーを処理する

カスタム アプリケーションを作成する際、開発者はしばしばエラー ハンドリングを行わなければなりません。これには、アプリケーションで発生したエラーをチェックするプログラム コードや、カスタム エラーを作成して発生させるプログラム コードの記述などの作業が伴います。InfoPath 2003 互換オブジェクト モデルでは、[ErrorObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorObject.aspx) オブジェクトと [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) コレクションを組み合わせて使用することによるエラー ハンドリングがサポートされています。 
  
InfoPath では、フォームに入力されたデータが XML スキーマ検証に失敗したとき、カスタム検証制約に違反があったとき、[DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.ReportError.aspx) オブジェクトの [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) メソッドによりエラーが生成されたとき、および [ErrorsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) コレクションの [Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ErrorsCollection.aspx) メソッドを使用してエラーが作成されたときにエラーが発生します。 
  
## <a name="overview-of-the-errorscollection-collection"></a>ErrorsCollection コレクションの概要

**ErrorsCollection** コレクションには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、コレクションに含まれている **ErrorObject** オブジェクトを管理できます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Add.aspx) メソッド  <br/> |**ErrorObject** オブジェクトを作成し、それをコレクションに追加します。  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Delete.aspx) メソッド  <br/> |指定した XML ノードと条件名に関連付けられている、 **ReportError** メソッドを使用して追加したカスタム エラー以外のすべての **ErrorObject** オブジェクトを削除します。  <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.DeleteAll.aspx) メソッド  <br/> |コレクションに含まれているすべての **ErrorObject** オブジェクトを削除します。  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Count.aspx) プロパティ  <br/> |コレクションに含まれている **ErrorObject** オブジェクトの数を取得します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Errors.Item.aspx) プロパティ  <br/> |指定したインデックス番号に基づく **ErrorObject** オブジェクトへの参照を取得します。  <br/> |
   
## <a name="overview-of-the-errorobject-object"></a>ErrorObject オブジェクトの概要

**ErrorObject** オブジェクトには、次のプロパティがあります。フォームの開発者は、これらを使用することにより、発生したエラーに関する情報にアクセスできます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[ConditionName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ConditionName.aspx) プロパティ  <br/> |**ErrorObject** オブジェクトの型に応じて、エラー条件の名前を取得するか、または **null** を返します。  <br/> |
|[DetailedErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.DetailedErrorMessage.aspx) プロパティ  <br/> |**ErrorObject** オブジェクトの詳細なエラー メッセージを取得または設定します。  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorCode.aspx) プロパティ  <br/> |**ErrorObject** オブジェクトのエラー コードを取得または設定します。  <br/> |
|[Node](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.Node.aspx) プロパティ  <br/> |**ErrorObject** オブジェクトに関連付けられている XML ノードへの参照を取得します。  <br/> |
|[ShortErrorMessage](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ShortErrorMessage.aspx) プロパティ  <br/> |**ErrorObject** オブジェクトの短いエラー メッセージを取得または設定します。  <br/> |
|[ErrorType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Error.ErrorType.aspx) プロパティ  <br/> |**ErrorObject** オブジェクトの型を取得します。  <br/> |
   
## <a name="using-the-errorscollection-and-errorobject"></a>ErrorsCollection および ErrorObject を使用する

**ErrorsCollection** コレクションにアクセスするには、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.Errors.aspx) オブジェクトの [Errors](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) プロパティを使用します。 **ErrorsCollection** コレクションはフォームの基になる XML ドキュメントと関連付けられているため、エラー発生時にはエラーは XML ドキュメント内で発生します。次の例は、Visual C# の **foreach** ループを使用して、フォームの基になる XML ドキュメント内にあるエラーをチェックする方法を示します。エラーがある場合は、関数で各エラーをループ処理し、 **ErrorObject** オブジェクトの **ShortErrorMessage** プロパティを使用してメッセージをユーザーに表示します。 
  
```cs
public void CheckErrors(IXMLDOMNode xmlNode)
{
   foreach(ErrorObject err in thisXDocument.Errors)
   {
      if(xmlNode==err.Node)
         thisXDocument.UI.Alert("The following error has occured: "
             + err.ShortErrorMessage + ".");
   }
}
```

上の関数は、フォームのデータ検証イベントハンドラーの 1 つから呼び出すことができます。たとえば、フォーム内のフィールドの [OnAfterChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._DataDOMEventSink_Event.OnAfterChange.aspx) イベント ハンドラー内で使用する場合なら、次に示すように [DataDOMEventObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEvent.Site.aspx) オブジェクトの [Site](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataDOMEventObject.aspx) プロパティを使用して、関数の呼び出し時に XML ノードを引数として渡します。 
  
```cs
CheckErrors(e.Site);
```

フォームの開発者は、InfoPath により生成されたエラーの処理に加えて、 **DataDOMEventObject** オブジェクトの **ReportError** メソッドまたは **ErrorsCollection** コレクションの **Add** メソッドを使用してカスタム エラーを発生させることもできます。 **ReportError** メソッドおよび **Add** メソッドの使用方法の詳細については、このトピックの先頭にあるメソッド名をクリックしてください。 
  
## <a name="handling-managed-code-exceptions"></a>マネージ コードの例外を処理する

try-catch 例外処理を使用すると、次のコードに示すようにマネージ コード フォーム テンプレート内で発生した例外を処理することができます。
  
```cs
DataAdapters dataAdapters;
dataAdapters = thisXDocument.DataAdapters; 
XMLFileAdapterObject queryXMLFile = 
   (XMLFileAdapterObject)dataAdapters["form1"];
// Perform the query.
try
{
   queryXMLFile.Query();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to query.\n\n" + ex.Message);
}
// Perform the submit.
try
{
   queryXMLFile.Submit();
}
catch (Exception ex)
{
   thisXDocument.UI.Alert("Failed to submit.\n\n" + ex.Message);
}
```

フォーム コード内で try-catch 例外処理を使用していないと、デバッグ中およびプレビュー中に、未処理の例外に関する情報が InfoPath によって InfoPath のエラー ダイアログ ボックスに表示されます。 
  

