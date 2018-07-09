---
title: XPathNavigator XPathNodeIterator クラスと
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- xpathnodeiterator class [infopath 2007],XPathNavigator class [InfoPath 2007],form XML data [InfoPath 2007], accessing,XML DOM [InfoPath 2007],converting MSXML5 script [InfoPath 2007],MSXML5 script [InfoPath 2007], converting
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: フォーム テンプレートのデータ ソースの XML データにアクセスして操作するには、Microsoft.Office.InfoPath 名前空間によって提供されるマネージ コード オブジェクト モデルの多くのメンバーは、System.Xml.XPath 名前空間の XPathNavigator クラスのインスタンスを作成するか、そのインスタンスが渡されます。InfoPath オブジェクト モデルのメンバーから返される XPathNavigator オブジェクトにアクセスした後、XPathNavigator クラスのプロパティとメソッドを使用してデータを操作できます。
ms.openlocfilehash: a672ea2733d971c829b77e0c18a74f26c7050b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799156"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="12c13-105">XPathNavigator XPathNodeIterator クラスと</span><span class="sxs-lookup"><span data-stu-id="12c13-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="12c13-p102">フォーム テンプレートのデータ ソースの XML データにアクセスして操作するには、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供されるマネージ コード オブジェクト モデルの多くのメンバーは、 **System.Xml.XPath** 名前空間の **XPathNavigator** クラスのインスタンスを作成するか、そのインスタンスが渡されます。InfoPath オブジェクト モデルのメンバーから返される **XPathNavigator** オブジェクトにアクセスした後、 **XPathNavigator** クラスのプロパティとメソッドを使用してデータを操作できます。</span><span class="sxs-lookup"><span data-stu-id="12c13-p102">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace. After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="12c13-p103">**XPathNavigator** クラスを使用する **Microsoft.Office.InfoPath** 名前空間のメンバーの中で最もよく使用されるメンバーは、 [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) クラスの [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) メソッドです。このメソッドを使用すると、 **DataSource** オブジェクトで表される保存データを操作できます。 **CreateNavigator** メソッドでは、 **DataSource** オブジェクトで表されるデータ ソースのルートに置かれる **XPathNavigator** オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="12c13-p103">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object. The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="12c13-110">スクリプトから MSXML5 を使用して Microsoft InfoPath 2003 のデータを操作する方法に慣れている場合は、 **CreateNavigator** メソッドを **DataObject** の **DOM** プロパティに代わるものと考えることができます。</span><span class="sxs-lookup"><span data-stu-id="12c13-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="12c13-111">XPathNavigator クラスを使用して、フォームのメイン データ ソースにアクセスする</span><span class="sxs-lookup"><span data-stu-id="12c13-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="12c13-p104">フォームのメイン データ ソースにアクセスするには、 [this](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) (C#) または **Me** (Visual Basic) キーワードから **CreateNavigator** メソッドを直接呼び出します。次の例では、 **CreateNavigator** メソッドを使用して、メイン データ ソースのルートに置かれる **XPathNavigator** オブジェクトを作成し、 **XPathNavigator** クラスの **OuterXml** プロパティを使用して、返される XML をメッセージ ボックスに表示します。</span><span class="sxs-lookup"><span data-stu-id="12c13-p104">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword. The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
```cs
XPathNavigator myNavigator = 
   this.CreateNavigator();
MessageBox.Show("Main data source XML: " +
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.CreateNavigator()
MessageBox.Show("Main data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

> [!NOTE]
> <span data-ttu-id="12c13-114">[this](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) または **Me** キーワードから **CreateNavigator** メソッドを直接呼び出すことは、 [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) プロパティを使用するか (  [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx))、`this.MainDataSource.CreateNavigator()` クラスの [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) プロパティに空文字列を渡して (  [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx))、`this.DataSources[""].CreateNavigator()` メソッドを呼び出すのと同じです。</span><span class="sxs-lookup"><span data-stu-id="12c13-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="12c13-115">メイン データ ソース内のフィールドを表す XML ノードを選択および設定する</span><span class="sxs-lookup"><span data-stu-id="12c13-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="12c13-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12c13-116"></span></span>

<span data-ttu-id="12c13-p105">データ ソース内のフィールドを表す単一の XML ノードを選択するには、 **XPathNavigator** クラスの **SelectSingleNode(String,IXmlNamespaceResolver)** メソッドを使用します。一連の繰り返しフィールドまたはグループを操作する場合は、 **XPathNavigator** クラスの **Select(String,IXmlNamespaceResolver)** メソッドを使用します。このメソッドは、ノードのコレクションを表す **XPathNodeIterator** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="12c13-p105">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class. If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class. This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="12c13-120">単一ノードの値を選択および設定する</span><span class="sxs-lookup"><span data-stu-id="12c13-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="12c13-p106">使用する必要があるオーバーロードの **SelectSingleNode** メソッドには、XPath 式を文字列として取る  _xpath_ パラメーターと、名前空間プレフィックスを解決するための _XmlNamespaceManager_ オブジェクトを取る  **resolver** パラメーターがあります。フォームのメイン データ ソース内の単一ノードを選択するには、  _xpath_ パラメーター用に選択するフィールドまたはグループを指定する XPath 式と、 **XmlForm** オブジェクトの [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) プロパティが返す **XmlNamespaceManager** オブジェクトを渡します。返される **XmlNamespaceManager** オブジェクトは、読み込み時に、フォーム テンプレートのフォーム定義ファイル (.xsf) によって定義されるすべての名前空間で初期化されます。</span><span class="sxs-lookup"><span data-stu-id="12c13-p106">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes. To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object. The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="12c13-p107">フォームのデータ ソース内のノードを選択する XPath 式を最も簡単に作成するには、[ **フィールド**] 作業ウィンドウ内でフィールドまたはグループを右クリックし、[ **XPath のコピー**] をクリックします。複雑な、または深い入れ子になった XML スキーマ内のノードにアクセスするための手動編集 XPath 式を作成してテストするには、フォームに **式ボックス** コントロールを追加し、フォームをプレビューして結果を表示します。</span><span class="sxs-lookup"><span data-stu-id="12c13-p107">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**. To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="12c13-p108">次の例では、 **SelectSingleNode** メソッドを使用して、  `EmailAlias` フィールド用の単一ノードを選択します。さらに、 **XPathNavigator** クラスの **SetValue** メソッドと [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) クラスの [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) プロパティを使用して、そのフィールドの値を現在のユーザーのエイリアスに設定します。</span><span class="sxs-lookup"><span data-stu-id="12c13-p108">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field. Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
```cs
XPathNavigator emailAlias = 
   this.CreateNavigator().SelectSingleNode(
      "/my:myFields/my:EmailAlias", NamespaceManager);
emailAlias.SetValue(this.Application.User.UserName.ToString());
```

```vb
Dim emailAlias As XPathNavigator = _
   Me.CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:EmailAlias", NamespaceManager)
emailAlias.SetValue(Me.Application.User.UserName.ToString())
```

<span data-ttu-id="12c13-128">XPath 式を作成する方法の詳細については、MSDN では、 [XML パス言語 (XPath) Version 1.0 の W3C 勧告](http://www.w3.org/TR/xpath)で XPath のリファレンスを参照してください。</span><span class="sxs-lookup"><span data-stu-id="12c13-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](http://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="12c13-129">xsi:nil 属性を持つノードの値を設定する</span><span class="sxs-lookup"><span data-stu-id="12c13-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="12c13-p109">ある特定のデータ型では、空白フィールドの値をプログラムで設定しようとすると、"スキーマの検証でデータ型以外のエラーが見つかりました。" というエラーが発生します。通常、このエラーの原因は、要素の [xsi:nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) 属性が **true** に設定されていることにあります。フォーム内の空白フィールドを表す基本 XML 要素を調べると、そのように設定されていることが見つかります。たとえば、次の空白の Date フィールドを表す XML フラグメントの **xsi:nil** 属性は **true** に設定されています。</span><span class="sxs-lookup"><span data-stu-id="12c13-p109">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors." Typically the cause of this error is that the element has the [xsi:nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**. If you examine the underlying XML element for the blank field in the form, you can see this setting. For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="12c13-p110">**xsi:nil** 属性が **true** に設定されている場合、要素自体は存在するが、値を持たない、つまり、この要素は null であることを示します。このようなノードに対してプログラムで値を設定しようとすると、現在この要素は null であるとしてフラグが設定されているため、"スキーマの検証でデータ型以外のエラーが見つかりました。" というメッセージが表示されます。InfoPath は、次のデータ型の null フィールドについては **xsi:nil** 属性を **true** に設定します。</span><span class="sxs-lookup"><span data-stu-id="12c13-p110">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null . If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null . InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="12c13-137">**Whole Number (integer)**</span><span class="sxs-lookup"><span data-stu-id="12c13-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="12c13-138">**Decimal (double)**</span><span class="sxs-lookup"><span data-stu-id="12c13-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="12c13-139">**Date (date)**</span><span class="sxs-lookup"><span data-stu-id="12c13-139">**Date (date)**</span></span>
    
- <span data-ttu-id="12c13-140">**Time (time)**</span><span class="sxs-lookup"><span data-stu-id="12c13-140">**Time (time)**</span></span>
    
- <span data-ttu-id="12c13-141">**Date and Time (dateTime)**</span><span class="sxs-lookup"><span data-stu-id="12c13-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="12c13-p111">このエラーを回避するには、コードで **xsi:nil** 属性の有無を調べる必要があります。この属性が存在する場合は、ノードの値を設定する前に、属性自体を削除します。次のサブルーチンでは、設定するノードに置かれる **XpathNavigator** オブジェクトを取得し、 **nil** 属性の有無を確認し、属性が存在する場合は削除します。</span><span class="sxs-lookup"><span data-stu-id="12c13-p111">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node. The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "http://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "http://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

<span data-ttu-id="12c13-144">たとえば、次の例では Date フィールドを設定していますが、この例に示すように、 **xsi:nil** 属性が存在するかどうかがわからないデータ型のフィールドを設定する前に、このサブルーチンを呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="12c13-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
```cs
// Access the main data source.
XPathNavigator myForm = this.CreateNavigator();
// Select the field.
XPathNavigator myDate = myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager);
// Check for and remove the "nil" attribute.
DeleteNil(myDate);
// Build the current date in the proper format. (yyyy-mm-dd)
string curDate = DateTime.Today.Year + "-" + DateTime.Today.Month + 
   "-" + DateTime.Today.Day;
