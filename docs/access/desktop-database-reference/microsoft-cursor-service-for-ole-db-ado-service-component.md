---
title: OLE DB の Microsoft カーソル サービス (ADO サービス コンポーネント)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d79d060922c6e7f28209242ebe82821c2ba97bfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288989"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="a16d6-102">Microsoft Cursor Service for OLE DB (ADO サービス コンポーネント)</span><span class="sxs-lookup"><span data-stu-id="a16d6-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="a16d6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a16d6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a16d6-p101">Microsoft Cursor Service for OLE DB は、データ プロバイダーのカーソル サポート機能を補完します。その結果、すべてのデータ プロバイダーで機能の統一感が向上します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p101">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers. As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="a16d6-p102">Cursor Service は、動的プロパティを利用可能にして特定のメソッドの動作を拡張します。たとえば、動的プロパティ [Optimize](optimize-property-dynamic-ado.md) を使用すると、一時インデックスの作成が可能になり、 [Find](find-method-ado.md) メソッドなどの特定の操作が容易になります。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p102">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods. For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="a16d6-p103">Cursor Service を使用すると、あらゆる場合での一括更新が可能になります。また、静的カーソルのみを提供するデータ プロバイダーでも、動的カーソルなどの、より機能的なカーソルを模擬的に利用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p103">The Cursor Service enables support for batch updating in all cases. It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="a16d6-110">キーワード</span><span class="sxs-lookup"><span data-stu-id="a16d6-110">Keyword</span></span>

<span data-ttu-id="a16d6-111">このサービス コンポーネントを呼び出すには、[Recordset](recordset-object-ado.md) オブジェクトまたは [Connection](connection-object-ado.md) オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="a16d6-112">動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="a16d6-112">Dynamic Properties</span></span>

<span data-ttu-id="a16d6-p104">Cursor Service for OLE DB を呼び出すと、次に示す動的プロパティが **Recordset** オブジェクトの [Properties](properties-collection-ado.md) コレクションに追加されます。**Connection** オブジェクトおよび **Recordset** オブジェクトのすべての動的プロパティの一覧については、「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」を参照してください。対応する OLE DB プロパティ名がある場合は、ADO プロパティ名の後にかっこで囲んで示しています。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p104">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection. The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md). The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="a16d6-p105">Cursor Service を呼び出した後、動的プロパティを変更しても、基になるデータ ソースで認識されない場合があります。たとえば、**Recordset** で *Command Time out* プロパティを設定しても、基になるデータ プロバイダーには認識されません。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p105">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked. For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

