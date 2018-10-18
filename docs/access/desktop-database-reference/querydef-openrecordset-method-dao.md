---
title: QueryDef.OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: b4908c36-c156-e269-e2ad-b1fa20ec4884
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822070(v=office.15)
ms:contentKeyID: 48547232
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 368c59f0ea207862c5b7ac5ea7f664295adb5188
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606837"
---
# <a name="querydefopenrecordset-method-dao"></a><span data-ttu-id="493e4-102">QueryDef.OpenRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="493e4-102">QueryDef.OpenRecordset Method (DAO)</span></span>


<span data-ttu-id="493e4-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="493e4-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="493e4-104">新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成して **Recordsets** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="493e4-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="493e4-105">構文</span><span class="sxs-lookup"><span data-stu-id="493e4-105">Syntax</span></span>

<span data-ttu-id="493e4-106">*式*です。何らか (***型***、***オプション***、 ***LockEdit***)</span><span class="sxs-lookup"><span data-stu-id="493e4-106">*expression* .OpenRecordset(***Type***, ***Options***, ***LockEdit***)</span></span>

<span data-ttu-id="493e4-107">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="493e4-107">*expression* A variable that represents a **QueryDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="493e4-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="493e4-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="493e4-109">名前</span><span class="sxs-lookup"><span data-stu-id="493e4-109">Name</span></span></p></th>
<th><p><span data-ttu-id="493e4-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="493e4-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="493e4-111">データ型</span><span class="sxs-lookup"><span data-stu-id="493e4-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="493e4-112">説明</span><span class="sxs-lookup"><span data-stu-id="493e4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="493e4-113">種類</span><span class="sxs-lookup"><span data-stu-id="493e4-113">Type</span></span></p></td>
<td><p><span data-ttu-id="493e4-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="493e4-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="493e4-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="493e4-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="493e4-116">開く <a href="recordsettypeenum-enumeration-dao.md">Recordset</a> の型を示す <strong><strong>RecordsetTypeEnum</strong></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="493e4-116">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="493e4-p101">Microsoft Access ワークスペースで <STRONG>Recordset</STRONG> を開くときに、型を指定しない場合、<STRONG>OpenRecordset</STRONG> は、テーブル タイプの <STRONG>Recordset</STRONG> を作成します (可能な場合)。リンクされたテーブルまたはクエリを指定した場合、<STRONG>OpenRecordset</STRONG> は、ダイナセット タイプの <STRONG>Recordset</STRONG> を作成します。</span><span class="sxs-lookup"><span data-stu-id="493e4-p101">If you open a <STRONG>Recordset</STRONG> in a Microsoft Access workspace and you don't specify a type, <STRONG>OpenRecordset</STRONG> creates a table-type <STRONG>Recordset</STRONG>, if possible. If you specify a linked table or query, <STRONG>OpenRecordset</STRONG> creates a dynaset-type <STRONG>Recordset</STRONG>.</span></span></P>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="493e4-119">選択肢</span><span class="sxs-lookup"><span data-stu-id="493e4-119">Options</span></span></p></td>
<td><p><span data-ttu-id="493e4-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="493e4-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="493e4-121"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="493e4-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="493e4-122">新しい <a href="recordsetoptionenum-enumeration-dao.md">Recordset</a> の特性を指定する <strong><strong>RecordsetOptionEnum</strong></strong> 定数の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="493e4-122">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="493e4-p102">定数 <STRONG>dbConsistent</STRONG> と <STRONG>dbInconsistent</STRONG> は互いに排他的なので、この 2 つを同時に使用するとエラーになります。Options で <STRONG>dbReadOnly</STRONG> 定数を使用する場合に Lockedits 引数を指定してもエラーになります。</span><span class="sxs-lookup"><span data-stu-id="493e4-p102">The constants <STRONG>dbConsistent</STRONG> and <STRONG>dbInconsistent</STRONG> are mutually exclusive, and using both causes an error. Supplying a lockedits argument when options uses the <STRONG>dbReadOnly</STRONG> constant also causes an error.</span></span></P>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="493e4-125">LockEdit</span><span class="sxs-lookup"><span data-stu-id="493e4-125">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="493e4-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="493e4-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="493e4-127"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="493e4-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="493e4-128"><a href="locktypeenum-enumeration-dao.md">Recordset</a> のロックを決定する <strong><strong>LockTypeEnum</strong></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="493e4-128">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <P><span data-ttu-id="493e4-p103"><STRONG>dbReadOnly</STRONG> を Options 引数または Lockedits 引数のどちらか一方で使用することはできますが、両方で使用することはできません。両方の引数で使用した場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="493e4-p103">You can use <STRONG>dbReadOnly</STRONG> in either the options argument or the lockedits argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span></P>


</td>
</tr>
</tbody>
</table>


<span data-ttu-id="493e4-131"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="493e4-131"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="493e4-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="493e4-132">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="493e4-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="493e4-133">Return value</span></span>
>>>>>>> <span data-ttu-id="493e4-134">master</span><span class="sxs-lookup"><span data-stu-id="493e4-134">master</span></span>

<span data-ttu-id="493e4-135">Recordset</span><span class="sxs-lookup"><span data-stu-id="493e4-135">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="493e4-136">解説</span><span class="sxs-lookup"><span data-stu-id="493e4-136">Remarks</span></span>

<span data-ttu-id="493e4-137">IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの [Recordset](recordsetoptionenum-enumeration-dao.md) を開く場合は、 \*\*\*\*dbSeeChanges\*\*\*\* 定数も使用する必要があり、使用しないとエラーが生じます。</span><span class="sxs-lookup"><span data-stu-id="493e4-137">You should also use the **[dbSeeChanges](recordsetoptionenum-enumeration-dao.md)** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="493e4-p104">ODBC データ ソースで複数の **Recordset** を開こうとすると、 **OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、 **Recordset** を開いた直後に、 **[MoveLast](recordset-movelast-method-dao.md)** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。</span><span class="sxs-lookup"><span data-stu-id="493e4-p104">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **[MoveLast](recordset-movelast-method-dao.md)** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="493e4-140">**Close** メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。</span><span class="sxs-lookup"><span data-stu-id="493e4-140">Closing a **Recordset** with the **Close** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <P><span data-ttu-id="493e4-141"><EM>ソース</EM>を指す場合、整数以外の値に連結された文字列、SQL ステートメントで構成され、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定 (たとえば、strSQL ="価格&gt;" &amp; lngPrice でと lngPrice =125,50)、<STRONG>レコード セット</STRONG>を開こうとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="493e4-141">If <EM>source</EM> refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the <STRONG>Recordset</STRONG>.</span></span> <span data-ttu-id="493e4-142">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。</span><span class="sxs-lookup"><span data-stu-id="493e4-142">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span></P>


