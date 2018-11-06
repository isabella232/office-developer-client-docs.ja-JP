---
title: 調整 (アクセスのデスクトップ データベースの参照)
TOCTitle: Reshaping
ms:assetid: 89c6a0d6-3bf4-36ae-26ec-d4e60f920490
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249605(v=office.15)
ms:contentKeyID: 48546174
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 49a61e72a4d9260b73275d84ce912ebc76f37652
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996455"
---
# <a name="reshaping"></a><span data-ttu-id="5ac1c-102">リシェイプ</span><span class="sxs-lookup"><span data-stu-id="5ac1c-102">Reshaping</span></span>

<span data-ttu-id="5ac1c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5ac1c-104">Shape コマンド句によって作成された**レコード セット**には、(通常は AS キーワードを使って*エイリアス*名を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-104">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword).</span></span> <span data-ttu-id="5ac1c-105">シェイプされた**Recordset**の別名は、まったく異なるコマンドで参照できます。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span></span> <span data-ttu-id="5ac1c-106">次のように再び使うことが、または*形状を変更*、新しい shape コマンドの前に立てられていた**レコード セット**です。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-106">That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command.</span></span> <span data-ttu-id="5ac1c-107">この機能をサポートするためには、ADO は、[形状の名前](reshape-name-property-dynamic-ado.md)プロパティを提供します。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="5ac1c-p102">リシェイプには 2 つの主要な関数があります。1 つは、既存の **Recordset** を新しい親 **Recordset** に関連付ける関数です。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="5ac1c-110">例</span><span class="sxs-lookup"><span data-stu-id="5ac1c-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="5ac1c-111">2 番目の関数は、構文を使用して、既存の子**Recordset**オブジェクトへのチャプター化されていないアクセスを有効にするのには`"SHAPE <recordset reshape name>"`です。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="5ac1c-112">[!メモ] 既存の **Recordset** に列を追加したり、パラメーター化された **Recordset** または挿入 COMPUTE 句内の **Recordset** オブジェクトをリシェイプしたり、リシェイプされる **Recordset** からの子孫の **Recordset** に集計操作を実行したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="5ac1c-113">形状が変更されている**レコード セット**と新しい図形コマンドを使う必要があります両方とも同じ \* \*[接続](connection-object-ado.md)オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="5ac1c-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


