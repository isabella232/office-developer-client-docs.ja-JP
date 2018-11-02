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
ms.openlocfilehash: ab969f2e26751a70a0f9ac9daf2ca17bcaa103c5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925976"
---
# <a name="databaseopenrecordset-method-dao"></a><span data-ttu-id="279ce-102">Database.OpenRecordset メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="279ce-102">Database.OpenRecordset method (DAO)</span></span>

<span data-ttu-id="279ce-103">**に適用されます:** Access 2013 |Office 2013</span><span class="sxs-lookup"><span data-stu-id="279ce-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="279ce-104">新しい **[Recordset](recordset-object-dao.md)** オブジェクトを作成して **Recordsets** コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="279ce-104">Creates a new **[Recordset](recordset-object-dao.md)** object and appends it to the **Recordsets** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="279ce-105">構文</span><span class="sxs-lookup"><span data-stu-id="279ce-105">Syntax</span></span>

<span data-ttu-id="279ce-106">*式*です。何らかの (_**名前**_、_**型**_、_**オプション**_、 _**LockEdit**_)</span><span class="sxs-lookup"><span data-stu-id="279ce-106">*expression* .OpenRecordset(_**Name**_, _**Type**_, _**Options**_, _**LockEdit**_)</span></span>

<span data-ttu-id="279ce-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="279ce-107">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="279ce-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="279ce-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="279ce-109">名前</span><span class="sxs-lookup"><span data-stu-id="279ce-109">Name</span></span></p></th>
<th><p><span data-ttu-id="279ce-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="279ce-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="279ce-111">データ型</span><span class="sxs-lookup"><span data-stu-id="279ce-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="279ce-112">説明</span><span class="sxs-lookup"><span data-stu-id="279ce-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="279ce-113">名前</span><span class="sxs-lookup"><span data-stu-id="279ce-113">Name</span></span></p></td>
<td><p><span data-ttu-id="279ce-114">必須</span><span class="sxs-lookup"><span data-stu-id="279ce-114">Required</span></span></p></td>
<td><p><span data-ttu-id="279ce-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="279ce-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="279ce-p101">新しい <strong>Recordset</strong> のレコードの取得元です。テーブル名、クエリ名、またはレコードを返す SQL ステートメントを指定できます。Microsoft Access データベース エンジンのデータベースに含まれるテーブル タイプの <strong>Recordset</strong> オブジェクトの場合は、テーブル名でのみ指定できます。  </span><span class="sxs-lookup"><span data-stu-id="279ce-p101">The source of the records for the new <strong>Recordset</strong>. The source can be a table name, a query name, or an SQL statement that returns records. For table-type <strong>Recordset</strong> objects in Microsoft Access database engine databases, the source can only be a table name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="279ce-119">型</span><span class="sxs-lookup"><span data-stu-id="279ce-119">Type</span></span></p></td>
<td><p><span data-ttu-id="279ce-120">省略可能</span><span class="sxs-lookup"><span data-stu-id="279ce-120">Optional</span></span></p></td>
<td><p><span data-ttu-id="279ce-121"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="279ce-121"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="279ce-122">開く <a href="recordsettypeenum-enumeration-dao.md">Recordset</a> の型を示す <strong><strong>RecordsetTypeEnum</strong></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="279ce-122">A <strong><a href="recordsettypeenum-enumeration-dao.md">RecordsetTypeEnum</a></strong> constant that indicates the type of <strong>Recordset</strong> to open.</span></span></p>

> [!NOTE]
> <span data-ttu-id="279ce-p102">Microsoft Access ワークスペースで **Recordset** を開くときに、型を指定しない場合、**OpenRecordset** は、テーブル タイプの **Recordset** を作成します (可能な場合)。リンクされたテーブルまたはクエリを指定した場合、**OpenRecordset** は、ダイナセット タイプの **Recordset** を作成します。</span><span class="sxs-lookup"><span data-stu-id="279ce-p102">If you open a **Recordset** in a Microsoft Access workspace and you don't specify a type, **OpenRecordset** creates a table-type **Recordset**, if possible. If you specify a linked table or query, **OpenRecordset** creates a dynaset-type **Recordset**.</span></span>


