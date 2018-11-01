---
title: レコードセットを使用する
TOCTitle: Working with Recordsets
ms:assetid: 9cd52866-2738-8150-381c-eee0b8a6cd36
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249711(v=office.15)
ms:contentKeyID: 48546608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d57f05905aa0f79c1a72638e70ede8bdabf73b8f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883688"
---
# <a name="working-with-recordsets"></a><span data-ttu-id="7b98f-102">レコードセットを使用する</span><span class="sxs-lookup"><span data-stu-id="7b98f-102">Working with Recordsets</span></span>


<span data-ttu-id="7b98f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7b98f-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="7b98f-p101">**Recordset** オブジェクトには、結果セット内のデータ順序の並べ替え、指定した基準に基づく特定のレコードの検索、さらにインデックスを使用した検索操作の最適化を実行できる機能が組み込まれています。これらの機能を使用できるかどうかは、プロバイダーによって異なり、 [Index](index-property-ado.md) プロパティなどの場合には、データ ソース自体の構造によっても異なります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p101">The **Recordset** object has built-in features that make it possible for you to rearrange the order of the data in the result set, to search for a specific record based on criteria that you supply, and even to optimize those search operations using indexes. Whether these features are available for use depends on the provider and in some cases — such as that of the [Index](index-property-ado.md) property — the structure of the data source itself.</span></span>

## <a name="arranging-data"></a><span data-ttu-id="7b98f-106">データの整列</span><span class="sxs-lookup"><span data-stu-id="7b98f-106">Arranging Data</span></span>

<span data-ttu-id="7b98f-p102">通常、 **Recordset** 内のデータを最も効率的に並べ替えるには、SQL コマンドで ORDER BY 句を指定して結果が返されるようにします。ただし、場合によっては、既に作成した **Recordset** のデータ順序を変更する必要があります。 **Sort** プロパティを使用すると、 **Recordset** の行をスキャンする順序を指定できます。さらに、 **Filter** プロパティを使用して、行のスキャン中にアクセスできる行を指定することもできます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p102">Often, the most efficient way to order the data in your **Recordset** is by specifying an ORDER BY clause in the SQL command used to return results to it. However, you might need to change the order of the data in a **Recordset** that has already been created. You can use the **Sort** property to establish the order in which rows of a **Recordset** are traversed. Furthermore, the **Filter** property determines which rows are accessible when traversing rows.</span></span>

<span data-ttu-id="7b98f-p103">**Sort** プロパティは、並べ替える **Recordset** のフィールド名を示す **String** 値を設定または返します。それぞれの名前はコンマで区切ります。名前の後には、スペース、およびキーワードとしてフィールドを昇順で並べ替える **ASC** または降順で並べ替える **DESC** を指定することもできます。既定では、キーワードを指定しない場合、フィールドは昇順で並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p103">The **Sort** property sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma and is optionally followed by a space and the keyword **ASC** (which sorts the field in ascending order) or **DESC** (which sorts the field in descending order). By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

<span data-ttu-id="7b98f-114">データは物理的に並べ替えられるわけではなく、インデックスで指定された順序でアクセスされるだけなので、並べ替え操作は効率的に行われます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-114">The sort operation is efficient because data is not physically rearranged but is simply accessed in the order specified by an index.</span></span>

<span data-ttu-id="7b98f-p104">**Sort** プロパティでは、 [CursorLocation](cursorlocation-property-ado.md) プロパティを **adUseClient** に設定する必要があります。インデックスがない場合、 **Sort** プロパティに指定されたフィールドごとに一時インデックスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p104">The **Sort** property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="7b98f-p105">**Sort** プロパティを空の文字列に設定すると、行は元の順序にリセットされ、一時インデックスが削除されます。既存のインデックスは削除されません。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p105">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="7b98f-119">という名前の*姓*、*ミドル ネームのイニシャル*、および*姓*の 3 つのフィールドが**レコード セット**に含まれていると仮定します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-119">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="7b98f-120">**Sort**プロパティを文字列に設定""、姓を降順と昇順の最初の名前に、**レコード セット**を順には。</span><span class="sxs-lookup"><span data-stu-id="7b98f-120">Set the **Sort** property to the string "", which will order the **Recordset** by last name in descending order and then by first name in ascending order.</span></span> <span data-ttu-id="7b98f-121">ミドル ネームは無視されます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-121">The middle initial is ignored.</span></span>

