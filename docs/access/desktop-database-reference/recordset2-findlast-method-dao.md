---
title: Recordset2.FindLast メソッド (DAO)
TOCTitle: FindLast Method
ms:assetid: 6a31dd00-8e05-6226-ebd8-703d2562b5c7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195400(v=office.15)
ms:contentKeyID: 48545428
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41ebfc954d15cfb5410cad344d6f12d3714c575a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477640"
---
# <a name="recordset2findlast-method-dao"></a><span data-ttu-id="effb9-102">Recordset2.FindLast メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="effb9-102">Recordset2.FindLast Method (DAO)</span></span>


<span data-ttu-id="effb9-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="effb9-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="effb9-104">ダイナセット タイプまたはスナップショット タイプの **[Recordset](recordset-object-dao.md)** オブジェクトで、指定された条件を満たす最後のレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="effb9-104">Locates the last record in a dynaset- or snapshot-type **[Recordset](recordset-object-dao.md)** object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="effb9-105">構文</span><span class="sxs-lookup"><span data-stu-id="effb9-105">Syntax</span></span>

<span data-ttu-id="effb9-106">*式*です。FindLast (***条件***)</span><span class="sxs-lookup"><span data-stu-id="effb9-106">*expression* .FindLast(***Criteria***)</span></span>

<span data-ttu-id="effb9-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="effb9-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="effb9-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="effb9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="effb9-109">名前</span><span class="sxs-lookup"><span data-stu-id="effb9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="effb9-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="effb9-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="effb9-111">データ型</span><span class="sxs-lookup"><span data-stu-id="effb9-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="effb9-112">説明</span><span class="sxs-lookup"><span data-stu-id="effb9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="effb9-113">基準</span><span class="sxs-lookup"><span data-stu-id="effb9-113">Criteria</span></span></p></td>
<td><p><span data-ttu-id="effb9-114">必須</span><span class="sxs-lookup"><span data-stu-id="effb9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="effb9-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="effb9-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="effb9-p101">レコードの検索に使用する文字列です。SQL ステートメントの WHERE 句に似ていますが、WHERE という語は付けません。</span><span class="sxs-lookup"><span data-stu-id="effb9-p101">A String used to locate the record. It is like the WHERE clause in an SQL statement, but without the word WHERE.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="effb9-118">注釈</span><span class="sxs-lookup"><span data-stu-id="effb9-118">Remarks</span></span>

<span data-ttu-id="effb9-p102">特定の条件を満たすレコードだけでなく、すべてのレコードを検索対象とする場合は、 **Move** メソッドを使用してレコード間を移動します。テーブル タイプの **Recordset** でレコードを検索するには、 **Seek** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="effb9-p102">If you want to include all the records in your search — not just those that meet a specific condition — use the **Move** methods to move from record to record. To locate a record in a table-type **Recordset**, use the **Seek** method.</span></span>

<span data-ttu-id="effb9-p103">条件を満たすレコードが検出されない場合、カレント レコードを参照するポインターは不明となり、 **NoMatch** プロパティが **True** に設定されます。recordset に条件を満たすレコードが複数含まれている場合の検出対象は、 **FindFirst** では最初に出現したもの、 **FindNext** では次に出現したもの、などとなります。</span><span class="sxs-lookup"><span data-stu-id="effb9-p103">If a record matching the criteria isn't located, the current record pointer is unknown, and the **NoMatch** property is set to **True**. If recordset contains more than one record that satisfies the criteria, **FindFirst** locates the first occurrence, **FindNext** locates the next occurrence, and so on.</span></span>

