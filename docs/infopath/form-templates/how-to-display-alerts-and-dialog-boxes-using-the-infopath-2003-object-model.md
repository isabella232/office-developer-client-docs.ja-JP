---
title: 通知と、InfoPath 2003 オブジェクト モデルを使用してダイアログ ボックスを表示します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003 と互換性のあるフォーム テンプレート] ダイアログ ボックスを表示するフォームのテンプレート [InfoPath 2007] ダイアログ ボックスで、アラートを表示するダイアログ ボックスを表示する InfoPath 2003 と互換性のあるフォーム テンプレートを InfoPath 2003 と互換性のあるフォーム テンプレートでの表示、、InfoPath 2003 と互換性のあるフォーム テンプレートは、警告を表示します。
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートの機能を拡張するコードを記述する場合は、ダイアログ ボックス内の情報をユーザーに提供すると便利なことがあります。
ms.openlocfilehash: 1cc0f4c7a6696eae2d3b7058898b4119cede79e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799121"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a>通知と、InfoPath 2003 オブジェクト モデルを使用してダイアログ ボックスを表示します。

InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートの機能を拡張するコードを記述する場合は、ダイアログ ボックス内の情報をユーザーに提供すると便利なことがあります。 ダイアログ ボックスおよび関連するユーザー インターフェイス要素をプログラムで表示するには InfoPath で、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスのメソッドを使用して、します。 
  
## <a name="overview-of-the-uiobject-interface"></a>UIObject インターフェイスの概要

[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスには、次のメソッドは、フォーム開発者がフォームの記入には、InfoPath のユーザーに表示されるダイアログ ボックスのさまざまな種類に使用できますが用意されています。 
  
|名前|説明|
|:-----|:-----|
|[警告](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |指定されたメッセージ文字列を含む単純なメッセージ ボックスが表示されます。 ユーザーから必要な入力がないとメッセージのみを表示する必要があるとき、このメソッドを使用する必要があります。 表示されるダイアログ ボックスは **[ok]** ボタンをクリックして終了します。  <br/> |
|[確認](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |ユーザーが入力可能なメッセージ ボックスをいくつかのボタンと共に表示します。 返される値は、 [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)列挙定数のいずれかです。  <br/> |
|[SetSaveAsDialogFileName](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |[名前を**付けて**保存] ダイアログ ボックスでフォームの既定のファイル名を設定します。  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |[名前を**付けて**保存] ダイアログ ボックスが開いたときに参照するときに開始される最初の場所を設定します。  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |現在開いているメッセージに関連付けられているフォームの既定の電子メール アプリケーションで新しい電子メール メッセージを作成します。  <br/> |
|[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |指定された .html ファイルおよび位置引数に基づいて、モーダル ダイアログ ボックスが表示されます。 複数のユーザーに簡単なメッセージを表示して、(以外は、 **[はい]** に用意されている簡単な確認は、ユーザーからのデータの一部を取得する必要がある場合、このメソッドを使用する必要があります。 | **いいえ** | **キャンセル**ボタンで**確認する**方法が表示されます)。  <br/> |
|[ShowSignatureDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |組み込みの **[デジタル署名**] ダイアログ ボックスが表示されます。  <br/> |
   
## <a name="using-the-uiobject-interface"></a>UIObject インターフェイスの使用

[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスへのアクセスが[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)インターフェイスの[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)は、それ自体は、`thisXDocument`で初期化されている変数、`_Startup`フォーム コードのクラスのメソッドです。 [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx)と[警告](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx)、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスのメソッドを使用して次の例に示します。 
  
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

この例では、HTML ファイルの show.html で定義されているカスタム ダイアログ ボックスを表示するのには、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスの[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを使用する方法を示します。 
  
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

Visual C# と Visual Basic のサンプルは、 [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドによって呼び出される] ダイアログ ボックスを定義する"show.html"という名前の HTML ファイルに依存します。 この HTML ファイルは、フォームからデータの一部が表示され、ユーザーが値を入力するテキスト ボックスを示しています。 ダイアログ ボックスが閉じられるときに、フォームにテキスト ボックスの値が返されます。 
  
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
> [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを実行するかをプレビューする完全信頼が必要です。 詳細については、[プレビューしその必要とする完全信頼フォーム テンプレートのデバッグ](how-to-preview-and-debug-form-templates-that-require-full-trust.md)を参照してください。 
  