<span data-ttu-id="7b98f-p107">並べ替え条件で参照するフィールド名に "ASC" または "DESC" を使用することはできません。これは、キーワード **ASC** および **DESC** と競合するためです。 **Recordset** を返すクエリで **AS** キーワードを使用して、競合する名前のフィールドにエイリアスを指定してください。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p107">No field referenced in a sort criteria string can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

<span data-ttu-id="7b98f-124">**Recordset** のフィルターの詳細については、「結果のフィルター処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b98f-124">For more details about **Recordset** filtering, see Filtering the Results later in this topic.</span></span>

## <a name="finding-a-specific-record"></a><span data-ttu-id="7b98f-125">特定のレコードの検索</span><span class="sxs-lookup"><span data-stu-id="7b98f-125">Finding a Specific Record</span></span>

<span data-ttu-id="7b98f-p108">ADO には、 [Recordset](find-method-ado.md) 内の特定のレコードを検索するための [Find](seek-method-ado.md) メソッドと **Seek** メソッドがあります。 **Find** メソッドはさまざまなプロバイダーでサポートされていますが、検索基準は 1 つしか設定できません。 **Seek** メソッドでは複数の検索基準を設定できますが、サポートするプロバイダーが限られます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p108">ADO provides the [Find](find-method-ado.md) and [Seek](seek-method-ado.md) methods for locating a particular record in a **Recordset**. The **Find** method is supported by a variety of providers but is limited to a single search criterion. The **Seek** method supports searching on multiple criteria, but is not supported by many providers.</span></span>

<span data-ttu-id="7b98f-p109">フィールドのインデックスを使用すると、 **Recordset** オブジェクトの **Find** メソッド、 **Sort** プロパティ、および **Filter** プロパティのパフォーマンスを大幅に向上できます。 **Field** オブジェクトの内部インデックスを作成するには、動的な [Optimize](optimize-property-dynamic-ado.md) プロパティを設定します。この動的プロパティは、 **CursorLocation** プロパティを **adUseClient** に設定したときに、 [Field](cursorlocation-property-ado.md) オブジェクトの **Properties** コレクションに追加されます。ただし、このインデックスは ADO 内部でのみ使用でき、外部からアクセスしたり、他の目的で使用することはできません。また、このインデックスは、 **Recordset** オブジェクトの [Index](index-property-ado.md) プロパティとは異なります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p109">Indexes on fields can greatly enhance the performance of the **Recordset** object's **Find** method and **Sort** and **Filter** properties. You can create an internal index for a **Field** object by setting its dynamic [Optimize](optimize-property-dynamic-ado.md) property. This dynamic property is added to the **Field** object's **Properties** collection when you set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**. Remember that this index is internal to ADO — you cannot gain access to it or use it for any other purpose. Also, this index is distinct from the **Recordset** object's [Index](index-property-ado.md) property.</span></span>

<span data-ttu-id="7b98f-p110">**Find** メソッドは、 **Recordset** の列 (フィールド) 内をすばやく検索します。 **Optimize** プロパティを使用して列のインデックスを作成すると、通常は **Find** メソッドの動作の速度が向上します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p110">The **Find** method quickly locates a value within a column (field) of a **Recordset**. You can often improve the speed of the **Find** method's operation on a column by using the **Optimize** property to create an index on it.</span></span>

<span data-ttu-id="7b98f-p111">**Find** メソッドでは、1 つのフィールドの内容しか検索できません。 **Seek** メソッドではインデックスが必要であり、その他の制限もあります。インデックスのベースではない複数のフィールドを検索する必要がある場合、またはプロバイダーがインデックスをサポートしていない場合は、 **Recordset** オブジェクトの **Filter** プロパティを使用して結果を絞り込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p111">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that aren't the basis of an index, or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

## <a name="find"></a><span data-ttu-id="7b98f-139">Find</span><span class="sxs-lookup"><span data-stu-id="7b98f-139">Find</span></span>

