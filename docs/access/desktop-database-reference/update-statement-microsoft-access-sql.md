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
ms.openlocfilehash: 4e7f27cb696b085b5c4536477ee3454df09cfabe
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881287"
---
# <a name="update-statement-microsoft-access-sql"></a>UPDATE ステートメント (Microsoft Access SQL)

**適用されます**Access 2013、Office 2013。

指定したテーブルのフィールドの値を指定の抽出条件に従って変更する更新クエリを作成します。

## <a name="syntax"></a>構文

更新*テーブル*セットの*新しい値**条件*です。

UPDATE ステートメントには、次の指定項目があります。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>指定項目</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>table</em></p></td>
<td><p>変更するデータのあるテーブルの名前。</p></td>
</tr>
<tr class="even">
<td><p><em>newvalue</em></p></td>
<td><p>更新後のレコードの特定のフィールドに挿入する値を決めるための式。</p></td>
</tr>
<tr class="odd">
<td><p><em>criteria</em></p></td>
<td><p>更新するレコードを抽出するための式。この式の条件を満たすレコードのみが更新されます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

UPDATE ステートメントは、多数のレコードを変更する場合や、変更するレコードが複数のテーブルに含まれている場合に特に便利です。

UPDATE ステートメントでは、複数のフィールドを同時に変更できます。次の例では、輸送先が英国であるレコードの Order Amount フィールドの値を 10%、Freight フィールドの値を 3%、それぞれ増やしています。

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- UPDATE ステートメントは、結果セットを作成しません。また、更新クエリを使用してレコードを更新すると、元に戻せません。どのレコードが変更されるかをあらかじめ確認する場合は、更新クエリを実行する前に、同じ抽出条件を使用する選択クエリを実行してその結果を調べてください。
- 誤ってレコードを更新した場合にも復旧できるように、常にデータのバックアップ コピーを作成しておくことをお勧めします。



## <a name="example"></a>使用例

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
