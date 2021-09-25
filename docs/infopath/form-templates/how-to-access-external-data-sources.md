---
title: 外部データ ソースにアクセスする
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- data connection classes [infopath 2007],secondary data sources [InfoPath 2007],data [InfoPath 2007], secondary,DataSource class [InfoPath 2007],accessing external data sources [InfoPath 2007],DataSourceCollection class [InfoPath 2007],DataConnectionCollection class [InfoPath 2007],DataConnection class [InfoPath 2007],InfoPath 2007, accessing external data,data [InfoPath 2007], external sources
ms.localizationpriority: medium
ms.assetid: db7c2521-a1ad-4802-b398-79575d3d310a
description: InfoPath フォーム テンプレートで作業しているときに、フォームのセカンダリ データ ソースにアクセスしてそこに含まれるデータを操作するコードを書くことができます。
ms.openlocfilehash: 2119564d31766e318434324fc553394c73d82f83
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564639"
---
# <a name="access-external-data-sources"></a>外部データ ソースにアクセスする

InfoPath フォーム テンプレートで作業しているときに、フォームのセカンダリ データ ソースにアクセスしてそこに含まれるデータを操作するコードを書くことができます。 
  
各セカンダリ データ ソースは、[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) クラスを使用してインスタンス化されたオブジェクトによって表現され、データベースや Web サービス クエリなどの外部データ ソースから取得された保管データに相当します。これらのデータ ソースがセカンダリと呼ばれる理由は、ユーザーが InfoPath フォームを保存する際、メインのデータ ソース (プライマリ データ ソース) のデータのみが保存され、これらのデータ ソースのデータは保存されないためです。データ ソースへの接続は、"データ接続" クラスを使用してインスタンス化されたオブジェクトによって表されます。このようなクラスには、XML Web サービスへのデータ接続を表す [WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) などがあります。 
  
インスタンス化された [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) オブジェクトは、データベースまたは Web サービス クエリからデータ接続によって返される XML データの格納場所を表し、"データ接続" クラスはデータ接続自体 ([ **データ**] タブの [ **データ接続**] コマンドを使用して定義および指定するデータ接続) を表します。 
  
InfoPath オブジェクト モデルは、[DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) クラスに関連した [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) クラスの使用によるフォームのセカンダリ データ ソースへのアクセスをサポートしています。 
  
InfoPath オブジェクト モデルは、フォームによって使用されるデータ接続に関する情報を格納したデータ接続クラスのセットも提供します。
  
> [!NOTE]
> Microsoft InfoPath 2003 では、データ接続のことをデータ アダプターと呼びます。 
  
データ接続には 2 つの種類があります。クエリ接続は、データを取得するために使用されます。取得されたデータは、セカンダリ データ ソースに格納されます。送信用接続は、データベースや Web サービスなどにデータを送信するために使用されます。送信されるデータは、メインまたはセカンダリのデータ ソースからコピーされます。 
  
## <a name="overview-of-the-datasourcecollection-class"></a>DataSourceCollection クラスの概要

[DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) クラスには、次のプロパティとメソッドがあります。フォームの開発者は、これらを使用することにより、フォームに含まれている [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) オブジェクトのインスタンスを管理できます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Count.aspx) プロパティ  <br/> |コレクションに含まれている **DataSource** オブジェクト インスタンスの数を返します。  <br/> |
|[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.GetEnumerator.aspx) メソッド  <br/> |コレクションの反復処理に使用できる **IEnumerator** を返します。  <br/> |
|[Item[Int32]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) プロパティ  <br/> |指定した **DataSource** オブジェクトへの参照をインデックス値で返します。  <br/> |
|[Item[String]](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.Item.aspx) プロパティ  <br/> |指定した **DataSource** オブジェクトへの参照を名前で返します。  <br/> |
   
## <a name="overview-of-the-datasource-class"></a>DataSource クラスの概要

[DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) クラスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、InfoPath セカンダリ データ ソースを操作することができます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) メソッド  <br/> |データ ソースへのアクセスおよび編集のための [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) オブジェクトを返します。  <br/> |
|[QueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.QueryConnection.aspx) プロパティ  <br/> |関連付けられたデータ接続オブジェクトへの参照を取得します。  <br/> データ接続に対してクエリを実行し、返されたデータを、 **DataSource** オブジェクトに関連付けられた XML ノードに XML として挿入するには、関連付けられたデータ接続オブジェクトの [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.Execute.aspx) メソッドを使用します。  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.Name.aspx) プロパティ  <br/> |**DataSource** オブジェクトの名前を取得します。  <br/> |
|[ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.ReadOnly.aspx) プロパティ  <br/> |データ ソースが読み取り専用状態かどうかを示す値を取得します。  <br/> |
|[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) メソッド  <br/> |指定した XML ノードの名前付きプロパティの値を取得します。このノードは、メイン データ ソースの **nonattribute** ノードである必要があります。    <br/> |
|[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) メソッド  <br/> |指定した XML ノードの名前付きプロパティの値を設定します。このノードは、メイン データ ソースの **nonattribute** ノードである必要があります。    <br/> |
   
## <a name="overview-of-the-data-connection-classes"></a>データ接続クラスの概要

データ接続にアクセスするためのクラスは、さまざまなプロパティとメソッドを提供し、これらは外部データ ソースへの接続を通じてデータを取得および送信します。 **DataSource** オブジェクトに関連付けられるデータ接続は、外部データ接続の種類に依存します。InfoPath は、データ接続にアクセスするために以下のクラスを実装します。 
  
