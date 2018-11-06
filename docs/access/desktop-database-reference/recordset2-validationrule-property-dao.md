---
title: Recordset2.ValidationRule プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: d46cc255-e588-e9e6-66d7-31fc26ae45b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835002(v=office.15)
ms:contentKeyID: 48547940
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 651e4d39861505f990b6d8f06809a566b88ee83b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998190"
---
# <a name="recordset2validationrule-property-dao"></a><span data-ttu-id="f4909-102">Recordset2.ValidationRule プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="f4909-102">Recordset2.ValidationRule property (DAO)</span></span>


<span data-ttu-id="f4909-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f4909-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4909-104">テーブルのフィールドを変更するかテーブルにフィールドを追加するときに、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4909-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4909-105">構文</span><span class="sxs-lookup"><span data-stu-id="f4909-105">Syntax</span></span>

<span data-ttu-id="f4909-106">*式*です。"入力規則"</span><span class="sxs-lookup"><span data-stu-id="f4909-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="f4909-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="f4909-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4909-108">注釈</span><span class="sxs-lookup"><span data-stu-id="f4909-108">Remarks</span></span>

<span data-ttu-id="f4909-p101">設定値または戻り値は、予約語 WHERE を指定しない SQL WHERE 句形式での比較を示す文字列型 ( **String**) の値となります。 **Fields** コレクションにまだ追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="f4909-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="f4909-p102">**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを示します。データが無効の場合は、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **ValidationText** プロパティが設定されている場合はそのテキストが表示され、それ以外は **ValidationRule** に指定されている式のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f4909-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="f4909-p103">**Recordset** オブジェクトの場合、 **ValidationRule** プロパティは値の取得のみ可能です。 **TableDef** オブジェクトの場合、 **ValidationRule** プロパティの使用方法は、次の表に示すように **TableDef** オブジェクトのステータスによって変わります。</span><span class="sxs-lookup"><span data-stu-id="f4909-p103">For a **Recordset** object, use of the **ValidationRule** property is read-only. For a **TableDef** object, use of the **ValidationRule** property depends on the status of the **TableDef** object, as the following table shows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4909-116">TableDef</span><span class="sxs-lookup"><span data-stu-id="f4909-116">TableDef</span></span></p></th>
<th><p><span data-ttu-id="f4909-117">使用例</span><span class="sxs-lookup"><span data-stu-id="f4909-117">Usage</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4909-118">ベース テーブル</span><span class="sxs-lookup"><span data-stu-id="f4909-118">Base table</span></span></p></td>
<td><p><span data-ttu-id="f4909-119">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="f4909-119">Read/write</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4909-120">リンク テーブル</span><span class="sxs-lookup"><span data-stu-id="f4909-120">Linked table</span></span></p></td>
<td><p><span data-ttu-id="f4909-121">値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="f4909-121">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f4909-122">検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f4909-122">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="f4909-p104">**Field** オブジェクトの **ValidationRule** プロパティで指定される文字列式は、該当する **Field** のみを参照できます。ユーザー定義関数、SQL 集計関数、またはクエリを参照することはできません。 **Field** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されているときに、このオブジェクトの **ValidationRule** プロパティを設定するには、この式の解析が正常に終了し (フィールド名を暗黙のオペランドとして)、 **True** と評価される必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="f4909-p104">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="f4909-p105">**Recordset** オブジェクトまたは **TableDef** オブジェクトの **ValidationRule** プロパティは、該当するオブジェクトの複数のフィールドを参照できます。このプロパティには、 **Field** オブジェクトに関する前述の制限が当てはまります。</span><span class="sxs-lookup"><span data-stu-id="f4909-p105">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="f4909-129">テーブル タイプの **Recordset** オブジェクトの場合、 **ValidationRule** プロパティは、テーブル タイプの **Recordset** オブジェクトの作成に使用する **TableDef** オブジェクトの **ValidationRule** プロパティの設定を継承します。</span><span class="sxs-lookup"><span data-stu-id="f4909-129">For a table-type **Recordset** object, the **ValidationRule** property inherits the **ValidationRule** property setting of the **TableDef** object that you use to create the table-type **Recordset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="f4909-130">文字列、整数以外の値に連結するプロパティを設定して、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定する場合 (たとえば、strRule ="価格&gt;" &amp; lngPrice でと lngPrice = 125,50)、エラーが発生時コードでは、任意のデータを検証しようとしています。</span><span class="sxs-lookup"><span data-stu-id="f4909-130">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="f4909-131">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="f4909-131">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span></P>