<span data-ttu-id="effb9-123">次の表に、各 **Find** メソッドの検索開始位置と検索方向を示します。</span><span class="sxs-lookup"><span data-stu-id="effb9-123">Each of the **Find** methods begins its search from the location and in the direction specified in the following table.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="effb9-124">Find メソッド</span><span class="sxs-lookup"><span data-stu-id="effb9-124">Find method</span></span></p></th>
<th><p><span data-ttu-id="effb9-125">検索開始位置</span><span class="sxs-lookup"><span data-stu-id="effb9-125">Begins searching at</span></span></p></th>
<th><p><span data-ttu-id="effb9-126">検索方向</span><span class="sxs-lookup"><span data-stu-id="effb9-126">Search direction</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="effb9-127"><strong>FindFirst</strong></span><span class="sxs-lookup"><span data-stu-id="effb9-127"><strong>FindFirst</strong></span></span></p></td>
<td><p><span data-ttu-id="effb9-128">レコードセットの先頭</span><span class="sxs-lookup"><span data-stu-id="effb9-128">Beginning of recordset</span></span></p></td>
<td><p><span data-ttu-id="effb9-129">レコードセットの末尾</span><span class="sxs-lookup"><span data-stu-id="effb9-129">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="effb9-130"><strong>FindLast</strong></span><span class="sxs-lookup"><span data-stu-id="effb9-130"><strong>FindLast</strong></span></span></p></td>
<td><p><span data-ttu-id="effb9-131">レコードセットの末尾</span><span class="sxs-lookup"><span data-stu-id="effb9-131">End of recordset</span></span></p></td>
<td><p><span data-ttu-id="effb9-132">レコードセットの先頭</span><span class="sxs-lookup"><span data-stu-id="effb9-132">Beginning of recordset</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="effb9-133"><strong>FindNext</strong></span><span class="sxs-lookup"><span data-stu-id="effb9-133"><strong>FindNext</strong></span></span></p></td>
<td><p><span data-ttu-id="effb9-134">カレント レコード</span><span class="sxs-lookup"><span data-stu-id="effb9-134">Current record</span></span></p></td>
<td><p><span data-ttu-id="effb9-135">レコードセットの末尾</span><span class="sxs-lookup"><span data-stu-id="effb9-135">End of recordset</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="effb9-136"><strong>FindPrevious</strong></span><span class="sxs-lookup"><span data-stu-id="effb9-136"><strong>FindPrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="effb9-137">カレント レコード</span><span class="sxs-lookup"><span data-stu-id="effb9-137">Current record</span></span></p></td>
<td><p><span data-ttu-id="effb9-138">レコードセットの先頭</span><span class="sxs-lookup"><span data-stu-id="effb9-138">Beginning of recordset</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="effb9-139">**Recordset** の末尾までデータが格納されていない状態で **FindLast** メソッドを使用すると、検索が始まる前に、Microsoft Access データベース エンジンによってレコードセットが末尾まで埋められます。</span><span class="sxs-lookup"><span data-stu-id="effb9-139">When you use the **FindLast** method, the Microsoft Access database engine fully populates your **Recordset** before beginning the search, if this hasn't already happened.</span></span>

<span data-ttu-id="effb9-p104">ただし、いずれかの **Find** メソッドを使用した場合と、 **Move** メソッドを使用した場合の結果は同じではありません。後者は、条件を指定せずに、最初のレコード、最後のレコード、次のレコード、または前のレコードをカレント レコードにするだけです。Find 操作の後に Move 操作を使用する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="effb9-p104">Using one of the **Find** methods isn't the same as using a **Move** method, however, which simply makes the first, last, next, or previous record current without specifying a condition. You can follow a Find operation with a Move operation.</span></span>

<span data-ttu-id="effb9-p105">**NoMatch** プロパティの値を必ず確認して、Find 操作が成功したかどうか調べてください。検索が成功した場合、 **NoMatch** は **False** です。失敗した場合、 **NoMatch** は **True** で、カレント レコードは未定義となります。この場合は、カレント レコードを参照するポインターを有効なレコードに戻す必要があります。</span><span class="sxs-lookup"><span data-stu-id="effb9-p105">Always check the value of the **NoMatch** property to determine whether the Find operation has succeeded. If the search succeeds, **NoMatch** is **False**. If it fails, **NoMatch** is **True** and the current record isn't defined. In this case, you must position the current record pointer back to a valid record.</span></span>

<span data-ttu-id="effb9-p106">**Find** メソッドを Microsoft Access データベース エンジンに接続された ODBC アクセスのレコードセットで使用すると、効率が悪い場合があります。特に大きなレコードセットを操作するときは、criteria の表現を変更すると、より迅速に特定のレコードを検出できる場合があります。</span><span class="sxs-lookup"><span data-stu-id="effb9-p106">Using the **Find** methods with Microsoft Access database engine-connected ODBC-accessed recordsets can be inefficient. You may find that rephrasing your criteria to locate a specific record is faster, especially when working with large recordsets.</span></span>

