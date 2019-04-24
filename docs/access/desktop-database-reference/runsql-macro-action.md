---
title: RunSQL マクロ アクション
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f3ef598ad50747d99ca884043e03ebfabfef8f63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308996"
---
# <a name="runsql-macro-action"></a><span data-ttu-id="3155e-102">RunSQL マクロ アクション</span><span class="sxs-lookup"><span data-stu-id="3155e-102">RunSQL macro action</span></span>

<span data-ttu-id="3155e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3155e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3155e-p101">**RunSQL** アクションを使用すると、Access のアクション クエリを、対応する SQL ステートメントを使用して実行できます。また、データ定義クエリも実行できます。</span><span class="sxs-lookup"><span data-stu-id="3155e-p101">You can use the **RunSQL** action to run a Access action query by using the corresponding SQL statement. You can also run a data-definition query.</span></span>

> [!NOTE]
> <span data-ttu-id="3155e-106">このアクションは、データベースが信頼されていない場合には許可されません。</span><span class="sxs-lookup"><span data-stu-id="3155e-106">This action will not be allowed if the database is not trusted.</span></span> 

## <a name="setting"></a><span data-ttu-id="3155e-107">設定値</span><span class="sxs-lookup"><span data-stu-id="3155e-107">Setting</span></span>

<span data-ttu-id="3155e-108">**RunSQL** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3155e-108">The **RunSQL** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3155e-109">アクションの引数</span><span class="sxs-lookup"><span data-stu-id="3155e-109">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3155e-110">説明</span><span class="sxs-lookup"><span data-stu-id="3155e-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3155e-111"><strong>SQL Statement/SQL ステートメント</strong></span><span class="sxs-lookup"><span data-stu-id="3155e-111"><strong>SQL Statement</strong></span></span></p></td>
<td><p><span data-ttu-id="3155e-p102">実行するアクション クエリまたはデータ定義クエリに対応する SQL ステートメントを指定します。このステートメントの最大長は 255 バイトです。この引数は省略できません。</span><span class="sxs-lookup"><span data-stu-id="3155e-p102">The SQL statement for the action query or data-definition query you want to run. The maximum length of this statement is 255 characters. This is a required argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3155e-115"><strong>Use Transaction/トランザクションの使用</strong></span><span class="sxs-lookup"><span data-stu-id="3155e-115"><strong>Use Transaction</strong></span></span></p></td>
<td><p><span data-ttu-id="3155e-p103">このクエリをトランザクションに含める場合は [ <strong>はい</strong>] を選択します。このトランザクションを使用しない場合は [ <strong>いいえ</strong>] を選択します。既定値は [ <strong>はい</strong>] です。この引数に [ <strong>いいえ</strong>] を選択すると、クエリの実行速度が上がります。  </span><span class="sxs-lookup"><span data-stu-id="3155e-p103">Select <strong>Yes</strong> to include this query in a transaction. Select <strong>No</strong> if you don't want to use a transaction. The default is <strong>Yes</strong>. If you select <strong>No</strong> for this argument, the query might run faster.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3155e-120">注釈</span><span class="sxs-lookup"><span data-stu-id="3155e-120">Remarks</span></span>

<span data-ttu-id="3155e-p104">アクション クエリを使用すると、レコードの追加、削除、および更新を実行したり、クエリの結果セットを新しいテーブルとして保存することができます。データ定義クエリを使用すると、テーブルの作成、変更、および削除とインデックスの作成および削除を実行できます。 **RunSQL** アクションを使用すると、ストアド クエリを使用せず、このような処理をマクロから直接実行できます。</span><span class="sxs-lookup"><span data-stu-id="3155e-p104">You can use action queries to append, delete, and update records and to save a query's result set as a new table. You can use data-definition queries to create, alter, and delete tables, and to create and delete indexes. You can use the **RunSQL** action to perform these operations directly from a macro without having to use stored queries.</span></span>

<span data-ttu-id="3155e-p105">255 バイトを超える SQL ステートメントを入力する必要がある場合は、Visual Basic for Applications (VBA) モジュールで **DoCmd** オブジェクトの **RunSQL** メソッドを使用します。VBA では、最大 32,768 バイトの SQL ステートメントを入力できます。</span><span class="sxs-lookup"><span data-stu-id="3155e-p105">If you need to type an SQL statement longer than 255 characters, use the **RunSQL** method of the **DoCmd** object in a Visual Basic for Applications (VBA) module instead. You can type SQL statements of up to 32,768 characters in VBA.</span></span>

