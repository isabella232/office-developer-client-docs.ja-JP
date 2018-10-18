---
title: TableDef.CreateIndex メソッド (DAO)
TOCTitle: CreateIndex Method
ms:assetid: 857b25c1-01fa-b926-0c74-7105e71b7505
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196791(v=office.15)
ms:contentKeyID: 48546062
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052970
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1c0dd3a48274c7a0affae9caa87ec762bea498ff
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606375"
---
# <a name="tabledefcreateindex-method-dao"></a><span data-ttu-id="cd78d-102">TableDef.CreateIndex メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="cd78d-102">TableDef.CreateIndex Method (DAO)</span></span>


<span data-ttu-id="cd78d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="cd78d-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="cd78d-p101">新しい **[Index](index-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="cd78d-p101">Creates a new **[Index](index-object-dao.md)** object (Microsoft Access workspaces only). .</span></span>

## <a name="syntax"></a><span data-ttu-id="cd78d-106">構文</span><span class="sxs-lookup"><span data-stu-id="cd78d-106">Syntax</span></span>

<span data-ttu-id="cd78d-107">*式*です。CreateIndex (***名***)</span><span class="sxs-lookup"><span data-stu-id="cd78d-107">*expression* .CreateIndex(***Name***)</span></span>

<span data-ttu-id="cd78d-108">\*式\***テーブル定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="cd78d-108">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="cd78d-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="cd78d-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cd78d-110">名前</span><span class="sxs-lookup"><span data-stu-id="cd78d-110">Name</span></span></p></th>
<th><p><span data-ttu-id="cd78d-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="cd78d-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="cd78d-112">データ型</span><span class="sxs-lookup"><span data-stu-id="cd78d-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="cd78d-113">説明</span><span class="sxs-lookup"><span data-stu-id="cd78d-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd78d-114">名前</span><span class="sxs-lookup"><span data-stu-id="cd78d-114">Name</span></span></p></td>
<td><p><span data-ttu-id="cd78d-115">省略可能</span><span class="sxs-lookup"><span data-stu-id="cd78d-115">Optional</span></span></p></td>
<td><p><span data-ttu-id="cd78d-116"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="cd78d-116"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="cd78d-p102">新しい <strong>Index</strong> オブジェクトの一意の名前を表す文字列型 (<strong>String</strong>) の値。有効な <strong>Index</strong> 名の詳細については、<strong>Name</strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd78d-p102">A <strong>String</strong> that uniquely names the new <strong>Index</strong> object. See the <strong>Name</strong> property for details on valid <strong>Index</strong> names.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cd78d-119"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="cd78d-119"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="cd78d-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="cd78d-120">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="cd78d-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="cd78d-121">Return value</span></span>
>>>>>>> <span data-ttu-id="cd78d-122">master</span><span class="sxs-lookup"><span data-stu-id="cd78d-122">master</span></span>

<span data-ttu-id="cd78d-123">Index</span><span class="sxs-lookup"><span data-stu-id="cd78d-123">Index</span></span>

## <a name="remarks"></a><span data-ttu-id="cd78d-124">注釈</span><span class="sxs-lookup"><span data-stu-id="cd78d-124">Remarks</span></span>

<span data-ttu-id="cd78d-125">**CreateIndex** メソッドを使用して、 **TableDef** オブジェクトの新しい **Index** オブジェクトを作成できます。</span><span class="sxs-lookup"><span data-stu-id="cd78d-125">You can use the **CreateIndex** method to create a new **Index** object for a **TableDef** object.</span></span> <span data-ttu-id="cd78d-126">**CreateIndex**の使用時に省略可能な名前の一部を省略した場合は、設定または新しいオブジェクトをコレクションに追加する前に、 **Name**プロパティをリセットするに適切な代入ステートメントを使用できます。</span><span class="sxs-lookup"><span data-stu-id="cd78d-126">If you omit the optional name part when you use **CreateIndex**, you can use an appropriate assignment statement to set or reset the **Name** property before you append the new object to a collection.</span></span> <span data-ttu-id="cd78d-127">オブジェクトの追加後に **Name** プロパティを設定できるかどうかは、 **Indexes** コレクションを格納しているオブジェクトの種類によって決まります。</span><span class="sxs-lookup"><span data-stu-id="cd78d-127">After you append the object, you may or may not be able to set its **Name** property, depending on the type of object that contains the **Indexes** collection.</span></span> <span data-ttu-id="cd78d-128">詳細については、 **Name** プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="cd78d-128">See the **Name** property topic for more details.</span></span>

<span data-ttu-id="cd78d-129">名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="cd78d-129">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="cd78d-130">コレクションから **Index** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cd78d-130">To remove an **Index** object from a collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span>

## <a name="example"></a><span data-ttu-id="cd78d-131">例</span><span class="sxs-lookup"><span data-stu-id="cd78d-131">Example</span></span>

<span data-ttu-id="cd78d-p104">次の使用例では、 **CreateIndex** メソッドを使用して 2 つの新しい **Index** オブジェクトを作成し、これを Employees という名前の **TableDef** オブジェクトの **Indexes** コレクションに追加します。次に、 **TableDef** オブジェクトの Indexes コレクション、新しい **Index** オブジェクトの **Fields** コレクション、および新しい **Index** オブジェクトの Properties コレクションを列挙します。このプロシージャを実行するには、CreateIndexOutput 関数が必要です。</span><span class="sxs-lookup"><span data-stu-id="cd78d-p104">This example uses the **CreateIndex** method to create two new **Index** objects and then appends them to the **Indexes** collection of the Employees **TableDef** object. It then enumerates the Indexes collection of the **TableDef** object, the **Fields** collection of the new **Index** objects, and the Properties collection of the new **Index** objects. The CreateIndexOutput function is required for this procedure to run.</span></span>

```vb
    Sub CreateIndexX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxCountry As Index 
     Dim idxFirstName As Index 
     Dim idxLoop As Index 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create first Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxCountry = .CreateIndex("CountryIndex") 
     With idxCountry 
     .Fields.Append .CreateField("Country") 
     .Fields.Append .CreateField("LastName") 
     .Fields.Append .CreateField("FirstName") 
     End With 
     .Indexes.Append idxCountry 
     
     ' Create second Index object, create and append Field 
     ' objects to the Index object, and then append the 
     ' Index object to the Indexes collection of the 
     ' TableDef. 
     Set idxFirstName = .CreateIndex 
     With idxFirstName 
     .Name = "FirstNameIndex" 
     .Fields.Append .CreateField("FirstName") 
     .Fields.Append .CreateField("LastName") 
     End With 
     .Indexes.Append idxFirstName 
     
     ' Refresh collection so that you can access new Index 
     ' objects. 
     .Indexes.Refresh 
     
     Debug.Print .Indexes.Count & " Indexes in " & _ 
     .Name & " TableDef" 
     
     ' Enumerate Indexes collection. 
     For Each idxLoop In .Indexes 
     Debug.Print " " & idxLoop.Name 
     Next idxLoop 
     
     ' Print report. 
     CreateIndexOutput idxCountry 
     CreateIndexOutput idxFirstName 
     
     ' Delete new Index objects because this is a 
     ' demonstration. 
     .Indexes.Delete idxCountry.Name 
     .Indexes.Delete idxFirstName.Name 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CreateIndexOutput(idxTemp As Index) 
     
     Dim fldLoop As Field 
     Dim prpLoop As Property 
     
     With idxTemp 
     ' Enumerate Fields collection of Index object. 
     Debug.Print "Fields in " & .Name 
     For Each fldLoop In .Fields 
     Debug.Print " " & fldLoop.Name 
     Next fldLoop 
     
     ' Enumerate Properties collection of Index object. 
     Debug.Print "Properties of " & .Name 
     For Each prpLoop In .Properties 
     Debug.Print " " & prpLoop.Name & " - " & _ 
     IIf(prpLoop = "", "[empty]", prpLoop) 
     Next prpLoop 
     End With 
     
    End Function
```
