---
title: Field.Required プロパティ (DAO)
TOCTitle: Required Property
ms:assetid: 2f1dbdeb-a37a-59b2-fdc2-f16c7ae1a575
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192247(v=office.15)
ms:contentKeyID: 48543999
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 77214fcad0f5b2cafe794282782df4446d37fcf6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887160"
---
# <a name="fieldrequired-property-dao"></a><span data-ttu-id="bdeb7-102">Field.Required プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="bdeb7-102">Field.Required Property (DAO)</span></span>


<span data-ttu-id="bdeb7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bdeb7-104">**[Field](field-object-dao.md)** オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-104">Sets or returns a value that indicates whether a **[Field](field-object-dao.md)** object requires a non-Null value.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdeb7-105">構文</span><span class="sxs-lookup"><span data-stu-id="bdeb7-105">Syntax</span></span>

<span data-ttu-id="bdeb7-106">*式*です。必須</span><span class="sxs-lookup"><span data-stu-id="bdeb7-106">*expression* .Required</span></span>

<span data-ttu-id="bdeb7-107">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdeb7-108">注釈</span><span class="sxs-lookup"><span data-stu-id="bdeb7-108">Remarks</span></span>

<span data-ttu-id="bdeb7-109">**Fields** コレクションにまだ追加されていない **Field** オブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-109">For a **Field** not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="bdeb7-110">**Required** プロパティを使用できるかどうかは、次の表に示すように、 [Fields](fields-collection-dao.md) コレクションが含まれているオブジェクトによって決まります。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-110">The availability of the **Required** property depends on the object that contains the [Fields](fields-collection-dao.md) collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bdeb7-111">Fields コレクションが属するオブジェクト</span><span class="sxs-lookup"><span data-stu-id="bdeb7-111">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="bdeb7-112">Required プロパティの使用</span><span class="sxs-lookup"><span data-stu-id="bdeb7-112">Then Required is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdeb7-113"><strong>Index</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="bdeb7-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bdeb7-114">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdeb7-115"><strong>QueryDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="bdeb7-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bdeb7-116">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="bdeb7-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdeb7-117"><strong>Recordset</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="bdeb7-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bdeb7-118">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="bdeb7-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdeb7-119"><strong>Relation</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="bdeb7-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bdeb7-120">サポートしません。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdeb7-121"><strong>TableDef</strong> オブジェクト</span><span class="sxs-lookup"><span data-stu-id="bdeb7-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="bdeb7-122">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bdeb7-p101">**Required** プロパティは、 **[AllowZeroLength](field-allowzerolength-property-dao.md)** 、 **[ValidateOnSet](field-validateonset-property-dao.md)** 、または **[ValidationRule](field-validationrule-property-dao.md)** プロパティと共に使用して、該当する [Field](field-value-property-dao.md) オブジェクトの \*\*\*\*Value\*\*\*\* プロパティの設定の妥当性を確認できます。 **Required** プロパティが **False** に設定されている場合、そのフィールドには **null** 値を始め、 **AllowZeroLength** プロパティと **ValidationRule** プロパティの設定で指定される条件を満たす値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-p101">You can use the **Required** property along with the **[AllowZeroLength](field-allowzerolength-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to determine the validity of the **[Value](field-value-property-dao.md)** property setting for that **Field** object. If the **Required** property is set to **False**, the field can contain **null** values as well as values that meet the conditions specified by the **AllowZeroLength** and **ValidationRule** property settings.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bdeb7-p102">[!メモ] このプロパティを <STRONG>Index</STRONG> オブジェクトまたは <STRONG>Field</STRONG> オブジェクトのいずれかに対して設定できる場合は、 <STRONG>Field</STRONG> オブジェクトに対して設定します。 <STRONG>Field</STRONG> オブジェクトに対するプロパティ設定の妥当性は、 <STRONG>Index</STRONG> オブジェクトより前にチェックされます。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-p102">When you can set this property for either an <STRONG>Index</STRONG> object or a <STRONG>Field</STRONG> object, set it for the <STRONG>Field</STRONG> object. The validity of the property setting for a <STRONG>Field</STRONG> object is checked before that of an <STRONG>Index</STRONG> object.</span></span></P>



## <a name="example"></a><span data-ttu-id="bdeb7-127">例</span><span class="sxs-lookup"><span data-stu-id="bdeb7-127">Example</span></span>

<span data-ttu-id="bdeb7-p103">次の使用例は、 **Required** プロパティを使用して、新しいレコードを追加するためにデータを含める必要がある、3 つの異なるテーブルのフィールドをレポート出力します。このプロシージャを実行するには、RequiredOutput プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="bdeb7-p103">This example uses the **Required** property to report which fields in three different tables must contain data in order for a new record to be added. The RequiredOutput procedure is required for this procedure to run.</span></span>

```vb 
Sub RequiredX() 
 
 Dim dbsNorthwind As Database 
 Dim tdfloop As TableDef 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 With dbsNorthwind 
 ' Show which fields are required in the Fields 
 ' collections of three different TableDef objects. 
 RequiredOutput .TableDefs("Categories") 
 RequiredOutput .TableDefs("Customers") 
 RequiredOutput .TableDefs("Employees") 
 .Close 
 End With 
 
End Sub 
 
Sub RequiredOutput(tdfTemp As TableDef) 
 
 Dim fldLoop As Field 
 
 ' Enumerate Fields collection of the specified TableDef 
 ' and show the Required property. 
 Debug.Print "Fields in " & tdfTemp.Name & ":" 
 For Each fldLoop In tdfTemp.Fields 
 Debug.Print , fldLoop.Name & ", Required = " & _ 
 fldLoop.Required 
 Next fldLoop 
 
End Sub 
 
```

