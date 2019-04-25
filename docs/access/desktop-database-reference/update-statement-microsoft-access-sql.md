---
title: UPDATE ステートメント (Microsoft Access SQL)
TOCTitle: UPDATE statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 10/18/2018
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 6a0404c21b308f6e389ee5577cc212763e660774
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306245"
---
# <a name="update-statement-microsoft-access-sql"></a>UPDATE ステートメント (Microsoft Access SQL)

**適用先**: Access 2013、Office 2013

指定したテーブルのフィールドの値を指定の抽出条件に従って変更する更新クエリを作成します。

## <a name="syntax"></a>構文

UPDATE *table* SET *newvalue* WHERE *criteria*;

UPDATE ステートメントでは次の引数を使用します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>パーツ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>変更するデータを含むテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>newvalue</em></p></td>
<td><p>更新後のレコードの特定のフィールドに挿入する値を決めるための式です。</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>レコードを更新するか決めるための式です。式の条件を満たすレコードのみが更新されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

UPDATE は、多数のレコードを変更する場合や、変更するレコードが複数のテーブルに含まれている場合に特に便利です。

複数のフィールドを同時に変更することができます。次に示すのは、"受注金額" の値が 10% ずつ、"運送料" の値が 3% ずつ増えている英国の運送会社の例です。

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- UPDATE ステートメントは、結果セットを作成しません。また、更新クエリを使用してレコードを更新すると、元に戻せません。どのレコードが変更されるかをあらかじめ確認する場合は、更新クエリを実行する前に、同じ抽出条件を使用する選択クエリを実行してその結果を調べてください。
- データのバックアップ コピーを常に維持してください。 間違ったレコードを更新した場合、バックアップ コピーからレコードを元に戻すことができます。



## <a name="example"></a>例

この使用例では、現在 ReportsTo の値が 2 であるすべての従業員レコードについて、ReportsTo フィールドの値を 5 に変更します。

```vb
    Sub UpdateX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
         
        ' Change values in the ReportsTo field to 5 for all  
        ' employee records that currently have ReportsTo  
        ' values of 2. 
        dbs.Execute "UPDATE Employees " _ 
            & "SET ReportsTo = 5 " _ 
            & "WHERE ReportsTo = 2;" 
             
        dbs.Close 
     
    End Sub
```
