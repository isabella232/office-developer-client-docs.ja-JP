---
title: Recordset.OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: 7d5ca4d5-5a0b-c0c8-d8e8-2c4e6c5f361f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196402(v=office.15)
ms:contentKeyID: 48545853
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 11d525abdb7c5cbd4ef72e81d856d2abfc6a3045
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284491"
---
# <a name="recordsetopenrecordset-method-dao"></a><span data-ttu-id="90e41-102">Recordset.OpenRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="90e41-102">Recordset.OpenRecordset Method (DAO)</span></span>

<span data-ttu-id="90e41-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="90e41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="90e41-104">新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成し、**Recordsets** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="90e41-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e41-105">構文</span><span class="sxs-lookup"><span data-stu-id="90e41-105">Syntax</span></span>

<span data-ttu-id="90e41-106">*式* 。OpenRecordset(***Type***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="90e41-106">*expression* .OpenRecordset(***Type***, ***Options***)</span></span>

<span data-ttu-id="90e41-107">*式* **Recordset** オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="90e41-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="90e41-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="90e41-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="90e41-109">名前</span><span class="sxs-lookup"><span data-stu-id="90e41-109">Name</span></span></p></th>
<th><p><span data-ttu-id="90e41-110">必須 / オプション</span><span class="sxs-lookup"><span data-stu-id="90e41-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="90e41-111">データ型</span><span class="sxs-lookup"><span data-stu-id="90e41-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="90e41-112">説明</span><span class="sxs-lookup"><span data-stu-id="90e41-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90e41-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="90e41-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="90e41-114">必須</span><span class="sxs-lookup"><span data-stu-id="90e41-114">Required</span></span></p></td>
<td><p><span data-ttu-id="90e41-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="90e41-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="90e41-p101">新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Office Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。</span><span class="sxs-lookup"><span data-stu-id="90e41-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e41-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="90e41-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="90e41-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="90e41-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="90e41-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="90e41-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="90e41-122"><strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong>は、開くための<strong>Recordset</strong> の型を示す定数。</span><span class="sxs-lookup"><span data-stu-id="90e41-122">A <a href="recordsettypeenum-enumeration-dao.md"><strong>RecordsetTypeEnum</strong></a> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="90e41-123"><strong>注</strong>: Microsoft Access ワークスペースで <STRONG>Recordset</STRONG> を開き、型を指定しない場合、可能であれば<STRONG>OpenRecordset</STRONG>はテーブル タイプの <STRONG>Recordset</STRONG> を作成します。</span><span class="sxs-lookup"><span data-stu-id="90e41-123"> > If you open a Recordset in a Microsoft Access workspace and you don't specify a type, OpenRecordset creates a table-type Recordset, if possible.</span></span> <span data-ttu-id="90e41-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="90e41-124">If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90e41-125"><em>オプション</em></span><span class="sxs-lookup"><span data-stu-id="90e41-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="90e41-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="90e41-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="90e41-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="90e41-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="90e41-128">新しい<strong>Recordset</strong>の特性を指定する<strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong>定数の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="90e41-128">A combination of <a href="recordsetoptionenum-enumeration-dao.md"><strong>RecordsetOptionEnum</strong></a> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="90e41-129"><strong>注</strong>: 定数 <STRONG>dbConsistent</STRONG> と <STRONG>dbInconsistent</STRONG> は互いに排他的なので、この 2 つを同時に使用するとエラーになります。</span><span class="sxs-lookup"><span data-stu-id="90e41-129">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="90e41-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span><span class="sxs-lookup"><span data-stu-id="90e41-130">Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90e41-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="90e41-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="90e41-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="90e41-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="90e41-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="90e41-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="90e41-134"><strong>Recordset</strong> のロックを決定する <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="90e41-134">A <a href="locktypeenum-enumeration-dao.md"><strong>LockTypeEnum</strong></a> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p></p><p><span data-ttu-id="90e41-135"><strong>注</strong>: <STRONG>dbReadOnly</STRONG> を Options 引数または Lockedits 引数のどちらか一方で使用することはできますが、両方で使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="90e41-135">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both.</span></span> <span data-ttu-id="90e41-136">両方の引数で使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="90e41-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="90e41-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="90e41-137">Return value</span></span>

<span data-ttu-id="90e41-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="90e41-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="90e41-139">注釈</span><span class="sxs-lookup"><span data-stu-id="90e41-139">Remarks</span></span>

<span data-ttu-id="90e41-p105">通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新たに変更された値を取得するコードを記述します。レコードを削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。この時点で、レコードを削除するかどうかの確認をユーザーに求めることができます。</span><span class="sxs-lookup"><span data-stu-id="90e41-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="90e41-143">IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、**dbSeeChanges** 定数も使用する必要があり、使用しないとエラーが生じます。</span><span class="sxs-lookup"><span data-stu-id="90e41-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="90e41-p106">ODBC データ ソースで複数の **Recordset** を開こうとすると、**OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、**Recordset** を開いた直後に、**MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。</span><span class="sxs-lookup"><span data-stu-id="90e41-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="90e41-146">**[Close](connection-close-method-dao.md)** メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。</span><span class="sxs-lookup"><span data-stu-id="90e41-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>

> [!NOTE]
> <span data-ttu-id="90e41-147">*source* が文字列と非整数値を連結したもので構成される SQL ステートメントを示し、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が使用されている場合 (たとえば、strSQL = "PRICE &gt; " &amp; lngPrice と lngPrice = 125,50)、**Recordset** を開こうとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="90e41-147">If source refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the Recordset.</span></span> <span data-ttu-id="90e41-148">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。</span><span class="sxs-lookup"><span data-stu-id="90e41-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>