<span data-ttu-id="7b98f-p112">**Find** メソッドでは、指定した条件を満たす行の **Recordset** を検索します。必要に応じて、検索の方向、開始行、および開始行からのオフセットを指定できます。条件が一致すると、カレント行の位置は、検出されたレコードに設定されます。条件を満たす行がない場合、カレント行の位置は、検索する方向によって、 **Recordset** の最後または最初に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p112">The **Find** method searches a **Recordset** for the row that satisfies a specified criterion. Optionally, the direction of the search, starting row, and offset from the starting row may be specified. If the criterion is met, the current row position is set on the found record; otherwise, the position is set to the end (or start) of the **Recordset**, depending on search direction.</span></span>

<span data-ttu-id="7b98f-p113">基準に指定できるのは、単一列の名前のみです。つまり、このメソッドでは複数列の検索はサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p113">Only a single-column name may be specified for the criterion. In other words, this method does not support multi-column searches.</span></span>

<span data-ttu-id="7b98f-145">条件の比較演算子があります」**\>**」(より大きい)、「**\<**(より小さい)、「=」(等号) にした場合は、「\>=」(より大きいか等しい)、"\<=」(以上)、"\<\>」(等しくない)、"LIKE"(パターン マッチング)、または。</span><span class="sxs-lookup"><span data-stu-id="7b98f-145">The comparison operator for the criterion may be "**\>**" (greater than), "**\<**" (less than), "=" (equal), "\>=" (greater than or equal), "\<=" (less than or equal), "\<\>" (not equal), or "LIKE" (pattern matching).</span></span>

<span data-ttu-id="7b98f-146">基準値には、文字列、浮動小数点数、または日付があります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-146">The criterion value may be a string, floating-point number, or date.</span></span> <span data-ttu-id="7b98f-147">文字列値は単一引用符で区切られたまたは」\#」(シャープ記号) のマークを付けます (など、"状態 = 'WA'」または」状態 = \#WA\#」)。</span><span class="sxs-lookup"><span data-stu-id="7b98f-147">String values are delimited with single quotes or "\#" (number sign) marks (for example, "state = 'WA'" or "state = \#WA\#").</span></span> <span data-ttu-id="7b98f-148">区切られた日付の値」\#」(シャープ記号) のマークを付けます (たとえば、」開始\_日\> \#97/7/22\#」)。</span><span class="sxs-lookup"><span data-stu-id="7b98f-148">Date values are delimited with "\#" (number sign) marks (for example, "start\_date \> \#7/22/97\#").</span></span>

<span data-ttu-id="7b98f-p115">比較演算子に "like" を使用する場合、文字列の値にアスタリスク (\*) を含めると、1 つまたは複数の文字または部分文字列を検索できます。たとえば、「state like 'M\*'」と指定すると、Maine や Massachusetts が検索されます。文字列の先頭と末尾にアスタリスクを使用して、その値に含まれる部分文字列を検索することもできます。たとえば、「state like '\*as\*'」と指定すると、Alaska、Arkansas、および Massachusetts が検索されます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p115">If the comparison operator is "like", the string value may contain an asterisk (\*) to find one or more occurrences of any character or substring. For example, "state like 'M\*'" matches Maine and Massachusetts. You can also use leading and trailing asterisks to find a substring contained within the values. For example, "state like '\*as\*'" matches Alaska, Arkansas, and Massachusetts.</span></span>

<span data-ttu-id="7b98f-p116">前の例のように、アスタリスクを使用できるのは、基準文字列の末尾、または検索文字列の先頭と末尾の両方の場合のみです。先頭のワイルドカード ('\*str') または文字列中のワイルドカード ('s\*r') としてアスタリスクを使用することはできません。この場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p116">Asterisks can be used only at the end of a criteria string or together at both the beginning and end of a criteria string, as shown above. You cannot use the asterisk as a leading wildcard ('\*str') or embedded wildcard ('s\*r'). This will cause an error.</span></span>

## <a name="seek-and-index"></a><span data-ttu-id="7b98f-156">Seek および Index</span><span class="sxs-lookup"><span data-stu-id="7b98f-156">Seek and Index</span></span>

