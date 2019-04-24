---
title: エラーを処理する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- エラー [infopath 2007],処理,FormErrorCollection [InfoPath 2007],InfoPath 2007,エラー処理,FormError [InfoPath 2007],エラー処理 [InfoPath 2007]
localization_priority: Normal
ms.assetid: 132cb698-d9a5-4767-b3d1-5dd1343a1ff4
description: カスタム アプリケーションを作成するときに、開発者はエラー処理を行わなければならないことがよくあります。エラー処理では、アプリケーションで発生したエラーをチェックしたり、カスタム エラーを作成して発生させたりするプログラミング コードを記述します。Microsoft.Office.InfoPath 名前空間によって提供される InfoPath オブジェクト モデルでは、FormError クラスを FormErrorCollection クラスと共に使用するエラー処理がサポートされています。
ms.openlocfilehash: 30cf649188b7e4cbc35469d2a50540bb13ecb38d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303606"
---
# <a name="handle-errors"></a>エラーを処理する

カスタム アプリケーションを作成するときに、開発者はエラー処理を行わなければならないことがよくあります。エラー処理では、アプリケーションで発生したエラーをチェックしたり、カスタム エラーを作成して発生させたりするプログラミング コードを記述します。[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath オブジェクト モデルでは、 [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) クラスを [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) クラスと共に使用するエラー処理がサポートされています。 
  
InfoPath では、次のような場合にエラーが発生する可能性があります。
  
- フォームに入力されたデータが XML スキーマの検証に失敗したとき。
    
- カスタム検証の制約に違反があったとき。
    
- [XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) イベント オブジェクトの [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) メソッドによってエラーが生成されたとき。 
    
- [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) クラスの [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) メソッドを使用してユーザー定義エラーが作成されたとき。 
    
## <a name="overview-of-the-formerrorcollection-class"></a>FormErrorCollection クラスの概要

[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) クラスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、コレクションに含まれている [FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) オブジェクトを管理できます。 
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) メソッド (+3 オーバーロード)  <br/> |**FormError** オブジェクトを作成し、それをコレクションに追加します。  <br/> |
|[Delete](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Delete.aspx) メソッド (+1 オーバーロード)  <br/> |指定したユーザー定義エラーをコレクションから削除します。  <br/> |
|[DeleteAll](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.DeleteAll.aspx) メソッド  <br/> |コレクションに含まれているすべての **FormError** オブジェクトを削除します。  <br/> |
|[GetErrors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.GetErrors.aspx) (+1 オーバーロード)  <br/> |指定した名前または型のすべての **FormError** オブジェクトをコレクションから返します。  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Count.aspx) プロパティ  <br/> |コレクションに含まれている **FormError** オブジェクトの数を取得します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Item.aspx) プロパティ  <br/> |指定したインデックス番号に基づく **FormError** オブジェクトへの参照を取得します。  <br/> |
   
## <a name="overview-of-the-formerror-class"></a>FormError クラスの概要

[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) クラスには、次のプロパティがあります。フォームの開発者は、これらを使用することにより、発生したエラーに関する情報にアクセスできます。 
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[DetailedMessage](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.DetailedMessage.aspx) プロパティ  <br/> |**FormError** オブジェクトの詳細なエラー メッセージを取得または設定します。  <br/> |
|[ErrorCode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.ErrorCode.aspx) プロパティ  <br/> |**FormError** オブジェクトのエラー コードを取得または設定します。  <br/> |
|[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) プロパティ  <br/> |**FormError** オブジェクトに関連付けられたノードにある **XPathNavigator** オブジェクトを取得します。  <br/> |
|[Message](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Message.aspx) プロパティ  <br/> |**FormError** オブジェクトの短いエラー メッセージを取得または設定します。  <br/> |
|[FormErrorType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.FormErrorType.aspx) プロパティ  <br/> |**FormError** オブジェクトの型を取得します。  <br/> |
   
## <a name="using-the-formerrorcollection-and-formerror-classes"></a>FormErrorCollection クラスおよび FormError クラスを使用する

