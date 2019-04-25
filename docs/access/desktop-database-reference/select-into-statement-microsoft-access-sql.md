---
title: SELECT.INTO ステートメント (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fd7152eaa7dd29f6d0bf5621d1b8b8b6f648673c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308723"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="1e466-102">SELECT.INTO ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1e466-102">SELECT…INTO Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="1e466-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e466-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e466-104">テーブル作成クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="1e466-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e466-105">構文</span><span class="sxs-lookup"><span data-stu-id="1e466-105">Syntax</span></span>

<span data-ttu-id="1e466-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span><span class="sxs-lookup"><span data-stu-id="1e466-106">SELECT field1[, field2[, …]] INTO newtable [IN externaldatabase]
    FROM source</span></span>

<span data-ttu-id="1e466-107">SELECT...INTO ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="1e466-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e466-108">パーツ</span><span class="sxs-lookup"><span data-stu-id="1e466-108">Part</span></span></p></th>
<th><p><span data-ttu-id="1e466-109">説明</span><span class="sxs-lookup"><span data-stu-id="1e466-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e466-110"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="1e466-110"><em>field1</em>  ,  <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="1e466-111">新しいテーブルにコピーするフィールドの名前です。</span><span class="sxs-lookup"><span data-stu-id="1e466-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e466-112"><em>newtable</em></span><span class="sxs-lookup"><span data-stu-id="1e466-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="1e466-p101">作成するテーブルの名前。名前付け規則に従った名前を指定します。引数 <em>newtable</em> と同じ名前のテーブルが既にある場合は、トラップ可能なエラーになります。</span><span class="sxs-lookup"><span data-stu-id="1e466-p101">The name of the table to be created. It must conform to standard naming conventions. If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e466-116"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="1e466-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="1e466-p102">外部データベースのパス。パスの記述方法については、「<a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN 句</a>」を参照してください。  </span><span class="sxs-lookup"><span data-stu-id="1e466-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e466-119"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="1e466-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="1e466-120">レコードの選択元になる既存テーブルの名前です。</span><span class="sxs-lookup"><span data-stu-id="1e466-120">The name of the existing table from which records are selected.</span></span> <span data-ttu-id="1e466-121">このテーブルまたはクエリは 1 つでも複数でも構いません。</span><span class="sxs-lookup"><span data-stu-id="1e466-121">This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1e466-122">注釈</span><span class="sxs-lookup"><span data-stu-id="1e466-122">Remarks</span></span>

<span data-ttu-id="1e466-p104">テーブル作成クエリを使用し、レコードをアーカイブしたり、テーブルのバックアップ コピーを作成したり、別のデータベースにエクスポートするか、データを一定期間表示するレポートの基礎として利用するためのコピーを作成したりできます。たとえば、同じテーブル作成クエリを毎月実行し、地域別の月間売上レポートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="1e466-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="1e466-p105">新規テーブルに主キーを設定する場合があります。テーブル作成クエリで作成したテーブルのフィールドは、クエリの元になるテーブルのフィールドのデータ型とフィールド サイズを継承しますが、それ以外のフィールド プロパティやテーブル プロパティは継承しません。</span><span class="sxs-lookup"><span data-stu-id="1e466-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="1e466-127">既存のテーブルにデータを追加するには、SELECT...INTO ステートメントではなく [INSERT INTO](insert-into-statement-microsoft-access-sql.md) ステートメントを使用して追加クエリを作成してください。</span><span class="sxs-lookup"><span data-stu-id="1e466-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="1e466-128">どのレコードが選択されるかをあらかじめ確認する場合は、テーブル作成クエリを実行する前に、同じ選択条件を使用する [SELECT](select-statement-microsoft-access-sql.md) ステートメントを実行してその結果を調べてください。</span><span class="sxs-lookup"><span data-stu-id="1e466-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="1e466-129">例</span><span class="sxs-lookup"><span data-stu-id="1e466-129">Example</span></span>

<span data-ttu-id="1e466-130">この例では、Employees テーブル内のすべてのレコードを選択し、それらを Emp Backup という名前の新しいテーブルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1e466-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

```vb
    Sub SelectIntoX() 
     
        Dim dbs As Database 
        Dim qdf As QueryDef 
     
        ' Modify this line to include the path to Northwind 
        ' on your computer. 
        Set dbs = OpenDatabase("Northwind.mdb") 
     
        ' Select all records in the Employees table  
        ' and copy them into a new table, Emp Backup. 
        dbs.Execute "SELECT Employees.* INTO " _ 
            & "[Emp Backup] FROM Employees;" 
             
        ' Delete the table because this is a demonstration. 
        dbs.Execute "DROP TABLE [Emp Backup];" 
         
        dbs.Close 
     
    End Sub
```
