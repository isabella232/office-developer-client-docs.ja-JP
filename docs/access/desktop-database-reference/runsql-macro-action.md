---
title: RunSQL マクロ アクション
TOCTitle: RunSQL Macro Action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c5fd5bea659b3df368f6e352d0ae233b5e066113
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875596"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="b4240-102">RunSQL マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="b4240-102">RunSQL Macro Action</span></span>


<span data-ttu-id="b4240-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b4240-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4240-p101">**RunSQL** アクションを使用すると、Access のアクション クエリを、対応する SQL ステートメントを使用して実行できます。また、データ定義クエリも実行できます。</span><span class="sxs-lookup"><span data-stu-id="b4240-p101">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement. You can also run a data-definition query.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b4240-p102">[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b4240-p102">This action will not be allowed if the database is not trusted. For more information about enabling macros, see the links in the See Also section of this article.</span></span></P>



## <a name="setting"></a><span data-ttu-id="b4240-108">設定</span><span class="sxs-lookup"><span data-stu-id="b4240-108">Setting</span></span>

<span data-ttu-id="b4240-109">**RunSQL** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b4240-109">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4240-110">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="b4240-110">Action argument</span></span></p></th>
<th><p><span data-ttu-id="b4240-111">説明</span><span class="sxs-lookup"><span data-stu-id="b4240-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4240-112"><strong>SQL Statement/SQL ステートメント</strong></span><span class="sxs-lookup"><span data-stu-id="b4240-112"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="b4240-p103">実行するアクション クエリまたはデータ定義クエリに対応する SQL ステートメントを指定します。このステートメントの最大長は 255 バイトです。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="b4240-p103">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4240-116"><strong>Use Transaction/トランザクションの使用</strong></span><span class="sxs-lookup"><span data-stu-id="b4240-116"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="b4240-p104">このクエリをトランザクションに含める場合は [ <strong>はい</strong>] を選択します。このトランザクションを使用しない場合は [ <strong>いいえ</strong>] を選択します。既定値は [ <strong>はい</strong>] です。この引数に [ <strong>いいえ</strong>] を選択すると、クエリの実行速度が上がります。  </span><span class="sxs-lookup"><span data-stu-id="b4240-p104">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b4240-121">解説</span><span class="sxs-lookup"><span data-stu-id="b4240-121">Remarks</span></span>

<span data-ttu-id="b4240-p105">アクション クエリを使用すると、レコードの追加、削除、および更新を実行したり、クエリの結果セットを新しいテーブルとして保存することができます。データ定義クエリを使用すると、テーブルの作成、変更、および削除とインデックスの作成および削除を実行できます。 **RunSQL** アクションを使用すると、ストアド クエリを使用せず、このような処理をマクロから直接実行できます。</span><span class="sxs-lookup"><span data-stu-id="b4240-p105">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="b4240-p106">255 バイトを超える SQL ステートメントを入力する必要がある場合は、Visual Basic for Applications (VBA) モジュールで **DoCmd** オブジェクトの **RunSQL** メソッドを使用します。VBA では、最大 32,768 バイトの SQL ステートメントを入力できます。</span><span class="sxs-lookup"><span data-stu-id="b4240-p106">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead. You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="b4240-p107">Access のクエリは、実際には、クエリ ウィンドウのデザイン グリッドを使用してクエリをデザインするときに作成される SQL ステートメントです。次の表は、Access のアクション クエリとデータ定義クエリ、およびこれらのクエリに対応する SQL ステートメントを示しています。</span><span class="sxs-lookup"><span data-stu-id="b4240-p107">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4240-129">クエリの種類</span><span class="sxs-lookup"><span data-stu-id="b4240-129">Query type</span></span></p></th>
<th><p><span data-ttu-id="b4240-130">SQL ステートメント</span><span class="sxs-lookup"><span data-stu-id="b4240-130">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4240-131"><strong>アクション</strong></span><span class="sxs-lookup"><span data-stu-id="b4240-131"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4240-132">追加</span><span class="sxs-lookup"><span data-stu-id="b4240-132">Append</span></span></p></td>
<td><p><span data-ttu-id="b4240-133">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="b4240-133">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4240-134">削除</span><span class="sxs-lookup"><span data-stu-id="b4240-134">Delete</span></span></p></td>
<td><p><span data-ttu-id="b4240-135">DELETE</span><span class="sxs-lookup"><span data-stu-id="b4240-135">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4240-136">テーブル作成</span><span class="sxs-lookup"><span data-stu-id="b4240-136">Make-table</span></span></p></td>
<td><p><span data-ttu-id="b4240-137">選択します。に</span><span class="sxs-lookup"><span data-stu-id="b4240-137">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4240-138">更新</span><span class="sxs-lookup"><span data-stu-id="b4240-138">Update</span></span></p></td>
<td><p><span data-ttu-id="b4240-139">UPDATE</span><span class="sxs-lookup"><span data-stu-id="b4240-139">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4240-140"><strong>データ定義 (SQL 固有)</strong></span><span class="sxs-lookup"><span data-stu-id="b4240-140"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4240-141">テーブルの作成</span><span class="sxs-lookup"><span data-stu-id="b4240-141">Create a table</span></span></p></td>
<td><p><span data-ttu-id="b4240-142">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="b4240-142">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4240-143">テーブルの変更</span><span class="sxs-lookup"><span data-stu-id="b4240-143">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="b4240-144">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="b4240-144">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4240-145">テーブルの削除</span><span class="sxs-lookup"><span data-stu-id="b4240-145">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="b4240-146">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="b4240-146">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4240-147">インデックスの作成</span><span class="sxs-lookup"><span data-stu-id="b4240-147">Create an index</span></span></p></td>
<td><p><span data-ttu-id="b4240-148">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="b4240-148">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4240-149">インデックスの削除</span><span class="sxs-lookup"><span data-stu-id="b4240-149">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="b4240-150">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="b4240-150">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4240-151">これらのステートメントと IN 句を組み合わせて使用すると、別のデータベース内のデータを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="b4240-151">You can also use an IN clause with these statements to modify data in another database.</span></span>


> [!NOTE]
> <P><span data-ttu-id="b4240-p108">[!メモ] 選択クエリまたはクロス集計クエリをマクロから実行するには、 <STRONG>OpenQuery</STRONG> アクションの "View/ビュー" 引数を使用して、既存の選択クエリまたはクロス集計クエリをデータシート ビューで開きます。また、同様に、既存のアクション クエリおよび SQL 固有のクエリを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="b4240-p108">To run a select query or crosstab query from a macro, use the View argument of the <STRONG>OpenQuery</STRONG> action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span></P>


