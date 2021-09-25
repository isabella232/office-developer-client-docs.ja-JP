---
title: Resync Command 動的プロパティ (ADO)
TOCTitle: Resync Command dynamic property (ADO)
ms:assetid: 5c0c0819-620a-6eb0-a217-69113ec8d094
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249322(v=office.15)
ms:contentKeyID: 48545081
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 70060c626754e5b81d8c1cfbee003523c983bdbc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576920"
---
# <a name="resync-command-dynamic-property-ado"></a>Resync Command 動的プロパティ (ADO)

**適用先:** Access 2013、Office 2013

[Unique Table](resync-method-ado.md) 動的プロパティに指定されているテーブルのデータを更新するために [Resync](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) メソッドが発行する、ユーザー指定のコマンド文字列を指定します。

## <a name="settings-and-return-values"></a>設定および戻り値

コマンド文字列である文字列型 (**String**) の値を設定または取得します。

## <a name="remarks"></a>注釈

[Recordset](recordset-object-ado.md) オブジェクトは、複数のベース テーブルに対して実行される JOIN 操作の結果です。影響を受ける行は、[Resync](resync-method-ado.md) メソッドの *AffectRecords* パラメーターによって異なります。[Unique Table](unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md) プロパティと **Resync Command** プロパティが設定されていない場合は、標準の **Resync** メソッドが実行されます。

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

**Resync Command** は、[CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定するときに、**Recordset** オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加される動的プロパティです。