<span data-ttu-id="7b98f-p117">基になるプロバイダーが **Recordset** オブジェクトのインデックスをサポートしている場合、**Index** プロパティと共に **Seek** メソッドを使用します。基になるプロバイダーが **Seek** をサポートしているかどうかを判別するには、[Supports](supports-method-ado.md)**(adSeek)** メソッドを使用します。プロバイダーがインデックスをサポートしているかどうかを判別するには、**Supports(adIndex)** メソッドを使用します。たとえば、[OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) は **Seek** および **Index** をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p117">Use the **Seek** method in conjunction with the **Index** property if the underlying provider supports indexes on the **Recordset** object. Use the [Supports](supports-method-ado.md)**(adSeek)** method to determine whether the underlying provider supports **Seek**, and the **Supports(adIndex)** method to determine whether the provider supports indexes. (For example, the [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) supports **Seek** and **Index**.)</span></span>

<span data-ttu-id="7b98f-p118">**Seek** メソッドで目的の行が見つからない場合、エラーは発生せず、行は **Recordset** の末尾に配置されます。このメソッドを実行する前に、 **Index** プロパティを必要なインデックスに設定してください。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p118">If **Seek** does not find the desired row, no error occurs, and the row is positioned at the end of the **Recordset**. Set the **Index** property to the desired index before executing this method.</span></span>

<span data-ttu-id="7b98f-p119">このメソッドは、サーバー側のカーソルでのみサポートされます。 **Recordset** オブジェクトの [CursorLocation](cursorlocation-property-ado.md) プロパティの値が **adUseClient** の場合、Seek はサポートされません。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p119">This method is supported only with server-side cursors. Seek is not supported when the **Recordset** object's [CursorLocation](cursorlocation-property-ado.md) property value is **adUseClient**.</span></span>

<span data-ttu-id="7b98f-164">このメソッドは、 **Recordset** オブジェクトが [adCmdTableDirect](commandtypeenum.md) の **CommandTypeEnum** 値で開かれている場合のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-164">This method can be used only when the **Recordset** object has been opened with a [CommandTypeEnum](commandtypeenum.md) value of **adCmdTableDirect**.</span></span>

## <a name="filtering-the-results"></a><span data-ttu-id="7b98f-165">結果のフィルター処理</span><span class="sxs-lookup"><span data-stu-id="7b98f-165">Filtering the Results</span></span>

<span data-ttu-id="7b98f-p120">**Find** メソッドでは、1 つのフィールドの内容しか検索できません。 **Seek** メソッドではインデックスが必要であり、その他の制限もあります。インデックスのベースではない複数のフィールドを検索する必要がある場合、またはプロバイダーがインデックスをサポートしていない場合は、 **Recordset** オブジェクトの **Filter** プロパティを使用して結果を絞り込む必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p120">The **Find** method limits your search to the contents of one field. The **Seek** method requires that you have an index and has other limitations as well. If you need to search on multiple fields that are not the basis of an index or if your provider does not support indexes, you can limit your results using the **Filter** property of the **Recordset** object.</span></span>

<span data-ttu-id="7b98f-p121">**Filter** プロパティを使用すると、 **Recordset** オブジェクト内の特定のレコードを抽出できます。フィルター処理後の **Recordset** は現在のカーソルになり、 **Filter** 基準を満たさないレコードは、 **Filter** が削除されるまで **Recordset** では使用できなくなります。 **AbsolutePosition** 、 **AbsolutePage** 、 **RecordCount** 、 **PageCount** など、現在のカーソルに基づいて値を返すその他のプロパティが影響を受けます。これは、 **Filter** プロパティを特定の値に設定すると、現在のレコードが新しい値を満たす最初のレコードに移動するためです。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p121">Use the **Filter** property to selectively screen out records in a **Recordset** object. The filtered **Recordset** becomes the current cursor, which means that records that do not satisfy the **Filter** criteria are not available in the **Recordset** until the **Filter** is removed. Other properties that return values based on the current cursor are affected, such as **AbsolutePosition**, **AbsolutePage**, **RecordCount**, and **PageCount**. This is because setting the **Filter** property to a specific value will move the current record to the first record that satisfies the new value.</span></span>

