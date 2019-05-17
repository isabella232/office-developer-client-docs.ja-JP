---
title: Database.OpenRecordset メソッド (DAO)
TOCTitle: OpenRecordset Method
ms:assetid: a243bc79-cac4-fe12-768d-d3d017954e78
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820966(v=office.15)
ms:contentKeyID: 48546753
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052939
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 73bb48db5b47ff1824e962ac44324a17ae0636ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294839"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="a74b0-102">Database.OpenRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="a74b0-102">Database.OpenRecordset Method (DAO)</span></span>

<span data-ttu-id="a74b0-103">**適用先**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a74b0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a74b0-104">新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成し、**Recordsets** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="a74b0-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a74b0-105">構文</span><span class="sxs-lookup"><span data-stu-id="a74b0-105">Syntax</span></span>

<span data-ttu-id="a74b0-106">*式* .OpenRecordset(_**Name**_、_**Type**_、_**Options**_、_**LockEdit**_)</span><span class="sxs-lookup"><span data-stu-id="a74b0-106">OpenRecordset( Name ,  Type ,  Options ,  LockEdit )</span></span>

<span data-ttu-id="a74b0-107">*式* **Database** オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a74b0-107">*expression*  A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a74b0-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a74b0-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a74b0-109">名前</span><span class="sxs-lookup"><span data-stu-id="a74b0-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a74b0-110">必須/省略可能</span><span class="sxs-lookup"><span data-stu-id="a74b0-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a74b0-111">データ型</span><span class="sxs-lookup"><span data-stu-id="a74b0-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="a74b0-112">説明</span><span class="sxs-lookup"><span data-stu-id="a74b0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a74b0-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="a74b0-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="a74b0-114">必須</span><span class="sxs-lookup"><span data-stu-id="a74b0-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a74b0-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="a74b0-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a74b0-p101">新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Office Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。</span><span class="sxs-lookup"><span data-stu-id="a74b0-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a74b0-119"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="a74b0-119"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="a74b0-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="a74b0-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="a74b0-121"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a74b0-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a74b0-122">開く <strong>Recordset</strong> の型を示す <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="a74b0-122">A <a href="recordsettypeenum-enumeration-dao.md"><strong>RecordsetTypeEnum</strong></a> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p><p><span data-ttu-id="a74b0-123"><strong>注</strong>: タイプを指定せずに <strong>Recordset</strong> を Microsoft Access ワークスペースで開くと、可能な場合は <strong>OpenRecordset</strong> はテーブルタイプの <strong>Recordset</strong> を作成します。</span><span class="sxs-lookup"><span data-stu-id="a74b0-123"> > If you open a Recordset in a Microsoft Access workspace and you don't specify a type, OpenRecordset creates a table-type Recordset, if possible.</span></span> <span data-ttu-id="a74b0-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="a74b0-124">If you specify a linked table or query, <strong>OpenRecordset</strong> creates a dynaset-type <strong>Recordset</strong>.</span></span></p>
</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a74b0-125"><em>オプション</em></span><span class="sxs-lookup"><span data-stu-id="a74b0-125"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="a74b0-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="a74b0-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="a74b0-127"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a74b0-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a74b0-128">新しい <strong>Recordset</strong> の特性を指定する <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> 定数の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="a74b0-128">A combination of <a href="recordsetoptionenum-enumeration-dao.md"><strong>RecordsetOptionEnum</strong></a> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="a74b0-129"><strong>注</strong>: 定数 <strong>dbConsistent</strong> と <strong>dbInconsistent</strong> は互いに排他的なので、この 2 つを同時に使用するとエラーになります。</span><span class="sxs-lookup"><span data-stu-id="a74b0-129">The constants <strong>dbConsistent</strong> and <strong>dbInconsistent</strong> are mutually exclusive, and using both causes an error.</span></span> <span data-ttu-id="a74b0-130">Options が <strong>dbReadOnly</strong> 定数を使用している場合に LockEdit 引数を指定した場合にも、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a74b0-130">Supplying a  LockEdit argument when  Options uses the <strong>dbReadOnly</strong> constant also causes an error.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a74b0-131"><em>LockEdit</em></span><span class="sxs-lookup"><span data-stu-id="a74b0-131"><em>LockEdit</em></span></span></p></td>
<td><p><span data-ttu-id="a74b0-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="a74b0-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="a74b0-133"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a74b0-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a74b0-134"><strong>Recordset</strong> のロックを決定する <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="a74b0-134">A <a href="locktypeenum-enumeration-dao.md"><strong>LockTypeEnum</strong></a> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p><p><span data-ttu-id="a74b0-135"><strong>注</strong>: <strong>dbReadOnly</strong> を Options 引数または LockedEdit 引数のどちらか一方で使用することはできますが、両方では使用できません。</span><span class="sxs-lookup"><span data-stu-id="a74b0-135">You can use <strong>dbReadOnly</strong> in either the Options argument or the LockedEdit argument, but not both.</span></span> <span data-ttu-id="a74b0-136">両方の引数で使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a74b0-136">If you use it for both arguments, a run-time error occurs.</span></span></p>
</td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="a74b0-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="a74b0-137">Return value</span></span>

<span data-ttu-id="a74b0-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="a74b0-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="a74b0-139">注釈</span><span class="sxs-lookup"><span data-stu-id="a74b0-139">Remarks</span></span>

