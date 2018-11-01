---
title: Field2.AllowZeroLength プロパティ (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: d3795634-527f-b4c5-b606-50f9945cac12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834791(v=office.15)
ms:contentKeyID: 48547908
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1ec717cdeda58ef8eabcb1cd62c2629018313db
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882526"
---
# <a name="field2allowzerolength-property-dao"></a><span data-ttu-id="75e08-102">Field2.AllowZeroLength プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="75e08-102">Field2.AllowZeroLength Property (DAO)</span></span>


<span data-ttu-id="75e08-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="75e08-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="75e08-104">長さが 0 の文字列 ("") が、テキスト型またはメモ型の [Field2](field-value-property-dao.md) オブジェクトの \*\*\*\*Value\*\*\*\* プロパティの有効な設定値かどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="75e08-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **Field2** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="75e08-105">構文</span><span class="sxs-lookup"><span data-stu-id="75e08-105">Syntax</span></span>

<span data-ttu-id="75e08-106">*式*です。AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="75e08-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="75e08-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="75e08-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="75e08-108">注釈</span><span class="sxs-lookup"><span data-stu-id="75e08-108">Remarks</span></span>

<span data-ttu-id="75e08-109">**Fields** コレクションに追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="75e08-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="75e08-110">**Fields** コレクションに追加されると、 **AllowZeroLength** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって異なります。</span><span class="sxs-lookup"><span data-stu-id="75e08-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75e08-111">Fields コレクションの所属先</span><span class="sxs-lookup"><span data-stu-id="75e08-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="75e08-112">AllowZeroLength プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="75e08-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75e08-113"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="75e08-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="75e08-114">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="75e08-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e08-115"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="75e08-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="75e08-116">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="75e08-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e08-117"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="75e08-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="75e08-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="75e08-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75e08-119"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="75e08-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="75e08-120">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="75e08-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75e08-121"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="75e08-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="75e08-122">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="75e08-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75e08-123">このプロパティを **[Required](field-required-property-dao.md)** 、 **[ValidateOnSet](field-validateonset-property-dao.md)** プロパティまたは **[ValidationRule](field-validationrule-property-dao.md)** プロパティと共に使用して、フィールドの値を検証できます。</span><span class="sxs-lookup"><span data-stu-id="75e08-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="75e08-124">例</span><span class="sxs-lookup"><span data-stu-id="75e08-124">Example</span></span>

<span data-ttu-id="75e08-p101">次の使用例では、 **AllowZeroLength** プロパティにより、ユーザーは **Field2** オブジェクトの値を空の文字列に設定できます。こうすると、ユーザーはデータが認識されていないレコードとデータが適用されていないレコードを区別できます。</span><span class="sxs-lookup"><span data-stu-id="75e08-p101">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field2** to an empty string. In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
