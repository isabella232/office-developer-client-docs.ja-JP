---
title: Field.ValidationRule プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: b07e644d-54d3-7199-6f99-178774e54398
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821784(v=office.15)
ms:contentKeyID: 48547123
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6f195d990212d54c78b246d1162ed384a21d48a2
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477422"
---
# <a name="fieldvalidationrule-property-dao"></a><span data-ttu-id="05982-102">Field.ValidationRule プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="05982-102">Field.ValidationRule Property (DAO)</span></span>


<span data-ttu-id="05982-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="05982-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="05982-p101">データの変更時またはテーブルへの追加時 (Microsoft Access ワークスペースのみ) に、フィールド内のデータを検証する値を設定または取得します。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="05982-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="05982-106">構文</span><span class="sxs-lookup"><span data-stu-id="05982-106">Syntax</span></span>

<span data-ttu-id="05982-107">*式*です。"入力規則"</span><span class="sxs-lookup"><span data-stu-id="05982-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="05982-108">\*式\***フィールド**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="05982-108">*expression* An expression that returns a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="05982-109">注釈</span><span class="sxs-lookup"><span data-stu-id="05982-109">Remarks</span></span>

<span data-ttu-id="05982-p102">設定値または戻り値は、WHERE 予約語のない SQL WHERE 句の形式による比較方法が記述された文字列型 (String) の値です。 **[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="05982-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="05982-p103">**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを指定します。データが有効でない場合、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **[ValidationText](field-validationtext-property-dao.md)** プロパティが指定されている場合はそのテキストが表示され、それ以外は、 **ValidationRule** に指定されている式のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="05982-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **[ValidationText](field-validationtext-property-dao.md)** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="05982-115">**[Field](field-object-dao.md)** オブジェクトの場合、 **ValidationRule** プロパティの使用方法は、 **Field** オブジェクトの追加先の **Fields** コレクションを含むオブジェクトによって変わります。</span><span class="sxs-lookup"><span data-stu-id="05982-115">For a **[Field](field-object-dao.md)** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05982-116">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="05982-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="05982-117">使用例</span><span class="sxs-lookup"><span data-stu-id="05982-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05982-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="05982-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="05982-119">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="05982-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05982-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="05982-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="05982-121">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="05982-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05982-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="05982-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="05982-123">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="05982-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05982-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="05982-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="05982-125">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="05982-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05982-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="05982-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="05982-127">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="05982-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="05982-128">検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="05982-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="05982-p104">**Field** オブジェクトの **ValidationRule** プロパティで指定される文字列式は、該当する **Field** のみを参照できます。ユーザー定義関数、SQL 集計関数、またはクエリを参照することはできません。 **Field** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されているときに、このオブジェクトの **ValidationRule** プロパティを設定するには、この式の解析が正常に終了し (フィールド名を暗黙のオペランドとして)、 **True** と評価される必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="05982-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <P><span data-ttu-id="05982-133">文字列、整数以外の値に連結するプロパティを設定して、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定する場合 (たとえば、strRule ="価格&gt;" &amp; lngPrice でと lngPrice = 125,50)、エラーが発生時コードでは、任意のデータを検証しようとしています。</span><span class="sxs-lookup"><span data-stu-id="05982-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="05982-134">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Acces データベース エンジンの SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="05982-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span></P>


