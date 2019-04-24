---
title: Field2 プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 5464d2de-f3d7-5d6b-4fc5-66df6a5540cb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194105(v=office.15)
ms:contentKeyID: 48544896
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b6e9e50148f4b87a957ff2317b1b39522d7d4e1c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292651"
---
# <a name="field2validationrule-property-dao"></a><span data-ttu-id="e13fa-102">Field2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="e13fa-102">Field2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="e13fa-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e13fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e13fa-p101">テーブルのフィールドを変更するかテーブルにフィールドを追加するときに、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e13fa-p101">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only). Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e13fa-106">構文</span><span class="sxs-lookup"><span data-stu-id="e13fa-106">Syntax</span></span>

<span data-ttu-id="e13fa-107">*式*。規則</span><span class="sxs-lookup"><span data-stu-id="e13fa-107">*expression* .ValidationRule</span></span>

<span data-ttu-id="e13fa-108">\*式\***Field2**オブジェクトを返すオブジェクト式を指定します。</span><span class="sxs-lookup"><span data-stu-id="e13fa-108">*expression* An expression that returns a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e13fa-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e13fa-109">Remarks</span></span>

<span data-ttu-id="e13fa-p102">設定値または戻り値は、WHERE 予約語のない SQL WHERE 句の形式による比較方法が記述された文字列型 (String) の値です。 **[Fields](fields-collection-dao.md)** コレクションに追加されていないオブジェクトでは、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="e13fa-p102">The settings or return values is a String that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **[Fields](fields-collection-dao.md)** collection, this property is read/write.</span></span>

<span data-ttu-id="e13fa-p103">**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを示します。データが無効の場合は、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **ValidationText** プロパティが設定されている場合はそのテキストが表示され、それ以外は **ValidationRule** に指定されている式のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e13fa-p103">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="e13fa-115">**Field2** オブジェクトでは、 **ValidationRule** プロパティの使用方法は、 **Field2** オブジェクトを追加する **Fields** コレクションが含まれているオブジェクトに応じて異なります。</span><span class="sxs-lookup"><span data-stu-id="e13fa-115">For a **Field2** object, use of the **ValidationRule** property depends on the object that contains the **Fields** collection to which the **Field2** object is appended.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e13fa-116">オブジェクトの追加先</span><span class="sxs-lookup"><span data-stu-id="e13fa-116">Object appended to</span></span></p></th>
<th><p><span data-ttu-id="e13fa-117">使用方法</span><span class="sxs-lookup"><span data-stu-id="e13fa-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e13fa-118"><strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="e13fa-118"><strong>Index</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fa-119">サポートされていません</span><span class="sxs-lookup"><span data-stu-id="e13fa-119">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fa-120"><strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="e13fa-120"><strong>QueryDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fa-121">読み取り専用</span><span class="sxs-lookup"><span data-stu-id="e13fa-121">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fa-122"><strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="e13fa-122"><strong>Recordset</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fa-123">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e13fa-123">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e13fa-124"><strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="e13fa-124"><strong>Relation</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fa-125">サポートされません。</span><span class="sxs-lookup"><span data-stu-id="e13fa-125">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e13fa-126"><strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="e13fa-126"><strong>TableDef</strong></span></span></p></td>
<td><p><span data-ttu-id="e13fa-127">読み取り/書き込み</span><span class="sxs-lookup"><span data-stu-id="e13fa-127">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e13fa-128">検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="e13fa-128">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="e13fa-p104">**Field2** オブジェクトの **ValidationRule** プロパティに指定されている文字列式は、その **Field2** オブジェクトのみを参照できます。この式は、ユーザー定義関数、SQL 集計関数、およびクエリは参照できません。 **Field2** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されている場合に、その **ValidationRule** プロパティを設定するには、文字列式が正常に解析され (明示されないオペランドとしてフィールド名を指定)、 **True** に評価されている必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="e13fa-p104">The string expression specified by the **ValidationRule** property of a **Field2** object can refer only to that **Field2**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field2** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>


> [!NOTE]
> <span data-ttu-id="e13fa-133">このプロパティに整数以外の値を連結した文字列を設定した場合、システムパラメーターでコンマ以外の小数点 (例: strrule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125, 50) を指定すると、エラーが発生します。コードがデータを検証しようとしています。</span><span class="sxs-lookup"><span data-stu-id="e13fa-133">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="e13fa-134">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、Microsoft Acces データベース エンジンの SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="e13fa-134">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access database engine SQL only accepts U.S. decimal characters.</span></span>


