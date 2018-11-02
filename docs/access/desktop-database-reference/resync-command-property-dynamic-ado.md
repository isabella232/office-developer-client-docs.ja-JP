---
title: コマンドの動的なプロパティ (ADO) の再同期します。
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 23d03c5c346b377333387a3be1c0f15bc091d235
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927943"
---
# <a name="resync-command-dynamic-property-ado"></a>コマンドの動的なプロパティ (ADO) の再同期します。

**適用されます**Access 2013、Office 2013。

[Unique Table](resync-method-ado.md) 動的プロパティに指定されているテーブルのデータを更新するために [Resync](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) メソッドが発行する、ユーザー指定のコマンド文字列を指定します。

## <a name="settings-and-return-values"></a>設定値および戻り値

コマンド文字列である文字列型 ( **String** ) の値を設定または取得します。

## <a name="remarks"></a>解説

[Recordset](recordset-object-ado.md) オブジェクトは、複数のベース テーブルに対して実行される JOIN 操作の結果です。 影響を受ける行は、 [Resync](resync-method-ado.md)メソッドの*AffectRecords*パラメーターに依存します。 **Unique Table** プロパティと [Resync Command](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) プロパティが設定されていない場合は、標準の **Resync** メソッドが実行されます。

**Resync Command** プロパティのコマンド文字列は、更新される行を一意に識別し、更新される行と同じ数および順序の列を含む 1 行を返す、パラメーター化されたコマンドまたはストアド プロシージャです。このコマンド文字列は、 **Unique Table** の各主キー列のパラメーターを格納します。パラメーターを指定しないと実行時エラーになります。パラメーターには、更新される行の主キーの値が自動的に設定されます。

次に SQL の例を 2 つ示します。

1.  **Recordset** がコマンドによって定義されている場合

    ```sql
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE city = Seattle
        ORDER BY CustomerID
    ```

    **Resync Command** プロパティは次のように設定されます。

    ```sql
     SELECT * FROM 
        (SELECT * FROM Customers JOIN Orders 
        ON Customers.CustomerID = Orders.CustomerID
        city = Seattle ORDER BY CustomerID)
     WHERE Orders.OrderID = ?"
    ```

    **Unique Table** は *Orders* であり、その主キー *OrderID*  はパラメーター化されています。SELECT 文中の SELECT 文では、元のコマンドが返すのと同じ数および順序の列をプログラムで簡易に実現しています。

2. **Recordset** がストアド プロシージャによって定義されている場合

    ```sql
        CREATE PROC Custorders @CustomerID char(5) AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID 
        WHERE Customers.CustomerID = @CustomerID
    ```

    **Resync** メソッドで次のストアド プロシージャを実行します。

    ```sql
        CREATE PROC CustordersResync @ordid int AS 
        SELECT * FROM Customers JOIN Orders ON 
        Customers.CustomerID = Orders.CustomerID
        WHERE Orders.ordid  = @ordid
    ```

    **Resync Command** プロパティは次のように設定されます。

    `"{call CustordersResync (?)}"`

ここでも、**Unique Table** は *Orders* であり、その主キー *OrderID* はパラメーター化されています。

**Resync Command** は、 **CursorLocation** プロパティを [adUseClient](properties-collection-ado.md) に設定するときに、 [Recordset](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加される動的プロパティです。