<span data-ttu-id="7b98f-p122">**Filter** プロパティには、バリアント型の引数を指定します。この値は、 **Filter** プロパティを使用するための 3 つの方法、つまり検索条件文字列、 **FilterGroupEnum** 定数、ブックマークの配列のうちの 1 つを表します。詳細については、「検索条件文字列によるフィルター処理」、「定数によるフィルター処理」、および「ブックマークによるフィルター処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p122">The **Filter** property takes a variant argument. This value represents one of three methods for using the **Filter** property: a criteria string, a **FilterGroupEnum** constant, or an array of bookmarks. For more information, see Filtering with a Criteria String, Filtering with a Constant, and Filtering with Bookmarks later in this topic.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7b98f-176">[!メモ] 選択するデータがわかっている場合は、 <STRONG>Filter</STRONG> プロパティを使用するのではなく、結果セットを効果的にフィルター処理する SQL ステートメントを使用して <STRONG>Recordset</STRONG> を開く方が効率的です。</span><span class="sxs-lookup"><span data-stu-id="7b98f-176">When you know the data you want to select, it is usually more efficient to open a <STRONG>Recordset</STRONG> with a SQL statement that effectively filters the result set, rather than relying on the <STRONG>Filter</STRONG> property.</span></span></P>



<span data-ttu-id="7b98f-p123">**Recordset** からフィルターを削除するには、 **adFilterNone** 定数を使用します。 **Filter** プロパティを長さ 0 の文字列 ("") に設定すると、 **adFilterNone** 定数を使用した場合と同じ結果になります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p123">To remove a filter from a **Recordset**, use the **adFilterNone** constant. Setting the **Filter** property to a zero-length string ("") has the same effect as using the **adFilterNone** constant.</span></span>

## <a name="filtering-with-a-criteria-string"></a><span data-ttu-id="7b98f-179">検索条件文字列によるフィルター処理</span><span class="sxs-lookup"><span data-stu-id="7b98f-179">Filtering with a Criteria String</span></span>

