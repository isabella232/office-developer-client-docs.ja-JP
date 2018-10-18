---
title: Recordset2.GetRows メソッド (DAO)
TOCTitle: GetRows Method
ms:assetid: e5c0a082-e9d2-359f-fed5-835ab91d2311
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835959(v=office.15)
ms:contentKeyID: 48548367
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 25c52cf132cdc2c85671a4589e45c5989e504b8b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25607033"
---
# <a name="recordset2getrows-method-dao"></a><span data-ttu-id="52fce-102">Recordset2.GetRows メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="52fce-102">Recordset2.GetRows Method (DAO)</span></span>


<span data-ttu-id="52fce-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="52fce-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="52fce-104">**[Recordset](recordset-object-dao.md)** オブジェクトから複数の行を取得します。</span><span class="sxs-lookup"><span data-stu-id="52fce-104">Retrieves multiple rows from a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="52fce-105">構文</span><span class="sxs-lookup"><span data-stu-id="52fce-105">Syntax</span></span>

<span data-ttu-id="52fce-106">*式*です。GetRows (***NumRows***)</span><span class="sxs-lookup"><span data-stu-id="52fce-106">*expression* .GetRows(***NumRows***)</span></span>

<span data-ttu-id="52fce-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="52fce-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="52fce-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="52fce-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="52fce-109">名前</span><span class="sxs-lookup"><span data-stu-id="52fce-109">Name</span></span></p></th>
<th><p><span data-ttu-id="52fce-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="52fce-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="52fce-111">データ型</span><span class="sxs-lookup"><span data-stu-id="52fce-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="52fce-112">説明</span><span class="sxs-lookup"><span data-stu-id="52fce-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="52fce-113">NumRows</span><span class="sxs-lookup"><span data-stu-id="52fce-113">NumRows</span></span></p></td>
<td><p><span data-ttu-id="52fce-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="52fce-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="52fce-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="52fce-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="52fce-116">取得する行数。</span><span class="sxs-lookup"><span data-stu-id="52fce-116">The number of rows to retrieve.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="52fce-117"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="52fce-117"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="52fce-118">戻り値</span><span class="sxs-lookup"><span data-stu-id="52fce-118">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="52fce-119">戻り値</span><span class="sxs-lookup"><span data-stu-id="52fce-119">Return value</span></span>
>>>>>>> <span data-ttu-id="52fce-120">master</span><span class="sxs-lookup"><span data-stu-id="52fce-120">master</span></span>

<span data-ttu-id="52fce-121">バリアント型 (Variant)</span><span class="sxs-lookup"><span data-stu-id="52fce-121">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="52fce-122">注釈</span><span class="sxs-lookup"><span data-stu-id="52fce-122">Remarks</span></span>

<span data-ttu-id="52fce-p101">**GetRows** メソッドは、**Recordset** からレコードをコピーするために使用します。**GetRows** は 2 次元配列を返します。最初の添え字ではフィールドを指定し、2 番目の添え字では行番号を指定します。たとえば次の例では、intField はフィールドを表し、intRecord は行番号を表します。</span><span class="sxs-lookup"><span data-stu-id="52fce-p101">Use the **GetRows** method to copy records from a **Recordset**. **GetRows** returns a two-dimensional array. The first subscript identifies the field and the second identifies the row number. For example, intField represents the field, and intRecord identifies the row number:</span></span>

<span data-ttu-id="52fce-127">avarRecords (intField、intRecord)</span><span class="sxs-lookup"><span data-stu-id="52fce-127">avarRecords(intField, intRecord)</span></span>

<span data-ttu-id="52fce-128">2 行目の最初のフィールドの値を取得するには、次のようなコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="52fce-128">To get the first field value in the second row returned, use code like the following:</span></span>

<span data-ttu-id="52fce-129">フィールド 1 = avarRecords(0,1)</span><span class="sxs-lookup"><span data-stu-id="52fce-129">field1 = avarRecords(0,1)</span></span>

<span data-ttu-id="52fce-130">1 行目の 2 番目のフィールドの値を取得するには、次のようなコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="52fce-130">To get the second field value in the first row, use code like the following:</span></span>

<span data-ttu-id="52fce-131">field2 = avarRecords(1,0)</span><span class="sxs-lookup"><span data-stu-id="52fce-131">field2 = avarRecords(1,0)</span></span>

<span data-ttu-id="52fce-132">avarRecords 変数は、**GetRows** によってデータが返されると、自動的に 2 次元配列となります。</span><span class="sxs-lookup"><span data-stu-id="52fce-132">The avarRecords variable automatically becomes a two-dimensional array when **GetRows** returns data.</span></span>

