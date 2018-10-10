---
title: Field2.DefaultValue プロパティ (DAO)
TOCTitle: DefaultValue Property
ms:assetid: 709c9580-520e-46ce-7d70-e409872184bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195744(v=office.15)
ms:contentKeyID: 48545563
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053121
f1_categories:
- Office.Version=v15
ms.openlocfilehash: cff7a319130786cfdab26546d49f83da5769c5f6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478448"
---
# <a name="field2defaultvalue-property-dao"></a><span data-ttu-id="896db-102">Field2.DefaultValue プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="896db-102">Field2.DefaultValue Property (DAO)</span></span>


<span data-ttu-id="896db-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="896db-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="896db-p101">**Field2** オブジェクトの既定値を設定または取得します。 [**Fields**](fields-collection-dao.md) コレクションに追加されていない **Field2** オブジェクトの場合、このプロパティは値の取得および設定が可能です (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="896db-p101">Sets or returns the default value of a **Field2** object. For a **Field2** object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="896db-106">構文</span><span class="sxs-lookup"><span data-stu-id="896db-106">Syntax</span></span>

<span data-ttu-id="896db-107">*式*です。既定値</span><span class="sxs-lookup"><span data-stu-id="896db-107">*expression* .DefaultValue</span></span>

<span data-ttu-id="896db-108">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="896db-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="896db-109">注釈</span><span class="sxs-lookup"><span data-stu-id="896db-109">Remarks</span></span>

<span data-ttu-id="896db-p102">設定値または戻り値は、最大 255 文字の文字列データ型 ( **String**) です。文字列または式を指定できます。プロパティの設定値が式の場合、ユーザー定義関数、Microsoft Access データベース エンジン SQL の集計関数、またはクエリ、フォーム、その他の **Field2** オブジェクトへの参照を含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="896db-p102">The setting or return value is a **String** data type that can contain a maximum of 255 characters. It can be either text or an expression. If the property setting is an expression, it can't contain user-defined functions, Microsoft Access database engine SQL aggregate functions, or references to queries, forms, or other **Field2** objects.</span></span>


> [!NOTE]
> <P><span data-ttu-id="896db-p103">[!メモ] <STRONG>TableDef</STRONG> オブジェクトで <STRONG>Field2</STRONG> オブジェクトの <STRONG>DefaultValue</STRONG> プロパティを "GenUniqueID( )" と呼ばれる特殊な値に設定することもできます。これにより、新規レコードを追加または作成すると、このフィールドに乱数が割り当てられ、各レコードに一意の識別子が設定されます。フィールドの <STRONG>Type</STRONG> プロパティは長整数型 ( <STRONG>Long</STRONG>) である必要があります。</span><span class="sxs-lookup"><span data-stu-id="896db-p103">You can also set the <STRONG>DefaultValue</STRONG> property of a <STRONG>Field2</STRONG> object on a <STRONG>TableDef</STRONG> object to a special value called "GenUniqueID( )". This causes a random number to be assigned to this field whenever a new record is added or created, thereby giving each record a unique identifier. The field's <STRONG>Type</STRONG> property must be <STRONG>Long</STRONG>.</span></span></P>



<span data-ttu-id="896db-116">**DefaultValue** プロパティを使用できるかどうかは、次の表に示すように、 **Fields** コレクションを含むオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="896db-116">The availability of the **DefaultValue** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="896db-117">Fields コレクションの所属先</span><span class="sxs-lookup"><span data-stu-id="896db-117">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="896db-118">DefaultValue プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="896db-118">Then DefaultValue is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="896db-119">Index オブジェクト</span><span class="sxs-lookup"><span data-stu-id="896db-119">Index object</span></span></p></td>
<td><p><span data-ttu-id="896db-120">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="896db-120">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="896db-121">QueryDef オブジェクト</span><span class="sxs-lookup"><span data-stu-id="896db-121">QueryDef object</span></span></p></td>
<td><p><span data-ttu-id="896db-122">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="896db-122">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="896db-123">Recordset オブジェクト</span><span class="sxs-lookup"><span data-stu-id="896db-123">Recordset object</span></span></p></td>
<td><p><span data-ttu-id="896db-124">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="896db-124">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="896db-125">Relation オブジェクト</span><span class="sxs-lookup"><span data-stu-id="896db-125">Relation object</span></span></p></td>
<td><p><span data-ttu-id="896db-126">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="896db-126">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="896db-127">TableDef オブジェクト</span><span class="sxs-lookup"><span data-stu-id="896db-127">TableDef object</span></span></p></td>
<td><p><span data-ttu-id="896db-128">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="896db-128">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="896db-p104">新しいレコードが作成されると、 **DefaultValue** プロパティの設定値は、フィールドの値として自動的に入力されます。 **Value** プロパティを設定することにより、フィールド値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="896db-p104">When a new record is created, the **DefaultValue** property setting is automatically entered as the value for the field. You can change the field value by setting its **Value** property.</span></span>

<span data-ttu-id="896db-131">**DefaultValue** プロパティは、オートナンバ型 ( **AutoNumber**) とロング バイナリ型 ( **Long Binary** ) のフィールドには適用されません。</span><span class="sxs-lookup"><span data-stu-id="896db-131">The **DefaultValue** property doesn't apply to **AutoNumber** and **Long Binary** fields.</span></span>

## <a name="example"></a><span data-ttu-id="896db-132">例</span><span class="sxs-lookup"><span data-stu-id="896db-132">Example</span></span>

<span data-ttu-id="896db-p105">次の使用例は、 **DefaultValue** プロパティを使用して、ユーザーに入力を要求するときに、フィールドの通常の値を通知するために表示します。また、他に入力がない場合に、 **DefaultValue** が使用されて新しいレコードにデータが設定される方法を示します。このプロシージャを実行するには、DefaultPrompt 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="896db-p105">This example uses the **DefaultValue** property to alert the user of a field's normal value while prompting for input. In addition, it demonstrates how new records will be filled using **DefaultValue** in the absence of any other input. The DefaultPrompt function is required for this procedure to run.</span></span>

```vb
    Sub DefaultValueX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim strOldDefault As String 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strCode As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Store original DefaultValue information and set the 
     ' property to a new value. 
     strOldDefault = _ 
     tdfEmployees.Fields!PostalCode.DefaultValue 
     tdfEmployees.Fields!PostalCode.DefaultValue = "98052" 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     ' Add a new record to the Recordset. 
     .AddNew 
     !FirstName = "Bruce" 
     !LastName = "Oberg" 
     
     ' Get user input. If user enters something, the field 
     ' will be filled with that data; otherwise, it will be 
     ' filled with the DefaultValue information. 
     strMessage = "Enter postal code for " & vbCr & _ 
     !FirstName & " " & !LastName & ":" 
     strCode = DefaultPrompt(strMessage, !PostalCode) 
     If strCode <> "" Then !PostalCode = strCode 
     .Update 
     
     ' Go to new record and print information. 
     .Bookmark = .LastModified 
     Debug.Print " FirstName = " & !FirstName 
     Debug.Print " LastName = " & !LastName 
     Debug.Print " PostalCode = " & !PostalCode 
     
     ' Delete new record because this is a demonstration. 
     .Delete 
     .Close 
     End With 
     
     ' Restore original DefaultValue property because this is a 
     ' demonstration. 
     tdfEmployees.Fields!PostalCode.DefaultValue = _ 
     strOldDefault 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function DefaultPrompt(strPrompt As String, _ 
     fldTemp As Field2) As String 
     
     Dim strFullPrompt As String 
     
     ' Ask user for new DefaultValue setting for the specified 
     ' Field object. 
     strFullPrompt = strPrompt & vbCr & _ 
     "[Default = " & fldTemp.DefaultValue & _ 
     ", Cancel - use default]" 
     DefaultPrompt = InputBox(strFullPrompt) 
     
    End Function
```