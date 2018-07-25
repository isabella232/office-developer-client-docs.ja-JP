---
title: XPathNavigator クラスおよび XPathNodeIterator クラスを操作する
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
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799156"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>XPathNavigator クラスおよび XPathNodeIterator クラスを操作する

フォーム テンプレートのデータ ソースの XML データにアクセスして操作するには、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供されるマネージ コード オブジェクト モデルの多くのメンバーは、 **System.Xml.XPath** 名前空間の **XPathNavigator** クラスのインスタンスを作成するか、そのインスタンスが渡されます。InfoPath オブジェクト モデルのメンバーから返される **XPathNavigator** オブジェクトにアクセスした後、 **XPathNavigator** クラスのプロパティとメソッドを使用してデータを操作できます。 
  
**XPathNavigator** クラスを使用する **Microsoft.Office.InfoPath** 名前空間のメンバーの中で最もよく使用されるメンバーは、 [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) クラスの [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) メソッドです。このメソッドを使用すると、 **DataSource** オブジェクトで表される保存データを操作できます。 **CreateNavigator** メソッドでは、 **DataSource** オブジェクトで表されるデータ ソースのルートに置かれる **XPathNavigator** オブジェクトを作成します。 
  
> [!TIP]
> スクリプトから MSXML5 を使用して Microsoft InfoPath 2003 のデータを操作する方法に慣れている場合は、 **CreateNavigator** メソッドを **DataObject** の **DOM** プロパティに代わるものと考えることができます。 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>XPathNavigator クラスを使用して、フォームのメイン データ ソースにアクセスする

