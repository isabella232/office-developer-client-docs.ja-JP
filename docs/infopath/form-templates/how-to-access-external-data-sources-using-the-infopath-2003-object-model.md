---
title: InfoPath 2003 オブジェクト モデルを使用して外部データ ソースにアクセスする
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- データ ソース [infopath 2007],infopath 2003 オブジェクト モデルを使用してアクセスする,InfoPath 2003 互換のフォーム テンプレート,外部データにアクセスする
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: InfoPath 2003 互換オブジェクト モデルを使用する InfoPath フォーム テンプレートの作業を行う際に、フォームのセカンダリ データ ソースにアクセスし、格納されているデータを操作するためのコードを書くことができます。
ms.openlocfilehash: 569f029b412328f4d49e3079eaf207dc1556fc4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431681"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用して外部データ ソースにアクセスする

InfoPath 2003 互換オブジェクト モデルを使用する InfoPath フォーム テンプレートの作業を行う際に、フォームのセカンダリ データ ソースにアクセスし、格納されているデータを操作するためのコードを書くことができます。
  
各セカンダリ データ ソースは、[DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インターフェイスを使用してインスタンス化されたオブジェクトによって表現され、データベースや Web サービス クエリなどの外部データ ソースから取得された保管データに応答します。これらのデータ ソースがセカンダリと呼ばれる理由は、ユーザーが InfoPath フォームを保存する際、メインのデータ ソースのデータのみが保存され、これらのデータ ソースのデータは保存されないためです。データ ソースへの接続は "データ アダプター" インターフェイスを使用してインスタンス化されたオブジェクトによって表されます。このようなインターフェイスには、XML Web サービスへのデータ接続を表す [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) などがあります。 
  
インスタンス化された [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) オブジェクトは、データベースまたは Web サービス クエリへのデータ接続によって返される XML データの格納場所を表し、データ アダプターはデータ接続自体を表します。 
  
InfoPath オブジェクト モデルは、[DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インターフェイスに関連した [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) インターフェイスの使用によるフォームのセカンダリ データ ソースへのアクセスをサポートしています。 
  
InfoPath オブジェクト モデルは、フォームによって使用されるデータ接続に関する情報を格納したデータ アダプター オブジェクトのセットも提供します。 
  
データ アダプターには、クエリ アダプターと送信アダプターの 2 種類があります。クエリ アダプターは、セカンダリ データ ソースに保管されるデータの取得に使用され、送信アダプターは、データベースや Web サービスなどへのデータの送信に使用されます。送信されるデータは、メインまたはセカンダリのデータ ソースからコピーされます。 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a>DataObjectsCollection インターフェイスの概要

[DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) インターフェイスは以下のプロパティとメソッドを提供します。フォームの開発者は、これらを使用して、フォームが格納する [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インスタンスを管理することができます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx) プロパティ  <br/> |コレクションに含まれる **DataSourceObject** インスタンスの数を返します。  <br/> |
|[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx) メソッド  <br/> |コレクションの反復処理に使用できる **IEnumerator** を返します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx) プロパティ  <br/> |指定した **DataSourceObject** インスタンスへの参照を返します。  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a>DataSourceObject インターフェイスの概要

[DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インターフェイスは、以下のメソッドとプロパティを提供します。フォームの開発者は、これらを使用して、InfoPath セカンダリ データ ソースを操作することができます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx) メソッド  <br/> |データ アダプター上でクエリを実行し、返されたデータを、 **DataSourceObject** に関連付けられた XML Document Object Model (DOM) に XML として挿入します。  <br/> |
|[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx) プロパティ  <br/> |**DataSourceObject** を使用してデータの格納と操作に使用される XML DOM への参照を返します。  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx) プロパティ  <br/> |**DataSourceObject** の名前を示す文字列値を返します。  <br/> |
|[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx) プロパティ  <br/> |関連付けられたデータ アダプター オブジェクトへの参照を返します。  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a>データ アダプター インターフェイスの概要

データ アダプターにアクセスするためのインターフェイスは、さまざまなプロパティとメソッドを提供し、これらは外部データ ソースへの接続を通じてデータを取得および送信します。[DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) オブジェクトに関連付けられるデータ アダプターは、外部データ接続の種類に依存します。InfoPath は、データ アダプターにアクセスするために以下のインターフェイスを実装します。 
  
