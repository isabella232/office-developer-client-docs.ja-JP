---
title: ForEachRecord データ ブロック
TOCTitle: ForEachRecord data block
ms:assetid: be369196-230e-1f92-e36b-667048eef2be
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822743(v=office.15)
ms:contentKeyID: 48547455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 84ab685b946e390645027790e5b1402561527ab6
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706346"
---
# <a name="foreachrecord-data-block"></a><span data-ttu-id="3645d-102">ForEachRecord データ ブロック</span><span class="sxs-lookup"><span data-stu-id="3645d-102">ForEachRecord data block</span></span>

<span data-ttu-id="3645d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="3645d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3645d-104">**ForEachRecord** データ ブロックは、ドメイン内のレコードごとにステートメントのセットを繰り返します。</span><span class="sxs-lookup"><span data-stu-id="3645d-104">A **ForEachRecord** data block repeats a set of statements for each record in a domain.</span></span>

> [!NOTE]
> <span data-ttu-id="3645d-105">[!メモ] **ForEachRecord** データ ブロックは、データ マクロでのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="3645d-105">The **ForEachRecord** data block is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="3645d-106">設定</span><span class="sxs-lookup"><span data-stu-id="3645d-106">Setting</span></span>

<span data-ttu-id="3645d-107">" **ForEachRecord** /レコードごと" アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="3645d-107">The **ForEachRecord** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3645d-108">引数</span><span class="sxs-lookup"><span data-stu-id="3645d-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="3645d-109">必須</span><span class="sxs-lookup"><span data-stu-id="3645d-109">Required</span></span></p></th>
<th><p><span data-ttu-id="3645d-110">説明</span><span class="sxs-lookup"><span data-stu-id="3645d-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3645d-111"><strong>で</strong></span><span class="sxs-lookup"><span data-stu-id="3645d-111"><strong>In</strong></span></span></p></td>
<td><p><span data-ttu-id="3645d-112">はい</span><span class="sxs-lookup"><span data-stu-id="3645d-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="3645d-p101">ステートメントを実行するレコードのドメインを識別する文字列を指定します。<em>In</em> 引数には、テーブル名、選択クエリ、または SQL ステートメントを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="3645d-p101">A string that identifies the domain of records to operate on. The <em>In</em> argument can contain the name of the table, a select query, or a SQL statement.</span></span></p><p><span data-ttu-id="3645d-115"><strong>注</strong>: 指定されたドメインにリンクされているテーブルまたは ODBC データ ソースに格納されたデータを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="3645d-115"><strong>NOTE</strong>: The specified domain cannot include data stored in a linked table or ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3645d-116"><strong>Where Condition</strong></span><span class="sxs-lookup"><span data-stu-id="3645d-116"><strong>Where Condition</strong></span></span></p></td>
<td><p><span data-ttu-id="3645d-117">いいえ</span><span class="sxs-lookup"><span data-stu-id="3645d-117">No</span></span></p></td>
<td><p><span data-ttu-id="3645d-p102"><strong>ForEachRecord</strong> データ ブロックを適用するデータの範囲を制限するための文字列式を指定します。たとえば、多くの場合、抽出条件は SQL 式の WHERE 句と同じ役割を果たします (ただし WHERE という語は使用しません)。抽出条件を省略すると、<strong>ForEachRecord</strong> データ ブロックは In<em></em> 引数で指定したドメイン全体に適用されます。抽出条件に含めるフィールドは、In<em></em> にも含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="3645d-p102">A string expression used to restrict the range of data on which the <strong>ForEachRecord</strong> data block is performed. For example, criteria is often equivalent to the WHERE clause in an SQL expression, without the word WHERE. If criteria is omitted, the <strong>ForEachRecord</strong> data block operates on the entire domain specified by the <em>In</em> argument. Any field that is included in criteria must also be a field in <em>In</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3645d-122"><strong>Alias</strong></span><span class="sxs-lookup"><span data-stu-id="3645d-122"><strong>Alias</strong></span></span></p></td>
<td><p><span data-ttu-id="3645d-123">いいえ</span><span class="sxs-lookup"><span data-stu-id="3645d-123">No</span></span></p></td>
<td><p><span data-ttu-id="3645d-124"><em></em>引数で指定されたドメインの代替名を提供する文字列です。</span><span class="sxs-lookup"><span data-stu-id="3645d-124">A string that provides an alternative name for the domain specified by the <em>In</em> argument.</span></span> <span data-ttu-id="3645d-125">あいまいな参照を防ぐへの参照のテーブル名を短くには、よく使用されます。<em>エイリアス</em>が指定されていない場合、テーブルまたはクエリの名前がエイリアスとして使用します。</span><span class="sxs-lookup"><span data-stu-id="3645d-125">Often used to shorten the table name for subsequent references to prevent possible ambiguous references.If <em>Alias</em> is not specified, the table or query name will be used as the alias.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3645d-126">注釈</span><span class="sxs-lookup"><span data-stu-id="3645d-126">Remarks</span></span>

<span data-ttu-id="3645d-127">[ForEachRecord](exitforeachrecord-macro-action.md) データ ブロックを即座に終了するには、" \*\*\*\*ExitForEachRecord/レコードごとに終了\*\*\*\* " アクションを使用します。</span><span class="sxs-lookup"><span data-stu-id="3645d-127">Use the **[ExitForEachRecord](exitforeachrecord-macro-action.md)** action to exit a **ForEachRecord** data block immediately.</span></span>

