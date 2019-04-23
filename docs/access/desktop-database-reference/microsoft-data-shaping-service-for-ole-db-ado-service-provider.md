---
title: Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5065b966608f8d6a3ef1cb05be890b9a1f147dc8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288961"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)


**適用先:** Access 2013、Office 2013

Microsoft Data Shaping Service for OLE DB サービス プロバイダーは、データ プロバイダーからの階層 (シェイプされた) [Recordset](recordset-object-ado.md) オブジェクトの構築をサポートします。

## <a name="provider-keyword"></a>プロバイダー キーワード

Data Shaping Service for OLE DB を呼び出すには、接続文字列のキーワードと値を次のように指定します。

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a>動的プロパティ

このサービス プロバイダーを呼び出すと、次に示す動的プロパティが [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>動的プロパティ名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Unique Reshape Names</strong></p></td>
<td><p><strong>Reshape Name</strong> プロパティの値が重複する <strong>Recordset</strong> オブジェクトを作成できるかどうかを示します。 この動的プロパティが <strong>True</strong> の場合、既存の <strong>Recordset</strong> と同じ名前で新しく <strong>Recordset</strong> を作成すると、新しい <strong>Recordset</strong> オブジェクトのリシェイプ名は、一意になるように変更されます。 このプロパティが <strong>False</strong> の場合、既存の <strong>Recordset</strong> と同じリシェイプ名を指定して新しく <strong>Recordset</strong> を作成すると、両方の <strong>Recordset</strong> オブジェクトのリシェイプ名が同じになります。 したがって、両方のレコードセットが存在する限り、どちらの <strong>Recordset</strong> もリシェイプできません。 このプロパティの既定値は <strong>False</strong> です。</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Provider</strong></p></td>
<td><p>シェイプする行を提供するプロバイダーの名前を指定します。プロバイダーを使用して行を提供しない場合、この値を NONE に指定することもできます。</p></td>
</tr>
</tbody>
</table>


値の設定が可能な動的プロパティは、プロパティ名を接続文字列のキーワードとして指定して設定することもできます。たとえば、Microsoft Visual Basic で **Data Provider** 動的プロパティを "MSDASQL" に設定するには、次のように指定します。

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

動的プロパティの名前を [Properties](properties-collection-ado.md) プロパティのインデックスとして指定して、動的プロパティを設定または取得することもできます。たとえば、 **Data Provider** 動的プロパティの値を取得して出力した後、新しい値を設定するには、次のように指定します。

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

データ シェイプの詳細については、「[データ シェイプの概要](data-shaping.md)」を参照してください。