<span data-ttu-id="a16d6-p106">アプリケーションが Cursor Service を必要とし、基になるプロバイダーの動的プロパティを設定する必要がある場合は、Cursor Service を呼び出す前に動的プロパティを設定します。コマンド オブジェクトのプロパティの設定値は、カーソルの位置に関係なく、常に基になるデータ プロバイダーに渡されます。したがって、いつでも、コマンド オブジェクトを使用してプロパティを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p106">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service. Command object property settings are always passed to the underlying data provider regardless of cursor location. Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="a16d6-121">[!メモ] 動的プロパティ DBPROP_SERVERDATAONINSERT は、基になるデータ プロバイダーでサポートされている場合でも、カーソル サービスではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="a16d6-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a16d6-122">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a16d6-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="a16d6-123">説明</span><span class="sxs-lookup"><span data-stu-id="a16d6-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-124">Auto Recalc</span><span class="sxs-lookup"><span data-stu-id="a16d6-124">Auto Recalc</span></span><br />
<span data-ttu-id="a16d6-125">(DBPROP_ADC_AUTORECALC)</span><span class="sxs-lookup"><span data-stu-id="a16d6-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="a16d6-p107">Data Shaping Service で作成されたレコードセットの場合、この値は計算列および集計列の計算頻度を示します。既定値 (1) の場合は、Data Shaping Service で値の変更が確認されるたびに再計算が行われます。この値が 0 の場合は、階層が最初に構築されたときにのみ計算列または集計列が計算されます。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p107">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated. The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed. If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16d6-129">Batch Size</span><span class="sxs-lookup"><span data-stu-id="a16d6-129">Batch Size</span></span><br />
<span data-ttu-id="a16d6-130">(DBPROP_ADC_BATCHSIZE)</span><span class="sxs-lookup"><span data-stu-id="a16d6-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="a16d6-p108">データ ストアに送信するまでにバッチ処理できる更新ステートメントの数を示します。1 回のバッチ処理に含めるステートメント数が多いほど、データ ストアとのやり取りの回数が少なくなります。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p108">Indicates the number of update statements that can be batched before being sent to the data store. The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-133">Cache Child Rows</span><span class="sxs-lookup"><span data-stu-id="a16d6-133">Cache Child Rows</span></span><br />
<span data-ttu-id="a16d6-134">(DBPROP_ADC_CACHECHILDROWS)</span><span class="sxs-lookup"><span data-stu-id="a16d6-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="a16d6-135">Data Shaping Service で作成されたレコードセットの場合、この値は、子レコードセットを後で使用できるようにキャッシュに保存しておくかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16d6-136">Cursor Engine Version</span><span class="sxs-lookup"><span data-stu-id="a16d6-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="a16d6-137">(DBPROP_ADC_CEVER)</span><span class="sxs-lookup"><span data-stu-id="a16d6-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="a16d6-138">使用する Cursor Service のバージョンを示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-139">Maintain Change Status</span><span class="sxs-lookup"><span data-stu-id="a16d6-139">Maintain Change Status</span></span><br />
<span data-ttu-id="a16d6-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span><span class="sxs-lookup"><span data-stu-id="a16d6-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="a16d6-141">複数のテーブルの結合で、行を再同期化するために使用するコマンドのテキストを示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16d6-142"><a href="optimize-property-dynamic-ado.md">最適化</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-p109">インデックスを作成するかどうかを示します。<strong>True</strong> に設定すると、特定の操作の実行速度を向上させるために一時的なインデックスの作成が許可されます。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p109">Indicates whether an index should be created. When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-146"><strong>Recordset</strong> の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-146">Indicates the name of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="a16d6-147">現在またはそれ以降のデータ シェイプ コマンドで参照される場合があります。</span><span class="sxs-lookup"><span data-stu-id="a16d6-147">May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16d6-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-149"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> プロパティが有効である場合に、<a href="resync-method-ado.md">Resync</a> メソッドで使用されるカスタム コマンド文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-151"><strong>Unique Table</strong> プロパティで参照されるテーブルを格納しているデータベースの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16d6-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-153"><strong>Unique Table</strong> プロパティで参照されるテーブルの所有者の名前を示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-155">挿入、更新、または削除によって変更された可能性がある複数のテーブルから作成された <strong>Recordset</strong> 内の 1 つのテーブル名を示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16d6-156">Update Criteria</span><span class="sxs-lookup"><span data-stu-id="a16d6-156">Update Criteria</span></span><br />
<span data-ttu-id="a16d6-157">(DBPROP_ADC_UPDATECRITERIA)</span><span class="sxs-lookup"><span data-stu-id="a16d6-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="a16d6-158">更新時に発生する競合の処理に使用される <strong>WHERE</strong> 句のフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span><span class="sxs-lookup"><span data-stu-id="a16d6-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="a16d6-160"><strong>Unique Table</strong> プロパティが有効である場合に、<a href="updatebatch-method-ado.md">UpdateBatch</a> メソッド (およびその動作) の後に、<strong>Resync</strong> メソッドを暗黙に呼び出すかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a16d6-p111">動的プロパティの名前を **Properties** コレクションのインデックスとして指定して、動的プロパティを設定または取得することもできます。たとえば、[Optimize](optimize-property-dynamic-ado.md) 動的プロパティの値を取得して出力した後、新しい値を設定するには、次のように指定します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-p111">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection. For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="a16d6-163">組み込みプロパティの動作</span><span class="sxs-lookup"><span data-stu-id="a16d6-163">Built-in Property Behavior</span></span>

<span data-ttu-id="a16d6-164">Cursor Service for OLE DB は、特定の組み込みプロパティの動作にも影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="a16d6-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a16d6-165">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="a16d6-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="a16d6-166">説明</span><span class="sxs-lookup"><span data-stu-id="a16d6-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-168"><strong>Recordset</strong> で利用可能なカーソルの種類を補完します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a16d6-169"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-170"><strong>Recordset</strong> で利用可能なロックの種類を補完します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-170">Supplements the types of locks available for a <strong>Recordset</strong>.</span></span> <span data-ttu-id="a16d6-171">一括更新を可能にします。</span><span class="sxs-lookup"><span data-stu-id="a16d6-171">Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a16d6-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="a16d6-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="a16d6-173"><strong>Recordset</strong> の並べ替えに使用するフィールド名、および各フィールドの並べ替え順序が昇順か降順かを指定します。</span><span class="sxs-lookup"><span data-stu-id="a16d6-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="a16d6-174">メソッドの動作</span><span class="sxs-lookup"><span data-stu-id="a16d6-174">Method Behavior</span></span>

<span data-ttu-id="a16d6-175">Cursor Service for OLE DB は、[Field](field-object-ado.md) オブジェクトの [Append](append-method-ado.md) メソッドや、**Recordset** オブジェクトの [Open](open-method-ado-recordset.md) メソッド、[Resync](resync-method-ado.md) メソッド、[UpdateBatch](updatebatch-method-ado.md) メソッド、および [Save](save-method-ado.md) メソッドにも影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="a16d6-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

