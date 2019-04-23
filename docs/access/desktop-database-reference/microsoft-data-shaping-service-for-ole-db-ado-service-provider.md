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
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="d6c97-102">Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="d6c97-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="d6c97-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d6c97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d6c97-104">Microsoft Data Shaping Service for OLE DB サービス プロバイダーは、データ プロバイダーからの階層 (シェイプされた) [Recordset](recordset-object-ado.md) オブジェクトの構築をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d6c97-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="d6c97-105">プロバイダー キーワード</span><span class="sxs-lookup"><span data-stu-id="d6c97-105">Provider Keyword</span></span>

<span data-ttu-id="d6c97-106">Data Shaping Service for OLE DB を呼び出すには、接続文字列のキーワードと値を次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d6c97-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="d6c97-107">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="d6c97-107">Dynamic Properties</span></span>

<span data-ttu-id="d6c97-108">このサービス プロバイダーを呼び出すと、次に示す動的プロパティが [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d6c97-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d6c97-109">動的プロパティ名</span><span class="sxs-lookup"><span data-stu-id="d6c97-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="d6c97-110">説明</span><span class="sxs-lookup"><span data-stu-id="d6c97-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d6c97-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="d6c97-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c97-112"><strong>Reshape Name</strong> プロパティの値が重複する <strong>Recordset</strong> オブジェクトを作成できるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d6c97-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="d6c97-113">この動的プロパティが <strong>True</strong> の場合、既存の <strong>Recordset</strong> と同じ名前で新しく <strong>Recordset</strong> を作成すると、新しい <strong>Recordset</strong> オブジェクトのリシェイプ名は、一意になるように変更されます。</span><span class="sxs-lookup"><span data-stu-id="d6c97-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="d6c97-114">このプロパティが <strong>False</strong> の場合、既存の <strong>Recordset</strong> と同じリシェイプ名を指定して新しく <strong>Recordset</strong> を作成すると、両方の <strong>Recordset</strong> オブジェクトのリシェイプ名が同じになります。</span><span class="sxs-lookup"><span data-stu-id="d6c97-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="d6c97-115">したがって、両方のレコードセットが存在する限り、どちらの <strong>Recordset</strong> もリシェイプできません。</span><span class="sxs-lookup"><span data-stu-id="d6c97-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="d6c97-116">このプロパティの既定値は <strong>False</strong> です。</span><span class="sxs-lookup"><span data-stu-id="d6c97-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d6c97-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="d6c97-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="d6c97-p102">シェイプする行を提供するプロバイダーの名前を指定します。プロバイダーを使用して行を提供しない場合、この値を NONE に指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d6c97-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d6c97-p103">値の設定が可能な動的プロパティは、プロパティ名を接続文字列のキーワードとして指定して設定することもできます。たとえば、Microsoft Visual Basic で **Data Provider** 動的プロパティを "MSDASQL" に設定するには、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d6c97-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="d6c97-p104">動的プロパティの名前を [Properties](properties-collection-ado.md) プロパティのインデックスとして指定して、動的プロパティを設定または取得することもできます。たとえば、 **Data Provider** 動的プロパティの値を取得して出力した後、新しい値を設定するには、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d6c97-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="d6c97-124">データ シェイプの詳細については、「[データ シェイプの概要](data-shaping.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d6c97-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

