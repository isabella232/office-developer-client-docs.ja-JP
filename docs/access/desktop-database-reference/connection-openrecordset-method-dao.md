---
title: Connection.OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 584a3e00-7589-90f1-aa6a-5d6116f0b5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194324(v=office.15)
ms:contentKeyID: 48544993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 059d701ec2eba8ece48978221696bbbc8bad06e4
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997029"
---
# <a name="connectionopenrecordset-method-dao"></a><span data-ttu-id="bb2df-102">Connection.OpenRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="bb2df-102">Connection.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="bb2df-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bb2df-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb2df-104">新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成して **Recordsets** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="bb2df-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb2df-105">構文</span><span class="sxs-lookup"><span data-stu-id="bb2df-105">Syntax</span></span>

<span data-ttu-id="bb2df-106">*式*です。何らかの (***名前***、***型***、***オプション***、 ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="bb2df-106">*expression* .OpenRecordset(***Name***, ***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="bb2df-107">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="bb2df-107">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb2df-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb2df-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bb2df-109">名前</span><span class="sxs-lookup"><span data-stu-id="bb2df-109">Name</span></span></p></th>
<th><p><span data-ttu-id="bb2df-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="bb2df-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="bb2df-111">データ型</span><span class="sxs-lookup"><span data-stu-id="bb2df-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="bb2df-112">説明</span><span class="sxs-lookup"><span data-stu-id="bb2df-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb2df-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="bb2df-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="bb2df-114">必須</span><span class="sxs-lookup"><span data-stu-id="bb2df-114">Required</span></span></p></td>
<td><p><span data-ttu-id="bb2df-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="bb2df-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="bb2df-p101">新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。  </span><span class="sxs-lookup"><span data-stu-id="bb2df-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb2df-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="bb2df-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="bb2df-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="bb2df-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="bb2df-121"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="bb2df-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="bb2df-122">開く <a href="recordsettypeenum-enumeration-dao.md">Recordset</a> の型を示す <strong><strong>RecordsetTypeEnum</strong></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="bb2df-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="bb2df-123"><strong>注</strong>:<strong><strong>レコード セット</strong>を開くには、Microsoft Access ワークスペースで、種類を指定しない場合は、作成、テーブル タイプの<strong>レコード セット</strong>可能な場合</strong>です。</span><span class="sxs-lookup"><span data-stu-id="bb2df-123"><strong>NOTE</strong>: If you open a <strong>Recordset</strong> in a Microsoft Access workspace and you don't specify a type, <strong>OpenRecordset</strong> creates a table-type <strong>Recordset</strong>, if possible.</span></span> <span data-ttu-id="bb2df-124"><strong>リンク テーブルまたはクエリを指定する場合、ダイナセット タイプの<strong>レコード セット</strong>が作成します。</strong></span><span class="sxs-lookup"><span data-stu-id="bb2df-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb2df-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="bb2df-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="bb2df-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="bb2df-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="bb2df-127"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="bb2df-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="bb2df-128">新しい <a href="recordsetoptionenum-enumeration-dao.md">Recordset</a> の特性を指定する <strong><strong>RecordsetOptionEnum</strong></strong> 定数の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="bb2df-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="bb2df-129"><strong>注</strong>: 定数を<strong>指定できます</strong>し、<strong>組み合わせて</strong>が、相互に排他的で両方を使用して、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bb2df-129"><strong>NOTE</strong>: The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="bb2df-130"><strong>DbReadOnly</strong>定数を使用するオプションと、lockedits 引数を指定すると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bb2df-130">Supplying a lockedits argument when options use the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb2df-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="bb2df-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="bb2df-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="bb2df-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="bb2df-133"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="bb2df-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="bb2df-134"><a href="locktypeenum-enumeration-dao.md">Recordset</a> のロックを決定する <strong><strong>LockTypeEnum</strong></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="bb2df-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="bb2df-135"><strong>注</strong>: オプションの引数と、引数 lockedits の片方だけに<strong>dbReadOnly</strong>を使用することができます。</span><span class="sxs-lookup"><span data-stu-id="bb2df-135"><strong>NOTE</strong>: You can use <strong>dbReadOnly</strong> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="bb2df-136">で両方の引数を使用する場合は、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bb2df-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="bb2df-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="bb2df-137">Return value</span></span>

<span data-ttu-id="bb2df-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="bb2df-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="bb2df-139">注釈</span><span class="sxs-lookup"><span data-stu-id="bb2df-139">Remarks</span></span>

<span data-ttu-id="bb2df-p105">通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新しく変更された値を取得するコードを記述します。レコードの削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。このとき、レコードを削除してもよいかどうかユーザーに確認できます。</span><span class="sxs-lookup"><span data-stu-id="bb2df-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="bb2df-143">IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、 **dbSeeChanges** 定数も使用する必要があり、使用しないとエラーが生じます。</span><span class="sxs-lookup"><span data-stu-id="bb2df-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="bb2df-p106">ODBC データ ソースで複数の **Recordset** を開こうとすると、 **OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、 **Recordset** を開いた直後に、 **MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。</span><span class="sxs-lookup"><span data-stu-id="bb2df-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="bb2df-146">[**Close**](connection-close-method-dao.md) メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。</span><span class="sxs-lookup"><span data-stu-id="bb2df-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="bb2df-147">*ソース*を指す場合、整数以外の値に連結された文字列、SQL ステートメントで構成され、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定 (たとえば、strSQL ="価格&gt;" &amp; lngPrice でと lngPrice =125,50)、**レコード セット**を開こうとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="bb2df-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="bb2df-148">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。</span><span class="sxs-lookup"><span data-stu-id="bb2df-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


