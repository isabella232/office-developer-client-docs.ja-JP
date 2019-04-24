---
title: リシェイプ (Access デスクトップデータベースリファレンス)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314778"
---
# <a name="reshaping"></a>リシェイプ

**適用先:** Access 2013、Office 2013

shape コマンドの句によって作成された**Recordset**には、(通常は as キーワードを使用して)*エイリアス*名を割り当てることができます。 The alias of a shaped **Recordset** can be referenced in an entirely different command. つまり、新しい shape コマンドで、以前に作成した**Recordset**を再利用したり、*リシェイプ*したりすることができます。 To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).

リシェイプには 2 つの主要な関数があります。1 つは、既存の **Recordset** を新しい親 **Recordset** に関連付ける関数です。

## <a name="example"></a>例

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

2番目の関数は、構文`"SHAPE <recordset reshape name>"`を使用して、既存の子**Recordset**オブジェクトへのチャプター化されていないアクセスを可能にすることです。

> [!NOTE]
> [!メモ] 既存の **Recordset** に列を追加したり、パラメーター化された **Recordset** または挿入 COMPUTE 句内の **Recordset** オブジェクトをリシェイプしたり、リシェイプされる **Recordset** からの子孫の **Recordset** に集計操作を実行したりすることはできません。 リシェイプする**Recordset**と新しい shape コマンドは、両方とも同じ * *[Connection](connection-object-ado.md)オブジェクトを使用する必要があります。