フォームのメイン データ ソースにアクセスするには、 [this](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) (C#) または **Me** (Visual Basic) キーワードから **CreateNavigator** メソッドを直接呼び出します。次の例では、 **CreateNavigator** メソッドを使用して、メイン データ ソースのルートに置かれる **XPathNavigator** オブジェクトを作成し、 **XPathNavigator** クラスの **OuterXml** プロパティを使用して、返される XML をメッセージ ボックスに表示します。 
  
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
> [this](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) または **Me** キーワードから **CreateNavigator** メソッドを直接呼び出すことは、 [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) プロパティを使用するか (  [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx))、`this.MainDataSource.CreateNavigator()` クラスの [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) プロパティに空文字列を渡して (  [](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx))、`this.DataSources[""].CreateNavigator()` メソッドを呼び出すのと同じです。 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>メイン データ ソース内のフィールドを表す XML ノードを選択および設定する
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

データ ソース内のフィールドを表す単一の XML ノードを選択するには、 **XPathNavigator** クラスの **SelectSingleNode(String,IXmlNamespaceResolver)** メソッドを使用します。一連の繰り返しフィールドまたはグループを操作する場合は、 **XPathNavigator** クラスの **Select(String,IXmlNamespaceResolver)** メソッドを使用します。このメソッドは、ノードのコレクションを表す **XPathNodeIterator** オブジェクトを返します。 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>単一ノードの値を選択および設定する

使用する必要があるオーバーロードの **SelectSingleNode** メソッドには、XPath 式を文字列として取る  _xpath_ パラメーターと、名前空間プレフィックスを解決するための _XmlNamespaceManager_ オブジェクトを取る  **resolver** パラメーターがあります。フォームのメイン データ ソース内の単一ノードを選択するには、  _xpath_ パラメーター用に選択するフィールドまたはグループを指定する XPath 式と、 **XmlForm** オブジェクトの [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) プロパティが返す **XmlNamespaceManager** オブジェクトを渡します。返される **XmlNamespaceManager** オブジェクトは、読み込み時に、フォーム テンプレートのフォーム定義ファイル (.xsf) によって定義されるすべての名前空間で初期化されます。 
  
> [!TIP]
> フォームのデータ ソース内のノードを選択する XPath 式を最も簡単に作成するには、[ **フィールド**] 作業ウィンドウ内でフィールドまたはグループを右クリックし、[ **XPath のコピー**] をクリックします。複雑な、または深い入れ子になった XML スキーマ内のノードにアクセスするための手動編集 XPath 式を作成してテストするには、フォームに **式ボックス** コントロールを追加し、フォームをプレビューして結果を表示します。 
  
次の例では、 **SelectSingleNode** メソッドを使用して、  `EmailAlias` フィールド用の単一ノードを選択します。さらに、 **XPathNavigator** クラスの **SetValue** メソッドと [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) クラスの [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) プロパティを使用して、そのフィールドの値を現在のユーザーのエイリアスに設定します。 
  
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

XPath 式の作成方法については、MSDN の「XPath リファレンス」と、「[XML Path Language (XPath) Version 1.0 W3C Recommendation](http://www.w3.org/TR/xpath)」を参照してください。
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>xsi:nil 属性を持つノードの値を設定する

ある特定のデータ型では、空白フィールドの値をプログラムで設定しようとすると、"スキーマの検証でデータ型以外のエラーが見つかりました。" というエラーが発生します。通常、このエラーの原因は、要素の [xsi:nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) 属性が **true** に設定されていることにあります。フォーム内の空白フィールドを表す基本 XML 要素を調べると、そのように設定されていることが見つかります。たとえば、次の空白の Date フィールドを表す XML フラグメントの **xsi:nil** 属性は **true** に設定されています。
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

**xsi:nil** 属性が **true** に設定されている場合、要素自体は存在するが、値を持たない、つまり、この要素は null であることを示します。このようなノードに対してプログラムで値を設定しようとすると、現在この要素は null であるとしてフラグが設定されているため、"スキーマの検証でデータ型以外のエラーが見つかりました。" というメッセージが表示されます。InfoPath は、次のデータ型の null フィールドについては **xsi:nil** 属性を **true** に設定します。 
  
- **Whole Number (integer)**
    
- **Decimal (double)**
    
- **Date (date)**
    
- **Time (time)**
    
- **Date and Time (dateTime)**
    
このエラーを回避するには、コードで **xsi:nil** 属性の有無を調べる必要があります。この属性が存在する場合は、ノードの値を設定する前に、属性自体を削除します。次のサブルーチンでは、設定するノードに置かれる **XpathNavigator** オブジェクトを取得し、 **nil** 属性の有無を確認し、属性が存在する場合は削除します。 
  
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

たとえば、次の例では Date フィールドを設定していますが、この例に示すように、 **xsi:nil** 属性が存在するかどうかがわからないデータ型のフィールドを設定する前に、このサブルーチンを呼び出すことができます。 
  
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
> InfoPath の **XPathNavigator** オブジェクトの実装は、 **SetTypedValue** メソッド (特定の型の値を使用してノードを設定するために使用) を公開していますが、InfoPath は、このメソッドを実装していません。代わりに、 **SetValue** メソッドを使用して、ノードのデータ型に適切な形式の文字列値を渡す必要があります。 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>繰り返しノードを選択および設定する

繰り返される回数が不確かなフィールドまたはグループの一式を指定するには、**XPathNavigator** クラスの **Select** メソッドを使用します。 このメソッドから返される XPathNodeIterator オブジェクトを使用して、指定したノードのコレクションを反復処理できます。 
  
次の例では、フォーム テンプレートに含まれる**箇条書き**または同様の反復コントロールが、`field1` という名前の繰り返し要素にバインドされていることを前提とします。 フィールドの XPath を **Select** メソッドに渡し、このメソッドから返された **XPathNodeIterator** を `nodes` 変数に割り当てます。 MoveNext メソッドを使用してノードのコレクションを反復処理し、Current プロパティを使用して、現在のノードに位置する **XPathNavigator** オブジェクトを返します。 最後に、**Value** プロパティを使用して、繰り返される各フィールドの値を取得し、表示します。 
  
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

前の例では、指定された繰り返しフィールド内で文字列値を処理しています。ただし、フィールド内に数値が含まれている場合は、同様のコードを使用してフィールド内の値の反復処理を行い、値の合計や平均を算出するなどの計算を実行できます。
  
同様に、 **Value** プロパティを使用して、繰り返しフィールドの各インスタンスの値を取得するのではなく、 **SetValue** メソッドを使用して、フィールドの反復処理を行って値を設定できます。次に例を示します。 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a>XPathNavigator クラスを使用して、外部データ ソースにアクセスする
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

フォームに関連付けられている外部データ ソースにアクセスするには、データ ソースの名前を [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) クラスの [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティに渡します。新しい外部データ ソースへの接続を作成したり、既存の外部データ ソース接続の名前の一覧を表示したりするには、リボンの [ **データ**] タブの [ **データ接続**] をクリックします。 
  
次のコード サンプルでは、 **CreateNavigator** メソッドを使用して外部データ ソース "CityList" のルートに置かれる **XPathNavigator** オブジェクトを作成し、 **XPathNavigator** クラスの **OuterXml** プロパティを使用して、返される XML をメッセージ ボックスに表示する方法を示します。このコード サンプルでは、XML ドキュメントや SharePoint リストなどの外部データ ソースに保存されている都市名のリストへのデータ接続を作成し、そのデータ接続に "CityList" という名前を付けていることを想定しています。 
  
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

外部データ ソースのルートに置かれる **XPathNavigator** オブジェクトにアクセスした後は、 **SelectSingleNode** および **SetValue** メソッドなど、 **XPathNavigator** クラスのメンバーを使用して、そのデータ ソース内のデータを操作できます。 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a>XPathNavigator クラスと XPathNodeIterator クラスを使用する InfoPath オブジェクト モデルのメンバー
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

次の表に、 **XPathNavigator** クラスを使用して XML データのアクセス、操作、および送信を行う **Microsoft.Office.InfoPath** 名前空間のすべてのメンバーの概要を示します。 
  
|**親クラス**|**メンバー**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) メソッド  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) メソッド  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) プロパティ  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) プロパティ  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) メソッド  <br/> |
||[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) メソッド  <br/> |
||[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) メソッド  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) メソッド  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) メソッド  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) メソッド  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) プロパティ  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) メソッド  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) プロパティ  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) プロパティ  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) メソッド  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) プロパティ  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) プロパティ  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド  <br/> |
||[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド  <br/> |
||[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッド  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) メソッド  <br/> |
||[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) メソッド  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) プロパティ  <br/> |
||[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) プロパティ  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) プロパティ。 **DataSource** オブジェクトを返します。このオブジェクトは、フォームの基になる XML ドキュメント (メイン データ ソース) のルートに置かれる **XPathNavigator** オブジェクトを作成する **CreateNavigator** メソッドを備えます。    <br/> |
||[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) メソッド  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) メソッド  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) メソッド  <br/> |
   
