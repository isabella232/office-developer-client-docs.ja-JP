---
title: 階層レコードセットの生成
TOCTitle: Fabricating hierarchical Recordsets
ms:assetid: 0a6e41ba-015e-c07e-8876-1e744256b876
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248836(v=office.15)
ms:contentKeyID: 48543153
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f644f25a04c5573a93aa106884473fed6b45440e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293204"
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

作成された**Recordset**は、ファイルに設定、操作、または永続化することができます。

