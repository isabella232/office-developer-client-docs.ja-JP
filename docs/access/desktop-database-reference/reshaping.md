---
title: リシェーピング (Access デスクトップ データベースリファレンス)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: af282f86f75d6208be19ab7c8b491dfd8b17dc92
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557821"
---
# <a name="reshaping"></a>リシェイプ

**適用先:** Access 2013、Office 2013

shape **コマンドの** 句によって作成された Recordset には、エイリアス名 (通常は AS キーワード) を割り当てることができます。 The alias of a shaped **Recordset** can be referenced in an entirely different command. つまり、新しい図形コマンドで、以前に形成された **Recordset** を再利用したり、形を変更したりすることができます。 To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).

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

2 番目の関数は、構文を使用して、既存の子 **Recordset** オブジェクトへのチャプター化されていないアクセスを有効にします `"SHAPE <recordset reshape name>"` 。

> [!NOTE]
> [!メモ] 既存の **Recordset** に列を追加したり、パラメーター化された **Recordset** または挿入 COMPUTE 句内の **Recordset** オブジェクトをリシェイプしたり、リシェイプされる **Recordset** からの子孫の **Recordset** に集計操作を実行したりすることはできません。 形状 **を変更** する Recordset コマンドと新しい図形コマンドは、両方とも同じ ** Connection オブジェクトを [使用する必要](connection-object-ado.md) があります。


