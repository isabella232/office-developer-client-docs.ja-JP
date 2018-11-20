---
title: Filter プロパティ (ADO)
TOCTitle: Filter property (ADO)
ms:assetid: 5abc528a-a6ee-34de-5d44-a3249194b0a0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249314(v=office.15)
ms:contentKeyID: 48545053
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 193cf5db350fdf0b30fe19da9a61026d1cd39aa9
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026471"
---
# <a name="filter-property-ado"></a><span data-ttu-id="85a6a-102">Filter プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="85a6a-102">Filter property (ADO)</span></span>


<span data-ttu-id="85a6a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="85a6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="85a6a-104">[Recordset](recordset-object-ado.md) のデータに対するフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="85a6a-104">Indicates a filter for data in a [Recordset](recordset-object-ado.md).</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="85a6a-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="85a6a-105">Settings and return values</span></span>

<span data-ttu-id="85a6a-106">次の中の 1 つを含む、バリアント型 ( **Variant** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="85a6a-106">Sets or returns a **Variant** value, which can contain one of the following:</span></span>

  - <span data-ttu-id="85a6a-107">**条件文字列**: **AND** 演算子または **OR** 演算子で連結された、1 つまたは複数の句で構成される文字列です。</span><span class="sxs-lookup"><span data-stu-id="85a6a-107">**Criteria string** — a string made up of one or more individual clauses concatenated with **AND** or **OR** operators.</span></span>

  - <span data-ttu-id="85a6a-108">**ブックマーク配列**: **Recordset** オブジェクト内のレコードを指す一意なブックマーク値の配列です。</span><span class="sxs-lookup"><span data-stu-id="85a6a-108">**Array of bookmarks** — an array of unique bookmark values that point to records in the **Recordset** object.</span></span>

  - <span data-ttu-id="85a6a-109">[FilterGroupEnum](filtergroupenum.md) 値。</span><span class="sxs-lookup"><span data-stu-id="85a6a-109">A [FilterGroupEnum](filtergroupenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="85a6a-110">解説</span><span class="sxs-lookup"><span data-stu-id="85a6a-110">Remarks</span></span>

<span data-ttu-id="85a6a-p101">**Filter** プロパティは、 **Recordset** オブジェクト内のレコードを選別するために使います。フィルター処理後の **Recordset** が現在のカーソルになります。 [AbsolutePosition](absoluteposition-property-ado.md)、[AbsolutePage](absolutepage-property-ado.md)、[RecordCount](recordcount-property-ado.md)、[PageCount](pagecount-property-ado.md) などの、現在のカーソルに基づいて値を返すその他のプロパティが影響を受けます。これは、 **Filter** プロパティを特定の値に設定すると、カレント レコードが新しい値を満たす最初のレコードに移動するからです。</span><span class="sxs-lookup"><span data-stu-id="85a6a-p101">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor. Other properties that return values based on the current cursor are affected, such as [AbsolutePosition](absoluteposition-property-ado.md), [AbsolutePage](absolutepage-property-ado.md), [RecordCount](recordcount-property-ado.md), and [PageCount](pagecount-property-ado.md). This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="85a6a-115">抽出条件文字列で構成されるフォーム*フィールド名-演算子-値*の句の (たとえば、"[氏名] = 'Smith'")。</span><span class="sxs-lookup"><span data-stu-id="85a6a-115">The criteria string is made up of clauses in the form *FieldName-Operator-Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="85a6a-116">個々 の句を**AND**で連結することにより複合句を作成することができます (など"[氏名] = 'Smith' AND FirstName = 'John'") または**OR** (など」)。</span><span class="sxs-lookup"><span data-stu-id="85a6a-116">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, ").</span></span> <span data-ttu-id="85a6a-117">複合句を作成するには個々 の句を**AND**で連結することにより (など"[氏名] = 'Smith' AND FirstName = 'John'") または**OR** (など」[氏名] = 'Smith' または [氏名] = 'Jones'")。</span><span class="sxs-lookup"><span data-stu-id="85a6a-117">You can create compound clauses by concatenating individual clauses with **AND** (for example, "LastName = 'Smith' AND FirstName = 'John'") or **OR** (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="85a6a-118">検索条件文字列を指定する際は、次の点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="85a6a-118">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="85a6a-119">*フィールド名*は、**レコード セット**からの有効なフィールド名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="85a6a-119">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="85a6a-120">フィールド名にスペースを含める場合は、名前を角かっこで囲みます。</span><span class="sxs-lookup"><span data-stu-id="85a6a-120">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="85a6a-121">*演算子*は、次のいずれかである必要があります: \<、 \>、 \<= \>= \< \>、=、または**のような**。</span><span class="sxs-lookup"><span data-stu-id="85a6a-121">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or **LIKE**.</span></span>

  - <span data-ttu-id="85a6a-122">*値*は、フィールドの値を比較する値 (たとえば、'Smith' \#8/24/95\#、12.345、または $50.00)。</span><span class="sxs-lookup"><span data-stu-id="85a6a-122">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="85a6a-123">文字列に単一引用符を使用し、シャープ記号 (\#) の日付にします。</span><span class="sxs-lookup"><span data-stu-id="85a6a-123">Use single quotes with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="85a6a-124">数値の場合、小数点、ドル記号、および指数表記を使用できます。</span><span class="sxs-lookup"><span data-stu-id="85a6a-124">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="85a6a-125">\**ような\*\*\*演算子*がある場合、*値*は、ワイルドカードを使用できます。</span><span class="sxs-lookup"><span data-stu-id="85a6a-125">If *Operator* is **LIKE**, *Value* can use wildcards.</span></span> <span data-ttu-id="85a6a-126">アスタリスクのみ (\*) し、パーセント記号 (%)、ワイルドカードを使用し、文字列の最後の文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="85a6a-126">Only the asterisk (\*) and percent sign (%) wild cards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="85a6a-127">*値*を null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="85a6a-127">*Value* cannot be null.</span></span>

    > [!NOTE]
    > <span data-ttu-id="85a6a-p105">[!メモ] フィルターの "値" に単一引用符 (') を含めるには、2 つの単一引用符を使って 1 つの単一引用符を表します。たとえば、O'Malley にフィルターを設定するには、条件文字列は、"col1 = 'O''Malley'" とします。フィルター値の先頭と末尾に単一引用符を含めるには、シャープ記号 (#) で文字列を囲みます。たとえば、'1' にフィルターを設定するには、条件文字列を "col1 = #'1'#" とします。</span><span class="sxs-lookup"><span data-stu-id="85a6a-p105">To include single quotation marks (') in the filter Value, use two single quotation marks to represent one. For example, to filter on O'Malley, the criteria string should be "col1 = 'O''Malley'". To include single quotation marks at both the beginning and the end of the filter value, enclose the string with pound signs (#). For example, to filter on '1', the criteria string should be "col1 = #'1'#".</span></span>

  - <span data-ttu-id="85a6a-p106">**AND** と **OR** の間に優先順位はありません。句はかっこでグループにまとめることができます。ただし、次のように、 **OR** で句を結合してできた句のグループを、 **AND** を使ってさらに別の句と結合することはできません。</span><span class="sxs-lookup"><span data-stu-id="85a6a-p106">There is no precedence between **AND** and **OR**. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an **OR** and then join the group to another clause with an **AND**, like this:</span></span>

  - <span data-ttu-id="85a6a-135">この場合は、フィルターを次のように構成します。</span><span class="sxs-lookup"><span data-stu-id="85a6a-135">Instead, you would construct this filter as</span></span>

  - <span data-ttu-id="85a6a-136">**LIKE**句では、先頭と末尾、パターンのワイルドカードを使用できます (たとえば、[氏名] のような '\*mit\*')、またはパターンの末尾にのみ (たとえば、[氏名] のような' Smit\*')。</span><span class="sxs-lookup"><span data-stu-id="85a6a-136">In a **LIKE** clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*'), or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

<span data-ttu-id="85a6a-137">フィルター定数を使うと、一括更新モードでレコード間に競合が発生した場合でも、たとえば最後の [UpdateBatch](updatebatch-method-ado.md) メソッドの呼び出しで変更されたレコードだけを表示するなどの方法で、簡単に競合を解消できます。</span><span class="sxs-lookup"><span data-stu-id="85a6a-137">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were affected during the last [UpdateBatch](updatebatch-method-ado.md) method call.</span></span>

<span data-ttu-id="85a6a-p107">たとえば、レコードが他のユーザーによって既に削除されている場合など、基になるデータとの競合が原因で、 **Filter** プロパティの設定に失敗する場合があります。このような場合、プロバイダーは [Errors](errors-collection-ado.md) コレクションに警告を返しますが、プログラムの実行は停止されません。実行時エラーは、要求したすべてのレコードで競合が発生した場合にのみ発生します。競合が発生したレコードを見つけるには、 [Status](status-property-ado-recordset.md) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="85a6a-p107">Setting the **Filter** property itself may fail because of a conflict with the underlying data (for example, a record has already been deleted by another user). In such a case, the provider returns warnings to the [Errors](errors-collection-ado.md) collection but does not halt program execution. A run-time error occurs only if there are conflicts on all the requested records. Use the [Status](status-property-ado-recordset.md) property to locate records with conflicts.</span></span>

<span data-ttu-id="85a6a-142">**Filter** プロパティを長さ 0 の文字列 ("") に設定すると、 **adFilterNone** 定数を使った場合と同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="85a6a-142">Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

<span data-ttu-id="85a6a-p108">**Filter** プロパティを設定すると、 **Recordset** のフィルター処理済みのレコードのサブセット内で最初のレコードに現在のレコードの位置が移動します。同様に、 **Filter** プロパティを消去すると、現在のレコードの位置は **Recordset** 内で最初のレコードに移動します。</span><span class="sxs-lookup"><span data-stu-id="85a6a-p108">Whenever the **Filter** property is set, the current record position moves to the first record in the filtered subset of records in the **Recordset**. Similarly, when the **Filter** property is cleared, the current record position moves to the first record in the **Recordset**.</span></span>

<span data-ttu-id="85a6a-145">[Filter](bookmark-property-ado.md) プロパティで使用する配列を作成するときに使用するブックマーク値については、 **Bookmark** プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="85a6a-145">See the [Bookmark](bookmark-property-ado.md) property for an explanation of bookmark values from which you can build an array to use with the **Filter** property.</span></span>

<span data-ttu-id="85a6a-146">**フィルター**の抽出条件の文字列形式でのみ (例:"受注日" \> ' 12/31/1999 ') 保存された**レコード セット**の内容に影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="85a6a-146">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="85a6a-147">**Bookmark** の配列または **FilterGroupEnum** の値を使用して作成された **Filter** は、永続化された Recordset の内容に影響しません。</span><span class="sxs-lookup"><span data-stu-id="85a6a-147">**Filters** created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted Recordset.</span></span> <span data-ttu-id="85a6a-148">これらの規則は、クライアント側カーソルまたはサーバー側カーソルで作成された **Recordset** にも当てはまります。</span><span class="sxs-lookup"><span data-stu-id="85a6a-148">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

> [!NOTE]
> <span data-ttu-id="85a6a-p110">[!メモ] 単一キー テーブルのキー フィールドを基にしてフィルタリングが行われ、キー フィールド値に変更が加えられた場合、 **adFilterPendingRecords** フラグをフィルター処理および変更された **Recordset** に一括更新モードで適用すると、結果の **Recordset** は空になります。次のいずれかの条件が満たされる場合は、空ではない **Recordset** が得られます。</span><span class="sxs-lookup"><span data-stu-id="85a6a-p110">When you apply the **adFilterPendingRecords** flag to a filtered and modified **Recordset** in the batch update mode, the resultant **Recordset** is empty if the filtering was based on the key field of a single-keyed table and the modification was made on the key field values. The resultant **Recordset** will be non-empty if one of the following is true:</span></span>
> - <span data-ttu-id="85a6a-151">単一キー テーブルの非キー フィールドを基にしてフィルタリングが行われた。</span><span class="sxs-lookup"><span data-stu-id="85a6a-151">The filtering was based on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="85a6a-152">複数キー テーブルの任意のフィールドを基にしてフィルタリングが行われた。</span><span class="sxs-lookup"><span data-stu-id="85a6a-152">The filtering was based on any fields in a multiple-keyed table.</span></span>
> - <span data-ttu-id="85a6a-153">単一キー テーブルの非キー フィールドに変更が加えられた。</span><span class="sxs-lookup"><span data-stu-id="85a6a-153">Modifications were made on non-key fields in a single-keyed table.</span></span>
> - <span data-ttu-id="85a6a-154">複数キー テーブルの任意のフィールドに変更が加えられた。</span><span class="sxs-lookup"><span data-stu-id="85a6a-154">Modifications were made on any fields in a multiple-keyed table.</span></span>

<span data-ttu-id="85a6a-p111">次の表に、フィルタリングと変更の条件の各組み合わせにおける **adFilterPendingRecords** の効果を示します。左側の列は変更の対象のキーを示します。変更は、任意の非キー フィールド、単一キー テーブルのキー フィールド、または複数キー テーブルの任意のキー フィールドに対して行われる可能性があります。1 行目は、フィルター条件を示します。フィルタリングは、任意の非キー フィールド、単一キー テーブルのキー フィールド、または複数キー テーブルの任意のキー フィールドに基づいて行われる可能性があります。この行と列が交差したセルが結果を示します。つまり、+ は、 **adFilterPendingRecords** を適用すると空でない **Recordset** が得られることを表します。 **-** は、空の **Recordset** が得られることを表します。</span><span class="sxs-lookup"><span data-stu-id="85a6a-p111">The following table summarizes the effects of **adFilterPendingRecords** in different combinations of filtering and modifications. The left column shows the possible modifications; modifications can be made on any of the non-keyed fields, on the key field in a single-keyed table, or on any of the key fields in a multiple-keyed table. The top row shows the filtering criterion; filtering can be based on any of the non-keyed fields, the key field in a single-keyed table, or any of the key fields in a multiple-keyed table. The intersecting cells show the results: + means that applying **adFilterPendingRecords** results in a non-empty **Recordset**; **-** means an empty **Recordset**.</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
</p></th>
<th><p><span data-ttu-id="85a6a-159">非キー</span><span class="sxs-lookup"><span data-stu-id="85a6a-159">Non keys</span></span></p></th>
<th><p><span data-ttu-id="85a6a-160">単一キー</span><span class="sxs-lookup"><span data-stu-id="85a6a-160">Single Key</span></span></p></th>
<th><p><span data-ttu-id="85a6a-161">複数キー</span><span class="sxs-lookup"><span data-stu-id="85a6a-161">Multiple Keys</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85a6a-162">非キー</span><span class="sxs-lookup"><span data-stu-id="85a6a-162">Non keys</span></span></p></td>
<td><p>+</p></td>
<td><p>+</p></td>
<td><p>+</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85a6a-163">単一キー</span><span class="sxs-lookup"><span data-stu-id="85a6a-163">Single Key</span></span></p></td>
<td><p>+</p></td>
<td><p>-</p></td>
<td><p><span data-ttu-id="85a6a-164">N/A</span><span class="sxs-lookup"><span data-stu-id="85a6a-164">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="85a6a-165">複数キー</span><span class="sxs-lookup"><span data-stu-id="85a6a-165">Multiple Keys</span></span></p></td>
<td><p>+</p></td>
<td><p><span data-ttu-id="85a6a-166">N/A</span><span class="sxs-lookup"><span data-stu-id="85a6a-166">N/A</span></span></p></td>
<td><p>+</p></td>
</tr>
</tbody>
</table>