<span data-ttu-id="a74b0-p105">通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新たに変更された値を取得するコードを記述します。レコードを削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。この時点で、レコードを削除するかどうかの確認をユーザーに求めることができます。</span><span class="sxs-lookup"><span data-stu-id="a74b0-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="a74b0-143">IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、**dbSeeChanges** 定数も使用する必要があり、使用しないとエラーが生じます。</span><span class="sxs-lookup"><span data-stu-id="a74b0-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="a74b0-p106">ODBC データ ソースで複数の **Recordset** を開こうとすると、**OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、**Recordset** を開いた直後に、**MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。</span><span class="sxs-lookup"><span data-stu-id="a74b0-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="a74b0-146">**[Close](connection-close-method-dao.md)** メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。</span><span class="sxs-lookup"><span data-stu-id="a74b0-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="a74b0-147">*source* が文字列と非整数値を連結したもので構成される SQL ステートメントを参照し、かつシステム パラメーターでコンマなどのピリオド以外の小数点の記号が使用されている場合 (たとえば、strSQL = "PRICE &gt; " &amp; lngPrice で lngPrice = 125,50)、**Recordset** を開こうとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a74b0-147">If source refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE > " & lngPrice, and lngPrice = 125,50), an error occurs when you try to open the Recordset.</span></span> <span data-ttu-id="a74b0-148">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。</span><span class="sxs-lookup"><span data-stu-id="a74b0-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="a74b0-149">\*\*リンクの提供元: \*\*[UtterAccess](https://www.utteraccess.com) コミュニティ。</span><span class="sxs-lookup"><span data-stu-id="a74b0-149">**Link provided by:** Community Member Icon The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="a74b0-150">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="a74b0-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="a74b0-151">Excel へ Access からデータを転送</span><span class="sxs-lookup"><span data-stu-id="a74b0-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="a74b0-152">例</span><span class="sxs-lookup"><span data-stu-id="a74b0-152">Example</span></span>

<span data-ttu-id="a74b0-153">次の例は、パラメーター クエリに基づく Recordset を開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a74b0-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="a74b0-154">**サンプル コードの提供元:** [Microsoft Access 2010 プログラマー用リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="a74b0-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Dim dbs As DAO.Database
    Dim qdf As DAO.QueryDef
    Dim rst As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Get the parameter query
    Set qfd = dbs.QueryDefs("qryMyParameterQuery")
    
    'Supply the parameter value
    qdf.Parameters("EnterStartDate") = Date
    qdf.Parameters("EnterEndDate") = Date + 7
    
    'Open a Recordset based on the parameter query
    Set rst = qdf.OpenRecordset()
```

<br/>

<span data-ttu-id="a74b0-155">次の例は、テーブルまたはクエリに基づいて Recordset を開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a74b0-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

```vb 
    Dim dbs As DAO.Database
    Dim rsTable As DAO.Recordset
    Dim rsQuery As DAO.Recordset
    
    Set dbs = CurrentDb
    
    'Open a table-type Recordset
    Set rsTable = dbs.OpenRecordset("Table1", dbOpenTable)
    
    'Open a dynaset-type Recordset using a saved query
    Set rsQuery = dbs.OpenRecordset("qryMyQuery", dbOpenDynaset)
```

<br/>

<span data-ttu-id="a74b0-156">次の例は、構造化照会言語 (SQL) ステートメントに基づいて Recordset を開く方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a74b0-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rsSQL As DAO.Recordset
    Dim strSQL As String
    
    Set dbs = CurrentDb
    
    'Open a snapshot-type Recordset based on an SQL statement
    strSQL = "SELECT * FROM Table1 WHERE Field2 = 33"
    Set rsSQL = dbs.OpenRecordset(strSQL, dbOpenSnapshot)
```

<br/>

<span data-ttu-id="a74b0-157">次の例は、Filter プロパティを使用して、以降に開かれる Recordset に含めるレコードを決定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a74b0-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

```vb
    Dim dbs As DAO.Database
    Dim rst As DAO.Recordset
    Dim rstFiltered As DAO.Recordset
    Dim strCity As String
    
    Set dbs = CurrentDb
    
    'Create the first filtered Recordset, returning customer records
    'for those visited between 30-60 days ago.
    Set rest = dbs.OpenRecordset(_ 
        "SELECT * FROM Customers WHERE LastVisitDate BETWEEN Date()-60 " & _
        "AND Date()-30 ORDER BY LastVisitDate DESC")
    
    'Begin row processing
    Do While Not rst.EOF
        
        'Retrieve the name of the first city in the selected rows
        strCity = rst!City
    
        'Now filter the Recordset to return only the customers from that city
        rst.Filter = "City = '" & strCity & "'"
        Set rstFiltered = rst.OpenRecordset
    
        'Process the rows
        Do While Not rstFiltered.EOF
            rstFiltered.Edit
            rstFiltered!ToBeVisited = True
            rstFiltered.Update
            rstFiltered.MoveNext
        Loop
    
        'We've done what was needed. Now exit
        Exit Do
        rst.MoveNext
       
    Loop
    
    'Cleanup
    rstFiltered.Close
    rst.Close
    
    Set rstFiltered = Nothing
    Set rst = Nothing
```



