---
title: Recordset.GetRows メソッド (DAO)
TOCTitle: GetRows method
ms:assetid: 59f6e4f0-e7b1-db60-31c7-3338b66d3345
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194427(v=office.15)
ms:contentKeyID: 48545031
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053362
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 35afc836bf2fb2a728453ac1ed240fd50a9673da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300505"
---
# <a name="recordsetgetrows-method-dao"></a><span data-ttu-id="02633-102">Recordset.GetRows メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="02633-102">Recordset.GetRows Method (DAO)</span></span>

<span data-ttu-id="02633-103">**適用先**: Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="02633-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="02633-104">**[Recordset](recordset-object-dao.md)** オブジェクトから複数行を取得します。</span><span class="sxs-lookup"><span data-stu-id="02633-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="02633-105">構文</span><span class="sxs-lookup"><span data-stu-id="02633-105">Syntax</span></span>

<span data-ttu-id="02633-106">*式* .GetRows (***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="02633-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="02633-107">*式* **Recordset** オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="02633-107">*expression*  A variable that represents a **Recordset** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="02633-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="02633-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="02633-109">名前</span><span class="sxs-lookup"><span data-stu-id="02633-109">Name</span></span></p></th>
<th><p><span data-ttu-id="02633-110">必須/省略可能</span><span class="sxs-lookup"><span data-stu-id="02633-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="02633-111">データ型</span><span class="sxs-lookup"><span data-stu-id="02633-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="02633-112">説明</span><span class="sxs-lookup"><span data-stu-id="02633-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="02633-113"><em>NumRows</em></span><span class="sxs-lookup"><span data-stu-id="02633-113"><em>NumRows</em></span></span></p></td>
<td><p><span data-ttu-id="02633-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="02633-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="02633-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="02633-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="02633-116">取得する行数。</span><span class="sxs-lookup"><span data-stu-id="02633-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="02633-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="02633-117">Return value</span></span>

<span data-ttu-id="02633-118">バリアント型</span><span class="sxs-lookup"><span data-stu-id="02633-118">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="02633-119">注釈</span><span class="sxs-lookup"><span data-stu-id="02633-119">Remarks</span></span>

<span data-ttu-id="02633-120">**GetRows** メソッドは、 **Recordset** からレコードをコピーするために使用します。</span><span class="sxs-lookup"><span data-stu-id="02633-120">Use the **GetRows** method to copy records from a **Recordset**.</span></span> <span data-ttu-id="02633-121">**GetRows** は 2 次元配列を返します。</span><span class="sxs-lookup"><span data-stu-id="02633-121">**GetRows** returns a two-dimensional array.</span></span> <span data-ttu-id="02633-122">1 番目の添え字でフィールドを指定し、2 番目の添え字で行番号を指定します。</span><span class="sxs-lookup"><span data-stu-id="02633-122">The first subscript identifies the field and the second identifies the row number.</span></span> <span data-ttu-id="02633-123">たとえば次の例では、  `intField` はフィールドを表し、`intRecord` は行番号を表します。</span><span class="sxs-lookup"><span data-stu-id="02633-123">For example,  `intField` represents the field, and  `intRecord` identifies the row number:</span></span>

`avarRecords(intField, intRecord)`

<span data-ttu-id="02633-124">2 番目の行に含まれる最初のフィールドの値を取得するには、次のようなコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="02633-124">To get the first field value in the second row returned, use code like the following:</span></span>

`field1 = avarRecords(0,1)`

<span data-ttu-id="02633-125">最初の行に含まれる 2 番目のフィールドの値を取得するには、次のようなコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="02633-125">To get the second field value in the first row, use code like the following:</span></span>

`field2 = avarRecords(1,0)`

<span data-ttu-id="02633-126">**GetRows** がデータを返すと、avarRecords 変数は自動的に 2 次元配列になります。</span><span class="sxs-lookup"><span data-stu-id="02633-126">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="02633-127">取得できる行数よりも多くの行を要求すると、**GetRows** は取得できる行数だけを返します。</span><span class="sxs-lookup"><span data-stu-id="02633-127">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="02633-128">配列のサイズは返された行数に応じて決まるため、Visual Basic for Applications の **UBound** 関数を使用すると、**GetRows** によって実際に取得された行数を確認できます。</span><span class="sxs-lookup"><span data-stu-id="02633-128">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="02633-129">たとえば、結果を varA という **Variant** に返した場合は、次のコードを使って実際に返された行数を判断できます。</span><span class="sxs-lookup"><span data-stu-id="02633-129">For example, if you returned the results into a Variant called varA, you could use the following code to determine how many rows were actually returned:</span></span>

`numReturned = UBound(varA,2) + 1`

<span data-ttu-id="02633-130">返される最初の行は配列の 0 要素にあるため、 「+ 1」を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="02633-130">You need to use "+ 1" because the first row returned is in the 0 element of the array.</span></span> <span data-ttu-id="02633-131">取得できる行数は、使用できるメモリの容量によって制限されます。</span><span class="sxs-lookup"><span data-stu-id="02633-131">The number of rows that you can retrieve is constrained by the amount of available memory.</span></span> <span data-ttu-id="02633-132">テーブルのサイズが大きい場合は、 **GetRows** を使用してテーブル全体を配列として取得しないでください。</span><span class="sxs-lookup"><span data-stu-id="02633-132">You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="02633-133">**GetRows** では、メモやロング バイナリを含む **Recordset** のすべてのフィールドが配列として返されるため、取得するフィールドを制限するクエリを使用すると有効な場合があります。</span><span class="sxs-lookup"><span data-stu-id="02633-133">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="02633-134">**GetRows** の呼び出し後は、カレント レコードが次の読み込まれていない行に設定されます。</span><span class="sxs-lookup"><span data-stu-id="02633-134">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="02633-135">つまり、**GetRows** を使用した場合のカレント レコードへの影響は、**Move** numrows の場合と同じです。</span><span class="sxs-lookup"><span data-stu-id="02633-135">That is, GetRows has the same effect on the current record as Move  numrows.</span></span>

<span data-ttu-id="02633-p105">すべての行を取得するために **GetRows** を複数回呼び出す場合は、 **[EOF](recordset-eof-property-dao.md)** プロパティを使用して、 **Recordset** の末尾まで確実に読み込まれるようにします。 **GetRows** は、 **Recordset** の末尾まで到達した場合や、要求された範囲内の行を読み込むことができない場合は、要求された数よりも少ないレコードを返します。たとえば、10 個のレコードを取得しようとしているが、5 番目のレコードを取得できない場合、 **GetRows** は 4 個のレコードを返し、5 番目のレコードをカレント レコードにします。この場合、実行時エラーは発生しません。このような現象は、ダイナセット タイプの **Recordset** で、他のユーザーがレコードを削除した場合などに発生します。このような場合の処理方法については、使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="02633-p105">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="02633-142">例</span><span class="sxs-lookup"><span data-stu-id="02633-142">Example</span></span>

<span data-ttu-id="02633-p106">次の例では、 **GetRows** メソッドを使用して、指定された数の行を **Recordset** から取得し、結果データを配列に格納します。 **GetRows** メソッドは、 **EOF** に到達したとき、または他のユーザーが削除したレコードを **GetRows** で取得しようとしたときの 2 つの場合に、要求された数よりも少ない行を返します。この関数は、後者の場合にのみ **False** を返します。このプロシージャを実行するには、GetRowsOK 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="02633-p106">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.</span></span>

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim intRows As Integer 
     Dim avarRecords As Variant 
     Dim intRecord As Integer 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT FirstName, LastName, Title " & _ 
     "FROM Employees ORDER BY LastName", dbOpenSnapshot) 
     
     With rstEmployees 
     Do While True 
     ' Get user input for number of rows. 
     strMessage = "Enter number of rows to retrieve." 
     intRows = Val(InputBox(strMessage)) 
     
     If intRows <= 0 Then Exit Do 
     
     ' If GetRowsOK is successful, print the results, 
     ' noting if the end of the file was reached. 
     If GetRowsOK(rstEmployees, intRows, _ 
     avarRecords) Then 
     If intRows > UBound(avarRecords, 2) + 1 Then 
     Debug.Print "(Not enough records in " & _ 
     "Recordset to retrieve " & intRows & _ 
     " rows.)" 
     End If 
     Debug.Print UBound(avarRecords, 2) + 1 & _ 
     " records found." 
     
     ' Print the retrieved data. 
     For intRecord = 0 To UBound(avarRecords, 2) 
     Debug.Print " " & _ 
     avarRecords(0, intRecord) & " " & _ 
     avarRecords(1, intRecord) & ", " & _ 
     avarRecords(2, intRecord) 
     Next intRecord 
     Else 
     ' Assuming the GetRows error was due to data 
     ' changes by another user, use Requery to 
     ' refresh the Recordset and start over. 
     If .Restartable Then 
     If MsgBox("GetRows failed--retry?", _ 
     vbYesNo) = vbYes Then 
     .Requery 
     Else 
     Debug.Print "GetRows failed!" 
     Exit Do 
     End If 
     Else 
     Debug.Print "GetRows failed! " & _ 
     "Recordset not Restartable!" 
     Exit Do 
     End If 
     End If 
     
     ' Because using GetRows leaves the current record 
     ' pointer at the last record accessed, move the 
     ' pointer back to the beginning of the Recordset 
     ' before looping back for another search. 
     .MoveFirst 
     Loop 
     End With 
     
     rstEmployees.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function GetRowsOK(rstTemp As Recordset, _ 
     intNumber As Integer, avarData As Variant) As Boolean 
     
     ' Store results of GetRows method in array. 
     avarData = rstTemp.GetRows(intNumber) 
     ' Return False only if fewer than the desired number of 
     ' rows were returned, but not because the end of the 
     ' Recordset was reached. 
     If intNumber > UBound(avarData, 2) + 1 And _ 
     Not rstTemp.EOF Then 
     GetRowsOK = False 
     Else 
     GetRowsOK = True 
     End If 
     
    End Function
```
