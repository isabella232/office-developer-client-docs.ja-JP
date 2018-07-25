---
title: フォーム データにアクセスする
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form data [infopath 2007],forms [InfoPath 2007], accessing properties,form templates [InfoPath 2007], accessing properties,opening forms [InfoPath 2007],printing forms [InfoPath 2007],forms [InfoPath 2007], printing,closing forms [InfoPath 2007],InfoPath 2007, accessing form data,forms [InfoPath 2007], accessing data source,forms [InfoPath 2007], closing,forms [InfoPath 2007], opening,printing [InfoPath 2007], forms,forms [InfoPath 2007], creating
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: InfoPath フォームの機能を拡張しようと思うと、多くの場合、フォームの基になる XML ドキュメントに関する情報へのアクセス、XML ドキュメントに記述されているデータへのアクセス、XML ドキュメントに対する何らかの操作の実行などの処理をプログラムで行う必要が出てきます。InfoPath オブジェクト モデルでは、XmlForm クラスと XmlFormCollection クラスを関連させて使用することにより、フォームの基になる XML ドキュメントにアクセスしたり、その XML ドキュメントを操作したりすることができます。
ms.openlocfilehash: c39862fd404575fe95bc1986ce7ab7d9689acfb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799149"
---
# <a name="access-form-data"></a>フォーム データにアクセスする

