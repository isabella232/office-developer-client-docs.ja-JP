---
title: Resync Command プロパティ -- 動的 (ADO)
TOCTitle: Resync Command Property--Dynamic (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8fc64a51044f219d4daae44a9c684506cd7bd5c6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477132"
---
# <a name="resync-command-property--dynamic-ado"></a><span data-ttu-id="fdb69-102">Resync Command プロパティ -- 動的 (ADO)</span><span class="sxs-lookup"><span data-stu-id="fdb69-102">Resync Command Property--Dynamic (ADO)</span></span>

<span data-ttu-id="fdb69-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdb69-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fdb69-104">[Unique Table](resync-method-ado.md) 動的プロパティに指定されているテーブルのデータを更新するために [Resync](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) メソッドが発行する、ユーザー指定のコマンド文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="fdb69-104">Specifies a user-supplied command string that the [Resync](resync-method-ado.md) method issues to refresh the data in the table named in the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) dynamic property.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="fdb69-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="fdb69-105">Settings and Return Values</span></span>

<span data-ttu-id="fdb69-106">コマンド文字列である文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="fdb69-106">Sets or returns a **String** value which is a command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdb69-107">解説</span><span class="sxs-lookup"><span data-stu-id="fdb69-107">Remarks</span></span>

<span data-ttu-id="fdb69-108">[Recordset](recordset-object-ado.md) オブジェクトは、複数のベース テーブルに対して実行される JOIN 操作の結果です。</span><span class="sxs-lookup"><span data-stu-id="fdb69-108">The [Recordset](recordset-object-ado.md) object is the result of a JOIN operation executed on multiple base tables.</span></span> <span data-ttu-id="fdb69-109">影響を受ける行は、 [Resync](resync-method-ado.md)メソッドの*AffectRecords*パラメーターに依存します。</span><span class="sxs-lookup"><span data-stu-id="fdb69-109">The rows affected depend on the *AffectRecords* parameter of the [Resync](resync-method-ado.md) method.</span></span> <span data-ttu-id="fdb69-110">**Unique Table** プロパティと [Resync Command](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) プロパティが設定されていない場合は、標準の **Resync** メソッドが実行されます。</span><span class="sxs-lookup"><span data-stu-id="fdb69-110">The standard **Resync** method is executed if the [Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) and **Resync Command** properties are not set.</span></span>

<span data-ttu-id="fdb69-p102">**Resync Command** プロパティのコマンド文字列は、更新される行を一意に識別し、更新される行と同じ数および順序の列を含む 1 行を返す、パラメーター化されたコマンドまたはストアド プロシージャです。このコマンド文字列は、 **Unique Table** の各主キー列のパラメーターを格納します。パラメーターを指定しないと実行時エラーになります。パラメーターには、更新される行の主キーの値が自動的に設定されます。</span><span class="sxs-lookup"><span data-stu-id="fdb69-p102">The command string of the **Resync Command** property is a parameterized command or stored procedure that uniquely identifies the row being refreshed, and returns a single row containing the same number and order of columns as the row to be refreshed. The command string contains a parameter for each primary key column in the **Unique Table**; otherwise, a run-time error is returned. The parameters are automatically filled in with primary key values from the row to be refreshed.</span></span>

<span data-ttu-id="fdb69-114">次に SQL の例を 2 つ示します。</span><span class="sxs-lookup"><span data-stu-id="fdb69-114">Here are two examples based on SQL:</span></span>

1.  <span data-ttu-id="fdb69-115">**Recordset** がコマンドによって定義されている場合</span><span class="sxs-lookup"><span data-stu-id="fdb69-115">The **Recordset** is defined by a command:</span></span>

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    <span data-ttu-id="fdb69-116">**Resync Command** プロパティは次のように設定されます。</span><span class="sxs-lookup"><span data-stu-id="fdb69-116">The **Resync Command** property is set to:</span></span>

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    <span data-ttu-id="fdb69-p103">**Unique Table** は *Orders* であり、その主キー *OrderID*  はパラメーター化されています。SELECT 文中の SELECT 文では、元のコマンドが返すのと同じ数および順序の列をプログラムで簡易に実現しています。</span><span class="sxs-lookup"><span data-stu-id="fdb69-p103">The **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized. The sub-select provides a simple way to programmatically ensure that the same number and order of columns are returned as by the original command.</span></span>

2. <span data-ttu-id="fdb69-119">**Recordset** がストアド プロシージャによって定義されている場合</span><span class="sxs-lookup"><span data-stu-id="fdb69-119">The **Recordset** is defined by a stored procedure:</span></span>

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    <span data-ttu-id="fdb69-120">**Resync** メソッドで次のストアド プロシージャを実行します。</span><span class="sxs-lookup"><span data-stu-id="fdb69-120">The **Resync** method should execute the following stored procedure:</span></span>

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    <span data-ttu-id="fdb69-121">**Resync Command** プロパティは次のように設定されます。</span><span class="sxs-lookup"><span data-stu-id="fdb69-121">The **Resync Command** property is set to:</span></span>

    `"{call CustordersResync (?)}"`

<span data-ttu-id="fdb69-122">ここでも、**Unique Table** は *Orders* であり、その主キー *OrderID* はパラメーター化されています。</span><span class="sxs-lookup"><span data-stu-id="fdb69-122">Once again, the **Unique Table** is *Orders* and its primary key, *OrderID*, is parameterized.</span></span>

<span data-ttu-id="fdb69-123">**Resync Command** は、 **CursorLocation** プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。</span><span class="sxs-lookup"><span data-stu-id="fdb69-123">**Resync Command** is a dynamic property appended to the **Recordset** object [Properties](properties-collection-ado.md) collection when the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**.</span></span>