// Set the value of the myDate field.
myDate.SetValue(strCurDate);
```

```vb
' Access the main data source.
Dim myForm As XPathNavigator = Me.CreateNavigator()
' Select the field.
Dim myDate As XPathNavigator = _
   myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager)
' Check for and remove the "nil" attribute.
DeleteNil(myDate)
' Build the current date in the proper format. (yyyy-mm-dd)
Dim curDate As String = DateTime.Today.Year + "-" + _
   DateTime.Today.Month + "-" + DateTime.Today.Day
' Set the value of the myDate field.
myDate.SetValue(strCurDate)
```

> [!NOTE]
> <span data-ttu-id="12c13-p112">InfoPath の **XPathNavigator** オブジェクトの実装は、 **SetTypedValue** メソッド (特定の型の値を使用してノードを設定するために使用) を公開していますが、InfoPath は、このメソッドを実装していません。代わりに、 **SetValue** メソッドを使用して、ノードのデータ型に適切な形式の文字列値を渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="12c13-p112">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method. You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="12c13-147">繰り返しノードを選択および設定する</span><span class="sxs-lookup"><span data-stu-id="12c13-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="12c13-148">繰り返しフィールドまたは不特定の数のグループのセットを指定するには、 **XPathNavigator**クラスの**選択**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="12c13-148">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="12c13-149">このメソッドは、指定されたノードのコレクションを反復処理に使用できる XPathNodeIterator オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="12c13-149">This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="12c13-150">次の例では、**箇条書きリスト**または同様の繰り返しコントロールという名前の繰り返し要素にバインドされているフォーム テンプレートが含まれていると仮定しています`field1`。</span><span class="sxs-lookup"><span data-stu-id="12c13-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="12c13-151">フィールドの XPath は、メソッドに渡される、**選択**、および返された**XPathNodeIterator**に割り当てられた、`nodes`変数です。</span><span class="sxs-lookup"><span data-stu-id="12c13-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="12c13-152">ノード、および現在のノードに配置されている**XPathNavigator**オブジェクトを返すには、現在のプロパティのコレクションを反復処理するには、MoveNext メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="12c13-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="12c13-153">最後に、取得し、各繰り返しフィールドの値を表示するのには**Value**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="12c13-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
```cs
string message = String.Empty;
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
while (nodes.MoveNext())
{
    message += nodes.Current.Value + System.Environment.NewLine;
}
MessageBox.Show(message);
```

```vb
Dim message As String = String.Empty
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Do While nodes.MoveNext
    message += nodes.Current.Value &amp; System.Environment.NewLine