<span data-ttu-id="effb9-p107">Microsoft Access データベース エンジンに接続している ODBC データベースでダイナセット タイプの大きな **Recordset** オブジェクトを操作している場合、 **Find** メソッド、 **Sort** プロパティ、または **Filter** プロパティを使用すると、処理速度が遅いことがあります。パフォーマンスを向上するには、カスタマイズした ORDER BY 句または WHERE 句のある SQL クエリ、パラメーター クエリ、またはインデックスが作成されている特定のレコードを取得する **QueryDef** オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="effb9-p107">When working with Microsoft Access database engine-connected ODBC databases and large dynaset-type **Recordset** objects, you might discover that using the **Find** methods or using the **Sort** or **Filter** property is slow. To improve performance, use SQL queries with customized ORDER BY or WHERE clauses, parameter queries, or **QueryDef** objects that retrieve specific indexed records.</span></span>

<span data-ttu-id="effb9-p108">日付を含むフィールドを検索するときは、米国バージョンの Microsoft Access データベース エンジンを使用していない場合でも、米国の日付形式 (month-day-year) を使用する必要があります。それ以外の日付形式を使用すると、データが検出されない場合があります。日付を変換するには、Visual Basic の **Format** 関数を使用します。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="effb9-p108">You should use the U.S. date format (month-day-year) when you search for fields containing dates, even if you're not using the U.S. version of the Microsoft Access database engine; otherwise, the data may not be found. Use the Visual Basic **Format** function to convert the date. For example:</span></span>

```vb
rstEmployees.FindFirst "HireDate > #" _ 
        & Format(mydate, 'm-d-yy' ) & "#" 
```

<span data-ttu-id="effb9-153">基準は、整数以外の値に連結された文字列の作成し、システムのパラメーターは、米国以外の小数点の記号、カンマなどを指定する場合 (たとえば、strSQL ="価格\>"& lngPrice でと lngPrice = 125,50) をしようとするときにエラーが発生しました。メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="effb9-153">If criteria is composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE \> " & lngPrice, and lngPrice = 125,50), an error occurs when you try to call the method.</span></span> <span data-ttu-id="effb9-154">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="effb9-154">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>


> [!NOTE]
> <UL>
> <LI>
> <P><span data-ttu-id="effb9-155">最高のパフォーマンスを<EM>基準</EM>する必要がありますいずれかの方法でフォーム"<EM>フィールド</EM> = <EM>値</EM>"<EM>フィールド</EM>が、インデックス付きのフィールド内にある基になるベース テーブル、または「<EM>フィールド</EM><EM>のプレフィックス</EM>と同じように」<EM>フィールド</EM>がある、<EM>プレフィックス</EM>と基になるベース テーブルでインデックス付きのフィールドは、プレフィックス検索文字列 (たとえば、「アート \*」) です。</span><span class="sxs-lookup"><span data-stu-id="effb9-155">For best performance, the <EM>criteria</EM> should be in either the form "<EM>field</EM> = <EM>value</EM>" where <EM>field</EM> is an indexed field in the underlying base table, or "<EM>field</EM> LIKE <EM>prefix</EM>" where <EM>field</EM> is an indexed field in the underlying base table and <EM>prefix</EM> is a prefix search string (for example, "ART\*" ).</span></span></P>
> <LI>
> <P><span data-ttu-id="effb9-p110">一般に、同じような検索を行う場合は、 <STRONG>Find</STRONG> メソッドよりも <STRONG>Seek</STRONG> メソッドを使用する方がパフォーマンスが優れています。ただし、これを使用できるのは、テーブル タイプの <STRONG>Recordset</STRONG> オブジェクトだけを検索対象とする場合です。</span><span class="sxs-lookup"><span data-stu-id="effb9-p110">In general, for equivalent types of searches, the <STRONG>Seek</STRONG> method provides better performance than the <STRONG>Find</STRONG> methods. This assumes that table-type <STRONG>Recordset</STRONG> objects alone can satisfy your needs.</span></span></P></LI></UL>

