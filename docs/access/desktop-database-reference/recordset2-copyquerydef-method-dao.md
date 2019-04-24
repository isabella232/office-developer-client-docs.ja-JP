---
title: Recordset2 の copyquerydef メソッド (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 8a643dae0b67cf4f2a2a0148619d9a8f4df7e6f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307365"
---
# <a name="recordset2copyquerydef-method-dao"></a><span data-ttu-id="141f1-102">Recordset2 の copyquerydef メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="141f1-102">Recordset2.CopyQueryDef method (DAO)</span></span>


<span data-ttu-id="141f1-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="141f1-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="141f1-104">recordset の**[](querydef-object-dao.md)** プレースホルダーで表される**[recordset](recordset-object-dao.md)** オブジェクトの作成\*\*\*\* に使用される querydef オブジェクトを返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="141f1-104">Returns a **[QueryDef](querydef-object-dao.md)** object that is a copy of the **QueryDef** used to create the **[Recordset](recordset-object-dao.md)** object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="141f1-105">.</span><span class="sxs-lookup"><span data-stu-id="141f1-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="141f1-106">構文</span><span class="sxs-lookup"><span data-stu-id="141f1-106">Syntax</span></span>

<span data-ttu-id="141f1-107">*式*。CopyQueryDef</span><span class="sxs-lookup"><span data-stu-id="141f1-107">*expression* .CopyQueryDef</span></span>

<span data-ttu-id="141f1-108">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="141f1-108">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="return-value"></a><span data-ttu-id="141f1-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="141f1-109">Return value</span></span>

<span data-ttu-id="141f1-110">QueryDef</span><span class="sxs-lookup"><span data-stu-id="141f1-110">QueryDef</span></span>

## <a name="remarks"></a><span data-ttu-id="141f1-111">注釈</span><span class="sxs-lookup"><span data-stu-id="141f1-111">Remarks</span></span>

<span data-ttu-id="141f1-112">**CopyQueryDef** メソッドを使用すると、 **Recordset** の作成に使用された **QueryDef** の複製である新しい **QueryDef** を作成できます。</span><span class="sxs-lookup"><span data-stu-id="141f1-112">You can use the **CopyQueryDef** method to create a new **QueryDef** that is a duplicate of the **QueryDef** used to create the **Recordset**.</span></span>

<span data-ttu-id="141f1-p102">**QueryDef** を使用してこの **Recordset** が作成されていない場合は、エラーが発生します。 **CopyQueryDef** メソッドを使用する前に、まず **OpenRecordset** メソッドを使用して **Recordset** を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="141f1-p102">If a **QueryDef** wasn't used to create this **Recordset**, an error occurs. You must first open a **Recordset** with the **OpenRecordset** method before using the **CopyQueryDef** method.</span></span>

<span data-ttu-id="141f1-115">このメソッドは、 **Recordset** オブジェクトを **QueryDef** から作成し、その **Recordset** を関数に渡し、その関数でレコードセットを変更するクエリなどを表す SQL を再作成する必要がある場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="141f1-115">This method is useful when you create a **Recordset** object from a **QueryDef**, and pass the **Recordset** to a function, and the function must re-create the SQL equivalent of the query, for example, to modify it in some way.</span></span>

## <a name="example"></a><span data-ttu-id="141f1-116">例</span><span class="sxs-lookup"><span data-stu-id="141f1-116">Example</span></span>

<span data-ttu-id="141f1-p103">次の例では、 **CopyQueryDef** メソッドを使用して既存の **Recordset** から **QueryDef** のコピーを作成し、SQL プロパティに句を追加することによってそのコピーを変更します。持続的な **QueryDef** の作成時には、SQL プロパティにスペース、セミコロン、またはラインフィードを追加できますが、SQL ステートメントに新しい句を追加するには、これらの余分な文字を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="141f1-p103">This example uses the **CopyQueryDef** method to create a copy of a **QueryDef** from an existing **Recordset** and modifies the copy by adding a clause to the SQL property. When you create a permanent **QueryDef**, spaces, semicolons, or linefeeds may be added to the SQL property; these extra characters must be stripped before any new clauses can be attached to the SQL statement.</span></span>

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

<span data-ttu-id="141f1-119">次の例では、CopyQueryNew() の使用例を示します。</span><span class="sxs-lookup"><span data-stu-id="141f1-119">This example shows a possible use of CopyQueryNew().</span></span>

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

