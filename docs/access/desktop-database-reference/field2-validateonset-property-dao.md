---
title: Field2.ValidateOnSet プロパティ (DAO)
TOCTitle: ValidateOnSet Property
ms:assetid: 07612730-8dad-4ef0-b19b-f76845973fc3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844969(v=office.15)
ms:contentKeyID: 48543075
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e9d43f5f8315eb5fa453851641e3468cdea90f20
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926256"
---
# <a name="field2validateonset-property-dao"></a><span data-ttu-id="a0e98-102">Field2.ValidateOnSet プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a0e98-102">Field2.ValidateOnSet property (DAO)</span></span>


<span data-ttu-id="a0e98-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a0e98-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="a0e98-104">**Field2** オブジェクトの **Value** プロパティを設定するときに、このオブジェクトの値をすぐに検証するかどうかを指定する値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="a0e98-104">Sets or returns a value that specifies whether or not the value of a **Field2** object is immediately validated when the object's **Value** property is set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e98-105">構文</span><span class="sxs-lookup"><span data-stu-id="a0e98-105">Syntax</span></span>

<span data-ttu-id="a0e98-106">*式*です。ValidateOnSet</span><span class="sxs-lookup"><span data-stu-id="a0e98-106">*expression* .ValidateOnSet</span></span>

<span data-ttu-id="a0e98-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a0e98-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0e98-108">注釈</span><span class="sxs-lookup"><span data-stu-id="a0e98-108">Remarks</span></span>

<span data-ttu-id="a0e98-109">**Recordset** オブジェクトの **Field2** オブジェクトのみが、 **ValidateOnSet** プロパティの値の取得および設定をサポートします。</span><span class="sxs-lookup"><span data-stu-id="a0e98-109">Only **Field2** objects in **Recordset** objects support the **ValidateOnSet** property as read/write.</span></span>

<span data-ttu-id="a0e98-p101">**ValidateOnSet** プロパティを **True** に設定すると、ユーザーが大量のメモ データを含むレコードを入力する場合に便利です。 **Update** を呼び出してデータが検証されるまで待機する方法では、別のフィールドが入力規則に違反していてデータが無効であることが判明した場合、長いメモ データをデータベースに書き込むのに費やした時間が無駄になることがあります。</span><span class="sxs-lookup"><span data-stu-id="a0e98-p101">Setting the **ValidateOnSet** property to **True** can be useful in a situation when a user is entering records that include substantial Memo data. Waiting until the **Update** call to validate the data can result in unnecessary time spent writing the lengthy Memo data to the database if it turns out that the data was invalid anyway because a validation rule was broken in another field.</span></span>

## <a name="example"></a><span data-ttu-id="a0e98-112">例</span><span class="sxs-lookup"><span data-stu-id="a0e98-112">Example</span></span>

<span data-ttu-id="a0e98-p102">この例では、 **ValidateOnSet** プロパティを使用して、データの入力時にエラーを処理する方法を示します。このプロシージャを実行するには、ValidateData 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="a0e98-p102">This example uses the **ValidateOnSet** property to demonstrate how one might trap for errors during data entry. The ValidateData function is required for this procedure to run.</span></span>

```vb
    Sub ValidateOnSetX() 
     
     Dim dbsNorthwind As Database 
     Dim fldDays As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Create and append a new Field object to the Fields 
     ' collection of the Employees table. 
     Set fldDays = _ 
     dbsNorthwind.TableDefs!Employees.CreateField( _ 
     "DaysOfVacation", dbInteger, 2) 
     fldDays.ValidationRule = "BETWEEN 1 AND 20" 
     fldDays.ValidationText = _ 
     "Number must be between 1 and 20!" 
     dbsNorthwind.TableDefs!Employees.Fields.Append fldDays 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     
     Do While True 
     ' Add new record. 
     .AddNew 
     
     ' Get user input for three fields. Verify that the 
     ' data do not violate the validation rules for any 
     ' of the fields. 
     If ValidateData(!FirstName, _ 
     "Enter first name.") = False Then Exit Do 
     If ValidateData(!LastName, _ 
     "Enter last name.") = False Then Exit Do 
     If ValidateData(!DaysOfVacation, _ 
     "Enter days of vacation.") = False Then Exit Do 
     
     .Update 
     .Bookmark = .LastModified 
     Debug.Print !FirstName & " " & !LastName & _ 
     " - " & "DaysOfVacation = " & !DaysOfVacation 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     Exit Do 
     Loop 
     
     ' Cancel AddNew method if any of the validation rules 
     ' were broken. 
     If .EditMode <> dbEditNone Then .CancelUpdate 
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     dbsNorthwind.TableDefs!Employees.Fields.Delete _ 
     fldDays.Name 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function ValidateData(fldTemp As Field2, _ 
     strMessage As String) As Boolean 
     
     Dim strInput As String 
     Dim errLoop As Error 
     
     ValidateData = True 
     ' ValidateOnSet is only read/write for Field objects in 
     ' Recordset objects. 
     fldTemp.ValidateOnSet = True 
     
     Do While True 
     strInput = InputBox(strMessage) 
     If strInput = "" Then Exit Do 
     ' Trap for errors when setting the Field value. 
     On Error GoTo Err_Data 
     If fldTemp.Type = dbInteger Then 
     fldTemp = Val(strInput) 
     Else 
     fldTemp = strInput 
     End If 
     On Error GoTo 0 
     If Not IsNull(fldTemp) Then Exit Do 
     Loop 
     
     If strInput = "" Then ValidateData = False 
     
     Exit Function 
     
    Err_Data: 
     
     If DBEngine.Errors.Count > 0 Then 
     ' Enumerate the Errors collection. The description 
     ' property of the last Error object will be set to 
     ' the ValidationText property of the relevant 
     ' field. 
     For Each errLoop In DBEngine.Errors 
     MsgBox "Error number: " & errLoop.Number & _ 
     vbCr & errLoop.Description 
     Next errLoop 
     End If 
     
     Resume Next 
     
    End Function
```
