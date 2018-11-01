---
title: 階層レコードセットを作成する
TOCTitle: Fabricating Hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10f2eb3d46bc0091f8ebadb5c6aea6efe4eb6758
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881364"
---
# <a name="fabricating-hierarchical-recordsets"></a><span data-ttu-id="7144e-102">階層レコードセットを作成する</span><span class="sxs-lookup"><span data-stu-id="7144e-102">Fabricating Hierarchical Recordsets</span></span>


<span data-ttu-id="7144e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7144e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7144e-104">次の例では、親、子、および孫の **Recordset** の列を定義するデータ シェイプ文法を使用することにより、基になるデータ ソースなしで階層レコードセットを作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="7144e-104">The following example shows how to fabricate a hierarchical Recordset without an underlying data source by using the data shaping grammar to define columns for parent, child, and grandchild **Recordsets**.</span></span>

<span data-ttu-id="7144e-p101">階層 **Recordset** を作成するには、Microsoft Data Shaping Service for OLE DB (MSDataShape) を指定する必要があり、 [Connection](connection-object-ado.md) オブジェクトの [Open](open-method-ado-connection.md) メソッドの接続文字列パラメーターで Data Provider 値に NONE を指定してもかまいません。詳細については、「 [データ シェイプに必要なプロバイダー](required-providers-for-data-shaping.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7144e-p101">To fabricate a hierarchical **Recordset**, you must specify the Microsoft Data Shaping Service for OLE DB (MSDataShape), and you may specify a Data Provider value of NONE in the connection string parameter of the [Connection](connection-object-ado.md) object's [Open](open-method-ado-connection.md) method. For more information, see [Required Providers for Data Shaping](required-providers-for-data-shaping.md).</span></span>

```vb
    Dim cn As New ADODB.Connection
    Dim rsCustomers As New ADODB.Recordset
    
    cn.Open "Provider=MSDataShape;Data Provider=NONE;"
     
    strShape = _
    "SHAPE APPEND NEW adInteger AS CustID," & _
                " NEW adChar(25) AS FirstName," & _
                " NEW adChar(25) AS LastName," & _
                " NEW adChar(12) AS SSN," & _
                " NEW adChar(50) AS Address," & _
             " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                            " NEW adInteger AS CustID," & _
                            " NEW adChar(20) AS BodyColor, " & _
                         " ((SHAPE APPEND NEW adChar(80) AS VIN_NO," & _
                                        " NEW adChar(20) AS Make, " & _
                                        " NEW adChar(20) AS Model," & _
                                        " NEW adChar(4) AS Year) " & _
                            " AS VINS RELATE VIN_NO TO VIN_NO))" & _
                " AS Vehicles RELATE CustID TO CustID) "
     
    rsCustomers.Open strShape, cn, adOpenStatic, adLockOptimistic, -1
```

<span data-ttu-id="7144e-107">後、作成された**レコード セット**で、設定、操作、またはそのファイルに永続化します。</span><span class="sxs-lookup"><span data-stu-id="7144e-107">After the **Recordset** has been fabricated, it can be populated, manipulated, or persisted to a file.</span></span>

