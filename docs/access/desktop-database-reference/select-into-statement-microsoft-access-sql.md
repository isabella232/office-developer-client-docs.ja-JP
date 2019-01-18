---
title: 選択します。INTO ステートメント (Microsoft Access SQL)
TOCTitle: SELECT.INTO statement (Microsoft Access SQL)
ms:assetid: 29f3bd55-52f5-a36e-4e33-4b3499c6ce8d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192059(v=office.15)
ms:contentKeyID: 48543897
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: fd7152eaa7dd29f6d0bf5621d1b8b8b6f648673c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28705499"
---
# <a name="selectinto-statement-microsoft-access-sql"></a><span data-ttu-id="1ac97-102">選択します。INTO ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="1ac97-102">SELECT.INTO statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="1ac97-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="1ac97-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1ac97-104">テーブル作成クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="1ac97-104">Creates a make-table query.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac97-105">構文</span><span class="sxs-lookup"><span data-stu-id="1ac97-105">Syntax</span></span>

<span data-ttu-id="1ac97-106">[ *Field1]*\[、*フィールド 2*\[をしています.\] \]に*新しい* \[ *externaldatabase*で\]*のソース*から</span><span class="sxs-lookup"><span data-stu-id="1ac97-106">SELECT *field1*\[, *field2*\[, …\]\] INTO *newtable* \[IN *externaldatabase*\] FROM *source*</span></span>

<span data-ttu-id="1ac97-107">SELECT...INTO ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="1ac97-107">The SELECT…INTO statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ac97-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="1ac97-108">Part</span></span></p></th>
<th><p><span data-ttu-id="1ac97-109">説明</span><span class="sxs-lookup"><span data-stu-id="1ac97-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ac97-110"><em>field1</em>、<em>field2</em></span><span class="sxs-lookup"><span data-stu-id="1ac97-110"><em>field1</em>, <em>field2</em></span></span></p></td>
<td><p><span data-ttu-id="1ac97-111">新しいテーブルにコピーするフィールドの名前。</span><span class="sxs-lookup"><span data-stu-id="1ac97-111">The name of the fields to be copied into the new table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac97-112"><em>newtable</em></span><span class="sxs-lookup"><span data-stu-id="1ac97-112"><em>newtable</em></span></span></p></td>
<td><p><span data-ttu-id="1ac97-p101">作成するテーブルの名前。名前付け規則に従った名前を指定します。引数 <em>newtable</em> と同じ名前のテーブルが既にある場合は、トラップ可能なエラーになります。</span><span class="sxs-lookup"><span data-stu-id="1ac97-p101">The name of the table to be created. It must conform to standard naming conventions. If <em>newtable</em> is the same as the name of an existing table, a trappable error occurs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1ac97-116"><em>externaldatabase</em></span><span class="sxs-lookup"><span data-stu-id="1ac97-116"><em>externaldatabase</em></span></span></p></td>
<td><p><span data-ttu-id="1ac97-p102">外部データベースのパス。パスの記述方法については、「<a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN 句</a>」を参照してください。  </span><span class="sxs-lookup"><span data-stu-id="1ac97-p102">The path to an external database. For a description of the path, see the <a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/in-clause-microsoft-access-sql">IN</a> clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1ac97-119"><em>source</em></span><span class="sxs-lookup"><span data-stu-id="1ac97-119"><em>source</em></span></span></p></td>
<td><p><span data-ttu-id="1ac97-p103">選択するレコードのある既存のテーブルの名前。単一のテーブル名、複数のテーブル名、またはクエリ名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="1ac97-p103">The name of the existing table from which records are selected. This can be single or multiple tables or a query.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="1ac97-122">解説</span><span class="sxs-lookup"><span data-stu-id="1ac97-122">Remarks</span></span>

<span data-ttu-id="1ac97-p104">テーブル作成クエリは、レコードのアーカイブやテーブルのバックアップ コピーの作成に使用できます。また、別のデータベースへエクスポートするコピーを作成する場合や、一定期間のデータを表示するレポートを作成する場合などにも使用できます。たとえば、地域別月間売上レポートを作成する場合は、毎月同じテーブル作成クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="1ac97-p104">You can use make-table queries to archive records, make backup copies of your tables, or make copies to export to another database or to use as a basis for reports that display data for a particular time period. For example, you could produce a Monthly Sales by Region report by running the same make-table query each month.</span></span>

> [!NOTE]
> - <span data-ttu-id="1ac97-p105">新規テーブルに主キーを設定する場合があります。テーブル作成クエリで作成したテーブルのフィールドは、クエリの元になるテーブルのフィールドのデータ型とフィールド サイズを継承しますが、それ以外のフィールド プロパティやテーブル プロパティは継承しません。</span><span class="sxs-lookup"><span data-stu-id="1ac97-p105">You may want to define a primary key for the new table. When you create the table, the fields in the new table inherit the data type and field size of each field in the query's underlying tables, but no other field or table properties are transferred.</span></span>
> - <span data-ttu-id="1ac97-127">既存のテーブルにデータを追加するには、SELECT...INTO ステートメントではなく [INSERT INTO](insert-into-statement-microsoft-access-sql.md) ステートメントを使用して追加クエリを作成してください。</span><span class="sxs-lookup"><span data-stu-id="1ac97-127">To add data to an existing table, use the [INSERT INTO](insert-into-statement-microsoft-access-sql.md) statement instead to create an append query.</span></span>
> - <span data-ttu-id="1ac97-128">どのレコードが選択されるかをあらかじめ確認する場合は、テーブル作成クエリを実行する前に、同じ選択条件を使用する [SELECT](select-statement-microsoft-access-sql.md) ステートメントを実行してその結果を調べてください。</span><span class="sxs-lookup"><span data-stu-id="1ac97-128">To find out which records will be selected before you run the make-table query, first examine the results of a [SELECT](select-statement-microsoft-access-sql.md) statement that uses the same selection criteria.</span></span>



## <a name="example"></a><span data-ttu-id="1ac97-129">使用例</span><span class="sxs-lookup"><span data-stu-id="1ac97-129">Example</span></span>

<span data-ttu-id="1ac97-130">次の使用例では、Employees テーブルのすべてのレコードを選択し、それを "Emp Backup" という新規テーブルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1ac97-130">This example selects all records in the Employees table and copies them into a new table named Emp Backup.</span></span>

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