InfoPath フォームの機能を拡張しようと思うと、多くの場合、フォームの基になる XML ドキュメントに関する情報へのアクセス、XML ドキュメントに記述されているデータへのアクセス、XML ドキュメントに対する何らかの操作の実行などの処理をプログラムで行う必要が出てきます。InfoPath オブジェクト モデルでは、[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスと [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) クラスを関連させて使用することにより、フォームの基になる XML ドキュメントにアクセスしたり、その XML ドキュメントを操作したりすることができます。 
  
[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスには、さまざまなプロパティとメソッドが用意されており、フォームの基になる XML ドキュメントを扱えるだけではなく、InfoPath のユーザー インターフェイスで行える多数の操作を実行することもできるため、このクラスは InfoPath オブジェクト モデルの中では最も便利な型の 1 つと言えます。 
  
## <a name="overview-of-the-xmlformcollection-class"></a>XmlFormCollection クラスの概要

[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) クラスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、コレクションに含まれている [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) オブジェクトを管理できます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) メソッド  <br/> |指定したフォームに基づいて新しいフォームを作成します。  <br/> |
|[New(String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) メソッド (オーバーロード 1)  <br/> |指定した開くモードの動作を使用して、指定したフォームに基づいて新しいフォームを作成します。  <br/> |
|[NewFromFormTemplate(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) メソッド  <br/> |指定したフォーム テンプレートに基づいて新しいフォームを作成します。  <br/> |
|[NewFromFormTemplate(String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) メソッド (オーバーロード 1)  <br/> |指定したフォーム テンプレートと XML データに基づいて新しいフォームを作成します。  <br/> |
|[NewFromFormTemplate(String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) メソッド (オーバーロード 2)  <br/> |指定したフォーム テンプレートと [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) オブジェクトで指定されるデータに基づいて新しいフォームを作成します。  <br/> |
|[NewFromFormTemplate(String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) メソッド (オーバーロード 3)  <br/> |指定した開くモードの動作を使用して、指定したフォーム テンプレートと **XPathNavigator** オブジェクトで指定されるデータに基づいて新しいフォームを作成します。  <br/> |
|[Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) メソッド  <br/> |指定したフォームを開きます。  <br/> |
|[Open(String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) メソッド (オーバーロード 1)  <br/> |指定した開くモードの動作を使用して、指定したフォームを開きます。  <br/> |
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx) プロパティ  <br/> |コレクションに含まれている **XmlForm** オブジェクトの数を取得します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx) プロパティ  <br/> |インデックス値で指定されたコレクション内の **XmlForm** オブジェクトへの参照を取得します。  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>XmlForm クラスの概要

[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、フォームの基になる XML ドキュメントとの相互作用により、その XML ドキュメントに対して操作を実行できます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx) メソッド  <br/> |フォームを閉じます。  <br/> |
|[GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx) メソッド  <br/> |現在のフォームの **Microsoft.Office.Core.WorkflowTasks** コレクションへの参照を取得します。  <br/> |
|[GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx) メソッド  <br/> |現在のフォームの **Microsoft.Office.Core.WorkflowTemplates** コレクションへの参照を取得します。  <br/> |
|[MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) メソッド  <br/> |現在のフォームを、パスまたは URL によって指定されたフォームとマージします。  <br/> |
|[MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) メソッド (オーバーロード 1)  <br/> |現在のフォームを、メソッドに渡された **XPathNavigator** によって返されるノードに指定されたターゲット フォームにマージします。  <br/> |
|[NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx) メソッド  <br/> |ホストしているアプリケーションまたは ASPX ページにカスタム値を提供します。  <br/> |
|[Print()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) メソッド  <br/> |フォームのアクティブ ビューに表示されているフォームの内容を印刷します。  <br/> |
|[Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) メソッド (オーバーロード 1)  <br/> |[ **印刷**] ダイアログ ボックスを表示することによって、フォームのアクティブ ビューに表示されているフォームの内容を印刷します。  <br/> |
|[Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx) メソッド  <br/> |現在関連付けられている Uniform Resource Locator (URL) にフォームを保存します。  <br/> |
|[SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx) メソッド  <br/> |指定した Uniform Resource Locator (URL) にフォームを保存します。  <br/> |
|[SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx) メソッド  <br/> |[ **名前を付けて保存**] ダイアログ ボックスを使用してフォームを保存するときの既定のファイル名を設定します。  <br/> |
|[SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx) メソッド  <br/> |[ **名前を付けて保存**] ダイアログ ボックスを使用してフォームを保存するときの既定のパスを設定します。  <br/> |
|[Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx) メソッド  <br/> |フォーム テンプレートに定義された送信処理を使用してフォームを送信します。  <br/> |
|[CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) プロパティ  <br/> |フォームの現在のビューを表す [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) オブジェクトを取得します。  <br/> |
|[DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) プロパティ  <br/> |フォームに関連付けられた [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) オブジェクトを取得します。  <br/> |
|[DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) プロパティ  <br/> |フォームに関連付けられた [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) オブジェクトを取得します。  <br/> |
|[Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx) プロパティ  <br/> |フォームのデータが最後に保存されてから変更されたかどうかを示す値を取得します。  <br/> |
|[Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx) プロパティ  <br/> |フォームに関連付けられた [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) への参照を取得します。  <br/> |
|[Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx) プロパティ  <br/> |
  [System.Reflection](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) を使用して、フォームのプライマリ フォーム コード ファイルに含まれる関数とグローバル変数にアクセスするための [System.Object](https://msdn.microsoft.com/en-us/library/system.reflection(v=vs.110).aspx) を取得します。  <br/> |
|[FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx) プロパティ  <br/> |サーバー上の複数のセッションにわたって状態情報を維持するためにブラウザー対応のフォームで使用できる、[System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) 型のプロパティ バッグへの参照を取得します。  <br/> |
|[Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx) プロパティ  <br/> |ホストされた InfoPath のインスタンスで実行しているコードでホスト アプリケーションのオブジェクト モデルにアクセスするために使用できる、[System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) を取得します。  <br/> |
|[Hosted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx) プロパティ  <br/> |InfoPath が別のアプリケーションでコントロールとしてホストされているかどうかを取得します。  <br/> |
|[HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx) プロパティ  <br/> |InfoPath をコントロールとしてホストしているアプリケーションの名前を取得します。  <br/> |
|[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) プロパティ  <br/> |フォームのメイン データ ソースを表す [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) オブジェクトを取得します。  <br/> |
|[NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) プロパティ  <br/> |フォームで使用されている名前空間を解決、追加、または削除するために使用できる [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) オブジェクトへの参照を取得します。  <br/> |
|[New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx) プロパティ  <br/> |フォームが新規かどうかを指定する値を取得します。  <br/> |
|[Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx) プロパティ  <br/> |フォームに関連付けられている [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) オブジェクトへの参照を取得します。  <br/> |
|[QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx) プロパティ  <br/> |フォームに関連付けられているデータ接続を表す [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) オブジェクトへの参照を取得します。  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx) プロパティ  <br/> |フォーム テンプレートが読み取り専用またはロックされているかどうかを示す値を取得します。  <br/> |
|[Recovered](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx) プロパティ  <br/> |フォームが最後に保存されたのが自動保存操作によるものかどうかを示す値を取得します。  <br/> |
|[Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx) プロパティ  <br/> |フォームがデジタル署名を使用してデジタル署名されているかどうかを示す値を取得します。  <br/> |
|[SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx) プロパティ  <br/> |フォームに関連付けられている [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) コレクションへの参照を取得します。  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx) プロパティ  <br/> |フォーム テンプレートに関連付けられた [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) への参照を取得します。  <br/> |
|[Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) プロパティ  <br/> |フォームに関連付けられたフォーム テンプレートのマニフェスト (.xsf) を表す [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) オブジェクトへの参照を取得します。  <br/> |
|[Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx) プロパティ  <br/> |フォームの Uniform Resource Identifier (URI) を取得します。  <br/> |
|[UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx) プロパティ  <br/> |フォームのロール名の現在のユーザーを取得または設定します。  <br/> |
|[ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) プロパティ  <br/> |フォーム テンプレートに関連付けられた [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) オブジェクトへの参照を取得します。  <br/> |
|[XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx) プロパティ  <br/> |フォームの基になる XML ドキュメント内の **xml:lang** 属性の値を取得します。  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>XmlFormCollection クラスを使用する

**XmlFormCollection** クラスは、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) クラスの [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティを通じてアクセスされます。 [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーによって提供されるオブジェクト モデルを使用して作成されたマネージ コード フォーム テンプレートでは、フォーム コードで **this** (C# の場合) キーワードまたは **Me** (Visual Basic の場合) キーワードを使用して、 **Application** クラスとそのメンバーにアクセスできます。 
  
次の例では、 **Application** クラスの **XmlForms** プロパティを使用して、InfoPath の実行中のインスタンスの **XDocumentsCollection** オブジェクトを参照する myForms という名前のオブジェクト変数を作成します。この変数を使用して、現在開いているフォームの数を表示します。 
  
```cs
// Create variable for accessing the XmlFormCollection.
XmlFormCollection myForms = this.Application.XmlForms;
// Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count);
```

```vb
// Create variable for accessing the XmlFormCollection.
Dim myForms As XmlFormCollection = Me.Application.XmlForms
' Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count)
```

myForms 変数は、新しいフォームを作成したり (いずれかの **New** メソッドまたは **NewFromTemplate** メソッドを使用)、既存のフォームを開いたり (いずれかの **Open** メソッドを使用) する場合にも使用できます。 
  
## <a name="using-the-xmlform-class"></a>XmlForm クラスを使用する

[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間のメンバーによって提供されるオブジェクト モデルを使用して作成されたマネージ コード フォーム テンプレートでは、フォーム コードで **this** (C# の場合) キーワードまたは **Me** (Visual Basic の場合) キーワードを使用して、( [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスへの参照を確立するオブジェクト変数を必要とすることなく) [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスのメンバーに直接アクセスできます。 
  
### <a name="accessing-a-forms-property-values"></a>フォームのプロパティ値にアクセスする

次の例では、 **this** キーワードまたは **Me** キーワードを使用して、 **XmlForm** クラスの **New**、 **ReadOnly**、 **Signed**、および **Uri** の各プロパティにアクセスし、現在のフォームについて返された値をメッセージ ボックスに表示します。 
  
```cs
MessageBox.Show(
   "Is new: " + this.New + System.Environment.NewLine +
   "Is read-only: " + this.ReadOnly + System.Environment.NewLine +
   "Is signed: " + this.Signed + System.Environment.NewLine +
   "Form URI: " + this.Uri);
```

```vb
MessageBox.Show( _
   "Is new: " &amp; Me.New &amp; System.Environment.NewLine &amp; _
   "Is read-only: " &amp; Me.ReadOnly &amp; System.Environment.NewLine + _
   "Is signed: " &amp; Me.Signed &amp; System.Environment.NewLine &amp; _
   "Form URI: " &amp; this.Uri)
```

### <a name="accessing-a-forms-data-source"></a>フォームのデータ ソースにアクセスする

フォーム データに関する **XmlForm** クラスの主要なプロパティは、 **MainDataSource** プロパティです。このプロパティは、現在のフォームの基になる XML データを表す [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) オブジェクトへの参照を返します (現在のフォームの基になる XML データは、フォームのメイン データ ソースまたは プライマリ データ ソースとも呼ばれます)。 **DataSource** クラスには [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) メソッドがあります。このメソッドは、フォームの基になる XML ドキュメントのルートに配置される [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) オブジェクトを作成します。その後で、 **XPathNavigator** クラスのプロパティとメソッドを使用して、フォームの基になる XML データ内を移動し、データを編集できます。 
  
次の例では、 **XmlForm** クラスの **MainDataSource** プロパティを使用して、フォームのメイン データ ソースのルートに配置される **XPathNavigator** オブジェクトを作成します。次に、 **XPathNavigator** クラスの **OuterXml** プロパティを使用して、フォームの基になる XML ドキュメントのすべての内容を取得し、表示します。 
  
```cs
// Get outer XML of the underlying XML document.
string myDoc = this.MainDataSource.CreateNavigator.OuterXml.ToString();
// Display XML.
MessageBox.Show(myDoc);
```

```vb
' Get outer XML of the underlying XML document.
Dim myDoc As String myDoc = _
   Me.MainDataSource.CreateNavigator.OuterXml.ToString()
' Display XML.
MessageBox.Show(myDoc)
```

> [!NOTE]
> InfoPath では、 **MainDataSource** プロパティを、 **this** キーワードまたは **Me** キーワードを使用して **XmlForm** オブジェクトにアクセスするときの既定のプロパティとして扱うので、 **XPathNavigator** オブジェクトを作成するためのコード行ではこのプロパティを省略できます。 
  
InfoPath フォーム テンプレートのビジネス ロジックでの **XPathNavigator** クラスの詳細については、「[XPathNavigator クラスおよび XPathNodeIterator クラスを操作する方法](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)」を参照してください。
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>フォームのフォーム テンプレート ファイルのデータにアクセスする

フォームに関連付けられているフォーム テンプレートに関する情報は、フォーム定義ファイル (.xsf) およびそこに格納されているソース XML データを含め、 **XmlForm** クラスを使用してアクセスすることもできます。この情報は、 [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) プロパティを使用してアクセスします。このプロパティは、現在のフォームに関連付けられているフォーム テンプレートを表す [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) オブジェクトへの参照を返します。 
  
次の例では、1 つ目のメッセージ ボックスに、 **Template** クラスを使用して取得できるデータの一部を表示します。表示されるデータには、Uniform Resource Identifier (URI) での場所 ( [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) プロパティを使用)、キャッシュ識別子 ( [CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx) プロパティを使用)、そのバージョン番号 ( [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) プロパティを使用) などがあります。2 つ目のメッセージ ボックスでは、 [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) クラスの **Manifest** プロパティを使用して、フォーム定義ファイル (.xsf) のソース XML を表示するために使用される **XPathNavigator** オブジェクトを作成します。 
  
```cs
// Display form template properties.
MessageBox.Show(
   "Cache ID: " + this.Template.CacheId + System.Environment.NewLine +
   "URI: " + this.ReadOnly + System.Environment.NewLine +
   "Version: " + this.Signed, "Form Template Properties");
// Display form definition file XML.
MessageBox.Show(this.Template.Manifest.OuterXml, 
   "Form Definition File XML");
```

```vb
' Display form template properties.
MessageBox.Show( _
   "Cache ID: " &amp; Me.Template.CacheId &amp; System.Environment.NewLine &amp;
   "URI: " &amp; Me.ReadOnly &amp; System.Environment.NewLine &amp;
   "Version: " &amp; Me.Signed, "Form Template Properties")
' Display form definition file XML.
MessageBox.Show(Me.Template.Manifest.OuterXml, _
   "Form Definition File XML")
```


