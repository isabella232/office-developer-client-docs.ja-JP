---
title: データ シェイプに必要なプロバイダー
TOCTitle: Required providers for data shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ffb45599c01121204fe036cfdf60f17865388cd4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306658"
---
# <a name="required-providers-for-data-shaping"></a><span data-ttu-id="eafc2-102">データ シェイプに必要なプロバイダー</span><span class="sxs-lookup"><span data-stu-id="eafc2-102">Required providers for data shaping</span></span>

<span data-ttu-id="eafc2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="eafc2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eafc2-p101">通常、データ シェイプには 2 つのプロバイダーが必要です。サービス プロバイダーの [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) はデータ シェイプの機能を提供し、データ プロバイダー (OLE DB Provider for SQL Server など) はシェイプされた [Recordset](recordset-object-ado.md) に設定するためのデータ行を提供します。</span><span class="sxs-lookup"><span data-stu-id="eafc2-p101">Data shaping typically requires two providers. The service provider, [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md), supplies the data shaping functionality, and a data provider, such as the OLE DB Provider for SQL Server, supplies rows of data to populate the shaped [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="eafc2-106">サービス プロバイダー (MSDataShape) の名前は、[Connection](connection-object-ado.md) オブジェクトの [Provider](provider-property-ado.md) プロパティの値または接続文字列のキーワード "Provider=MSDataShape;" として指定できます。</span><span class="sxs-lookup"><span data-stu-id="eafc2-106">The name of the service provider (MSDataShape) can be specified as the value of the [Connection](connection-object-ado.md) object [Provider](provider-property-ado.md) property or the connection string keyword "Provider=MSDataShape;".</span></span>

<span data-ttu-id="eafc2-107">データプロバイダーの名前は、OLE DB のデータシェイプサービスによって**connection**オブジェクトの[Properties](properties-collection-ado.md)コレクションに追加されるか、または接続文字列のキーワード "\* で、データ**プロバイダー**の動的プロパティの値として指定できます。*データプロバイダー = \* \* \* プロバイダー*"。</span><span class="sxs-lookup"><span data-stu-id="eafc2-107">The name of the data provider can be specified as the value of the **Data Provider** dynamic property, which is added to the **Connection** object [Properties](properties-collection-ado.md) collection by the Data Shaping Service for OLE DB, or the connection string keyword "\**Data Provider=\*\*\*provider*".</span></span>

<span data-ttu-id="eafc2-p102">**Recordset** にデータを設定しない場合は (たとえば、NEW キーワードを指定して列を作成する **Recordset** など)、データ プロバイダーは必要ありません。このような場合は、"**Data Provider=** none;" を指定します。</span><span class="sxs-lookup"><span data-stu-id="eafc2-p102">No data provider is required if the **Recordset** is not populated (for example, as in a fabricated **Recordset** where columns are created with the NEW keyword). In that case, specify "**Data Provider=** none;".</span></span>

## <a name="example"></a><span data-ttu-id="eafc2-110">例</span><span class="sxs-lookup"><span data-stu-id="eafc2-110">Example</span></span>

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

