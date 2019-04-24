---
title: Recordset の findprevious メソッド (DAO)
TOCTitle: FindPrevious Method
ms:assetid: 62f26b0b-f3f1-a6fe-e84d-f93623e1f7f9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194940(v=office.15)
ms:contentKeyID: 48545252
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052885
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: bbd678c460ed6c54a38e76faa2a2492cfd4e3384
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300491"
---
# <a name="recordsetfindprevious-method-dao"></a><span data-ttu-id="b658e-102">Recordset の findprevious メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="b658e-102">Recordset.FindPrevious method (DAO)</span></span>

<span data-ttu-id="b658e-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="b658e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b658e-p101">ダイナセット タイプまたはスナップショット タイプの **[Recordset](recordset-object-dao.md)** オブジェクトで、指定された条件を満たす前のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="b658e-p101">Locates the previous record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="b658e-106">構文</span><span class="sxs-lookup"><span data-stu-id="b658e-106">Syntax</span></span>

<span data-ttu-id="b658e-107">*式*。findprevious (***抽出条件***)</span><span class="sxs-lookup"><span data-stu-id="b658e-107">*expression* .FindPrevious(***Criteria***)</span></span>

<span data-ttu-id="b658e-108">\*式\***Recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="b658e-108">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="b658e-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b658e-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b658e-110">名前</span><span class="sxs-lookup"><span data-stu-id="b658e-110">Name</span></span></p></th>
<th><p><span data-ttu-id="b658e-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="b658e-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="b658e-112">データ型</span><span class="sxs-lookup"><span data-stu-id="b658e-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="b658e-113">説明</span><span class="sxs-lookup"><span data-stu-id="b658e-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b658e-114"><em>Criteria</em></span><span class="sxs-lookup"><span data-stu-id="b658e-114"><em>Criteria</em></span></span></p></td>
<td><p><span data-ttu-id="b658e-115">必須</span><span class="sxs-lookup"><span data-stu-id="b658e-115">Required</span></span></p></td>
<td><p><span data-ttu-id="b658e-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="b658e-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="b658e-117">レコードの検索に使用する文字列です。</span><span class="sxs-lookup"><span data-stu-id="b658e-117">A String used to locate the record.</span></span> <span data-ttu-id="b658e-118">SQL ステートメントの WHERE 句に似ていますが、WHERE という語は付けません。</span><span class="sxs-lookup"><span data-stu-id="b658e-118">It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="b658e-119">注釈</span><span class="sxs-lookup"><span data-stu-id="b658e-119">Remarks</span></span>