**XPathNavigator** オブジェクトを返すか受け取る InfoPath オブジェクト モデル メンバーに加え、次のメソッドでは、ビューで指定または選択された項目の XML ノードに対して反復処理を行うため、 **System.Xml.XPath** 名前空間の **XPathNodeIterator** クラスのインスタンスを返します。 
  
|**親クラス**|**メンバー**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド  <br/> |
||[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) メソッド  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>XPathNavigator クラスと XPathNodeIterator クラスを使用して、ビューで選択されたデータを操作する
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

次の例では、 **XPathNavigator** クラスと **XPathNodeIterator** クラスのメンバーを使用して、次のシーケンスのフォーム データを操作します。 
  
1. **DataSource** クラスの **CreateNavigator** メソッドを使用して、 repeatingTableRow1 という名前の **XPathNavigator** オブジェクト変数を作成します。このオブジェクト変数は、既定では、フォームの基になる XML ドキュメント (メイン データ ソース) のルートに置かれます。
    
2. **XPathNavigator** クラスの **SelectSingleNode** メソッドを使用して、 **XPathNavigator** オブジェクトの位置を、データ ソースの group2 にバインドされた [ **繰り返しテーブル**] コントロールの先頭行に移動します。 
    
3. repeatingTableRow1 オブジェクト変数を **View** クラスの **SelectNodes** メソッドに渡し、その行のノードを選択します。 
    
4. selectedNodes という名前の **XPathNodeIterator** オブジェクト変数を宣言し、 **View** クラスの **GetSelectedNodes** メソッドを使用して、 **XPathNodeIterator** オブジェクトに選択されたノードを入力します。 
    
5. **XPathNodeIterator** クラスの **Count** プロパティを使用して、 selectedNodes オブジェクト変数に含まれているノード数を表示します。 
    
6. For/Each ループを使用して、selectedNodes オブジェクト変数のノードに対して反復処理を行い、 **XPathNavigator** クラスの **Name**、 **InnerXml**、および **Value** プロパティを使用して各ノードに関する情報を表示します。 
    
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

InfoPath フォーム テンプレートからの XML データの操作方法の詳細については、「InfoPath 2007 フォーム テンプレートで XPathNavigator クラスを使用して XML データを操作する」を参照してください。
  

