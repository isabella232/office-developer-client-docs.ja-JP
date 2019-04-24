---
title: OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: da6ce86e-957e-21f8-07ac-8acd57326a12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835325(v=office.15)
ms:contentKeyID: 48548082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 08120f4ebb6b2d9989051171a0c71b6d9fcf6e5c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307253"
---
# <a name="recordset2openrecordset-method-dao"></a><span data-ttu-id="972dd-102">OpenRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="972dd-102">Recordset2.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="972dd-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="972dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="972dd-104">新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成して **Recordsets** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="972dd-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="972dd-105">構文</span><span class="sxs-lookup"><span data-stu-id="972dd-105">Syntax</span></span>

<span data-ttu-id="972dd-106">*式*。OpenRecordset ([***種類***]、[***オプション]***)</span><span class="sxs-lookup"><span data-stu-id="972dd-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="972dd-107">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="972dd-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="972dd-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="972dd-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="972dd-109">名前</span><span class="sxs-lookup"><span data-stu-id="972dd-109">Name</span></span></p></th>
<th><p><span data-ttu-id="972dd-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="972dd-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="972dd-111">データ型</span><span class="sxs-lookup"><span data-stu-id="972dd-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="972dd-112">説明</span><span class="sxs-lookup"><span data-stu-id="972dd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="972dd-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="972dd-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="972dd-114">必須</span><span class="sxs-lookup"><span data-stu-id="972dd-114">Required</span></span></p></td>
<td><p><span data-ttu-id="972dd-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="972dd-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="972dd-p101">新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。  </span><span class="sxs-lookup"><span data-stu-id="972dd-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="972dd-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="972dd-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="972dd-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="972dd-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="972dd-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="972dd-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="972dd-122">開く<strong>Recordset</strong>の種類を示す<strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="972dd-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="972dd-123"><strong>注</strong>: Microsoft access ワークスペースで<STRONG>レコードセット</STRONG>を開き、種類を指定しない場合、 <STRONG>OpenRecordset</STRONG>はテーブルタイプの<STRONG>recordset</STRONG>を作成します (可能な場合)。</span><span class="sxs-lookup"><span data-stu-id="972dd-123"><strong>NOTE</strong>: If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible.</span></span> <span data-ttu-id="972dd-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="972dd-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="972dd-125"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="972dd-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="972dd-126">Optional</span><span class="sxs-lookup"><span data-stu-id="972dd-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="972dd-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="972dd-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="972dd-128">新しい<strong>Recordset</strong>の特性を指定する<strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>定数の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="972dd-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="972dd-129"><strong>注</strong>: <STRONG>dbconsistent</STRONG>および<STRONG>dbInconsistent</STRONG>定数は相互に排他的です。両方を使用するとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="972dd-129"><strong>NOTE</strong>: The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="972dd-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span><span class="sxs-lookup"><span data-stu-id="972dd-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="972dd-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="972dd-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="972dd-132">Optional</span><span class="sxs-lookup"><span data-stu-id="972dd-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="972dd-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="972dd-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="972dd-134"><strong>Recordset</strong>のロックを決定する<strong><a href="locktypeenum-enumeration-dao.md">locktypeenum</a></strong>定数。</span><span class="sxs-lookup"><span data-stu-id="972dd-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="972dd-135"><strong>注</strong>: <STRONG>dbreadonly</STRONG>は、options 引数または lockedits 引数のいずれかで使用できますが、両方を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="972dd-135"><strong>NOTE</strong>: You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="972dd-136">If you use it for both arguments, a run-time error occurs.</span><span class="sxs-lookup"><span data-stu-id="972dd-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="972dd-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="972dd-137">Return value</span></span>

<span data-ttu-id="972dd-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="972dd-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="972dd-139">注釈</span><span class="sxs-lookup"><span data-stu-id="972dd-139">Remarks</span></span>

<span data-ttu-id="972dd-p105">通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新たに変更された値を取得するコードを記述します。レコードを削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。この時点で、レコードを削除するかどうかの確認をユーザーに求めることができます。</span><span class="sxs-lookup"><span data-stu-id="972dd-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="972dd-143">IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、定数 **dbSeeChanges** も使用する必要があり、使用しないとエラーが生じます。</span><span class="sxs-lookup"><span data-stu-id="972dd-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="972dd-p106">ODBC データ ソースで複数の **Recordset** を開こうとすると、 **OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、 **Recordset** を開いた直後に、 **MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。</span><span class="sxs-lookup"><span data-stu-id="972dd-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="972dd-146">[**Close**](connection-close-method-dao.md) メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。</span><span class="sxs-lookup"><span data-stu-id="972dd-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="972dd-147">*source*が整数以外の値で連結された文字列で構成されている SQL ステートメントを参照しており、システムパラメーターでコンマ以外の小数点 (たとえば、strsql = "PRICE &gt; " &amp; lngPrice、lngPrice = など) を指定している場合。125, 50) **Recordset**を開こうとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="972dd-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="972dd-148">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。</span><span class="sxs-lookup"><span data-stu-id="972dd-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


