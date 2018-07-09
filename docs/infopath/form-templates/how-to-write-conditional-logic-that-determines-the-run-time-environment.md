---
title: 実行時環境を決定する条件付きロジックを記述します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- running in infopath [infopath 2007],run-time environment [InfoPath 2007],running in browser [InfoPath 2007],InfoPath 2007, determining run-time environment
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: Application クラスの Environment プロパティは、Environment オブジェクトへの参照を取得します。これを使用すると、どの実行時の環境 (InfoPath、Web ブラウザー、またはモバイル ブラウザー) を使ってフォームが開かれたかを判断することができます。
ms.openlocfilehash: b854d6a3b65fcc37375480bef9f1909d84407b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799119"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="aa673-104">実行時環境を決定する条件付きロジックを記述します。</span><span class="sxs-lookup"><span data-stu-id="aa673-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="aa673-105">[Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) クラスの [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティは、 [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) オブジェクトへの参照を取得します。これを使用すると、どの実行時の環境 (InfoPath、Web ブラウザー、またはモバイル ブラウザー) を使ってフォームが開かれたかを判断することができます。</span><span class="sxs-lookup"><span data-stu-id="aa673-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aa673-106">例</span><span class="sxs-lookup"><span data-stu-id="aa673-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="aa673-107">フォームが実行されている実行時の環境を判断する</span><span class="sxs-lookup"><span data-stu-id="aa673-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="aa673-p101">[Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) クラスは、フォーム テンプレートを開くために使用された編集環境を判断することができる [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) プロパティおよび [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) プロパティを提供します。これらの両方のプロパティが **false** を返す場合、フォーム テンプレートは Microsoft InfoPath エディターで開かれています。いずれかのプロパティが **true** を返す場合、フォーム テンプレートは対応するプロパティのプログラムで InfoPath Forms Services を実行している Microsoft SharePoint Server 2010 上で、適切に構成されたドキュメント ライブラリから開かれています。 [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property プロパティの場合は Web ブラウザー、 [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) プロパティの場合はモバイル ブラウザーです。</span><span class="sxs-lookup"><span data-stu-id="aa673-p101">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template. If both properties return **false**, the form template was opened in the Microsoft InfoPath editor. If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="aa673-p102">次の例では、フォームがブラウザーまたはモバイル ブラウザーで開かれた場合は、field1 ([ **テキスト ボックス**] コントロールにバインドされている) の値が、フォームが開かれた実行時の環境を示す文字列に設定されます。フォームが InfoPath で開かれた場合は、 **System.Windows.Forms.MessageBox.Show** メソッド (このメソッドは、フォームがブラウザーで実行されているときは使用できません) を使用してメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="aa673-p102">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in. If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="aa673-p103">以下のコード例のフォーム テンプレートを作成するときは、Backstage ビューの [ **新規作成**] タブで [ **空白**] テンプレートを選択します (または、[ **フォームのオプション**] ダイアログ ボックスの [ **互換性**] カテゴリにある、[ **フォームの種類**] ドロップダウン リストの [ **Web ブラウザー フォーム**] を選択します)。 **MessageBox** クラスをサポートするには、Visual Studio 2012 の [ **参照の追加**] ダイアログ ボックスの [ **.NET**] タブで、 **System.Windows.Forms** への参照を追加します。次に、フォーム コード モジュールの宣言セクションで、 **System.Windows.Forms** の **using** または **Imports** ディレクティブを追加します。</span><span class="sxs-lookup"><span data-stu-id="aa673-p103">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view. (Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the . **NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


