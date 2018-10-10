---
title: UPDATE ステートメント (Microsoft Access SQL)
TOCTitle: UPDATE Statement (Microsoft Access SQL)
ms:assetid: 08f9c3d6-c020-ecf1-5748-43b93a76dfbb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845036(v=office.15)
ms:contentKeyID: 48543111
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- jetsql40.chm5277583
dev_langs:
- sql
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3affce9346e9e322bc588ca1c3be24867a1469d6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477436"
---
# <a name="update-statement-microsoft-access-sql"></a><span data-ttu-id="c2e53-102">UPDATE ステートメント (Microsoft Access SQL)</span><span class="sxs-lookup"><span data-stu-id="c2e53-102">UPDATE Statement (Microsoft Access SQL)</span></span>


<span data-ttu-id="c2e53-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2e53-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c2e53-104">指定したテーブルのフィールドの値を指定の抽出条件に従って変更する更新クエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="c2e53-104">Creates an update query that changes values in fields in a specified table based on specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2e53-105">構文</span><span class="sxs-lookup"><span data-stu-id="c2e53-105">Syntax</span></span>

<span data-ttu-id="c2e53-106">更新*テーブル*セットの*新しい値\*\*条件*です。</span><span class="sxs-lookup"><span data-stu-id="c2e53-106">UPDATE *table* SET *newvalue* WHERE *criteria*;</span></span>

<span data-ttu-id="c2e53-107">UPDATE ステートメントには、次の指定項目があります。</span><span class="sxs-lookup"><span data-stu-id="c2e53-107">The UPDATE statement has these parts:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2e53-108">指定項目</span><span class="sxs-lookup"><span data-stu-id="c2e53-108">Part</span></span></p></th>
<th><p><span data-ttu-id="c2e53-109">説明</span><span class="sxs-lookup"><span data-stu-id="c2e53-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2e53-110"><em>table</em></span><span class="sxs-lookup"><span data-stu-id="c2e53-110"><em>table</em></span></span></p></td>
<td><p><span data-ttu-id="c2e53-111">変更するデータのあるテーブルの名前。</span><span class="sxs-lookup"><span data-stu-id="c2e53-111">The name of the table containing the data you want to modify.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2e53-112"><em>newvalue</em></span><span class="sxs-lookup"><span data-stu-id="c2e53-112"><em>newvalue</em></span></span></p></td>
<td><p><span data-ttu-id="c2e53-113">更新後のレコードの特定のフィールドに挿入する値を決めるための式。</span><span class="sxs-lookup"><span data-stu-id="c2e53-113">An expression that determines the value to be inserted into a particular field in the updated records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2e53-114"><em>criteria</em></span><span class="sxs-lookup"><span data-stu-id="c2e53-114"><em>criteria</em></span></span></p></td>
<td><p><span data-ttu-id="c2e53-p101">更新するレコードを抽出するための式。この式の条件を満たすレコードのみが更新されます。</span><span class="sxs-lookup"><span data-stu-id="c2e53-p101">An expression that determines which records will be updated. Only records that satisfy the expression are updated.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c2e53-117">解説</span><span class="sxs-lookup"><span data-stu-id="c2e53-117">Remarks</span></span>

<span data-ttu-id="c2e53-118">UPDATE ステートメントは、多数のレコードを変更する場合や、変更するレコードが複数のテーブルに含まれている場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="c2e53-118">UPDATE is especially useful when you want to change many records or when the records that you want to change are in multiple tables.</span></span>

<span data-ttu-id="c2e53-p102">UPDATE ステートメントでは、複数のフィールドを同時に変更できます。次の例では、輸送先が英国であるレコードの Order Amount フィールドの値を 10%、Freight フィールドの値を 3%、それぞれ増やしています。</span><span class="sxs-lookup"><span data-stu-id="c2e53-p102">You can change several fields at the same time. The following example increases the Order Amount values by 10 percent and the Freight values by 3 percent for shippers in the United Kingdom:</span></span>

```sql
UPDATE Orders 
SET OrderAmount = OrderAmount * 1.1, 
Freight = Freight * 1.03 
WHERE ShipCountry = 'UK';
```


> [!IMPORTANT]
> <UL>
> <LI>
> <P><span data-ttu-id="c2e53-p103">UPDATE ステートメントは、結果セットを作成しません。また、更新クエリを使用してレコードを更新すると、元に戻せません。どのレコードが変更されるかをあらかじめ確認する場合は、更新クエリを実行する前に、同じ抽出条件を使用する選択クエリを実行してその結果を調べてください。</span><span class="sxs-lookup"><span data-stu-id="c2e53-p103">UPDATE does not generate a result set. Also, after you update records using an update query, you cannot undo the operation. If you want to know which records were updated, first examine the results of a select query that uses the same criteria, and then run the update query.</span></span></P>
> <LI>
> <P><span data-ttu-id="c2e53-p104">誤ってレコードを更新した場合にも復旧できるように、常にデータのバックアップ コピーを作成しておくことをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c2e53-p104">Maintain backup copies of your data at all times. If you update the wrong records, you can retrieve them from your backup copies.</span></span></P></LI></UL>



## <a name="example"></a><span data-ttu-id="c2e53-126">使用例</span><span class="sxs-lookup"><span data-stu-id="c2e53-126">Example</span></span>

<span data-ttu-id="c2e53-127">この使用例では、現在 ReportsTo の値が 2 であるすべての従業員レコードについて、ReportsTo フィールドの値を 5 に変更します。</span><span class="sxs-lookup"><span data-stu-id="c2e53-127">This example changes values in the ReportsTo field to 5 for all employee records that currently have ReportsTo values of 2.</span></span>

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