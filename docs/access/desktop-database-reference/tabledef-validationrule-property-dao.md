---
title: TableDef.ValidationRule プロパティ (DAO)
TOCTitle: ValidationRule Property
ms:assetid: 7dcd6f2c-45bc-a50b-727d-589371d5803f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196425(v=office.15)
ms:contentKeyID: 48545864
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052925
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 44329a4cc320e9adcc0612629bcc3fdcd179a1c3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699578"
---
# <a name="tabledefvalidationrule-property-dao"></a><span data-ttu-id="9569c-102">TableDef.ValidationRule プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="9569c-102">TableDef.ValidationRule property (DAO)</span></span>

<span data-ttu-id="9569c-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9569c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9569c-104">テーブルのフィールドを変更するかテーブルにフィールドを追加するときに、フィールド内のデータを検証する値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。文字列型 ( **String**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9569c-104">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9569c-105">構文</span><span class="sxs-lookup"><span data-stu-id="9569c-105">Syntax</span></span>

<span data-ttu-id="9569c-106">*式*です。"入力規則"</span><span class="sxs-lookup"><span data-stu-id="9569c-106">*expression* .ValidationRule</span></span>

<span data-ttu-id="9569c-107">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="9569c-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9569c-108">注釈</span><span class="sxs-lookup"><span data-stu-id="9569c-108">Remarks</span></span>

<span data-ttu-id="9569c-p101">設定値または戻り値は、予約語 WHERE を指定しない SQL WHERE 句形式での比較を示す文字列型 ( **String**) の値となります。 **Fields** コレクションにまだ追加されていないオブジェクトの場合、このプロパティは値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="9569c-p101">The settings or return values is a **String** that describes a comparison in the form of an SQL WHERE clause without the WHERE reserved word. For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="9569c-p102">**ValidationRule** プロパティは、フィールドに有効なデータが含まれているかどうかを示します。データが無効の場合は、トラップ可能な実行時エラーが発生します。エラー メッセージには、 **ValidationText** プロパティが設定されている場合はそのテキストが表示され、それ以外は **ValidationRule** に指定されている式のテキストが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9569c-p102">The **ValidationRule** property determines whether or not a field contains valid data. If the data is not valid, a trappable run-time error occurs. The returned error message is the text of the **ValidationText** property, if specified, or the text of the expression specified by **ValidationRule**.</span></span>

<span data-ttu-id="9569c-114">検証は、Microsoft Access データベース エンジンを使用しているデータベースに対してのみサポートされます。</span><span class="sxs-lookup"><span data-stu-id="9569c-114">Validation is supported only for databases that use the Microsoft Access database engine.</span></span>

<span data-ttu-id="9569c-p103">**Field** オブジェクトの **ValidationRule** プロパティで指定される文字列式は、該当する **Field** のみを参照できます。ユーザー定義関数、SQL 集計関数、またはクエリを参照することはできません。 **Field** オブジェクトの **ValidateOnSet** プロパティが **True** に設定されているときに、このオブジェクトの **ValidationRule** プロパティを設定するには、この式の解析が正常に終了し (フィールド名を暗黙のオペランドとして)、 **True** と評価される必要があります。 **ValidateOnSet** プロパティが **False** に設定されている場合、 **ValidationRule** プロパティの設定は無視されます。</span><span class="sxs-lookup"><span data-stu-id="9569c-p103">The string expression specified by the **ValidationRule** property of a **Field** object can refer only to that **Field**. The expression can't refer to user-defined functions, SQL aggregate functions, or queries. To set a **Field** object's **ValidationRule** property when its **ValidateOnSet** property setting is **True**, the expression must successfully parse (with the field name as an implied operand) and evaluate to **True**. If its **ValidateOnSet** property setting is **False**, the **ValidationRule** property setting is ignored.</span></span>

<span data-ttu-id="9569c-p104">**Recordset** オブジェクトまたは **TableDef** オブジェクトの **ValidationRule** プロパティは、該当するオブジェクトの複数のフィールドを参照できます。このプロパティには、 **Field** オブジェクトに関する前述の制限が当てはまります。</span><span class="sxs-lookup"><span data-stu-id="9569c-p104">The **ValidationRule** property of a **Recordset** or **TableDef** object can refer to multiple fields in that object. The restrictions noted earlier in this topic for the **Field** object apply.</span></span>

<span data-ttu-id="9569c-p105">リンク テーブルに基づく **TableDef** オブジェクトの場合、 **ValidationRule** プロパティは、基になるベース テーブルの **ValidationRule** プロパティの設定値を継承します。基になるベース テーブルが検証をサポートしていない場合、このプロパティの値は長さ 0 の文字列 ("") となります。</span><span class="sxs-lookup"><span data-stu-id="9569c-p105">For a **TableDef** object based on an linked table, the **ValidationRule** property inherits the **ValidationRule** property setting of the underlying base table. If the underlying base table doesn't support validation, the value of this property is a zero-length string ("").</span></span>

> [!NOTE]
> <span data-ttu-id="9569c-123">文字列、整数以外の値に連結するプロパティを設定して、システム ・ パラメーターは、米国以外の小数点の記号、カンマなどを指定する場合 (たとえば、strRule ="価格&gt;" &amp; lngPrice でと lngPrice = 125,50)、エラーが発生時コードでは、任意のデータを検証しようとしています。</span><span class="sxs-lookup"><span data-stu-id="9569c-123">If you set the property to a string concatenated with a non-integer value, and the system parameters specify a non-U.S. decimal character such as a comma (for example, strRule = "PRICE &gt; " &amp; lngPrice, and lngPrice = 125,50), an error will result when your code attempts to validate any data.</span></span> <span data-ttu-id="9569c-124">連結時に数値がシステムの既定の小数点の記号を使って文字列に変換されますが、SQL で小数点の記号として使用できるのはピリオドのみであるためです。</span><span class="sxs-lookup"><span data-stu-id="9569c-124">This is because during concatenation, the number will be converted to a string using your system's default decimal character, and Microsoft Access SQL only accepts U.S. decimal characters.</span></span>