Loop
MessageBox.Show(message)
```

<span data-ttu-id="12c13-p115">前の例では、指定された繰り返しフィールド内で文字列値を処理しています。ただし、フィールド内に数値が含まれている場合は、同様のコードを使用してフィールド内の値の反復処理を行い、値の合計や平均を算出するなどの計算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="12c13-p115">The previous example works with string values in the specified repeating field. However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="12c13-156">同様に、 **Value** プロパティを使用して、繰り返しフィールドの各インスタンスの値を取得するのではなく、 **SetValue** メソッドを使用して、フィールドの反復処理を行って値を設定できます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="12c13-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
```cs
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
int myInt = 1;
while (nodes.MoveNext())
{
   nodes.Current.SetValue(myInt.ToString());
   myInt = myInt + 1;
}
```

```vb
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Dim myInt As Integer = 1
Do While nodes.MoveNext
   nodes.Current.SetValue(myInt.ToString())
   myInt = myInt + 1
Loop
```

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="12c13-157">XPathNavigator クラスを使用して、外部データ ソースにアクセスする</span><span class="sxs-lookup"><span data-stu-id="12c13-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="12c13-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12c13-158"></span></span>

<span data-ttu-id="12c13-p116">フォームに関連付けられている外部データ ソースにアクセスするには、データ ソースの名前を [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) クラスの [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティに渡します。新しい外部データ ソースへの接続を作成したり、既存の外部データ ソース接続の名前の一覧を表示したりするには、リボンの [ **データ**] タブの [ **データ接続**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="12c13-p116">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class. To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="12c13-p117">次のコード サンプルでは、 **CreateNavigator** メソッドを使用して外部データ ソース "CityList" のルートに置かれる **XPathNavigator** オブジェクトを作成し、 **XPathNavigator** クラスの **OuterXml** プロパティを使用して、返される XML をメッセージ ボックスに表示する方法を示します。このコード サンプルでは、XML ドキュメントや SharePoint リストなどの外部データ ソースに保存されている都市名のリストへのデータ接続を作成し、そのデータ接続に "CityList" という名前を付けていることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="12c13-p117">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box. This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
```cs
XPathNavigator myNavigator = 
   this.DataSources["CityList"].CreateNavigator();
