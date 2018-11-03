---
title: TableDef.ReplicaFilter プロパティ (DAO)
TOCTitle: ReplicaFilter Property
ms:assetid: f44273de-2b6a-750f-cb7c-12c3ac2da503
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836681(v=office.15)
ms:contentKeyID: 48548683
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1055548
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dbd8ecc670742d6b9f88dd9c608d2304e26a8d09
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929665"
---
# <a name="tabledefreplicafilter-property-dao"></a><span data-ttu-id="25671-102">TableDef.ReplicaFilter プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="25671-102">TableDef.ReplicaFilter property (DAO)</span></span>


<span data-ttu-id="25671-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="25671-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="25671-p101">フル レプリカのレコードのどの部分を該当するテーブルにレプリケートするかを示す、部分レプリカ内の **[TableDef](tabledef-object-dao.md)** オブジェクトの値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="25671-p101">Sets or returns a value on a **[TableDef](tabledef-object-dao.md)** object within a partial replica that indicates which subset of records is replicated to that table from a full replica. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="25671-106">構文</span><span class="sxs-lookup"><span data-stu-id="25671-106">Syntax</span></span>

<span data-ttu-id="25671-107">*式*です。ReplicaFilter</span><span class="sxs-lookup"><span data-stu-id="25671-107">*expression* .ReplicaFilter</span></span>

<span data-ttu-id="25671-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="25671-108">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="25671-109">注釈</span><span class="sxs-lookup"><span data-stu-id="25671-109">Remarks</span></span>

<span data-ttu-id="25671-110">設定値または戻り値は、次の表に示すように、レプリケートするレコードの部分を示す文字列型 ( **String**) またはブール型 ( **Boolean**) の値です。</span><span class="sxs-lookup"><span data-stu-id="25671-110">The setting or return value is a **String** or **Boolean** that indicates which subset of records is replicated, as specified in the following table:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="25671-111">値</span><span class="sxs-lookup"><span data-stu-id="25671-111">Value</span></span></p></th>
<th><p><span data-ttu-id="25671-112">説明</span><span class="sxs-lookup"><span data-stu-id="25671-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="25671-113">文字列</span><span class="sxs-lookup"><span data-stu-id="25671-113">A string</span></span></p></td>
<td><p><span data-ttu-id="25671-114">部分レプリカ テーブル内のレコードをフル レプリカからレプリケートするために、そのレコードが満たす必要がある条件です。</span><span class="sxs-lookup"><span data-stu-id="25671-114">A criteria that a record in the partial replica table must satisfy in order to be replicated from the full replica.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="25671-115"><strong>True</strong></span><span class="sxs-lookup"><span data-stu-id="25671-115"><strong>True</strong></span></span></p></td>
<td><p><span data-ttu-id="25671-116">すべてのレコードをレプリケートします。</span><span class="sxs-lookup"><span data-stu-id="25671-116">Replicates all records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="25671-117"><strong>False</strong></span><span class="sxs-lookup"><span data-stu-id="25671-117"><strong>False</strong></span></span></p></td>
<td><p><span data-ttu-id="25671-118">(既定値) レコードをレプリケートしません。</span><span class="sxs-lookup"><span data-stu-id="25671-118">(Default) Doesn't replicate any records.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="25671-119">このプロパティは、SQL WHERE 句 (キーワード WHERE は省略) に似ていますが、条件にサブクエリ、 **Count** などの集計関数、またはユーザー定義関数を指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="25671-119">This property is similar to an SQL WHERE clause (without the word WHERE), but you cannot specify subqueries, aggregate functions (such as **Count**), or user-defined functions within the criteria.</span></span>

<span data-ttu-id="25671-p102">フル レプリカと部分レプリカの間でのみ、データを同期することができます。2 つの部分レプリカ間でデータを同期することはできません。また、部分レプリカでは、レプリケートするレコードに制限を設定できますが、レプリケートするフィールドを指定することはできません。</span><span class="sxs-lookup"><span data-stu-id="25671-p102">You can only synchronize data between a full replica and a partial replica. You can't synchronize data between two partial replicas. Also, with partial replication you can set restrictions on which records are replicated, but you can't indicate which fields are replicated.</span></span>

