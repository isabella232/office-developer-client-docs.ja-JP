---
<span data-ttu-id="0089d-101"><<<<<<< ヘッド タイトル: 並べ替えプロパティ (ADO) TOCTitle: 並べ替えプロパティ (ADO) === タイトル: 並べ替えのプロパティ (ADO) TOCTitle: プロパティ (ADO) を並べ替える</span><span class="sxs-lookup"><span data-stu-id="0089d-101"><<<<<<< HEAD title: Sort Property (ADO) TOCTitle: Sort Property (ADO) ======= title: Sort property (ADO) TOCTitle: Sort property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0089d-102">マスターの ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15) ms:contentKeyID: 48548652 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="0089d-102">master ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15) ms:contentKeyID: 48548652 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="0089d-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="0089d-103"><<<<<<< HEAD</span></span>
# <a name="sort-property-ado"></a><span data-ttu-id="0089d-104">Sort プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0089d-104">Sort Property (ADO)</span></span>
=======
# <a name="sort-property-ado"></a><span data-ttu-id="0089d-105">Sort プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="0089d-105">Sort property (ADO)</span></span>
>>>>>>> <span data-ttu-id="0089d-106">master</span><span class="sxs-lookup"><span data-stu-id="0089d-106">master</span></span>


<span data-ttu-id="0089d-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0089d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0089d-108">[Recordset](recordset-object-ado.md) の並べ替えに使用するフィールド名、および各フィールドの並べ替え順序が昇順か降順かを示します。</span><span class="sxs-lookup"><span data-stu-id="0089d-108">Indicates one or more field names on which the [Recordset](recordset-object-ado.md) is sorted, and whether each field is sorted in ascending or descending order.</span></span>

<span data-ttu-id="0089d-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="0089d-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="0089d-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="0089d-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="0089d-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="0089d-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="0089d-112">master</span><span class="sxs-lookup"><span data-stu-id="0089d-112">master</span></span>

<span data-ttu-id="0089d-p101">**Recordset** の並べ替えに使用するフィールド名を示す文字列型 ( **String** ) の値を設定または取得します。各フィールド名はコンマで区切って指定し、フィールド名に続けて空白およびキーワードとして、フィールドを昇順で並べ替えることを示す **ASC** または降順で並べ替えることを示す **DESC** を指定できます。既定では、キーワードを指定しなかった場合、フィールドは昇順に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="0089d-p101">Sets or returns a **String** value that indicates the field names in the **Recordset** on which to sort. Each name is separated by a comma, and is optionally followed by a blank and the keyword, **ASC**, which sorts the field in ascending order, or **DESC**, which sorts the field in descending order. By default, if no keyword is specified, the field is sorted in ascending order.</span></span>

## <a name="remarks"></a><span data-ttu-id="0089d-116">解説</span><span class="sxs-lookup"><span data-stu-id="0089d-116">Remarks</span></span>

<span data-ttu-id="0089d-p102">このプロパティを使用するには、[CursorLocation](cursorlocation-property-ado.md) プロパティが **adUseClient** に設定されている必要があります。インデックスが存在しない場合は、 **Sort** プロパティで指定した各フィールドについて一時インデックスが作成されます。</span><span class="sxs-lookup"><span data-stu-id="0089d-p102">This property requires the [CursorLocation](cursorlocation-property-ado.md) property to be set to **adUseClient**. A temporary index will be created for each field specified in the **Sort** property if an index does not already exist.</span></span>

<span data-ttu-id="0089d-119">並べ替え処理では、データは物理的に並べ替えられるわけではなく、インデックスで指定された順序でアクセスされるだけなので効率的です。</span><span class="sxs-lookup"><span data-stu-id="0089d-119">The sort operation is efficient because data is not physically rearranged, but is simply accessed in the order specified by the index.</span></span>

<span data-ttu-id="0089d-p103">**Sort** プロパティを空の文字列に設定すると、行は元の順序にリセットされ、一時インデックスは削除されます。既存のインデックスは削除されません。</span><span class="sxs-lookup"><span data-stu-id="0089d-p103">Setting the **Sort** property to an empty string will reset the rows to their original order and delete temporary indexes. Existing indexes will not be deleted.</span></span>

<span data-ttu-id="0089d-122">という名前の*姓*、*ミドル ネームのイニシャル*、および*姓*の 3 つのフィールドが**レコード セット**に含まれていると仮定します。</span><span class="sxs-lookup"><span data-stu-id="0089d-122">Suppose a **Recordset** contains three fields named *firstName*, *middleInitial*, and *lastName*.</span></span> <span data-ttu-id="0089d-123">**Sort**プロパティを設定、文字列では、「姓 DESC、firstName ASC」には順序**レコード セット**の姓で降順に並べ替え次に、昇順の最初の名前です。</span><span class="sxs-lookup"><span data-stu-id="0089d-123">Set the **Sort** property to the string, "lastName DESC, firstName ASC", which will order the **Recordset** by last name in descending order, then by first name in ascending order.</span></span> <span data-ttu-id="0089d-124">ミドルネームのイニシャルは無視されます。</span><span class="sxs-lookup"><span data-stu-id="0089d-124">The middle initial is ignored.</span></span>

<span data-ttu-id="0089d-p105">"ASC" または "DESC" というフィールド名は、キーワード **ASC** および **DESC** と競合するので使用できません。名前が競合する場合は、 **Recordset** を返すクエリで **AS** キーワードを使用して、名前が競合するフィールドに別名を指定します。</span><span class="sxs-lookup"><span data-stu-id="0089d-p105">No field can be named "ASC" or "DESC" because those names conflict with the keywords **ASC** and **DESC**. Give a field with a conflicting name an alias by using the **AS** keyword in the query that returns the **Recordset**.</span></span>

