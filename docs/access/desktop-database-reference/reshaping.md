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
# <a name="reshaping"></a><span data-ttu-id="e3c7b-102">リシェイプ</span><span class="sxs-lookup"><span data-stu-id="e3c7b-102">Reshaping</span></span>

<span data-ttu-id="e3c7b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e3c7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e3c7b-104">shape コマンドの句によって作成された**Recordset**には、(通常は as キーワードを使用して)*エイリアス*名を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="e3c7b-104">A **Recordset** created by a clause of a shape command may be assigned an *alias* name (typically with the AS keyword).</span></span> <span data-ttu-id="e3c7b-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span><span class="sxs-lookup"><span data-stu-id="e3c7b-105">The alias of a shaped **Recordset** can be referenced in an entirely different command.</span></span> <span data-ttu-id="e3c7b-106">つまり、新しい shape コマンドで、以前に作成した**Recordset**を再利用したり、*リシェイプ*したりすることができます。</span><span class="sxs-lookup"><span data-stu-id="e3c7b-106">That is, you may reuse, or *reshape*, a previously shaped **Recordset** in a new shape command.</span></span> <span data-ttu-id="e3c7b-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span><span class="sxs-lookup"><span data-stu-id="e3c7b-107">To support this feature, ADO provides a property, [Reshape Name](reshape-name-property-dynamic-ado.md).</span></span>

<span data-ttu-id="e3c7b-p102">リシェイプには 2 つの主要な関数があります。1 つは、既存の **Recordset** を新しい親 **Recordset** に関連付ける関数です。</span><span class="sxs-lookup"><span data-stu-id="e3c7b-p102">Reshaping has two main functions. The first is to associate an existing **Recordset** with a new parent **Recordset**.</span></span>

## <a name="example"></a><span data-ttu-id="e3c7b-110">例</span><span class="sxs-lookup"><span data-stu-id="e3c7b-110">Example</span></span>

```vb 
 
. . . 
rs1.Open "SHAPE {select * from Customers} " & _ 
 "APPEND ({select * from Orders} AS chapOrders " & _ 
 "RELATE CustomerID to CustomerID)", cn 
 
rs2.Open "SHAPE {select * from Employees} " & _ 
 "APPEND (chapOrders RELATE EmployeeID to EmployeeID)", cn 
. . . 
```

<span data-ttu-id="e3c7b-111">2番目の関数は、構文`"SHAPE <recordset reshape name>"`を使用して、既存の子**Recordset**オブジェクトへのチャプター化されていないアクセスを可能にすることです。</span><span class="sxs-lookup"><span data-stu-id="e3c7b-111">The second function is to enable non-chaptered access to existing child **Recordset** objects, using the syntax `"SHAPE <recordset reshape name>"`.</span></span>

> [!NOTE]
> <span data-ttu-id="e3c7b-112">[!メモ] 既存の **Recordset** に列を追加したり、パラメーター化された **Recordset** または挿入 COMPUTE 句内の **Recordset** オブジェクトをリシェイプしたり、リシェイプされる **Recordset** からの子孫の **Recordset** に集計操作を実行したりすることはできません。</span><span class="sxs-lookup"><span data-stu-id="e3c7b-112">You cannot append columns to an existing **Recordset**, reshape a parameterized **Recordset** or the **Recordset** objects in any intervening COMPUTE clause, or perform aggregate operations on any **Recordset** descendant from the **Recordset** being reshaped.</span></span> <span data-ttu-id="e3c7b-113">リシェイプする**Recordset**と新しい shape コマンドは、両方とも同じ \* \*[Connection](connection-object-ado.md)オブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3c7b-113">The **Recordset** being reshaped and the new shape command must both use the same \*\*[Connection](connection-object-ado.md) object.</span></span>


