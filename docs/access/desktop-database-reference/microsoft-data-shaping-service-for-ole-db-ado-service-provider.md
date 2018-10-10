---
title: Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a72dcc754f39144da4476c9262b93b920fbfbdf6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478105"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a>Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)


**適用されます**Access 2013 |。Office 2013

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
<td><p><strong>変形の名前</strong>プロパティの値が重複して<strong>レコード セット</strong>オブジェクトを許可するかどうかを示します。 新しい<strong>レコード セット</strong>が作成され、この動的プロパティが<strong>True</strong>の場合、既存の<strong>レコード セット</strong>として名前の形状を変更、同じユーザーが指定したし、新しい<strong>レコード セット</strong>オブジェクトのリシェイプ名が一意になるように変更します。 このプロパティが<strong>False</strong>であり、新しい<strong>レコード セット</strong>が作成され、既存の<strong>レコード セット</strong>として名前の形状を変更、同じユーザーが指定した、両方の<strong>レコード セット</strong>オブジェクトには、同じ名前の形状を変更する必要があります。 したがって、どちらの<strong>Recordset</strong>もリシェイプできません両方のレコード セットが存在する限りに。 このプロパティの既定値は <strong>False</strong> です。</p></td>
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

データ シェイプの詳細については、「[データ シェイプの概要](data-shaping-summary.md)」を参照してください。

