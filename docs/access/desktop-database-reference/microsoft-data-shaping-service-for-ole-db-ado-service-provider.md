---
title: Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)
TOCTitle: Microsoft Data Shaping Service for OLE DB (ADO Service Provider)
ms:assetid: 6e6e5f39-6f43-7c7b-5812-796096d1d31b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249436(v=office.15)
ms:contentKeyID: 48545511
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9f18ae0a218adb65d453c3f54eb7af43af68097c
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870724"
---
# <a name="microsoft-data-shaping-service-for-ole-db-ado-service-provider"></a><span data-ttu-id="d591a-102">Microsoft Data Shaping Service for OLE DB (ADO サービス プロバイダー)</span><span class="sxs-lookup"><span data-stu-id="d591a-102">Microsoft Data Shaping Service for OLE DB (ADO Service Provider)</span></span>


<span data-ttu-id="d591a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d591a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d591a-104">Microsoft Data Shaping Service for OLE DB サービス プロバイダーは、データ プロバイダーからの階層 (シェイプされた) [Recordset](recordset-object-ado.md) オブジェクトの構築をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d591a-104">The Microsoft Data Shaping Service for OLE DB service provider supports the construction of hierarchical (shaped) [Recordset](recordset-object-ado.md) objects from a data provider.</span></span>

## <a name="provider-keyword"></a><span data-ttu-id="d591a-105">プロバイダー キーワード</span><span class="sxs-lookup"><span data-stu-id="d591a-105">Provider Keyword</span></span>

<span data-ttu-id="d591a-106">Data Shaping Service for OLE DB を呼び出すには、接続文字列のキーワードと値を次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d591a-106">To invoke the Data Shaping Service for OLE DB, specify the following keyword and value in the connection string.</span></span>

```vb 
 
"Provider=MSDataShape" 
```

## <a name="dynamic-properties"></a><span data-ttu-id="d591a-107">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="d591a-107">Dynamic Properties</span></span>

<span data-ttu-id="d591a-108">このサービス プロバイダーを呼び出すと、次に示す動的プロパティが [Connection](connection-object-ado.md) オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="d591a-108">When this service provider is invoked, the following dynamic properties are added to the [Connection](connection-object-ado.md) object's [Properties](properties-collection-ado.md) collection.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d591a-109">動的プロパティ名</span><span class="sxs-lookup"><span data-stu-id="d591a-109">Dynamic Property Name</span></span></p></th>
<th><p><span data-ttu-id="d591a-110">説明</span><span class="sxs-lookup"><span data-stu-id="d591a-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d591a-111"><strong>Unique Reshape Names</strong></span><span class="sxs-lookup"><span data-stu-id="d591a-111"><strong>Unique Reshape Names</strong></span></span></p></td>
<td><p><span data-ttu-id="d591a-112"><strong>変形の名前</strong>プロパティの値が重複して<strong>レコード セット</strong>オブジェクトを許可するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d591a-112">Indicates whether <strong>Recordset</strong> objects with duplicate values for their <strong>Reshape Name</strong> properties are allowed.</span></span> <span data-ttu-id="d591a-113">新しい<strong>レコード セット</strong>が作成され、この動的プロパティが<strong>True</strong>の場合、既存の<strong>レコード セット</strong>として名前の形状を変更、同じユーザーが指定したし、新しい<strong>レコード セット</strong>オブジェクトのリシェイプ名が一意になるように変更します。</span><span class="sxs-lookup"><span data-stu-id="d591a-113">If this dynamic property is <strong>True</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as an existing <strong>Recordset</strong>, then the new <strong>Recordset</strong> object's reshape name is modified to make it unique.</span></span> <span data-ttu-id="d591a-114">このプロパティが<strong>False</strong>であり、新しい<strong>レコード セット</strong>が作成され、既存の<strong>レコード セット</strong>として名前の形状を変更、同じユーザーが指定した、両方の<strong>レコード セット</strong>オブジェクトには、同じ名前の形状を変更する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d591a-114">If this property is <strong>False</strong> and a new <strong>Recordset</strong> is created with the same user-specified reshape name as the existing <strong>Recordset</strong>, both <strong>Recordset</strong> objects will have the same reshape name.</span></span> <span data-ttu-id="d591a-115">したがって、どちらの<strong>Recordset</strong>もリシェイプできません両方のレコード セットが存在する限りに。</span><span class="sxs-lookup"><span data-stu-id="d591a-115">Therefore, neither <strong>Recordset</strong> can be reshaped as long as both recordsets exist.</span></span> <span data-ttu-id="d591a-116">このプロパティの既定値は <strong>False</strong> です。</span><span class="sxs-lookup"><span data-stu-id="d591a-116">The default value of the property is <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d591a-117"><strong>Data Provider</strong></span><span class="sxs-lookup"><span data-stu-id="d591a-117"><strong>Data Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="d591a-p102">シェイプする行を提供するプロバイダーの名前を指定します。プロバイダーを使用して行を提供しない場合、この値を NONE に指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d591a-p102">Indicates the name of the provider that will supply rows to be shaped. This value may be NONE if a provider will not be used to supply rows.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d591a-p103">値の設定が可能な動的プロパティは、プロパティ名を接続文字列のキーワードとして指定して設定することもできます。たとえば、Microsoft Visual Basic で **Data Provider** 動的プロパティを "MSDASQL" に設定するには、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d591a-p103">You may also set writable dynamic properties by specifying their names as keywords in the connection string. For example, in Microsoft Visual Basic, set the **Data Provider** dynamic property to "MSDASQL" by specifying:</span></span>

```vb 
 
Dim cn as New ADODB.Connection 
cn.Open "Provider=MSDataShape;Data Provider=MSDASQL" 
```

<span data-ttu-id="d591a-p104">動的プロパティの名前を [Properties](properties-collection-ado.md) プロパティのインデックスとして指定して、動的プロパティを設定または取得することもできます。たとえば、 **Data Provider** 動的プロパティの値を取得して出力した後、新しい値を設定するには、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="d591a-p104">You may also set or retrieve a dynamic property by specifying its name as the index to the [Properties](properties-collection-ado.md) property. For example, get and print the current value of the **Data Provider** dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print cn.Properties("Data Provider") 
cn.Properties("Data Provider") = "MSDASQL" 
```

<span data-ttu-id="d591a-124">データ シェイプの詳細については、「[データ シェイプの概要](data-shaping.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d591a-124">For more information about data shaping, see [Data Shaping](data-shaping.md).</span></span>

