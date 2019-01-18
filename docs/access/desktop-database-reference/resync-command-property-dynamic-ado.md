---
title: コマンドの動的なプロパティ (ADO) の再同期します。
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa1fe05e6aa7edf04ad74864eb30a03403323c8e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713332"
---
# <a name="resync-command-dynamic-property-ado"></a><span data-ttu-id="cf846-102">コマンドの動的なプロパティ (ADO) の再同期します。</span><span class="sxs-lookup"><span data-stu-id="cf846-102">Resync Command dynamic property (ADO)</span></span>

<span data-ttu-id="cf846-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cf846-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cf846-104">[Unique Table](resync-method-ado.md) 動的プロパティに指定されているテーブルのデータを更新するために [Resync](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) メソッドが発行する、ユーザー指定のコマンド文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf846-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cf846-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="cf846-105">Settings and return values</span></span>

<span data-ttu-id="cf846-106">コマンド文字列である文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="cf846-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf846-107">解説</span><span class="sxs-lookup"><span data-stu-id="cf846-107">Remarks</span></span>

<span data-ttu-id="cf846-108">[Recordset](recordset-object-ado.md) オブジェクトは、複数のベース テーブルに対して実行される JOIN 操作の結果です。</span><span class="sxs-lookup"><span data-stu-id="cf846-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="cf846-109">影響を受ける行は、 [Resync](resync-method-ado.md)メソッドの*AffectRecords*パラメーターに依存します。</span><span class="sxs-lookup"><span data-stu-id="cf846-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="cf846-110">**Unique Table** プロパティと [Resync Command](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) プロパティが設定されていない場合は、標準の **Resync** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="cf846-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="cf846-p102">**Resync Command** プロパティのコマンド文字列は、更新される行を一意に識別し、更新される行と同じ数および順序の列を含む 1 行を返す、パラメーター化されたコマンドまたはストアド プロシージャです。このコマンド文字列は、 **Unique Table** の各主キー列のパラメーターを格納します。パラメーターを指定しないと実行時エラーになります。パラメーターには、更新される行の主キーの値が自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="cf846-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="cf846-114">次に SQL の例を 2 つ示します。</span><span class="sxs-lookup"><span data-stu-id="cf846-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="cf846-115">**Recordset** がコマンドによって定義されている場合</span><span class="sxs-lookup"><span data-stu-id="cf846-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="cf846-116">**Resync Command** プロパティは次のように設定されます。</span><span class="sxs-lookup"><span data-stu-id="cf846-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="cf846-p103">**Unique Table** は *Orders* であり、その主キー *OrderID*  はパラメーター化されています。SELECT 文中の SELECT 文では、元のコマンドが返すのと同じ数および順序の列をプログラムで簡易に実現しています。</span><span class="sxs-lookup"><span data-stu-id="cf846-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="cf846-119">**Recordset** がストアド プロシージャによって定義されている場合</span><span class="sxs-lookup"><span data-stu-id="cf846-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="cf846-120">**Resync** メソッドで次のストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="cf846-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="cf846-121">**Resync Command** プロパティは次のように設定されます。</span><span class="sxs-lookup"><span data-stu-id="cf846-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="cf846-122">ここでも、**Unique Table** は *Orders* であり、その主キー *OrderID* はパラメーター化されています。</span><span class="sxs-lookup"><span data-stu-id="cf846-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="cf846-123">**Resync Command** は、 **CursorLocation** プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。</span><span class="sxs-lookup"><span data-stu-id="cf846-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>