<span data-ttu-id="52fce-133">取得できる行数よりも多くの行を要求すると、 **GetRows** は取得できる行数だけを返します。</span><span class="sxs-lookup"><span data-stu-id="52fce-133">If you request more rows than are available, then **GetRows** returns only the number of available rows.</span></span> <span data-ttu-id="52fce-134">配列のサイズは返された行数に応じて決まるため、Visual Basic for Applications の **UBound** 関数を使用すると、 **GetRows** によって実際に取得された行数を確認できます。</span><span class="sxs-lookup"><span data-stu-id="52fce-134">You can use the Visual Basic for Applications **UBound** function to determine how many rows **GetRows** actually retrieved, because the array is sized to fit the number of returned rows.</span></span> <span data-ttu-id="52fce-135">たとえば、**バリアント**varA という名前に結果を格納する場合は、実際に返された行の数を決定する次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="52fce-135">For example, if you returned the results into a **Variant** called varA, you could use the following code to determine how many rows were actually returned:</span></span>

<span data-ttu-id="52fce-136">numReturned = UBound(varA,2) + 1</span><span class="sxs-lookup"><span data-stu-id="52fce-136">numReturned = UBound(varA,2) + 1</span></span>

<span data-ttu-id="52fce-p103">返された最初の行は配列の 0 番目の要素となるため、"+ 1" を付ける必要があります。取得できる行数は、使用できるメモリの容量によって制限されます。テーブルのサイズが大きい場合は、**GetRows** を使用してテーブル全体を配列として取得しないでください。</span><span class="sxs-lookup"><span data-stu-id="52fce-p103">You need to use "+ 1" because the first row returned is in the 0 element of the array. The number of rows that you can retrieve is constrained by the amount of available memory. You shouldn't use **GetRows** to retrieve an entire table into an array if it is large.</span></span>

<span data-ttu-id="52fce-140">**GetRows** は、メモ型 (Memo) およびロング バイナリ型 (Long Binary) のフィールドを含む、 **Recordset** のすべてのフィールドが配列として返されるので、クエリを使用して取得する行数を制限した方がよい場合があります。</span><span class="sxs-lookup"><span data-stu-id="52fce-140">Because **GetRows** returns all fields of the **Recordset** into the array, including Memo and Long Binary fields, you might want to use a query that restricts the fields returned.</span></span>

<span data-ttu-id="52fce-141">**GetRows** の呼び出し後、まだ読み込まれていない次の行がカレント レコードになります。</span><span class="sxs-lookup"><span data-stu-id="52fce-141">After you call **GetRows**, the current record is positioned at the next unread row.</span></span> <span data-ttu-id="52fce-142">**GetRows**は、numrows の**移動**現在のレコードに同じです。</span><span class="sxs-lookup"><span data-stu-id="52fce-142">That is, **GetRows** has the same effect on the current record as **Move**numrows.</span></span>

<span data-ttu-id="52fce-p105">複数の **GetRows** 呼び出しを使用してすべての行を取得しようとする場合は、 **[EOF](recordset2-eof-property-dao.md)** プロパティを使用して、 **Recordset** の末尾に達していないことを確認してください。 **Recordset** の末尾に達した場合や、要求された範囲のある行を取得できない場合、 **GetRows** は要求された数よりも少ない行を返します。たとえば、10 件のレコードを取得しようといる場合、5 番目のレコードを取得できないときは、 **GetRows** は 4 件のレコードを取得し、5 番目のレコードをカレント レコードにします。この場合、実行時エラーは発生しません。ダイナセット タイプの **Recordset** で別のユーザーがレコードを削除した場合に、このような状況が起こります。このような場合の処理方法については、使用例を参照してください。</span><span class="sxs-lookup"><span data-stu-id="52fce-p105">If you are trying to retrieve all the rows by using multiple **GetRows** calls, use the **[EOF](recordset2-eof-property-dao.md)** property to be sure that you're at the end of the **Recordset**. **GetRows** returns less than the number requested if it's at the end of the **Recordset**, or if it can't retrieve a row in the range requested. For example, if you're trying to retrieve 10 records, but you can't retrieve the fifth record, **GetRows** returns four records and makes the fifth record the current record. This will not generate a run-time error. This might occur if another user deletes a record in a dynaset-type **Recordset**. See the example for a demonstration of how to handle this.</span></span>

## <a name="example"></a><span data-ttu-id="52fce-149">例</span><span class="sxs-lookup"><span data-stu-id="52fce-149">Example</span></span>

<span data-ttu-id="52fce-p106">この例では、 **GetRows** メソッドを使用して、指定した数の行を **Recordset** から取得し、結果データを配列に設定します。 **GetRows** メソッドでは、 **EOF** に達した場合、および他のユーザーによって削除されたレコードを **GetRows** が取得しようとした場合に、指定よりも少ない数の行が返されます。2 番目の場合のみ、 **False** が返されます。このプロシージャを実行するには、GetRowsOK 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="52fce-p106">This example uses the **GetRows** method to retrieve a specified number of rows from a **Recordset** and to fill an array with the resulting data. The **GetRows** method will return fewer than the desired number of rows in two cases: either if **EOF** has been reached, or if **GetRows** tried to retrieve a record that was deleted by another user. The function returns **False** only if the second case occurs. The GetRowsOK function is required for this procedure to run.</span></span>

```vb
    Sub GetRowsX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
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
     
    Function GetRowsOK(rstTemp As Recordset2, _ 
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
