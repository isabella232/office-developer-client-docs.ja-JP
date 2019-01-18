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
# <a name="reshaping"></a><span data-ttu-id="c530b-102">リシェイプ</span><span class="sxs-lookup"><span data-stu-id="c530b-102">Reshaping</span></span>

<span data-ttu-id="c530b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="c530b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c530b-104">Shape コマンド句によって作成された**レコード セット**には、(通常は AS キーワードを使って*エイリアス*名を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="c530b-104">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword).</span></span> <span data-ttu-id="c530b-105">シェイプされた**Recordset**の別名は、まったく異なるコマンドで参照できます。</span><span class="sxs-lookup"><span data-stu-id="c530b-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span></span> <span data-ttu-id="c530b-106">次のように再び使うことが、または*形状を変更*、新しい shape コマンドの前に立てられていた**レコード セット**です。</span><span class="sxs-lookup"><span data-stu-id="c530b-106">That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command.</span></span> <span data-ttu-id="c530b-107">この機能をサポートするためには、ADO は、[形状の名前](reshape-name-property-dynamic-ado.md)プロパティを提供します。</span><span class="sxs-lookup"><span data-stu-id="c530b-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="c530b-p102">リシェイプには 2 つの主要な関数があります。1 つは、既存の **Recordset** を新しい親 **Recordset** に関連付ける関数です。</span><span class="sxs-lookup"><span data-stu-id="c530b-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="c530b-110">例</span><span class="sxs-lookup"><span data-stu-id="c530b-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="c530b-111">2 番目の関数は、構文を使用して、既存の子**Recordset**オブジェクトへのチャプター化されていないアクセスを有効にするのには`"SHAPE <recordset reshape name>"`です。</span><span class="sxs-lookup"><span data-stu-id="c530b-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="c530b-112">[!メモ] 既存の **Recordset** に列を追加したり、パラメーター化された **Recordset** または挿入 COMPUTE 句内の **Recordset** オブジェクトをリシェイプしたり、リシェイプされる **Recordset** からの子孫の **Recordset** に集計操作を実行したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="c530b-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="c530b-113">形状が変更されている**レコード セット**と新しい図形コマンドを使う必要があります両方とも同じ \* \*[接続](connection-object-ado.md)オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="c530b-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