</td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="279ce-125">選択肢</span><span class="sxs-lookup"><span data-stu-id="279ce-125">Options</span></span></p></td>
<td><p><span data-ttu-id="279ce-126">省略可能</span><span class="sxs-lookup"><span data-stu-id="279ce-126">Optional</span></span></p></td>
<td><p><span data-ttu-id="279ce-127"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="279ce-127"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="279ce-128">新しい <a href="recordsetoptionenum-enumeration-dao.md">Recordset</a> の特性を指定する <strong><strong>RecordsetOptionEnum</strong></strong> 定数の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="279ce-128">A combination of <strong><a href="recordsetoptionenum-enumeration-dao.md">RecordsetOptionEnum</a></strong> constants that specify characteristics of the new <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="279ce-p103">**dbConsistent** 定数と **dbInconsistent** 定数は互いに排他的なので、この 2 つを同時に使用するとエラーになります。Options で **dbReadOnly** 定数を使用する場合に LockEdit 引数を指定してもエラーになります。</span><span class="sxs-lookup"><span data-stu-id="279ce-p103">The constants **dbConsistent** and **dbInconsistent** are mutually exclusive, and using both causes an error. Supplying a LockEdit argument when Options uses the **dbReadOnly** constant also causes an error.</span></span>


</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="279ce-131">LockEdit</span><span class="sxs-lookup"><span data-stu-id="279ce-131">LockEdit</span></span></p></td>
<td><p><span data-ttu-id="279ce-132">省略可能</span><span class="sxs-lookup"><span data-stu-id="279ce-132">Optional</span></span></p></td>
<td><p><span data-ttu-id="279ce-133"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="279ce-133"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="279ce-134"><a href="locktypeenum-enumeration-dao.md">Recordset</a> のロックを決定する <strong><strong>LockTypeEnum</strong></strong> 定数。</span><span class="sxs-lookup"><span data-stu-id="279ce-134">A <strong><a href="locktypeenum-enumeration-dao.md">LockTypeEnum</a></strong> constant that determines the locking for the <strong>Recordset</strong>.</span></span></p>

> [!NOTE]
> <span data-ttu-id="279ce-p104">**dbReadOnly** を Options 引数または LockedEdit 引数のどちらか一方で使用することはできますが、両方で使用することはできません。両方の引数で使用した場合、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="279ce-p104">You can use **dbReadOnly** in either the Options argument or the LockedEdit argument, but not both. If you use it for both arguments, a run-time error occurs.</span></span>


</td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="279ce-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="279ce-137">Return value</span></span>

<span data-ttu-id="279ce-138">Recordset</span><span class="sxs-lookup"><span data-stu-id="279ce-138">Recordset</span></span>

## <a name="remarks"></a><span data-ttu-id="279ce-139">注釈</span><span class="sxs-lookup"><span data-stu-id="279ce-139">Remarks</span></span>

<span data-ttu-id="279ce-p105">通常、ユーザーがレコードを更新中にこのエラーが発生した場合は、フィールドの内容を更新して、新しく変更された値を取得するコードを記述します。レコードの削除中にこのエラーが発生した場合は、新しいレコード データと、そのデータが最近変更されたことを示すメッセージをユーザーに表示するという方法もあります。このとき、レコードを削除してもよいかどうかユーザーに確認できます。</span><span class="sxs-lookup"><span data-stu-id="279ce-p105">Typically, if the user gets this error while updating a record, your code should refresh the contents of the fields and retrieve the newly modified values. If the error occurs while deleting a record, your code could display the new record data to the user and a message indicating that the data has recently changed. At this point, your code can request a confirmation that the user still wants to delete the record.</span></span>

