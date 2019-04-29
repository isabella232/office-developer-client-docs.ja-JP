---
title: InfoPath 2003 オブジェクト モデルを使用して警告とダイアログ ボックスを表示する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003 互換のフォームテンプレート、ダイアログボックスの表示、フォームテンプレート [infopath 2007]、ダイアログボックスの表示、警告、infopath の2003互換フォームテンプレートに表示されるダイアログボックス、infopath の2003互換フォームテンプレートでの表示、InfoPath 2003 互換フォームテンプレート、警告を表示する
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートの機能を拡張するためのコードを書く際、ユーザーにダイアログ ボックス形式で情報を表示すると便利な場合があります。
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409483"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用して警告とダイアログ ボックスを表示する

InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートの機能を拡張するためのコードを書く際、ユーザーにダイアログ ボックス形式で情報を表示すると便利な場合があります。 プログラムによってダイアログボックスと関連するユーザーインターフェイス要素を表示する方法については、「 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスのメソッドを使用する」をご利用ください。 
  
## <a name="overview-of-the-uiobject-interface"></a>UIObject インターフェイスの概要

[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスには、次のメソッドが用意されています。フォームの開発者は、フォームに入力するときに、さまざまな種類のダイアログボックスを InfoPath ユーザーに表示するために使用することができます。 
  
|名前|説明|
|:-----|:-----|
|[通知](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |指定したメッセージ文字列を含む単純なメッセージ ボックスを表示します。このメソッドは、ユーザーからの入力が必要なく、メッセージを表示する必要がある場合にのみ使用します。表示されるダイアログ ボックスは、[**OK**] ボタンをクリックして閉じることができます。<br/> |
|[Confirm](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |ユーザーが入力可能なメッセージ ボックスをいくつかのボタンと共に表示します。 返される値は、 [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)列挙定数のいずれかです。  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |[**名前を付けて保存**] ダイアログ ボックスにフォームの既定のファイル名を設定します。  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |[**名前を付けて保存**] ダイアログ ボックスが開いたときに参照を開始する場所を設定します。  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |既定の電子メールアプリケーションで新しい電子メールメッセージを作成し、現在開いているフォームをメッセージに添付します。  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |指定した .html ファイルと場所引数に基づいてモーダル ダイアログ ボックスを表示します。 このメソッドは、ユーザーに対して単純なメッセージ以外を表示する場合に、ユーザーから何らかのデータを取得する必要がある場合に使用します (**はい** | **いいえ** | **Confirm**メソッドによって表示される **[キャンセル]** ボタン)。  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |組み込みの [**デジタル署名**] ダイアログ ボックスを表示します。  <br/> |
   
## <a name="using-the-uiobject-interface"></a>UIObject インターフェイスの使用

[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスは、XDocument インターフェイスの[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)プロパティを通じ[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)てアクセスされます。これには`thisXDocument` 、フォームのコードクラスの`_Startup`メソッドで初期化された変数を通じてアクセスします。 次の例では、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスの[showmailitem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx)および[Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx)メソッドの使用方法を示します。 
  
```cs
thisXDocument.UI.ShowMailItem("someone@example.com","", "", 
   "Updated Form", "Here is the updated form that you requested.");
thisXDocument.UI.Alert("The email message has been created.");
```

```vb
thisXDocument.UI.ShowMailItem("someone@example.com", "", "", _
   "Updated Form", "Here is the updated form that you requested.")
thisXDocument.UI.Alert("The email message has been created.")
```

## <a name="using-the-showmodaldialog-method"></a>ShowModalDialog メソッドの使用

この例では、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスの[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを使用して、html ファイルの show .html で定義されたカスタムダイアログボックスを表示する方法を示します。 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Write your code here.
   thisXDocument.UI.ShowModalDialog(
      "show.html",(object)thisXDocument,200,450,50,50);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Write your code here.
   thisXDocument.UI.ShowModalDialog( _
      "show.html", _
      DirectCast(thisXDocument, Object), 200, 450, 50, 50)
End Sub

```

visual C# と visual Basic の両方のサンプルは、 [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドによって呼び出されるダイアログボックスを定義する ".html を表示する" という名前の html ファイルに依存しています。 この HTML ファイルは、フォームからのデータを表示し、ユーザーが値を入力するためのテキスト ボックスを表示します。 テキスト ボックス内の値は、ダイアログ ボックスが閉じたときにフォームに返されます。 
  
```html
<HTML>
   <HEAD>
      <script language="JScript">
function BtnClick()
{
   xdocument = window.dialogArguments;
   myXml = xdocument.DOM.xml
   aForm = oForm.elements;
   aForm.textBox.value = myXml;
}
      </script>
   </HEAD>
   <BODY>
      <H1><FONT face="Arial">This is a modal dialog box</FONT> &nbsp;
      </H1>
      <BUTTON onclick="BtnClick()" id="BUTTON1" type="button">
         Get XML DOM
      </BUTTON>
      <FORM ID="oForm">
         <INPUT Type="text" name="textBox">
      </FORM>
   </BODY>
</HTML>

```

> [!IMPORTANT]
> [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを実行またはプレビューするには、完全な信頼が必要です。 詳細については、「[完全信頼が必要なフォームテンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-form-templates-that-require-full-trust.md)」を参照してください。 
  

