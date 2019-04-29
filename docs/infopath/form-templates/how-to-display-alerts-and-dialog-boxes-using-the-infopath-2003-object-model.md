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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="52b69-104">InfoPath 2003 オブジェクト モデルを使用して警告とダイアログ ボックスを表示する</span><span class="sxs-lookup"><span data-stu-id="52b69-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="52b69-105">InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートの機能を拡張するためのコードを書く際、ユーザーにダイアログ ボックス形式で情報を表示すると便利な場合があります。</span><span class="sxs-lookup"><span data-stu-id="52b69-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="52b69-106">プログラムによってダイアログボックスと関連するユーザーインターフェイス要素を表示する方法については、「 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスのメソッドを使用する」をご利用ください。</span><span class="sxs-lookup"><span data-stu-id="52b69-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="52b69-107">UIObject インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="52b69-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="52b69-108">[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスには、次のメソッドが用意されています。フォームの開発者は、フォームに入力するときに、さまざまな種類のダイアログボックスを InfoPath ユーザーに表示するために使用することができます。</span><span class="sxs-lookup"><span data-stu-id="52b69-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="52b69-109">名前</span><span class="sxs-lookup"><span data-stu-id="52b69-109">Name</span></span>|<span data-ttu-id="52b69-110">説明</span><span class="sxs-lookup"><span data-stu-id="52b69-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="52b69-111">通知</span><span class="sxs-lookup"><span data-stu-id="52b69-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="52b69-p102">指定したメッセージ文字列を含む単純なメッセージ ボックスを表示します。このメソッドは、ユーザーからの入力が必要なく、メッセージを表示する必要がある場合にのみ使用します。表示されるダイアログ ボックスは、[**OK**] ボタンをクリックして閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="52b69-p102">Displays a simple message box that contains a specified message string. This method should be used when no input is required from the user and only a message needs to be displayed. The dialog box displayed is closed by clicking the **OK** button.  </span></span><br/> |
|[<span data-ttu-id="52b69-115">Confirm</span><span class="sxs-lookup"><span data-stu-id="52b69-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="52b69-116">ユーザーが入力可能なメッセージ ボックスをいくつかのボタンと共に表示します。</span><span class="sxs-lookup"><span data-stu-id="52b69-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="52b69-117">返される値は、 [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)列挙定数のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="52b69-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="52b69-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="52b69-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="52b69-119">[**名前を付けて保存**] ダイアログ ボックスにフォームの既定のファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="52b69-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="52b69-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="52b69-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="52b69-121">[**名前を付けて保存**] ダイアログ ボックスが開いたときに参照を開始する場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="52b69-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="52b69-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="52b69-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="52b69-123">既定の電子メールアプリケーションで新しい電子メールメッセージを作成し、現在開いているフォームをメッセージに添付します。</span><span class="sxs-lookup"><span data-stu-id="52b69-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="52b69-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="52b69-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="52b69-125">指定した .html ファイルと場所引数に基づいてモーダル ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="52b69-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="52b69-126">このメソッドは、ユーザーに対して単純なメッセージ以外を表示する場合に、ユーザーから何らかのデータを取得する必要がある場合に使用します (**はい**</span><span class="sxs-lookup"><span data-stu-id="52b69-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="52b69-127">**いいえ**</span><span class="sxs-lookup"><span data-stu-id="52b69-127">**No**</span></span> | <span data-ttu-id="52b69-128">**Confirm**メソッドによって表示される **[キャンセル]** ボタン)。</span><span class="sxs-lookup"><span data-stu-id="52b69-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="52b69-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="52b69-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="52b69-130">組み込みの [**デジタル署名**] ダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="52b69-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="52b69-131">UIObject インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="52b69-131">Using the UIObject Interface</span></span>

<span data-ttu-id="52b69-132">[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスは、XDocument インターフェイスの[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)プロパティを通じ[](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)てアクセスされます。これには`thisXDocument` 、フォームのコードクラスの`_Startup`メソッドで初期化された変数を通じてアクセスします。</span><span class="sxs-lookup"><span data-stu-id="52b69-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="52b69-133">次の例では、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスの[showmailitem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx)および[Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx)メソッドの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="52b69-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
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

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="52b69-134">ShowModalDialog メソッドの使用</span><span class="sxs-lookup"><span data-stu-id="52b69-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="52b69-135">この例では、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスの[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを使用して、html ファイルの show .html で定義されたカスタムダイアログボックスを表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="52b69-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
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

<span data-ttu-id="52b69-136">visual C# と visual Basic の両方のサンプルは、 [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドによって呼び出されるダイアログボックスを定義する ".html を表示する" という名前の html ファイルに依存しています。</span><span class="sxs-lookup"><span data-stu-id="52b69-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="52b69-137">この HTML ファイルは、フォームからのデータを表示し、ユーザーが値を入力するためのテキスト ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="52b69-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="52b69-138">テキスト ボックス内の値は、ダイアログ ボックスが閉じたときにフォームに返されます。</span><span class="sxs-lookup"><span data-stu-id="52b69-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
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
> <span data-ttu-id="52b69-139">[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを実行またはプレビューするには、完全な信頼が必要です。</span><span class="sxs-lookup"><span data-stu-id="52b69-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="52b69-140">詳細については、「[完全信頼が必要なフォームテンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-form-templates-that-require-full-trust.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52b69-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