<span data-ttu-id="279ce-143">IDENTITY 列を持つ Microsoft SQL Server 6.0 以降のテーブルに対して Microsoft Access データベース エンジンが接続された ODBC ワークスペースの **Recordset** を開く場合は、 **dbSeeChanges** 定数も使用する必要があり、使用しないとエラーが生じます。</span><span class="sxs-lookup"><span data-stu-id="279ce-143">You should also use the **dbSeeChanges** constant if you open a **Recordset** in a Microsoft Access database engine-connected ODBC workspace against a Microsoft SQL Server 6.0 (or later) table that has an IDENTITY column, otherwise an error may result.</span></span>

<span data-ttu-id="279ce-p106">ODBC データ ソースで複数の **Recordset** を開こうとすると、 **OpenRecordset** に対する前の呼び出しで接続がビジー状態となるため、失敗する場合があります。これを回避する方法の 1 つは、 **Recordset** を開いた直後に、 **MoveLast** メソッドを使用して **Recordset** の末尾までデータを読み込むことです。</span><span class="sxs-lookup"><span data-stu-id="279ce-p106">Opening more than one **Recordset** on an ODBC data source may fail because the connection is busy with a prior **OpenRecordset** call. One way around this is to fully populate the **Recordset** by using the **MoveLast** method as soon as the **Recordset** is opened.</span></span>

<span data-ttu-id="279ce-146">[**Close**](connection-close-method-dao.md) メソッドを使用して **Recordset** を閉じると、そのレコードセットは自動的に **Recordsets** コレクションから削除されます。</span><span class="sxs-lookup"><span data-stu-id="279ce-146">Closing a **Recordset** with the **[Close](connection-close-method-dao.md)** method automatically deletes it from the **Recordsets** collection.</span></span>


> [!NOTE]
> <span data-ttu-id="279ce-147">*ソース*を指す場合、整数以外の値に連結された文字列、SQL ステートメントで構成され、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定 (たとえば、strSQL ="価格&gt;" &amp; lngPrice でと lngPrice =125,50)、**レコード セット**を開こうとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="279ce-147">If *source* refers to an SQL statement composed of a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strSQL = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error occurs when you try to open the **Recordset**.</span></span> <span data-ttu-id="279ce-148">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみになるからです。</span><span class="sxs-lookup"><span data-stu-id="279ce-148">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and SQL only accepts U.S. decimal characters.</span></span>

<span data-ttu-id="279ce-149">**でリンクが用意されている** [UtterAccess](https://www.utteraccess.com)のコミュニティです。</span><span class="sxs-lookup"><span data-stu-id="279ce-149">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="279ce-150">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="279ce-150">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="279ce-151">ExcelへAccess からデータを転送</span><span class="sxs-lookup"><span data-stu-id="279ce-151">Transfer data from Access to Excel</span></span>](https://www.utteraccess.com/forum/transfer-data-access-ex-t1672619.html)

## <a name="example"></a><span data-ttu-id="279ce-152">例</span><span class="sxs-lookup"><span data-stu-id="279ce-152">Example</span></span>

<span data-ttu-id="279ce-153">次の例は、パラメーター クエリに基づく Recordset を開く方法を示します。</span><span class="sxs-lookup"><span data-stu-id="279ce-153">The following example shows how to open a Recordset that is based on a parameter query.</span></span>

<span data-ttu-id="279ce-154">**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。</span><span class="sxs-lookup"><span data-stu-id="279ce-154">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

<span data-ttu-id="279ce-155">次の例は、テーブルまたはクエリに基づいて Recordset を開く方法を示します。</span><span class="sxs-lookup"><span data-stu-id="279ce-155">The following example shows how to open a Recordset based on a table or a query.</span></span>

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

<span data-ttu-id="279ce-156">次の例は、構造化照会言語 (SQL) ステートメントに基づいて Recordset を開く方法を示します。</span><span class="sxs-lookup"><span data-stu-id="279ce-156">The following example shows how to open a Recordset based on a Structured Query Language (SQL) statement.</span></span>

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

<span data-ttu-id="279ce-157">次の例は、 Filter プロパティを使用して、以降に開かれる Recordset に含めるレコードを決定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="279ce-157">The following sample shows how to use the Filter property to determine the records to be included in a subsequently opened Recordset.</span></span>

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