フォームに関連付けられた **FormErrorCollection** オブジェクトにアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) オブジェクトの [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用します。 **FormErrorCollection** オブジェクトはフォームの基になる XML ドキュメントに関連付けられているため、エラーが発生した場合は、現在の XML ドキュメント内でそのエラーや追加のエラーにアクセスし、エラーを管理することができます。次の例では、ループを使用して、フォームの基になる XML ドキュメント内にあるエラーをチェックする方法を示します。エラーがある場合は、関数で各エラーをループ処理し、 **FormError** オブジェクトの **Message** プロパティを使用して、ユーザーにメッセージ ボックスを表示します。 
  
```cs
public void CheckErrors(XPathNavigator xmlNode)
{
   foreach(FormError err in this.Errors)
   {
      if(xmlNode.InnerXml == err.Site.InnerXml)
         MessageBox.Show("The following error has occured: "
             + err.Message);
   }
}
```

```vb
Public Sub CheckErrors(ByVal xmlNode As XPathNavigator)
   Dim err As FormError
   For Each err In Me.Errors
      If xmlNode.InnerXml = err.Site.InnerXml Then
         MessageBox.Show("The following error has occured: " _
             &amp; err.Message)
   End If
End Sub
```

上の関数は、フォームのデータ検証イベント ハンドラーの 1 つから呼び出すことができます。たとえば、フォーム内のフィールドの [Changed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEvent.Changed.aspx) イベントのイベント ハンドラーで使用した場合、関数の呼び出しにより、次のように [XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) イベント オブジェクトの [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) プロパティを使用して XML ノードが引数として渡されます。 
  
```cs
CheckErrors(e.Site);
```

```vb
CheckErrors(e.Site)
```

InfoPath によって生成されるエラーの処理に加えて、フォームの開発者は、[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) イベント オブジェクトの [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) メソッド、または [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) クラスの [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) メソッドを使用して、カスタム エラーを生成することもできます。 [ReportError(XPathNavigator, Boolean, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) メソッドまたは [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) メソッドの使用方法については、このトピックの先頭にあるそれぞれのメソッドのリンクをクリックしてください。 
  
## <a name="handling-managed-code-exceptions"></a>マネージ コードの例外を処理する

try-catch 例外処理を使用すると、次のコードに示すようにマネージ コード フォーム テンプレート内で発生した例外を処理することができます。
  
```cs
FileQueryConnection queryXMLFile = 
   (FileQueryConnection)this.DataConnections["form1"];
// Perform the query.
try
{
   queryXMLFile.Execute();
}
catch (Exception ex)
{
   MessageBox.Show("Failed to query." + System.Environment.NewLine 
      + ex.Message);
}
```

```vb
Dim queryXMLFile As FileQueryConnection = _
   DirectCast(Me.DataConnections("form1"), FileQueryConnection)
' Perform the query.
Try
   queryXMLFile.Execute();
Catch ex As Exception
   MessageBox.Show("Failed to query." &amp; System.Environment.NewLine 
      &amp; ex.Message)
End Try
```

フォーム コード内で try-catch 例外処理を使用していないと、デバッグ中およびプレビュー中に、未処理の例外に関する情報が InfoPath によって InfoPath のエラー ダイアログ ボックスに表示されます。また、既定では、マネージ コード フォーム テンプレートを展開した場合の実行時には、未処理の例外は Info Path エラー ダイアログ ボックスに表示されません。実行時に未処理の例外に関する情報を表示するには、次の手順を使用します。
  
### <a name="enable-notifications-for-unhandled-managed-code-exceptions-at-run-time"></a>未処理のマネージ コード例外の実行時の通知を有効にする

1. InfoPath デザイン モードを開いて、[ **ファイル**] タブをクリックします。 
    
2. [ **オプション**] をクリックして、[ **基本設定**] カテゴリの [ **InfoPath オプション**] をクリックします。 
    
3. [ **詳細設定**] タブで、[ **Visual Basic または Visual C# コードのエラーを表示する**] チェック ボックスをオンにします。 
    

