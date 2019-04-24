---
title: ForEachRecord データブロック
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292329"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="257f3-102">ForEachRecord データブロック</span><span class="sxs-lookup"><span data-stu-id="257f3-102">ForEachRecord data block</span></span>

<span data-ttu-id="257f3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="257f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="257f3-104">**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="257f3-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="257f3-105">**ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="257f3-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="257f3-106">Setting</span><span class="sxs-lookup"><span data-stu-id="257f3-106">Setting</span></span>

<span data-ttu-id="257f3-107">ForEachRecord アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="257f3-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="257f3-108">引数</span><span class="sxs-lookup"><span data-stu-id="257f3-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="257f3-109">必須</span><span class="sxs-lookup"><span data-stu-id="257f3-109">Required</span></span></p></th>
<th><p><span data-ttu-id="257f3-110">説明</span><span class="sxs-lookup"><span data-stu-id="257f3-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="257f3-111"><strong>順番</strong></span><span class="sxs-lookup"><span data-stu-id="257f3-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="257f3-112">はい</span><span class="sxs-lookup"><span data-stu-id="257f3-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="257f3-p101">実行するステートメントの対象レコードのドメインを識別する文字列。In<em></em> 引数には、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="257f3-p101">A string that identifies the domain of records to operate on. The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="257f3-115"><strong>注</strong>: 指定されたドメインには、リンクテーブルまたは ODBC データソースに格納されているデータを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="257f3-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="257f3-116">Where Condition/Where 条件式</span><span class="sxs-lookup"><span data-stu-id="257f3-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="257f3-117">いいえ</span><span class="sxs-lookup"><span data-stu-id="257f3-117">No</span></span></p></td>
<td><p><span data-ttu-id="257f3-p102"><strong>ForEachRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>ForEachRecord</strong> データ ブロックは In<em></em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、In<em></em> にも含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="257f3-p102">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed. For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE. If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument. Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="257f3-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="257f3-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="257f3-123">いいえ</span><span class="sxs-lookup"><span data-stu-id="257f3-123">No</span></span></p></td>
<td><p><span data-ttu-id="257f3-124">In<em></em> 引数で指定したドメインの別名となる文字列。</span><span class="sxs-lookup"><span data-stu-id="257f3-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="257f3-125">多くの場合、あいまいな参照を防ぐために、後で参照するためにテーブル名を短くするために使用されます。<em>alias</em>が指定されていない場合は、テーブル名またはクエリ名がエイリアスとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="257f3-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="257f3-126">注釈</span><span class="sxs-lookup"><span data-stu-id="257f3-126">Remarks</span></span>

<span data-ttu-id="257f3-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span><span class="sxs-lookup"><span data-stu-id="257f3-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