|**名前**|**説明**|
|:-----|:-----|
|[ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx) インターフェイス  <br/> |ADO/OLEDB データ ソースに接続します。Microsoft Access および Microsoft SQL Server に限定されます。  <br/> |
|[SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx) インターフェイス  <br/> |SharePoint リストまたはドキュメント ライブラリに接続します。  <br/> |
|[WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) インターフェイス  <br/> |XML Web サービスに接続します。  <br/> |
|[XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx) オブジェクト  <br/> |XML ファイルに接続します。  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a>DataSourceObjects インターフェイスと DataSourceObject インターフェイスの使用

**DataSourceObjects** コレクションは、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) インターフェイスの [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) プロパティを通じてアクセスされます。たとえば、Employees という名のセカンダリ データ ソースを作成し、このデータ ソースが Northwind Traders Microsoft Access データベースの Employees テーブルからデータを取得する場合、 **DataSourceObjects** コレクションを使用して、取得されたデータを表す **DataObject** オブジェクトへの参照を設定することができます。 
  
以下のコード例では、セカンダリ データ ソースの名前は、 **DataObjectsCollection** インターフェイスのアクセサー プロパティに渡され、その後 **DataSourceObject** オブジェクトへの参照を返します。セカンダリ データ ソースからのデータは、 **DataSourceObject** インターフェイスの **DOM** プロパティを使用してメッセージ ボックス内に表示され、XML DOM の **xml** プロパティにアクセスできます。 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataObjectsCollection of the form.
   // You must explicitly cast to the DataSourceObject type 
   // before you can access the data object.
   DataSourceObject myDataObject = 
      thisXDocument.DataObjects["Employees"] as DataSourceObject;
   // Display the data from the secondary data source using the 
   // XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object
   ' from the DataObjectsCollection of the form.
   Dim myDataObject As DataSourceObject = _
      thisXDocument.DataObjects("Employees")
   ' Display the data from the secondary data source using the 
   ' XML DOM.
   thisXDocument.UI.Alert("Data Adapter: " + myDataObject.DOM.xml)
End Sub
```

セカンダリ データ ソースに格納されているデータを操作するには、 **DataSourceObject** インターフェイスの **DOM** プロパティを使用して、データを格納している XML DOM への参照を返します。XML DOM への参照がある場合、そのあらゆるプロパティまたはメソッドを使用して、そこに格納されているデータを操作できます。 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a>DataAdaptersCollection インターフェイスと DataAdapterObject インターフェイスの使用

[DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) インターフェイスは、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) インターフェイスの **DataAdapters** プロパティを通じてアクセスされます。たとえば、Employees という名のセカンダリ データ ソースを作成し、このデータ ソースが Northwind Traders Microsoft Access データベースの Employees テーブルからデータを取得する場合、 **DataAdapterObjects** コレクションを使用して、データベースへの接続を表す **DataAdapterObject** への参照を設定することができます。 
  
以下のコード例では、セカンダリ データ ソースの名前は、 **DataAdaptersCollection** のアクセサー プロパティに渡され、この場合は、その後、Northwind Microsoft Access データベースへの接続を表す **ADOAdapterObject** のインスタンスへの参照を返します。これを正常に動作させるには、 **ADOAdapterObject** として返されるオブジェクトを明示的にキャストする必要があります。メッセージ ボックス内での ADO 接続文字列の表示には [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) インターフェイスの **Connection** プロパティが使用されます。 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Instantiate a variable to access the specified data object
   // from the DataAdaptersCollection of the form. 
   // You must explicitly cast to the specific adapter type
   // (ADOAdapterObject) before you can access the data adapter.
   ADOAdapterObject myADOAdapter = 
      thisXDocument.DataAdapters["Employees"] as ADOAdapterObject;
   // Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Instantiate a variable to access the specified data object. 
   ' You must explicitly cast to the specific adapter type
   ' (ADOAdapterObject) before you can access the data adapter.
   Dim myADOAdapter As ADOAdapterObject = _
      thisXDocument.DataAdapters("Employees")
   ' Display the connection information for the data adapter.
   thisXDocument.UI.Alert("Data Adapter: " + myADOAdapter.Connection)
End Sub
```