|**名前**|**説明**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) クラス  <br/> |ADO/OLEDB データ ソースのクエリを実行します。Microsoft Access および Microsoft SQL Server に限定されます。  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) クラス  <br/> |ADO/OLEDB データ ソースにデータを送信します。Microsoft Access および Microsoft SQL Server に限定されます。  <br/> |
|[SharePointListRWQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWQueryConnection.aspx) クラス  <br/> |SharePoint リストまたはドキュメント ライブラリのクエリを実行します。  <br/> |
|[SharePointListRWSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharePointListRWSubmitConnection.aspx) <br/> |SharePoint リストまたはドキュメント ライブラリにデータを送信します。  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) クラス  <br/> |XML Web サービスに接続します。  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) クラス  <br/> |XML ファイルのクエリを実行します。  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) クラス  <br/> |XML ファイルにデータを送信します。  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) クラス  <br/> |フォームを電子メールの添付ファイルとして送信します。  <br/> |
|[BdcQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcQueryConnection.aspx) クラス  <br/> |SharePoint Foundation 2010 または SharePoint Server 2010 を実行しているサーバーで、外部リストのクエリを実行します。  <br/> |
|[BdcSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.BdcSubmitConnection.aspx) クラス  <br/> |SharePoint Foundation 2010 または SharePoint Server 2010 を実行しているサーバー上の外部リストにデータを送信します。  <br/> |
   
## <a name="using-the-datasourcecollection-and-the-datasource-classes"></a>DataSourceCollection クラスと DataSource クラスを使用する

フォーム テンプレートに関連付けられたデータ ソースのコレクションを表す **DataSourceCollection** オブジェクトにアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) クラスの [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用します。たとえば、Northwind データベースの Employees テーブルからデータを取得する Employees という名前のセカンダリ データ ソースを作成した場合、 **DataSourceCollection** オブジェクトを使用して、取得されたデータを表す **DataSource** オブジェクトへの参照を設定することができます。 
  
以下のコード例では、 **DataSourceCollection** クラスのアクセサー プロパティにセカンダリ データ ソースの名前が渡されて、取得された Employees テーブルのデータを表す **DataSource** オブジェクトへの参照が返されます。その後、 **DataSource** クラスの **CreateNavigator** メソッドを使用して **XPathNavigator** クラスの **InnerXml** プロパティにアクセスすることにより、セカンダリ データ ソースから取得されたデータを格納している XML ノードがメッセージ ボックスに表示されます。 
  
```cs
// Instantiate a variable to access the specified data source
// from the DataSourceCollection of the form.
DataSource myDataSource = 
   this.DataSources["Employees"];
// Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " +
   myDataSource.CreateNavigator().InnerXml.ToString());
```

```vb
' Instantiate a variable to access the specified data source
' from the DataSourceCollection of the form.
Dim myDataSource As DataSource = _
   Me.DataSources("Employees")
' Display the XML data from the secondary data source.
MessageBox.Show("Data source data: " &amp; _
   myDataSource.CreateNavigator().InnerXml.ToString())
```

セカンダリ データ ソースに格納されているデータを操作するには、 **DataSource** クラスの **CreateNavigator** メソッドを使用して、そのセカンダリ データが格納されているノードにある **XPathNavigator** オブジェクトへの参照を取得します。 **XPathNavigator** クラスのプロパティまたはメソッドを使用して、データを操作できます。 詳細については、「[XPathNavigator クラスおよび XPathNodeIterator クラスを操作する方法](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)」を参照してください。
  
## <a name="using-the-dataconnectioncollection-and-the-dataconnection-classes"></a>DataConnectionCollection クラスと DataConnection クラスを使用する

フォーム テンプレートに関連付けられたデータ接続のコレクションを表す [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) オブジェクトにアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx) クラスの **DataConnections** プロパティを使用します。たとえば、Northwind データベースの Employees テーブルからデータを取得する Employees という名前のセカンダリ データ ソースを作成した場合、フォーム テンプレートに関連付けられた **DataConnectionCollection** オブジェクトを使用して、データベースへの接続を表す **DataConnection** への参照を設定することができます。 
  
以下のコード例では、 **DataConnectionCollection** クラスのアクセサー プロパティにセカンダリ データ ソースの名前が渡されて、今度は、Northwind データベースへの接続を表す **ADOQueryConnection** オブジェクトへの参照が返されます。これを正常に動作させるには、返されるオブジェクトを **ADOQueryConnection** 型に明示的にキャストする必要があります。メッセージ ボックス内での ADO 接続文字列の表示には [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.Connection.aspx) インターフェイスの **Connection** プロパティが使用されます。 
  
```cs
// Instantiate a variable to access the specified data connection
// from the DataConnectionCollection of the form. 
// You must cast to the specific data connection type
// (ADOQueryConnection) before you can access the data connection.
ADOQueryConnection myADOConnection = 
   (ADOQueryConnection)this.DataConnections["Employees"];
// Display the connection information for the data connection.
MessageBox.Show("Connection string: " + myADOConnection.Connection);
```

```vb
' Instantiate a variable to access the specified data connection
' from the DataConnectionCollection of the form. 
' You must cast to the specific data connection type
' (ADOQueryConnection) before you can access the data connection.
Dim myADOConnection As ADOQueryConnection = _
   DirectCast(Me.DataConnections("Employees"), ADOQueryConnection)
' Display the connection information for the data connection.
MessageBox.Show("Connection string: " &amp; myADOConnection.Connection)
```

## <a name="see-also"></a>関連項目



[InfoPath Forms Services で動作する InfoPath フォーム テンプレートを作成する](creating-infopath-form-templates-that-work-with-infopath-forms-services.md)

