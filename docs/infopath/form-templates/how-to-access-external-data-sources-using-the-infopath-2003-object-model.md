---
title: InfoPath 2003 オブジェクト モデルを使用して外部データ ソースのアクセス
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- data sources [infopath 2007], accessing with infopath 2003 object model,InfoPath 2003-compatible form templates, accessing external data
localization_priority: Normal
ms.assetid: 9fd9ca47-abf1-48dd-8668-dfee27161793
description: InfoPath 2003 互換オブジェクト モデルを使用する InfoPath フォーム テンプレートの作業を行う際に、フォームのセカンダリ データ ソースにアクセスし、格納されているデータを操作するためのコードを書くことができます。
ms.openlocfilehash: cf06cdc6a02eba855442cdab4c3c698ed3f4425f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799109"
---
# <a name="access-external-data-sources-using-the-infopath-2003-object-model"></a><span data-ttu-id="e33a3-104">InfoPath 2003 オブジェクト モデルを使用して外部データ ソースのアクセス</span><span class="sxs-lookup"><span data-stu-id="e33a3-104">Access External Data Sources Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="e33a3-105">InfoPath 2003 互換オブジェクト モデルを使用する InfoPath フォーム テンプレートの作業を行う際に、フォームのセカンダリ データ ソースにアクセスし、格納されているデータを操作するためのコードを書くことができます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-105">When working with an InfoPath form template that uses the InfoPath 2003 compatible object model, you can write code to access the form's secondary data sources and manipulate the data that they contain.</span></span>
  
