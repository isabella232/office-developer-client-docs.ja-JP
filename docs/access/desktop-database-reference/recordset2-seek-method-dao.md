---
title: Recordset2.Seek メソッド (DAO)
TOCTitle: Seek Method
ms:assetid: 9871619b-a303-c97d-54c0-defc8d9b87f5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197940(v=office.15)
ms:contentKeyID: 48546489
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1fe810516f5c9b79897267650e757bbf856b4ac
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479000"
---
# <a name="recordset2seek-method-dao"></a><span data-ttu-id="2f9d6-102">Recordset2.Seek メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="2f9d6-102">Recordset2.Seek Method (DAO)</span></span>


<span data-ttu-id="2f9d6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2f9d6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2f9d6-104">インデックス付きのテーブル タイプの **Recordset** オブジェクトで、現在のインデックスの指定された条件を満たすレコードを検索し、そのレコードをカレント レコードにします (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-104">Locates the record in an indexed table-type **Recordset** object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="2f9d6-105">構文</span><span class="sxs-lookup"><span data-stu-id="2f9d6-105">Syntax</span></span>

<span data-ttu-id="2f9d6-106">*式*です。(***比較***、 ***Key1***、 ***Key2***、 ***key3 以降***、 ***Key4***、 ***Key5***、 ***Key6***、 ***Key7***、 ***Key8***、 ***Key9***、 ***Key10***、 ***Key11***、 ***Key12***、 ***Key13***) を求める</span><span class="sxs-lookup"><span data-stu-id="2f9d6-106">*expression* .Seek(***Comparison***, ***Key1***, ***Key2***, ***Key3***, ***Key4***, ***Key5***, ***Key6***, ***Key7***, ***Key8***, ***Key9***, ***Key10***, ***Key11***, ***Key12***, ***Key13***)</span></span>

<span data-ttu-id="2f9d6-107">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-107">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="2f9d6-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2f9d6-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2f9d6-109">名前</span><span class="sxs-lookup"><span data-stu-id="2f9d6-109">Name</span></span></p></th>
<th><p><span data-ttu-id="2f9d6-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="2f9d6-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="2f9d6-111">データ型</span><span class="sxs-lookup"><span data-stu-id="2f9d6-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="2f9d6-112">説明</span><span class="sxs-lookup"><span data-stu-id="2f9d6-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2f9d6-113">Comparison</span><span class="sxs-lookup"><span data-stu-id="2f9d6-113">Comparison</span></span></p></td>
<td><p><span data-ttu-id="2f9d6-114">必須</span><span class="sxs-lookup"><span data-stu-id="2f9d6-114">Required</span></span></p></td>
<td><p><span data-ttu-id="2f9d6-115"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="2f9d6-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="2f9d6-116">&lt;、&lt;=、=、&gt;=、&gt; のうちいずれかの文字列式です。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-116">One of the following string expressions: &lt;, &lt;=, =, &gt;=, or &gt;.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2f9d6-117">Key1, Key2...Key13</span><span class="sxs-lookup"><span data-stu-id="2f9d6-117">Key1, Key2...Key13</span></span></p></td>
<td><p><span data-ttu-id="2f9d6-118">必須</span><span class="sxs-lookup"><span data-stu-id="2f9d6-118">Required</span></span></p></td>
<td><p><span data-ttu-id="2f9d6-119"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="2f9d6-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="2f9d6-120"><strong>Recordset</strong> オブジェクトの <strong>Index</strong> プロパティの設定で指定された現在のインデックスのフィールドに対応する 1 つ以上の値です。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-120">One or more values corresponding to fields in the <strong>Recordset</strong> object's current index, as specified by its <strong>Index</strong> property setting.</span></span> <span data-ttu-id="2f9d6-121">引数 key は最大 13 個まで使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-121">You can use up to 13 key arguments.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="2f9d6-122">注釈</span><span class="sxs-lookup"><span data-stu-id="2f9d6-122">Remarks</span></span>

<span data-ttu-id="2f9d6-p102">**Seek** を使用する前に、 **Index** プロパティで現在のインデックスを設定しておく必要があります。インデックスが一意でないキー フィールドを指している場合、 **Seek** は条件を満たす最初のレコードを返します。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-p102">You must set the current index with the **Index** property before you use **Seek**. If the index identifies a nonunique key field, **Seek** locates the first record that satisfies the criteria.</span></span>

<span data-ttu-id="2f9d6-125">**Seek**メソッドは、指定されたキー フィールドを検索し、key1 と対照的に指定した抽出条件を満たす最初のレコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-125">The **Seek** method searches through the specified key fields and locates the first record that satisfies the criteria specified by comparison and key1.</span></span> <span data-ttu-id="2f9d6-126">レコードを検出すると、そのレコードをカレント レコードにし、 **NoMatch** プロパティを **False** に設定します。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-126">Once found, it makes that record current and sets the **NoMatch** property to **False**.</span></span> <span data-ttu-id="2f9d6-127">**Seek** メソッドで一致するレコードが見つからなかった場合は、 **NoMatch** プロパティが **True** に設定され、カレント レコードは未定義となります。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-127">If the **Seek** method fails to locate a match, the **NoMatch** property is set to **True**, and the current record is undefined.</span></span>

<span data-ttu-id="2f9d6-128">比較では場合、等号 (=) より大きいか等しい (\>=)、またはより大きい (\>)、 **Seek**はインデックスの先頭から開始し、正方向に検索します。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-128">If comparison is equal (=), greater than or equal (\>=), or greater than (\>), **Seek** starts at the beginning of the index and searches forward.</span></span>

<span data-ttu-id="2f9d6-129">比較の場合よりも小さい (\<) と同じかそれより小さい、または (\<=)、**シーク**はインデックスの末尾から開始し、逆方向検索します。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-129">If comparison is less than (\<) or less than or equal (\<=), **Seek** starts at the end of the index and searches backward.</span></span> <span data-ttu-id="2f9d6-130">しかし、インデックスの末尾に重複するインデックスのエントリがある場合、 **Seek** は重複するエントリのうち任意のエントリから始まり、先頭に向かって検索を進めます。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-130">However, if there are duplicate index entries at the end of the index, **Seek** starts at an arbitrary entry among the duplicates and then searches backward.</span></span>

<span data-ttu-id="2f9d6-131">インデックスで定義されているすべてのフィールドには、値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-131">You must specify values for all fields defined in the index.</span></span> <span data-ttu-id="2f9d6-132">複数列のインデックスを指定して **Seek** を使用するときに、インデックスのすべてのフィールドに comparison の値を指定しない場合は、comparison に等値演算子 (=) を使用できません。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-132">If you use **Seek** with a multiple-column index, and you don't specify a comparison value for every field in the index, then you cannot use the equal (=) operator in the comparison.</span></span> <span data-ttu-id="2f9d6-133">一部 (key2、key3 以降) に、抽出条件フィールドのデフォルトと一致していない可能性がありますが、Null にするためです。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-133">That's because some of the criteria fields (key2, key3, and so on) will default to Null, which will probably not match.</span></span> <span data-ttu-id="2f9d6-134">このため、等値演算子が正しく機能するのは、検索対象以外のすべてのキーが **null** であるレコードが存在する場合だけです。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-134">Therefore, the equal operator will work correctly only if you have a record which is all **null** except the key you're looking for.</span></span> <span data-ttu-id="2f9d6-135">大きいか等しいを使用することをお勧めしますが (\>=) 演算子代わりにします。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-135">It's recommended that you use the greater than or equal (\>=) operator instead.</span></span>

<span data-ttu-id="2f9d6-136">引数 key1 は、現在のインデックスに対応するフィールドと同じフィールドのデータ型でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-136">The key1 argument must be of the same field data type as the corresponding field in the current index.</span></span> <span data-ttu-id="2f9d6-137">たとえば、現在のインデックスを指す場合、数値フィールド (従業員 ID など)、key1 は数値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-137">For example, if the current index refers to a number field (such as Employee ID), key1 must be numeric.</span></span> <span data-ttu-id="2f9d6-138">同様に、現在のインデックスを指す場合、テキスト フィールド (姓など)、key1 は文字列である必要があります。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-138">Similarly, if the current index refers to a Text field (such as Last Name), key1 must be a string.</span></span>

<span data-ttu-id="2f9d6-139">**Seek** を使用するときは、カレント レコードが設定されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-139">There doesn't have to be a current record when you use **Seek**.</span></span>

<span data-ttu-id="2f9d6-140">**[Indexes](indexes-collection-dao.md)** コレクションを使用すると、既存のインデックスを列挙できます。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-140">You can use the **[Indexes](indexes-collection-dao.md)** collection to enumerate the existing indexes.</span></span>

<span data-ttu-id="2f9d6-p107">ダイナセット タイプまたはスナップショット タイプの **Recordset** で、既存のインデックスでは対応できない特定の条件を満たすレコードを検索するには、 **[Find](recordset2-findfirst-method-dao.md)** メソッドを使用します。特定の条件を満たすレコードだけでなく、すべてのレコードを対象にするには、 **[Move](recordset-movefirst-method-dao.md)** メソッドを使用してレコード間を移動します。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-p107">To locate a record in a dynaset- or snapshot-type **Recordset** that satisfies a specific condition that is not covered by existing indexes, use the **[Find](recordset2-findfirst-method-dao.md)** methods. To include all records, not just those that satisfy a specific condition, use the **[Move](recordset-movefirst-method-dao.md)** methods to move from record to record.</span></span>

<span data-ttu-id="2f9d6-p108">リンク テーブルはテーブル タイプの **Recordset** オブジェクトとして開くことができないため、 **Seek** メソッドはリンク テーブルに対して使用できません。しかし、 **[OpenDatabase](dbengine-opendatabase-method-dao.md)** メソッドを使用してインストール可能な ISAM (ODBC でない) データベースを直接開いた場合は、そのデータベース内のテーブルに対して **Seek** を使用できます。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-p108">You can't use the **Seek** method on a linked table because you can't open linked tables as table-type **Recordset** objects. However, if you use the **[OpenDatabase](dbengine-opendatabase-method-dao.md)** method to directly open an installable ISAM (non-ODBC) database, you can use **Seek** on tables in that database.</span></span>

## <a name="example"></a><span data-ttu-id="2f9d6-145">例</span><span class="sxs-lookup"><span data-stu-id="2f9d6-145">Example</span></span>

<span data-ttu-id="2f9d6-146">この例では、 **Seek** メソッドを使用して、ユーザーが ID 番号に基づき製品を検索できるようにする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-146">This example demonstrates the **Seek** method by allowing the user to search for a product based on an ID number.</span></span>

```vb
    Sub SeekX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim intFirst As Integer 
     Dim intLast As Integer 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' You must open a table-type Recordset to use an index, 
     ' and hence the Seek method. 
     Set rstProducts = _ 
     dbsNorthwind.OpenRecordset("Products", dbOpenTable) 
     
     With rstProducts 
     ' Set the index. 
     .Index = "PrimaryKey" 
     
     ' Get the lowest and highest product IDs. 
     .MoveLast 
     intLast = !ProductID 
     .MoveFirst 
     intFirst = !ProductID 
     
     Do While True 
     ' Display current record information and ask user 
     ' for ID number. 
     strMessage = "Product ID: " & !ProductID & vbCr & _ 
     "Name: " & !ProductName & vbCr & vbCr & _ 
     "Enter a product ID between " & intFirst & _ 
     " and " & intLast & "." 
     strSeek = InputBox(strMessage) 
     
     If strSeek = "" Then Exit Do 
     
     ' Store current bookmark in case the Seek fails. 
     varBookmark = .Bookmark 
     
     .Seek "=", Val(strSeek) 
     
     ' Return to the current record if the Seek fails. 
     If .NoMatch Then 
     MsgBox "ID not found!" 
     .Bookmark = varBookmark 
     End If 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
```

<br/>

<span data-ttu-id="2f9d6-p109">次の例では、 **NoMatch** プロパティを使用して **Seek** および **FindFirst** が成功したかどうか確認し、成功しなかった場合は適切なフィードバックを表示します。このプロシージャを実行するには、SeekMatch プロシージャと FindMatch プロシージャが必要です。</span><span class="sxs-lookup"><span data-stu-id="2f9d6-p109">This example uses the **NoMatch** property to determine whether a **Seek** and a **FindFirst** were successful, and if not, to give appropriate feedback. The SeekMatch and FindMatch procedures are required for this procedure to run.</span></span>

```vb
    Sub NoMatchX() 
     
     Dim dbsNorthwind As Database 
     Dim rstProducts As Recordset2 
     Dim rstCustomers As Recordset2 
     Dim strMessage As String 
     Dim strSeek As String 
     Dim strCountry As String 
     Dim varBookmark As Variant 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Default is dbOpenTable; required if Index property will 
     ' be used. 
     Set rstProducts = dbsNorthwind.OpenRecordset("Products") 
     
     With rstProducts 
     .Index = "PrimaryKey" 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with Seek method" & vbCr & _ 
     "Product ID: " & !ProductID & vbCr & _ 
     "Product Name: " & !ProductName & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter a product ID." 
     strSeek = InputBox(strMessage) 
     If strSeek = "" Then Exit Do 
     
     ' Call procedure that seeks for a record based on 
     ' the ID number supplied by the user. 
     SeekMatch rstProducts, Val(strSeek) 
     Loop 
     
     .Close 
     End With 
     
     Set rstCustomers = dbsNorthwind.OpenRecordset( _ 
     "SELECT CompanyName, Country FROM Customers " & _ 
     "ORDER BY CompanyName", dbOpenSnapshot) 
     
     With rstCustomers 
     
     Do While True 
     ' Show current record information; ask user for 
     ' input. 
     strMessage = "NoMatch with FindFirst method" & _ 
     vbCr & "Customer Name: " & !CompanyName & _ 
     vbCr & "Country: " & !Country & vbCr & _ 
     "NoMatch = " & .NoMatch & vbCr & vbCr & _ 
     "Enter country on which to search." 
     strCountry = Trim(InputBox(strMessage)) 
     If strCountry = "" Then Exit Do 
     
     ' Call procedure that finds a record based on 
     ' the country name supplied by the user. 
     FindMatch rstCustomers, _ 
     "Country = '" & strCountry & "'" 
     Loop 
     
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub SeekMatch(rstTemp As Recordset, _ 
     intSeek As Integer) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .Seek "=", intSeek 
     
     ' If Seek method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub 
     
    Sub FindMatch(rstTemp As Recordset, _ 
     strFind As String) 
     
     Dim varBookmark As Variant 
     Dim strMessage As String 
     
     With rstTemp 
     ' Store current record location. 
     varBookmark = .Bookmark 
     .FindFirst strFind 
     
     ' If Find method fails, notify user and return to the 
     ' last current record. 
     If .NoMatch Then 
     strMessage = _ 
     "Not found! Returning to current record." & _ 
     vbCr & vbCr & "NoMatch = " & .NoMatch 
     MsgBox strMessage 
     .Bookmark = varBookmark 
     End If 
     
     End With 
     
    End Sub
```