<span data-ttu-id="25671-p103">異なるレコードのセットをレプリケートする場合、通常、レプリカ フィルターをリセットします。たとえば、ある営業社員が別の営業社員の地域を一時的に引き継ぐ場合、データベース アプリケーションでは、一時的に両地域のデータをレプリケートしてから、前のフィルターに戻すことができます。この場合、アプリケーションでは、 **ReplicaFilter** プロパティをリセットしてから、部分レプリカを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="25671-p103">Usually, you reset a replica filter when you want to replicate a different set of records. For example, when a sales representative temporarily takes over another sales representative's region, the database application can temporarily replicate data for both regions and then return to the previous filter. In this scenario, the application resets the **ReplicaFilter** property and then repopulates the partial replica.</span></span>

<span data-ttu-id="25671-126">アプリケーションでレプリカ フィルターを変更する場合、次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="25671-126">If your application changes replica filters, you should follow these steps:</span></span>

1.  <span data-ttu-id="25671-127">**[Synchronize](database-synchronize-method-dao.md)** メソッドを使用して、フル レプリカをフィルター変更中の部分レプリカと同期します。</span><span class="sxs-lookup"><span data-stu-id="25671-127">Use the **[Synchronize](database-synchronize-method-dao.md)** method to synchronize your full replica with the partial replica in which the filters are being changed.</span></span>

2.  <span data-ttu-id="25671-128">**ReplicaFilter** プロパティを使用して、レプリカ フィルターに必要な変更を行います。</span><span class="sxs-lookup"><span data-stu-id="25671-128">Use the **ReplicaFilter** property to make the desired changes to the replica filter.</span></span>

3.  <span data-ttu-id="25671-129">**[PopulatePartial](database-populatepartial-method-dao.md)** メソッドを使用して、部分レプリカからすべてのレコードを削除し、新規レプリカのフィルター抽出条件に合うすべてのレコードをフル レプリカから転送します。</span><span class="sxs-lookup"><span data-stu-id="25671-129">Use the **[PopulatePartial](database-populatepartial-method-dao.md)** method to remove all records from the partial replica and transfer all records from the full replica that meet the new replica filter criteria.</span></span>

<span data-ttu-id="25671-p104">フィルターを削除するには、 **ReplicaFilter** プロパティを **False** に設定します。すべてのフィルターを削除して、 **PopulatePartial** メソッドを呼び出すと、部分レプリカのレプリケートされたテーブルにレコードが表示されることはありません。</span><span class="sxs-lookup"><span data-stu-id="25671-p104">To remove a filter, set the **ReplicaFilter** property to **False**. If you remove all filters and invoke the **PopulatePartial** method, no records will appear in any replicated tables in the partial replica.</span></span>


> [!NOTE]
> <P><span data-ttu-id="25671-132">[!メモ] レプリカ フィルターを変更し、最初に <STRONG>PopulatePartial</STRONG> メソッドを呼び出さずに <STRONG>Synchronize</STRONG> メソッドを呼び出すと、トラップ可能なエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="25671-132">If a replica filter has changed, and the <STRONG>Synchronize</STRONG> method is invoked without first invoking <STRONG>PopulatePartial</STRONG>, a trappable error occurs.</span></span></P>



## <a name="example"></a><span data-ttu-id="25671-133">例</span><span class="sxs-lookup"><span data-stu-id="25671-133">Example</span></span>

<span data-ttu-id="25671-134">次の例では、 **ReplicaFilter** プロパティを使用して、カリフォルニア地域の顧客レコードのみレプリケートします。</span><span class="sxs-lookup"><span data-stu-id="25671-134">The following example uses the **ReplicaFilter** property to replicate only customer records from the California region.</span></span>

```vb 
Sub ReplicaFilterX() 
 
 ' This example assumes the current open database 
 ' is the replica. 
 Dim tdfCustomers As TableDef 
 Dim strFilter As String 
 Dim dbsTemp As Database 
 
 Set dbsTemp = OpenDatabase("Northwind.mdb") 
 Set tdfCustomers = dbsTemp.TableDefs("Customers") 
 
 ' Synchronize with full replica 
 ' before setting replica filter. 
 dbsTemp.Synchronize "C:\SALES\FY96.MDB" 
 
 strFilter = "Region = 'CA'" 
 tdfCustomers.ReplicaFilter = strFilter 
 dbsTemp.PopulatePartial "C:\SALES\FY96.MDB" 
 
 ' Now remove the replica filter (for example purposes 
 ' only). 
 tdfCustomers.ReplicaFilter = False 
 ' Repopulate the database. 
 dbsTemp.PopulatePartial "C:\SALES\DATA96.MDB" 
 
End Sub 
 
```

