---
title: 調整 (アクセスのデスクトップ データベースの参照)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c820e82669789d7c3806cc1fd38a2eb6844b722e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711904"
---
# <a name="reshaping"></a>リシェイプ

**適用されます**Access 2013、Office 2013。

Shape コマンド句によって作成された**レコード セット**には、(通常は AS キーワードを使って*エイリアス*名を割り当てることができます。 シェイプされた**Recordset**の別名は、まったく異なるコマンドで参照できます。 次のように再び使うことが、または*形状を変更*、新しい shape コマンドの前に立てられていた**レコード セット**です。 この機能をサポートするためには、ADO は、[形状の名前](reshape-name-property-dynamic-ado.md)プロパティを提供します。

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

2 番目の関数は、構文を使用して、既存の子**Recordset**オブジェクトへのチャプター化されていないアクセスを有効にするのには`"SHAPE <recordset reshape name>"`です。

> [!NOTE]
> [!メモ] 既存の **Recordset** に列を追加したり、パラメーター化された **Recordset** または挿入 COMPUTE 句内の **Recordset** オブジェクトをリシェイプしたり、リシェイプされる **Recordset** からの子孫の **Recordset** に集計操作を実行したりすることはできません。 形状が変更されている**レコード セット**と新しい図形コマンドを使う必要があります両方とも同じ * *[接続](connection-object-ado.md)オブジェクトです。


