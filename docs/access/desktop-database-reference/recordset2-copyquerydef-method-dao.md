---
title: Recordset2.CopyQueryDef メソッド (DAO)
TOCTitle: CopyQueryDef Method
ms:assetid: 36689ac0-f8a6-1f3e-4170-799141373777
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192474(v=office.15)
ms:contentKeyID: 48544170
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053073
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d65f46433aa3071ce9709f1c3841dda45e02a5b6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870388"
---
# <a name="recordset2copyquerydef-method-dao"></a><span data-ttu-id="5dfbc-102">Recordset2.CopyQueryDef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="5dfbc-102">Recordset2.CopyQueryDef Method (DAO)</span></span>


<span data-ttu-id="5dfbc-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="5dfbc-104">レコード セットのプレース ホルダー (Microsoft Access ワークスペースのみ) で表される**[Recordset](recordset-object-dao.md)** オブジェクトを作成するのには**クエリ定義**のコピーである**[QueryDef](querydef-object-dao.md)** オブジェクトの使用を返します。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="5dfbc-105">.</span><span class="sxs-lookup"><span data-stu-id="5dfbc-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="5dfbc-106">構文</span><span class="sxs-lookup"><span data-stu-id="5dfbc-106">Syntax</span></span>

<span data-ttu-id="5dfbc-107">*式*です。CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="5dfbc-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="5dfbc-108">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-108">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="return-value"></a><span data-ttu-id="5dfbc-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="5dfbc-109">Return value</span></span>

<span data-ttu-id="5dfbc-110">QueryDef</span><span class="sxs-lookup"><span data-stu-id="5dfbc-110">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="5dfbc-111">注釈</span><span class="sxs-lookup"><span data-stu-id="5dfbc-111">Remarks</span></span>

<span data-ttu-id="5dfbc-112">**CopyQueryDef** メソッドを使用すると、 **Recordset** を作成するために使用された **QueryDef** のコピーである、新しい **QueryDef** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-112">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="5dfbc-p102">この **Recordset** の作成に **QueryDef** を使用していない場合はエラーが発生します。 **CopyQueryDef** メソッドを使用する前に **OpenRecordset** メソッドで **Recordset** を開いておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-p102">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs. You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="5dfbc-115">このメソッドは、 **QueryDef** から **Recordset** オブジェクトを作成し、関数に **Recordset** を渡し、なんらかの方法でクエリを変更するなど、関数がクエリと同等の SQL を再作成する必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-115">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="5dfbc-116">例</span><span class="sxs-lookup"><span data-stu-id="5dfbc-116">Example</span></span>

<span data-ttu-id="5dfbc-p103">この例では、 **CopyQueryDef** メソッドを使用して既存の **Recordset** から **QueryDef** のコピーを作成し、SQL プロパティに句を追加して QueryDef のコピーを変更します。永続的な **QueryDef** を作成するときは、SQL プロパティにスペース、セミコロン、または改行を追加できますが、この余分な文字は、SQL ステートメントに新しい句を追加する前に除去しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-p103">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

```vb
    Function CopyQueryNew(rstTemp As Recordset, _ 
     strAdd As String) As QueryDef 
     
     Dim strSQL As String 
     Dim strRightSQL As String 
     
     Set CopyQueryNew = rstTemp.CopyQueryDef 
     With CopyQueryNew 
     ' Strip extra characters. 
     strSQL = .SQL 
     strRightSQL = Right(strSQL, 1) 
     Do While strRightSQL = " " Or strRightSQL = ";" Or _ 
     strRightSQL = Chr(10) Or strRightSQL = vbCr 
     strSQL = Left(strSQL, Len(strSQL) - 1) 
     strRightSQL = Right(strSQL, 1) 
     Loop 
     .SQL = strSQL & strAdd 
     End With 
     
    End Function 
```     

<br/>

<span data-ttu-id="5dfbc-119">次に、CopyQueryNew() の使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="5dfbc-119">This example shows a possible use of CopyQueryNew().</span></span>

```vb
Sub CopyQueryDefX() 
 
 Dim dbsNorthwind As Database 
 Dim qdfEmployees As QueryDef 
 Dim rstEmployees As Recordset2 
 Dim intCommand As Integer 
 Dim strOrderBy As String 
 Dim qdfCopy As QueryDef 
 Dim rstCopy As Recordset 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 Set qdfEmployees = dbsNorthwind.CreateQueryDef( _ 
 "NewQueryDef", "SELECT FirstName, LastName, " & _ 
 "BirthDate FROM Employees") 
 Set rstEmployees = qdfEmployees.OpenRecordset( _ 
 dbOpenForwardOnly) 
 
 Do While True 
 intCommand = Val(InputBox( _ 
 "Choose field on which to order a new " & _ 
 "Recordset:" & vbCr & "1 - FirstName" & vbCr & _ 
 "2 - LastName" & vbCr & "3 - BirthDate" & vbCr & _ 
 "[Cancel - exit]")) 
 Select Case intCommand 
 Case 1 
 strOrderBy = " ORDER BY FirstName" 
 Case 2 
 strOrderBy = " ORDER BY LastName" 
 Case 3 
 strOrderBy = " ORDER BY BirthDate" 
 Case Else 
 Exit Do 
 End Select 
 Set qdfCopy = CopyQueryNew(rstEmployees, strOrderBy) 
 Set rstCopy = qdfCopy.OpenRecordset(dbOpenSnapshot, _ 
 dbForwardOnly) 
 With rstCopy 
 Do While Not .EOF 
 Debug.Print !LastName & ", " & !FirstName & _ 
 " - " & !BirthDate 
 .MoveNext 
 Loop 
 .Close 
 End With 
 Exit Do 
 Loop 
 
 rstEmployees.Close 
 ' Delete new QueryDef because this is a demonstration. 
 dbsNorthwind.QueryDefs.Delete qdfEmployees.Name 
 dbsNorthwind.Close 
 
End Sub 
 
```