<span data-ttu-id="3155e-p106">Access のクエリは、実際には、クエリ ウィンドウのデザイン グリッドを使用してクエリをデザインするときに作成される SQL ステートメントです。次の表は、Access のアクション クエリとデータ定義クエリ、およびこれらのクエリに対応する SQL ステートメントを示しています。</span><span class="sxs-lookup"><span data-stu-id="3155e-p106">Access queries are actually SQL statements that are created when you design a query by using the design grid in the Query window. The following table shows the Access action queries and data-definition queries and their corresponding SQL statements.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3155e-128">クエリの種類</span><span class="sxs-lookup"><span data-stu-id="3155e-128">Query type</span></span></p></th>
<th><p><span data-ttu-id="3155e-129">SQL ステートメント</span><span class="sxs-lookup"><span data-stu-id="3155e-129">SQL statement</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3155e-130"><strong>アクション</strong></span><span class="sxs-lookup"><span data-stu-id="3155e-130"><strong>Action</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3155e-131">追加</span><span class="sxs-lookup"><span data-stu-id="3155e-131">Append</span></span></p></td>
<td><p><span data-ttu-id="3155e-132">INSERT INTO</span><span class="sxs-lookup"><span data-stu-id="3155e-132">INSERT INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3155e-133">削除</span><span class="sxs-lookup"><span data-stu-id="3155e-133">Delete</span></span></p></td>
<td><p><span data-ttu-id="3155e-134">DELETE</span><span class="sxs-lookup"><span data-stu-id="3155e-134">DELETE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3155e-135">テーブル作成</span><span class="sxs-lookup"><span data-stu-id="3155e-135">Make-table</span></span></p></td>
<td><p><span data-ttu-id="3155e-136">[...] を選択します。分ける</span><span class="sxs-lookup"><span data-stu-id="3155e-136">SELECT...INTO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3155e-137">更新</span><span class="sxs-lookup"><span data-stu-id="3155e-137">Update</span></span></p></td>
<td><p><span data-ttu-id="3155e-138">UPDATE</span><span class="sxs-lookup"><span data-stu-id="3155e-138">UPDATE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3155e-139"><strong>データ定義 (SQL 固有)</strong></span><span class="sxs-lookup"><span data-stu-id="3155e-139"><strong>Data-definition (SQL-specific)</strong></span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3155e-140">テーブルの作成</span><span class="sxs-lookup"><span data-stu-id="3155e-140">Create a table</span></span></p></td>
<td><p><span data-ttu-id="3155e-141">CREATE TABLE</span><span class="sxs-lookup"><span data-stu-id="3155e-141">CREATE TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3155e-142">テーブルの変更</span><span class="sxs-lookup"><span data-stu-id="3155e-142">Alter a table</span></span></p></td>
<td><p><span data-ttu-id="3155e-143">ALTER TABLE</span><span class="sxs-lookup"><span data-stu-id="3155e-143">ALTER TABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3155e-144">テーブルの削除</span><span class="sxs-lookup"><span data-stu-id="3155e-144">Delete a table</span></span></p></td>
<td><p><span data-ttu-id="3155e-145">DROP TABLE</span><span class="sxs-lookup"><span data-stu-id="3155e-145">DROP TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3155e-146">インデックスの作成</span><span class="sxs-lookup"><span data-stu-id="3155e-146">Create an index</span></span></p></td>
<td><p><span data-ttu-id="3155e-147">CREATE INDEX</span><span class="sxs-lookup"><span data-stu-id="3155e-147">CREATE INDEX</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3155e-148">インデックスの削除</span><span class="sxs-lookup"><span data-stu-id="3155e-148">Delete an index</span></span></p></td>
<td><p><span data-ttu-id="3155e-149">DROP INDEX</span><span class="sxs-lookup"><span data-stu-id="3155e-149">DROP INDEX</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3155e-150">これらのステートメントと IN 句を組み合わせて使用すると、別のデータベース内のデータを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="3155e-150">You can also use an IN clause with these statements to modify data in another database.</span></span>

> [!NOTE]
> <span data-ttu-id="3155e-p107">[!メモ] 選択クエリまたはクロス集計クエリをマクロから実行するには、 **OpenQuery** アクションの "View/ビュー" 引数を使用して、既存の選択クエリまたはクロス集計クエリをデータシート ビューで開きます。また、同様に、既存のアクション クエリおよび SQL 固有のクエリを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="3155e-p107">To run a select query or crosstab query from a macro, use the View argument of the **OpenQuery** action to open an existing select query or crosstab query in Datasheet view. You can also run existing action queries and SQL-specific queries in the same way.</span></span>