MessageBox.Show("External data source XML: " + 
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.DataSources("CityList").CreateNavigator()
MessageBox.Show("External data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

<span data-ttu-id="12c13-163">外部データ ソースのルートに置かれる **XPathNavigator** オブジェクトにアクセスした後は、 **SelectSingleNode** および **SetValue** メソッドなど、 **XPathNavigator** クラスのメンバーを使用して、そのデータ ソース内のデータを操作できます。</span><span class="sxs-lookup"><span data-stu-id="12c13-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="12c13-164">XPathNavigator クラスと XPathNodeIterator クラスを使用する InfoPath オブジェクト モデルのメンバー</span><span class="sxs-lookup"><span data-stu-id="12c13-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="12c13-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12c13-165"></span></span>

<span data-ttu-id="12c13-166">次の表に、 **XPathNavigator** クラスを使用して XML データのアクセス、操作、および送信を行う **Microsoft.Office.InfoPath** 名前空間のすべてのメンバーの概要を示します。</span><span class="sxs-lookup"><span data-stu-id="12c13-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="12c13-167">**親クラス**</span><span class="sxs-lookup"><span data-stu-id="12c13-167">**Parent Class**</span></span>|<span data-ttu-id="12c13-168">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="12c13-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12c13-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="12c13-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="12c13-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="12c13-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="12c13-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-173">ClickedEventArgs</span><span class="sxs-lookup"><span data-stu-id="12c13-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="12c13-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-175">ContextChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="12c13-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="12c13-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-177">データ ソース</span><span class="sxs-lookup"><span data-stu-id="12c13-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="12c13-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="12c13-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="12c13-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="12c13-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="12c13-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="12c13-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="12c13-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="12c13-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="12c13-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-187">FormError</span><span class="sxs-lookup"><span data-stu-id="12c13-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="12c13-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="12c13-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="12c13-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="12c13-191">FormTemplate</span><span class="sxs-lookup"><span data-stu-id="12c13-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="12c13-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-193">MergeEventArgs</span><span class="sxs-lookup"><span data-stu-id="12c13-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="12c13-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="12c13-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="12c13-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-197">Signature</span><span class="sxs-lookup"><span data-stu-id="12c13-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="12c13-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-199">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="12c13-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="12c13-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-201">View</span><span class="sxs-lookup"><span data-stu-id="12c13-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="12c13-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="12c13-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="12c13-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="12c13-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="12c13-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="12c13-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="12c13-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="12c13-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="12c13-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="12c13-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="12c13-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="12c13-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="12c13-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="12c13-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) プロパティ。 **DataSource** オブジェクトを返します。このオブジェクトは、フォームの基になる XML ドキュメント (メイン データ ソース) のルートに置かれる **XPathNavigator** オブジェクトを作成する **CreateNavigator** メソッドを備えます。  </span><span class="sxs-lookup"><span data-stu-id="12c13-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="12c13-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="12c13-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="12c13-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="12c13-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="12c13-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="12c13-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="12c13-218">**XPathNavigator** オブジェクトを返すか受け取る InfoPath オブジェクト モデル メンバーに加え、次のメソッドでは、ビューで指定または選択された項目の XML ノードに対して反復処理を行うため、 **System.Xml.XPath** 名前空間の **XPathNodeIterator** クラスのインスタンスを返します。</span><span class="sxs-lookup"><span data-stu-id="12c13-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="12c13-219">**親クラス**</span><span class="sxs-lookup"><span data-stu-id="12c13-219">**Parent Class**</span></span>|<span data-ttu-id="12c13-220">**メンバー**</span><span class="sxs-lookup"><span data-stu-id="12c13-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="12c13-221">View</span><span class="sxs-lookup"><span data-stu-id="12c13-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="12c13-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="12c13-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="12c13-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="12c13-224">XPathNavigator クラスと XPathNodeIterator クラスを使用して、ビューで選択されたデータを操作する</span><span class="sxs-lookup"><span data-stu-id="12c13-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="12c13-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="12c13-225"></span></span>

<span data-ttu-id="12c13-226">次の例では、 **XPathNavigator** クラスと **XPathNodeIterator** クラスのメンバーを使用して、次のシーケンスのフォーム データを操作します。</span><span class="sxs-lookup"><span data-stu-id="12c13-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="12c13-227">**DataSource** クラスの **CreateNavigator** メソッドを使用して、 repeatingTableRow1 という名前の **XPathNavigator** オブジェクト変数を作成します。このオブジェクト変数は、既定では、フォームの基になる XML ドキュメント (メイン データ ソース) のルートに置かれます。</span><span class="sxs-lookup"><span data-stu-id="12c13-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="12c13-228">**XPathNavigator** クラスの **SelectSingleNode** メソッドを使用して、 **XPathNavigator** オブジェクトの位置を、データ ソースの group2 にバインドされた [ **繰り返しテーブル**] コントロールの先頭行に移動します。</span><span class="sxs-lookup"><span data-stu-id="12c13-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="12c13-229">repeatingTableRow1 オブジェクト変数を **View** クラスの **SelectNodes** メソッドに渡し、その行のノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="12c13-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="12c13-230">selectedNodes という名前の **XPathNodeIterator** オブジェクト変数を宣言し、 **View** クラスの **GetSelectedNodes** メソッドを使用して、 **XPathNodeIterator** オブジェクトに選択されたノードを入力します。</span><span class="sxs-lookup"><span data-stu-id="12c13-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="12c13-231">**XPathNodeIterator** クラスの **Count** プロパティを使用して、 selectedNodes オブジェクト変数に含まれているノード数を表示します。</span><span class="sxs-lookup"><span data-stu-id="12c13-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="12c13-232">For/Each ループを使用して、selectedNodes オブジェクト変数のノードに対して反復処理を行い、 **XPathNavigator** クラスの **Name**、 **InnerXml**、および **Value** プロパティを使用して各ノードに関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="12c13-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   this.CreateNavigator().SelectSingleNode(
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
// Get selected nodes.
XPathNodeIterator selectedNodes = 
   CurrentView.GetSelectedNodes();
// Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString());
// Loop through collection and display information.
foreach (XPathNavigator selectedNode in selectedNodes)
{
   MessageBox.Show(selectedNode.Name);
   MessageBox.Show(selectedNode.InnerXml);
   MessageBox.Show(selectedNode.Value);
}
```

```vb
' Create XPathNavigator and specify XPath for nodes.
Dim repeatingTableRow1 As XPathNavigator  = _
   Me.CreateNavigator().SelectSingleNode( _
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager)
' Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1)
' Get selected nodes.
Dim selectedNodes As XPathNodeIterator = _
   CurrentView.GetSelectedNodes()
' Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString())
' Loop through collection and display information.
Dim selectedNode As XPathNavigator
For Each selectedNode In selectedNodes
   MessageBox.Show(selectedNode.Name)
   MessageBox.Show(selectedNode.InnerXml)
   MessageBox.Show(selectedNode.Value)
Next
```

<span data-ttu-id="12c13-233">InfoPath フォーム テンプレートから XML データを操作する方法の詳細についてをクリックしてください XML データを使用して InfoPath 2007 フォーム テンプレートで XPathNavigator クラスです。</span><span class="sxs-lookup"><span data-stu-id="12c13-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