<span data-ttu-id="e33a3-p101">各セカンダリ データ ソースは、[DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インターフェイスを使用してインスタンス化されたオブジェクトによって表現され、データベースや Web サービス クエリなどの外部データ ソースから取得された保管データに応答します。これらのデータ ソースがセカンダリと呼ばれる理由は、ユーザーが InfoPath フォームを保存する際、メインのデータ ソースのデータのみが保存され、これらのデータ ソースのデータは保存されないためです。データ ソースへの接続は "データ アダプター" インターフェイスを使用してインスタンス化されたオブジェクトによって表されます。このようなインターフェイスには、XML Web サービスへのデータ接続を表す [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) などがあります。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p101">Each secondary data source is represented by an object instantiated using the [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) interface, and corresponds to stored data, obtained from some external source of data, such as a database or a Web Service query. These data sources are referred to as secondary because when the user saves an InfoPath form, the user is saving the data only in the main data source, not the data in the secondary data sources. The connection to a data source is represented by an object instantiated using one of the "data adapter" interfaces, such as the [WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) interface, which represents a data connection to an XML Web Service.</span></span> 
  
<span data-ttu-id="e33a3-109">インスタンス化された [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) オブジェクトは、データベースまたは Web サービス クエリへのデータ接続によって返される XML データの格納場所を表し、データ アダプターはデータ接続自体を表します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-109">The instantiated [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) object represents the storage of XML data returned by a data connection (to a database or Web Service query), and the data adapter represents the data connection itself.</span></span> 
  
<span data-ttu-id="e33a3-110">InfoPath オブジェクト モデルは、[DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インターフェイスに関連した [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) インターフェイスの使用によるフォームのセカンダリ データ ソースへのアクセスをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="e33a3-110">The InfoPath object model supports access to a form's secondary data sources through the use of the [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) interface in association with the [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) interface.</span></span> 
  
<span data-ttu-id="e33a3-111">InfoPath オブジェクト モデルは、フォームによって使用されるデータ接続に関する情報を格納したデータ アダプター オブジェクトのセットも提供します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-111">The InfoPath object model also provides a set of data adapter objects, containing information about the data connections used by the form.</span></span> 
  
<span data-ttu-id="e33a3-p102">データ アダプターには、クエリ アダプターと送信アダプターの 2 種類があります。クエリ アダプターは、セカンダリ データ ソースに保管されるデータの取得に使用され、送信アダプターは、データベースや Web サービスなどへのデータの送信に使用されます。送信されるデータは、メインまたはセカンダリのデータ ソースからコピーされます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p102">There are two kinds of data adapters: Query adapters and Submit adapters. Query adapters are used to obtain the data that is then stored in a secondary data source whereas Submit adapters are used to submit data, to a database or Web service, for example. The submitted data is copied from the main or secondary data sources.</span></span> 
  
## <a name="overview-of-the-dataobjectscollection-interface"></a><span data-ttu-id="e33a3-115">DataObjectsCollection インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="e33a3-115">Overview of the DataObjectsCollection Interface</span></span>

<span data-ttu-id="e33a3-116">[DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) インターフェイスは以下のプロパティとメソッドを提供します。フォームの開発者は、これらを使用して、フォームが格納する [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インスタンスを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-116">The [DataObjectsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjectsCollection.aspx) interface provides the following properties and methods, which form developers can use to manage the [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) instances that the form contains.</span></span> 
  
|<span data-ttu-id="e33a3-117">**名前**</span><span class="sxs-lookup"><span data-stu-id="e33a3-117">**Name**</span></span>|<span data-ttu-id="e33a3-118">**説明**</span><span class="sxs-lookup"><span data-stu-id="e33a3-118">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e33a3-119">[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="e33a3-119">[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Count.aspx) property</span></span>  <br/> |<span data-ttu-id="e33a3-120">コレクションに含まれる **DataSourceObject** インスタンスの数を返します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-120">Returns a count of the number of **DataSourceObject** instances contained in the collection.</span></span>  <br/> |
|<span data-ttu-id="e33a3-121">[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="e33a3-121">[GetEnumerator](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.GetEnumerator.aspx) method</span></span>  <br/> |<span data-ttu-id="e33a3-122">コレクションの反復処理に使用できる **IEnumerator** を返します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-122">Returns an **IEnumerator** that can be used to iterate through the collection.</span></span>  <br/> |
|<span data-ttu-id="e33a3-123">[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="e33a3-123">[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObjects.Item.aspx) property</span></span>  <br/> |<span data-ttu-id="e33a3-124">指定した **DataSourceObject** インスタンスへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-124">Returns a reference to the specified **DataSourceObject** instance.</span></span>  <br/> |
   
## <a name="overview-of-the-datasourceobject-interface"></a><span data-ttu-id="e33a3-125">DataSourceObject インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="e33a3-125">Overview of the DataSourceObject Interface</span></span>

<span data-ttu-id="e33a3-126">[DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) インターフェイスは、以下のメソッドとプロパティを提供します。フォームの開発者は、これらを使用して、InfoPath セカンダリ データ ソースを操作することができます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-126">The [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) interface provides the following method and properties, which form developers can use to interact with an InfoPath secondary data source.</span></span> 
  
|<span data-ttu-id="e33a3-127">**名前**</span><span class="sxs-lookup"><span data-stu-id="e33a3-127">**Name**</span></span>|<span data-ttu-id="e33a3-128">**説明**</span><span class="sxs-lookup"><span data-stu-id="e33a3-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e33a3-129">[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx) メソッド</span><span class="sxs-lookup"><span data-stu-id="e33a3-129">[Query](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Query.aspx) method</span></span>  <br/> |<span data-ttu-id="e33a3-130">データ アダプター上でクエリを実行し、返されたデータを、 **DataSourceObject** に関連付けられた XML Document Object Model (DOM) に XML として挿入します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-130">Executes the query on the data adapter and inserts the returned data as XML into the XML Document Object Model (DOM) associated with the **DataSourceObject**.</span></span>  <br/> |
|<span data-ttu-id="e33a3-131">[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="e33a3-131">[DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.DOM.aspx) property</span></span>  <br/> |<span data-ttu-id="e33a3-132">**DataSourceObject** を使用してデータの格納と操作に使用される XML DOM への参照を返します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-132">Returns a reference to the XML DOM used to store and manipulate data using the **DataSourceObject**.</span></span>  <br/> |
|<span data-ttu-id="e33a3-133">[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="e33a3-133">[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.Name.aspx) property</span></span>  <br/> |<span data-ttu-id="e33a3-134">**DataSourceObject** の名前を示す文字列値を返します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-134">Returns a string value indicating the name of the **DataSourceObject**.</span></span>  <br/> |
|<span data-ttu-id="e33a3-135">[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx) プロパティ</span><span class="sxs-lookup"><span data-stu-id="e33a3-135">[QueryAdapter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataObject.QueryAdapter.aspx) property</span></span>  <br/> |<span data-ttu-id="e33a3-136">関連付けられたデータ アダプター オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-136">Returns a reference to the associated data adapter object.</span></span>  <br/> |
   
## <a name="overview-of-the-data-adapter-interfaces"></a><span data-ttu-id="e33a3-137">データ アダプター インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="e33a3-137">Overview of the Data Adapter Interfaces</span></span>

<span data-ttu-id="e33a3-p103">データ アダプターにアクセスするためのインターフェイスは、さまざまなプロパティとメソッドを提供し、これらは外部データ ソースへの接続を通じてデータを取得および送信します。[DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) オブジェクトに関連付けられるデータ アダプターは、外部データ接続の種類に依存します。InfoPath は、データ アダプターにアクセスするために以下のインターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p103">The interfaces for accessing data adapters provide different properties and methods that retrieve and submit data through connections to external data sources; the data adapter that is associated with a [DataSourceObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataSourceObject.aspx) object is dependent on the type of external data connection. InfoPath implements the following interfaces for accessing data adapters.</span></span> 
  
|<span data-ttu-id="e33a3-140">**名前**</span><span class="sxs-lookup"><span data-stu-id="e33a3-140">**Name**</span></span>|<span data-ttu-id="e33a3-141">**説明**</span><span class="sxs-lookup"><span data-stu-id="e33a3-141">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e33a3-142">[ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx) インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e33a3-142">[ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapterObject.aspx) interface</span></span>  <br/> |<span data-ttu-id="e33a3-143">ADO/OLEDB データ ソースに接続します。Microsoft Access および Microsoft SQL Server に限定されます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-143">Connects to ADO/OLEDB data sources; limited to Microsoft Access and Microsoft SQL Server™.</span></span>  <br/> |
|<span data-ttu-id="e33a3-144">[SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx) インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e33a3-144">[SharepointListAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SharepointListAdapterObject.aspx) interface</span></span>  <br/> |<span data-ttu-id="e33a3-145">SharePoint リストまたはドキュメント ライブラリに接続します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-145">Connects to a SharePoint list or document library.</span></span>  <br/> |
|<span data-ttu-id="e33a3-146">[WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) インターフェイス</span><span class="sxs-lookup"><span data-stu-id="e33a3-146">[WebServiceAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WebServiceAdapterObject.aspx) interface</span></span>  <br/> |<span data-ttu-id="e33a3-147">XML Web サービスに接続します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-147">Connects to XML Web services.</span></span>  <br/> |
|<span data-ttu-id="e33a3-148">[XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx) オブジェクト</span><span class="sxs-lookup"><span data-stu-id="e33a3-148">[XMLFileAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLFileAdapterObject.aspx) object</span></span>  <br/> |<span data-ttu-id="e33a3-149">XML ファイルに接続します。</span><span class="sxs-lookup"><span data-stu-id="e33a3-149">Connects to an XML file.</span></span>  <br/> |
   
## <a name="using-the-datasourceobjects-and-the-datasourceobject-interfaces"></a><span data-ttu-id="e33a3-150">DataSourceObjects インターフェイスと DataSourceObject インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="e33a3-150">Using the DataSourceObjects and the DataSourceObject Interfaces</span></span>

<span data-ttu-id="e33a3-p104">**DataSourceObjects** コレクションは、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) インターフェイスの [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) プロパティを通じてアクセスされます。たとえば、Employees という名のセカンダリ データ ソースを作成し、このデータ ソースが Northwind Traders Microsoft Access データベースの Employees テーブルからデータを取得する場合、 **DataSourceObjects** コレクションを使用して、取得されたデータを表す **DataObject** オブジェクトへの参照を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p104">The **DataSourceObjects** collection is accessed through the [DataObjects](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataObjects.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface. For example, if you create a secondary data source named Employees that retrieves data from the Employees table in the Northwind Traders Microsoft Access database, you can use the **DataSourceObjects** collection to set a reference to a **DataObject** object that represents the retrieved data.</span></span> 
  
<span data-ttu-id="e33a3-p105">以下のコード例では、セカンダリ データ ソースの名前は、 **DataObjectsCollection** インターフェイスのアクセサー プロパティに渡され、その後 **DataSourceObject** オブジェクトへの参照を返します。セカンダリ データ ソースからのデータは、 **DataSourceObject** インターフェイスの **DOM** プロパティを使用してメッセージ ボックス内に表示され、XML DOM の **xml** プロパティにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p105">In the following code sample, the name of the secondary data source is passed to the accessor property of the **DataObjectsCollection** interface, which returns a reference to the **DataSourceObject** object. The data from the secondary data source is displayed in a message box by using the **DOM** property of the **DataSourceObject** interface to access the **xml** property of the XML DOM.</span></span> 
  
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

<span data-ttu-id="e33a3-p106">セカンダリ データ ソースに格納されているデータを操作するには、 **DataSourceObject** インターフェイスの **DOM** プロパティを使用して、データを格納している XML DOM への参照を返します。XML DOM への参照がある場合、そのあらゆるプロパティまたはメソッドを使用して、そこに格納されているデータを操作できます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p106">To manipulate the data that is contained in a secondary data source, use the **DOM** property of the **DataSourceObject** interface to return a reference to the XML DOM containing the data. When you have the reference to the XML DOM, you can use any of its properties or methods to manipulate the data that it contains.</span></span> 
  
## <a name="using-the-dataadapterscollection-and-the-dataadapterobject-interfaces"></a><span data-ttu-id="e33a3-157">DataAdaptersCollection インターフェイスと DataAdapterObject インターフェイスの使用</span><span class="sxs-lookup"><span data-stu-id="e33a3-157">Using the DataAdaptersCollection and the DataAdapterObject Interfaces</span></span>

<span data-ttu-id="e33a3-p107">[DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) インターフェイスは、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) インターフェイスの **DataAdapters** プロパティを通じてアクセスされます。たとえば、Employees という名のセカンダリ データ ソースを作成し、このデータ ソースが Northwind Traders Microsoft Access データベースの Employees テーブルからデータを取得する場合、 **DataAdapterObjects** コレクションを使用して、データベースへの接続を表す **DataAdapterObject** への参照を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p107">The [DataAdaptersCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.DataAdaptersCollection.aspx) interface is accessed through the [DataAdapters](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DataAdapters.aspx) property of the **XDocument** interface. For example, if you create a secondary data source named Employees that retrieves data from the Employees table in the Northwind Traders Microsoft Access database, you can use the **DataAdapterObjects** collection to set a reference to the **DataAdapterObject** that represents the connection to the database.</span></span> 
  
<span data-ttu-id="e33a3-p108">以下のコード例では、セカンダリ データ ソースの名前は、 **DataAdaptersCollection** のアクセサー プロパティに渡され、この場合は、その後、Northwind Microsoft Access データベースへの接続を表す **ADOAdapterObject** のインスタンスへの参照を返します。これを正常に動作させるには、 **ADOAdapterObject** として返されるオブジェクトを明示的にキャストする必要があります。メッセージ ボックス内での ADO 接続文字列の表示には [ADOAdapterObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) インターフェイスの **Connection** プロパティが使用されます。</span><span class="sxs-lookup"><span data-stu-id="e33a3-p108">In the following code sample, the name of the secondary data source is passed to the accessor property of the **DataAdaptersCollection**, which, in this case, returns a reference to an instance of the **ADOAdapterObject** that represents the connection to the Northwind Microsoft Access database. For this to work properly, you must explicitly cast the object being returned as an **ADOAdapterObject**. The [Connection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ADOAdapter2.Connection.aspx) property of the **ADOAdapterObject** interface is used to display the ADO connection string in a message box.</span></span> 
  
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


