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
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="041da-104">通知と、InfoPath 2003 オブジェクト モデルを使用してダイアログ ボックスを表示します。</span><span class="sxs-lookup"><span data-stu-id="041da-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="041da-105">InfoPath 2003 オブジェクト モデルを使用するフォーム テンプレートの機能を拡張するコードを記述する場合は、ダイアログ ボックス内の情報をユーザーに提供すると便利なことがあります。</span><span class="sxs-lookup"><span data-stu-id="041da-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="041da-106">ダイアログ ボックスおよび関連するユーザー インターフェイス要素をプログラムで表示するには InfoPath で、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスのメソッドを使用して、します。</span><span class="sxs-lookup"><span data-stu-id="041da-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="041da-107">UIObject インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="041da-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="041da-108">[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスには、次のメソッドは、フォーム開発者がフォームの記入には、InfoPath のユーザーに表示されるダイアログ ボックスのさまざまな種類に使用できますが用意されています。</span><span class="sxs-lookup"><span data-stu-id="041da-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="041da-109">名前</span><span class="sxs-lookup"><span data-stu-id="041da-109">Name</span></span>|<span data-ttu-id="041da-110">説明</span><span class="sxs-lookup"><span data-stu-id="041da-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="041da-111">警告</span><span class="sxs-lookup"><span data-stu-id="041da-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="041da-112">指定されたメッセージ文字列を含む単純なメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="041da-112">Displays a simple message box that contains a specified message string.</span></span> <span data-ttu-id="041da-113">ユーザーから必要な入力がないとメッセージのみを表示する必要があるとき、このメソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="041da-113">This method should be used when no input is required from the user and only a message needs to be displayed.</span></span> <span data-ttu-id="041da-114">表示されるダイアログ ボックスは **[ok]** ボタンをクリックして終了します。</span><span class="sxs-lookup"><span data-stu-id="041da-114">The dialog box displayed is closed by clicking the **OK** button.</span></span>  <br/> |
|[<span data-ttu-id="041da-115">確認</span><span class="sxs-lookup"><span data-stu-id="041da-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="041da-116">ユーザーが入力可能なメッセージ ボックスをいくつかのボタンと共に表示します。</span><span class="sxs-lookup"><span data-stu-id="041da-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="041da-117">返される値は、 [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx)列挙定数のいずれかです。</span><span class="sxs-lookup"><span data-stu-id="041da-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="041da-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="041da-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="041da-119">[名前を**付けて**保存] ダイアログ ボックスでフォームの既定のファイル名を設定します。</span><span class="sxs-lookup"><span data-stu-id="041da-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="041da-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="041da-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="041da-121">[名前を**付けて**保存] ダイアログ ボックスが開いたときに参照するときに開始される最初の場所を設定します。</span><span class="sxs-lookup"><span data-stu-id="041da-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="041da-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="041da-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="041da-123">現在開いているメッセージに関連付けられているフォームの既定の電子メール アプリケーションで新しい電子メール メッセージを作成します。</span><span class="sxs-lookup"><span data-stu-id="041da-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="041da-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="041da-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="041da-125">指定された .html ファイルおよび位置引数に基づいて、モーダル ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="041da-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="041da-126">複数のユーザーに簡単なメッセージを表示して、(以外は、 **[はい]** に用意されている簡単な確認は、ユーザーからのデータの一部を取得する必要がある場合、このメソッドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="041da-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="041da-127">**いいえ**</span><span class="sxs-lookup"><span data-stu-id="041da-127">**No**</span></span> | <span data-ttu-id="041da-128">**キャンセル**ボタンで**確認する**方法が表示されます)。</span><span class="sxs-lookup"><span data-stu-id="041da-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="041da-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="041da-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="041da-130">組み込みの **[デジタル署名**] ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="041da-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="041da-131">UIObject インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="041da-131">Using the UIObject Interface</span></span>

<span data-ttu-id="041da-132">[UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスへのアクセスが[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx)インターフェイスの[UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx)は、それ自体は、`thisXDocument`で初期化されている変数、`_Startup`フォーム コードのクラスのメソッドです。</span><span class="sxs-lookup"><span data-stu-id="041da-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="041da-133">[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx)と[警告](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx)、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスのメソッドを使用して次の例に示します。</span><span class="sxs-lookup"><span data-stu-id="041da-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
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

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="041da-134">ShowModalDialog メソッドの使用</span><span class="sxs-lookup"><span data-stu-id="041da-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="041da-135">この例では、HTML ファイルの show.html で定義されているカスタム ダイアログ ボックスを表示するのには、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx)インターフェイスの[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを使用する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="041da-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
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

<span data-ttu-id="041da-136">Visual C# と Visual Basic のサンプルは、 [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドによって呼び出される] ダイアログ ボックスを定義する"show.html"という名前の HTML ファイルに依存します。</span><span class="sxs-lookup"><span data-stu-id="041da-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="041da-137">この HTML ファイルは、フォームからデータの一部が表示され、ユーザーが値を入力するテキスト ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="041da-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="041da-138">ダイアログ ボックスが閉じられるときに、フォームにテキスト ボックスの値が返されます。</span><span class="sxs-lookup"><span data-stu-id="041da-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
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
> <span data-ttu-id="041da-139">[ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx)メソッドを実行するかをプレビューする完全信頼が必要です。</span><span class="sxs-lookup"><span data-stu-id="041da-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="041da-140">詳細については、[プレビューしその必要とする完全信頼フォーム テンプレートのデバッグ](how-to-preview-and-debug-form-templates-that-require-full-trust.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="041da-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

