---
title: 階層レコードセットの生成
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2cf3af43e288fc95bc7a8b21f90955f1061ac050
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552963"
---
# <a name="fabricating-hierarchical-recordsets"></a>階層レコードセットの生成


**適用先:** Access 2013、Office 2013

次の例では、親、子、および孫の **Recordset** の列を定義するデータ シェイプ文法を使用することにより、基になるデータ ソースなしで階層レコードセットを作成する方法を示します。

階層 **Recordset** を作成するには、Microsoft Data Shaping Service for OLE DB (MSDataShape) を指定する必要があり、 [Connection](connection-object-ado.md) オブジェクトの [Open](open-method-ado-connection.md) メソッドの接続文字列パラメーターで Data Provider 値に NONE を指定してもかまいません。詳細については、「 [データ シェイプに必要なプロバイダー](required-providers-for-data-shaping.md)」を参照してください。

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

Recordset が **作成** された後は、ファイルにデータを取り込み、操作、または永続化できます。