<span data-ttu-id="7b98f-180">抽出条件文字列で構成された*演算子の値をフィールド名*の形式の句で (たとえば、"[氏名] = 'Smith'")。</span><span class="sxs-lookup"><span data-stu-id="7b98f-180">The criteria string is made up of clauses in the form *FieldName Operator Value* (for example, "LastName = 'Smith'").</span></span> <span data-ttu-id="7b98f-181">複合句を作成するには、個々 の句を連結することによりと (たとえば、"[氏名] = 'Smith' AND FirstName = 'John'") したり (たとえば、)。</span><span class="sxs-lookup"><span data-stu-id="7b98f-181">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, ).</span></span> <span data-ttu-id="7b98f-182">複合句を作成するには、個々 の句を連結することによりと (など」[氏名] = 'Smith' AND FirstName = 'John'") や (など"[氏名] = 'Smith' または [氏名] = 'Jones'")。</span><span class="sxs-lookup"><span data-stu-id="7b98f-182">You can create compound clauses by concatenating individual clauses with AND (for example, "LastName = 'Smith' AND FirstName = 'John'") and OR (for example, "LastName = 'Smith' OR LastName = 'Jones'").</span></span> <span data-ttu-id="7b98f-183">検索条件文字列を指定する際は、次の点に注意してください。</span><span class="sxs-lookup"><span data-stu-id="7b98f-183">Use the following guidelines for criteria strings:</span></span>

  - <span data-ttu-id="7b98f-184">*フィールド名*は、**レコード セット**からの有効なフィールド名である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-184">*FieldName* must be a valid field name from the **Recordset**.</span></span> <span data-ttu-id="7b98f-185">フィールド名にスペースを含める場合は、名前を角かっこで囲みます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-185">If the field name contains spaces, you must enclose the name in square brackets.</span></span>

  - <span data-ttu-id="7b98f-186">*演算子*は、次のいずれかである必要があります: \<、 \>、 \<= \>= \< \>=、または。</span><span class="sxs-lookup"><span data-stu-id="7b98f-186">*Operator* must be one of the following: \<, \>, \<=, \>=, \<\>, =, or LIKE.</span></span>

  - <span data-ttu-id="7b98f-187">*値*は、フィールドの値を比較する値 (たとえば、'Smith' \#8/24/95\#、12.345、または $50.00)。</span><span class="sxs-lookup"><span data-stu-id="7b98f-187">*Value* is the value with which you will compare the field values (for example, 'Smith', \#8/24/95\#, 12.345, or $50.00).</span></span> <span data-ttu-id="7b98f-188">文字列に単一引用符 (') を使用し、シャープ記号 (\#) の日付にします。</span><span class="sxs-lookup"><span data-stu-id="7b98f-188">Use single quotation marks (') with strings and pound signs (\#) with dates.</span></span> <span data-ttu-id="7b98f-189">数値の場合、小数点、ドル記号、および指数表記を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-189">For numbers, you can use decimal points, dollar signs, and scientific notation.</span></span> <span data-ttu-id="7b98f-190">*演算子*は、*値*は、ワイルドカードを使用できます。 場合、</span><span class="sxs-lookup"><span data-stu-id="7b98f-190">If *Operator* is LIKE, *Value* can use wildcards.</span></span> <span data-ttu-id="7b98f-191">アスタリスクのみ (\*) パーセント記号 (%) とワイルドカードを使用し、文字列の最後の文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-191">Only the asterisk (\*) and percent sign (%) wildcards are allowed, and they must be the last character in the string.</span></span> <span data-ttu-id="7b98f-192">*値*を null にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="7b98f-192">*Value* cannot be null.</span></span>
    

    > [!NOTE]
    > <P><span data-ttu-id="7b98f-193">フィルター<EM>値</EM>に一重引用符 (') は、いずれかを表す 2 つの単一引用符を使用します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-193">To include single quotation marks (') in the filter <EM>Value</EM>, use two single quotation marks to represent one.</span></span> <span data-ttu-id="7b98f-194">たとえば、 <EM>O'Malley</EM>にフィルターを適用する抽出条件文字列する必要があります"col1 = 'O' Malley'"。</span><span class="sxs-lookup"><span data-stu-id="7b98f-194">For example, to filter on <EM>O'Malley</EM>, the criteria string should be "col1 = 'O''Malley'".</span></span> <span data-ttu-id="7b98f-195">フィルター値の先頭と末尾の両方に単一引用符を使用するには、文字列をシャープ記号 (#) で囲みます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-195">To include single quotation marks at both the beginning and the end of the filter value, enclose the string in pound signs (#).</span></span> <span data-ttu-id="7b98f-196">たとえば、 <EM>'</EM>1' には、フィルター処理、条件文字列する必要があります"col1 = #' 1' #"します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-196">For example, to filter on <EM>'1'</EM>, the criteria string should be "col1 = #'1'#".</span></span></P>



<span data-ttu-id="7b98f-p128">AND と OR には優先順位はありません。かっこを使用して句をグループ化できます。ただし、次のように OR で結合したグループ句を、AND を使用してさらに別の句に結合することはできません。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p128">There is no precedence between AND and OR. Clauses can be grouped within parentheses. However, you cannot group clauses joined by an OR and then join the group to another clause with an AND, like this:</span></span>

```vb 
 
(LastName = 'Smith' OR LastName = 'Jones') AND FirstName = 'John' 
```

<span data-ttu-id="7b98f-200">この場合は、このフィルターを次のように構成します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-200">Instead, you would construct this filter as:</span></span>

```vb 
 
(LastName = 'Smith' AND FirstName = 'John') OR (LastName = 'Jones' AND FirstName = 'John') 
```

<span data-ttu-id="7b98f-201">LIKE 句では、先頭と末尾、パターンのワイルドカードを使用できます (たとえば、[氏名] のような '\*mit\*') または (など) のパターンの終了時にのみ、またはパターンの終了時にのみ (たとえば、[氏名] のような' Smit\*')。</span><span class="sxs-lookup"><span data-stu-id="7b98f-201">In a LIKE clause, you can use a wildcard at the beginning and end of the pattern (for example, LastName Like '\*mit\*') or only at the end of the pattern (for example, ) or only at the end of the pattern (for example, LastName Like 'Smit\*').</span></span>

## <a name="filtering-with-a-constant"></a><span data-ttu-id="7b98f-202">定数によるフィルター処理</span><span class="sxs-lookup"><span data-stu-id="7b98f-202">Filtering with a Constant</span></span>

<span data-ttu-id="7b98f-203">**Recordsets** のフィルター処理では、次の定数を使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-203">The following constants are available for filtering **Recordsets**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7b98f-204">定数</span><span class="sxs-lookup"><span data-stu-id="7b98f-204">Constant</span></span></p></th>
<th><p><span data-ttu-id="7b98f-205">説明</span><span class="sxs-lookup"><span data-stu-id="7b98f-205">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7b98f-206"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="7b98f-206"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="7b98f-207"><strong>Delete</strong>、<strong>Resync</strong>、<strong>UpdateBatch</strong>、または <strong>CancelBatch</strong> の最後の呼び出しによって影響を受けたレコードのみを表示するようにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-207">Filters for viewing only records effected by the last <strong>Delete</strong>, <strong>Resync</strong>, <strong>UpdateBatch</strong>, or <strong>CancelBatch</strong> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b98f-208"><strong>競合</strong></span><span class="sxs-lookup"><span data-stu-id="7b98f-208"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="7b98f-209">最後のバッチ更新が失敗したレコードを表示するようにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-209">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b98f-210"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="7b98f-210"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="7b98f-211">現在のキャッシュ内のレコード、つまりデータベースからレコードを取得するための最後の呼び出しの結果を表示するようにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-211">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7b98f-212"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="7b98f-212"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="7b98f-213">現在のフィルターを削除し、すべてのレコードを復元して表示します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-213">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7b98f-214"><strong>行と列</strong></span><span class="sxs-lookup"><span data-stu-id="7b98f-214"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="7b98f-p129">変更が行われたが、変更内容がサーバーにまだ送信されていないレコードのみを表示するようにフィルター処理します。バッチ更新モードの場合のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p129">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7b98f-217">フィルター定数を使用すると、バッチ更新モードでレコードに競合が発生した場合、 **UpdateBatch** メソッドの最後の呼び出しで影響を受けたレコードのみを表示するなどの方法で、競合を簡単に解決できます。次に例を示します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-217">The filter constants make it easier to resolve individual record conflicts during batch update mode by allowing you to view, for example, only those records that were effected during the last **UpdateBatch** method call, as shown in the following example:</span></span>

```vb 
 
'BeginDeleteGroup 
    'add some bogus records 
    With objRs1 
        For i = 0 To 8 
            .AddNew 
            .Fields("CompanyName") = "Shipper Number " & i + 1 
            .Fields("Phone") = "(425) 555-000" & (i + 1) 
            .Update 
        Next i 
         
    're-connect & update 
        .ActiveConnection = GetNewConnection 
        .UpdateBatch 
         
    'filter on newly added records 
        .Filter = adFilterAffectedRecords 
        Debug.Print "Deleting the " & .RecordCount & _ 
                    " records you just added." 
         
    'delete the newly added bogus records 
        .Delete adAffectGroup 
        .Filter = adFilterNone 
        Debug.Print .RecordCount & " records remain." 
         
        .Close 
    End With 
'EndDeleteGroup 
```

## <a name="filtering-with-bookmarks"></a><span data-ttu-id="7b98f-218">ブックマークによるフィルター処理</span><span class="sxs-lookup"><span data-stu-id="7b98f-218">Filtering with Bookmarks</span></span>

<span data-ttu-id="7b98f-219">最後に、バリアント型のブックマークの配列を **Filter** プロパティに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-219">Finally, you can pass a variant array of bookmarks to the **Filter** property.</span></span> <span data-ttu-id="7b98f-220">結果カーソルに含まれるのは、ブックマークがプロパティに渡されたレコードのみです。</span><span class="sxs-lookup"><span data-stu-id="7b98f-220">The resulting cursor will contain only those records whose bookmark was passed in to the property.</span></span> <span data-ttu-id="7b98f-221">次のコード例では、 *[商品名]* フィールドに"B"が含まれて、**レコード セット**内のレコードからブックマークの配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-221">The following code example creates an array of bookmarks from the records in a **Recordset** which have a "B" in the *ProductName* field.</span></span> <span data-ttu-id="7b98f-222">次に、配列を **Filter** プロパティに渡し、フィルター処理された **Recordset** に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="7b98f-222">It then passes the array to the **Filter** property and displays information about the resulting filtered **Recordset**.</span></span>

```vb 
 
'BeginFilterBkmk 
    Dim vBkmkArray() As Variant 
    Dim i As Integer 
 
    'Recordset created using "SELECT * FROM Products" as command. 
    'So, we will check to see if ProductName has a capital B, and 
    'if so, add to the array. 
    i = 0 
    Do While Not objRs.EOF 
        If InStr(1, objRs("ProductName"), "B") Then 
            ReDim Preserve vBkmkArray(i) 
            vBkmkArray(i) = objRs.Bookmark 
            i = i + 1 
            Debug.Print objRs("ProductName") 
        End If 
        objRs.MoveNext 
    Loop 
     
    'Filter using the array of bookmarks. 
    objRs.Filter = vBkmkArray 
     
    objRs.MoveFirst 
    Do While Not objRs.EOF 
        Debug.Print objRs("ProductName") 
        objRs.MoveNext 
    Loop 
    'EndFilterBkmk 
```

## <a name="creating-a-clone-of-a-recordset"></a><span data-ttu-id="7b98f-223">Recordset の複製の作成</span><span class="sxs-lookup"><span data-stu-id="7b98f-223">Creating a Clone of a Recordset</span></span>

<span data-ttu-id="7b98f-p131">複数の **Recordset** オブジェクトの複製を作成するには、 **Clone** メソッドを使用します。特に、特定のレコードセット内の現在のレコードを複数保持する場合に、このメソッドを使用します。 **Clone** メソッドを使用すると、同じ定義を使用して新規の **Recordset** オブジェクトを作成して開くよりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p131">Use the **Clone** method to create multiple, duplicate **Recordset** objects, particularly if you want to maintain more than one current record in a given set of records. Using the **Clone** method is more efficient than creating and opening a new **Recordset** object with the same definition as the original.</span></span>

<span data-ttu-id="7b98f-p132">新規に作成された複製の現在のレコードは、当初は最初のレコードに設定されます。複製の Recordset の現在のレコードのポインターは、複製元の Recordset とは同期しません。また、その逆も同様です。各 Recordset 内を別々に移動できます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p132">The current record of a newly created clone is originally set to the first record. The current record pointer in a cloned **Recordset** is not synchronized with the original or vice versa. You can navigate independently in each **Recordset**.</span></span>

<span data-ttu-id="7b98f-p133">1 つの **Recordset** オブジェクトに加えた変更は、カーソルの種類に関係なく、すべての複製で表示できます。ただし、複製元の [Recordset](requery-method-ado.md) で **Requery** を実行した後は、複製は複製元の Recordset とは同期しなくなります。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p133">Changes you make to one **Recordset** object are visible in all of its clones regardless of cursor type. However, after you execute [Requery](requery-method-ado.md) on the original **Recordset**, the clones will no longer be synchronized to the original.</span></span>

<span data-ttu-id="7b98f-231">複製元の **Recordset** を閉じても、そのコピーは開いたままです。また、コピーを閉じても、複製元またはその他のコピーは開いたままです。</span><span class="sxs-lookup"><span data-stu-id="7b98f-231">Closing the original **Recordset** does not close its copies, nor does closing a copy close the original or any of the other copies.</span></span>

<span data-ttu-id="7b98f-p134">**Recordset** オブジェクトがブックマークをサポートする場合のみ、オブジェクトの複製を作成できます。ブックマークの値は共通です。つまり、1 つの **Recordset** オブジェクトのブックマークで、すべての複製の同じレコードを参照できます。</span><span class="sxs-lookup"><span data-stu-id="7b98f-p134">You can clone a **Recordset** object only if it supports bookmarks. Bookmark values are interchangeable; that is, a bookmark reference from one **Recordset** object refers to the same record in any of its clones.</span></span>

