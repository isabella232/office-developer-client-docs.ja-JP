---
title: データ シェイプに必要なプロバイダー
TOCTitle: Required Providers for Data Shaping
ms:assetid: eb8933fb-d533-3ea7-e045-35c1ca585765
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250194(v=office.15)
ms:contentKeyID: 48548488
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: de8634503c81bd2c66eeda0c64a8b1ff1b6f5363
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885356"
---
# <a name="required-providers-for-data-shaping"></a>データ シェイプに必要なプロバイダー


**適用されます**Access 2013、Office 2013。

通常、データ シェイプには 2 つのプロバイダーが必要です。サービス プロバイダーの [Data Shaping Service for OLE DB](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) はデータ シェイプの機能を提供し、データ プロバイダー (OLE DB Provider for SQL Server など) はシェイプされた [Recordset](recordset-object-ado.md) に設定するためのデータ行を提供します。

サービス プロバイダー (MSDataShape) の名前は、[Connection](connection-object-ado.md) オブジェクトの [Provider](provider-property-ado.md) プロパティの値または接続文字列のキーワード "Provider=MSDataShape;" として指定できます。

OLE DB、または接続文字列キーワードのデータ シェイプ サービスで**接続**オブジェクト[のプロパティ](properties-collection-ado.md)コレクションに追加される、 **Data Provider**動的プロパティの値としてデータ プロバイダーの名前を指定することができます」**データ プロバイダー =。 プロバイダー*」です。

**Recordset** にデータを設定しない場合は (たとえば、NEW キーワードを指定して列を作成する **Recordset** など)、データ プロバイダーは必要ありません。このような場合は、"**Data Provider=** none;" を指定します。

## <a name="example"></a>例

```vb 
 
Dim cnn As New ADODB.Connection 
cnn.Provider = "MSDataShape" 
cnn.Open "Data Provider=SQLOLEDB;Integrated Security=SSPI;Database=Northwind" 
```