<span data-ttu-id="b658e-p103">特定の条件を満たすレコードだけでなく、すべてのレコードを検索対象とする場合は、 **Move** メソッドを使用してレコード間を移動します。テーブル タイプの **Recordset** でレコードを検索するには、 **Seek** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="b658e-p103">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="b658e-p104">条件を満たすレコードが検出されない場合、カレント レコードを参照するポインターは不明となり、 **NoMatch** プロパティが **True** に設定されます。recordset に条件を満たすレコードが複数含まれている場合の検出対象は、 **FindFirst** では最初に出現したもの、 **FindNext** では次に出現したもの、などとなります。</span><span class="sxs-lookup"><span data-stu-id="b658e-p104">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="b658e-124">次の表に、各 **Find** メソッドの検索開始位置と検索方向を示します。</span><span class="sxs-lookup"><span data-stu-id="b658e-124">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b658e-125">Find メソッド</span><span class="sxs-lookup"><span data-stu-id="b658e-125">Find method</span></span></p></th>
<th><p><span data-ttu-id="b658e-126">検索開始位置</span><span class="sxs-lookup"><span data-stu-id="b658e-126">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="b658e-127">検索方向</span><span class="sxs-lookup"><span data-stu-id="b658e-127">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b658e-128"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="b658e-128"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="b658e-129">レコードセットの先頭</span><span class="sxs-lookup"><span data-stu-id="b658e-129">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="b658e-130">レコードセットの末尾</span><span class="sxs-lookup"><span data-stu-id="b658e-130">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b658e-131"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="b658e-131"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="b658e-132">レコードセットの末尾</span><span class="sxs-lookup"><span data-stu-id="b658e-132">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="b658e-133">レコードセットの先頭</span><span class="sxs-lookup"><span data-stu-id="b658e-133">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b658e-134"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="b658e-134"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="b658e-135">カレント レコード</span><span class="sxs-lookup"><span data-stu-id="b658e-135">Current record</span></span></p></td>
<td><p><span data-ttu-id="b658e-136">レコードセットの末尾</span><span class="sxs-lookup"><span data-stu-id="b658e-136">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b658e-137"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="b658e-137"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="b658e-138">カレント レコード</span><span class="sxs-lookup"><span data-stu-id="b658e-138">Current record</span></span></p></td>
<td><p><span data-ttu-id="b658e-139">レコードセットの先頭</span><span class="sxs-lookup"><span data-stu-id="b658e-139">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b658e-p105">ただし、いずれかの **Find** メソッドを使用した場合と、 **Move** メソッドを使用した場合の結果は同じではありません。後者は、条件を指定せずに、最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするだけです。Find 操作の後に Move 操作を使用する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="b658e-p105">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="b658e-p106">**NoMatch** プロパティの値を必ず確認して、Find 操作が成功したかどうか調べてください。検索が成功した場合、 **NoMatch** は **False** です。失敗した場合、 **NoMatch** は **True** で、カレント レコードは未定義となります。この場合は、カレント レコードを参照するポインターを有効なレコードに戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="b658e-p106">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="b658e-p107">**Find** メソッドを Microsoft Access データベース エンジンに接続された ODBC アクセスのレコードセットで使用すると、効率が悪い場合があります。特に大きなレコードセットを操作するときは、criteria の表現を変更すると、より迅速に特定のレコードを検出できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="b658e-p107">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="b658e-p108">Microsoft Access データベース エンジンに接続している ODBC データベースでダイナセット タイプの大きな **Recordset** オブジェクトを操作している場合、 **Find** メソッド、 **Sort** プロパティ、または **Filter** プロパティを使用すると、処理速度が遅いことがあります。パフォーマンスを向上するには、カスタマイズした ORDER BY 句または WHERE 句のある SQL クエリ、パラメーター クエリ、またはインデックスが作成されている特定のレコードを取得する **QueryDef** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="b658e-p108">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="b658e-p109">日本語版の Microsoft Access データベース エンジンを使用する場合であっても、日付が格納されたフィールドを検索するときは米国の日付形式 (month-day-year) を使用することが推奨され、使用しないとデータが検出されないことがあります。Visual Basic の **Format** 関数を使用して、日付を変換してください。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="b658e-p109">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
    rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="b658e-153">criteria が整数以外の値で連結された文字列で構成されており、システムパラメーターでコンマ以外の小数点 (例: strsql = "PRICE \> " & lngPrice, and lngPrice = 125, 50) を指定した場合は、次の操作を実行するとエラーが発生します。メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="b658e-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="b658e-154">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Access の SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="b658e-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>

> [!NOTE]
> - <span data-ttu-id="b658e-155">\*\* 最適なパフォーマンスを得るには、*条件*が、基になるベーステーブルのインデックス付きフィールドであるか、"field LIKE *prefix*" で\*\* あるというフォームの\*\* "*フィールド* = *値*" である必要があります。基になるベーステーブルと*プレフィックス*のインデックスフィールドは、プレフィックス検索文字列 ("ART \*" など) です。</span><span class="sxs-lookup"><span data-stu-id="b658e-155">For best performance, the *criteria* should be in either the form "*field* = *value*" where *field* is an indexed field in the underlying base table, or "*field* LIKE *prefix*" where *field* is an indexed field in the underlying base table and *prefix* is a prefix search string (for example, "ART\*").</span></span>
> - <span data-ttu-id="b658e-p111">一般に、同じような検索を行う場合は、 **Find** メソッドよりも **Seek** メソッドを使用する方がパフォーマンスが優れています。ただし、これを使用できるのは、テーブル タイプの **Recordset** オブジェクトだけを検索対象とする場合です。</span><span class="sxs-lookup"><span data-stu-id="b658e-p111">In general, for equivalent types of searches, the **Seek** method provides better performance than the **Find** methods. This assumes that table-type **Recordset** objects alone can satisfy your needs.</span></span>
