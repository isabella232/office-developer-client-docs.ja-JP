---
title: 行数をカウントする (Access デスクトップデータベースリファレンス)
TOCTitle: Counting rows
ms:assetid: ff684c5e-7f41-0dae-beea-f5c71f79bd84
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250312(v=office.15)
ms:contentKeyID: 48548963
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2388978185ac29149f7f15150ccfdbc559cc910f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295416"
---
# <a name="counting-rows"></a><span data-ttu-id="5fe8c-102">行のカウント</span><span class="sxs-lookup"><span data-stu-id="5fe8c-102">Counting rows</span></span>


<span data-ttu-id="5fe8c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fe8c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5fe8c-p101">**RecordCount** プロパティは、 **Recordset** 内のレコード数を示す長整数型 ( **Long** ) の値を返します。 **Recordset** オブジェクト内のレコード数を調べるには、 **RecordCount** プロパティを使用します。レコード数を特定できない場合、またはプロバイダーやカーソルの種類が **RecordCount** をサポートしていない場合は、このプロパティは -1 を返します。閉じている **Recordset** の **RecordCount** プロパティを読み取ると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5fe8c-p101">The **RecordCount** property returns a **Long** value that indicates the number of records in the **Recordset**. Use the **RecordCount** property to find out how many records are in a **Recordset** object. The property returns -1 when ADO cannot determine the number of records or if the provider or cursor type does not support **RecordCount**. Reading the **RecordCount** property on a closed **Recordset** causes an error.</span></span>

<span data-ttu-id="5fe8c-p102">**RecordCount** プロパティの値は、プロバイダーの機能とカーソルの種類によって異なります。 **RecordCount** プロパティは、前方スクロール カーソルの場合は -1 を返し、静的カーソルまたはキーセット カーソルの場合は実際の数を返し、動的カーソルの場合はデータ ソースによって -1 または実際の数を返します。</span><span class="sxs-lookup"><span data-stu-id="5fe8c-p102">The **RecordCount** property depends on the capabilities of the provider and the type of cursor. The **RecordCount** property will return -1 for a forward-only cursor, the actual count for a static or keyset cursor, and either -1 or the actual count for a dynamic cursor, depending on the data source.</span></span>

<span data-ttu-id="5fe8c-p103">「[3 章: データを調べる](chapter-3-examining-data.md)」にあるサンプル **Recordset** は、前方スクロール カーソルが開いているため -1 を返します。**RecordCount** プロパティを使用するには、より高度なカーソル (静的カーソルまたはキーセット カーソル) で **Recordset** を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="5fe8c-p103">The sample **Recordset** introduced in [Examining Data](chapter-3-examining-data.md) would return –1 because a forward-only cursor was opened. In order to use the **RecordCount** property, you would need to open the **Recordset** with a more sophisticated cursor (static or keyset).</span></span>

<span data-ttu-id="5fe8c-p104">場合によっては、データ ソースからすべてのレコードを最初にフェッチしないと、プロバイダーまたはカーソルが **RecordCount** 値を提供できないことがあります。このような種類のフェッチを強制的に行うには、 **Recordset** **MoveLast** メソッドを呼び出してから **RecordCount** を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5fe8c-p104">In certain cases, your provider or cursor might be unable to provide the **RecordCount** value without first fetching all records from the data source. To force this type of fetch, call the **Recordset** **MoveLast** method before calling **RecordCount**.</span></span>

<span data-ttu-id="5fe8c-114">**Recordset** **Open** メソッドを呼び出すコード行を次の行に置き換えると、</span><span class="sxs-lookup"><span data-stu-id="5fe8c-114">If you were to replace the line of code that calls the **Recordset** **Open** method with the following:</span></span>

```vb 
 
oRs.Open sSQL, sCnStr, adOpenStatic, adLockOptimistic, adCmdText 
```

<span data-ttu-id="5fe8c-p105">**Microsoft OLE DB Provider for SQL Server** の静的カーソルは [RecordCount](microsoft-ole-db-provider-for-sql-server.md) をサポートしているため、 **RecordCount** プロパティを使用できます。たとえば、次のコードを実行すると、カーソルが **RecordCount** プロパティをサポートしている場合、コマンドが返すレコード数がデバッグ ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5fe8c-p105">you would be able to use the **RecordCount** property because static cursors with the [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) support **RecordCount**. For example, the following code would print out the number of records returned by the command to the debug window, assuming the cursor supports the **RecordCount** property:</span></span>

```vb 
 
Debug.Print oRs.RecordCount ' Output: 4 
```

<span data-ttu-id="5fe8c-117">ここからは、これらのさらに高度な (ただし負荷が高い) カーソルとロックの種類の設定を使用します。</span><span class="sxs-lookup"><span data-stu-id="5fe8c-117">From this point forward, assume that these more capable (but more expensive) cursor and lock type settings are used.</span></span>

