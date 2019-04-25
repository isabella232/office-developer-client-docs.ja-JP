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
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="7fd0b-102">UPDATE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="7fd0b-102">UPDATE Statement (Microsoft Access SQL)</span></span>

<span data-ttu-id="7fd0b-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7fd0b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7fd0b-104">指定したテーブルのフィールドの値を指定の抽出条件に従って変更する更新クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fd0b-105">構文</span><span class="sxs-lookup"><span data-stu-id="7fd0b-105">Syntax</span></span>

<span data-ttu-id="7fd0b-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span><span class="sxs-lookup"><span data-stu-id="7fd0b-106">UPDATE *table* 
    SET *newvalue* 
    WHERE *criteria*;</span></span>

<span data-ttu-id="7fd0b-107">UPDATE ステートメントでは次の引数を使用します。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-107">The UPDATE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7fd0b-108">パーツ</span><span class="sxs-lookup"><span data-stu-id="7fd0b-108">Part</span></span></p></th>
<th><p><span data-ttu-id="7fd0b-109">説明</span><span class="sxs-lookup"><span data-stu-id="7fd0b-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7fd0b-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="7fd0b-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="7fd0b-111">変更するデータを含むテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7fd0b-112"><em>newvalue</em></span><span class="sxs-lookup"><span data-stu-id="7fd0b-112"><em>newvalue</em></span></span></p></td>
<td><p><span data-ttu-id="7fd0b-113">更新後のレコードの特定のフィールドに挿入する値を決めるための式です。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7fd0b-114"><em>criteria</em></span><span class="sxs-lookup"><span data-stu-id="7fd0b-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="7fd0b-p101">レコードを更新するか決めるための式です。式の条件を満たすレコードのみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-p101">An expression that determines which records will be updated. Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="7fd0b-117">注釈</span><span class="sxs-lookup"><span data-stu-id="7fd0b-117">Remarks</span></span>

<span data-ttu-id="7fd0b-118">UPDATE は、多数のレコードを変更する場合や、変更するレコードが複数のテーブルに含まれている場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="7fd0b-p102">複数のフィールドを同時に変更することができます。次に示すのは、"受注金額" の値が 10% ずつ、"運送料" の値が 3% ずつ増えている英国の運送会社の例です。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-p102">You can change several fields at the same time. The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
- <span data-ttu-id="7fd0b-p103">UPDATE ステートメントは、結果セットを作成しません。また、更新クエリを使用してレコードを更新すると、元に戻せません。どのレコードが変更されるかをあらかじめ確認する場合は、更新クエリを実行する前に、同じ抽出条件を使用する選択クエリを実行してその結果を調べてください。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-p103">UPDATE does not generate a result set. Also, after you update records using an update query, you cannot undo the operation. If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span>
- <span data-ttu-id="7fd0b-124">データのバックアップ コピーを常に維持してください。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-124">Maintain backup copies of your data at all times.</span></span> <span data-ttu-id="7fd0b-125">間違ったレコードを更新した場合、バックアップ コピーからレコードを元に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-125">Maintain backup copies of your data at all times. If you update the wrong records, you can retrieve them from your backup copies.</span></span>



## <a name="example"></a><span data-ttu-id="7fd0b-126">例</span><span class="sxs-lookup"><span data-stu-id="7fd0b-126">Example</span></span>

<span data-ttu-id="7fd0b-127">この使用例では、現在 ReportsTo の値が 2 であるすべての従業員レコードについて、ReportsTo フィールドの値を 5 に変更します。</span><span class="sxs-lookup"><span data-stu-id="7fd0b-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

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
