---
title: TableDef.CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 713f2530369a824a6d7204655ded4333f7fe2765
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308443"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="e2dd1-102">TableDef.CreateField メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="e2dd1-102">TableDef.CreateField Method (DAO)</span></span>

<span data-ttu-id="e2dd1-103">**適用先**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2dd1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2dd1-104">新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e2dd1-105">構文</span><span class="sxs-lookup"><span data-stu-id="e2dd1-105">Syntax</span></span>

<span data-ttu-id="e2dd1-106">*式* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span><span class="sxs-lookup"><span data-stu-id="e2dd1-106">CreateField( Name ,  Type ,  Size )</span></span>

<span data-ttu-id="e2dd1-107">*式* **TableDef** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-107">*expression*  A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e2dd1-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e2dd1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e2dd1-109">名前</span><span class="sxs-lookup"><span data-stu-id="e2dd1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e2dd1-110">必須/省略可能</span><span class="sxs-lookup"><span data-stu-id="e2dd1-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="e2dd1-111">データ型</span><span class="sxs-lookup"><span data-stu-id="e2dd1-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="e2dd1-112">説明</span><span class="sxs-lookup"><span data-stu-id="e2dd1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e2dd1-113"><em>名前</em></span><span class="sxs-lookup"><span data-stu-id="e2dd1-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="e2dd1-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="e2dd1-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="e2dd1-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e2dd1-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e2dd1-116">新しい <strong>Field</strong> オブジェクトの名前を一意に指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="e2dd1-117">有効な <strong>Field</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-117">See the <a href="connection-name-property-dao.md"><strong>Name</strong></a> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e2dd1-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="e2dd1-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="e2dd1-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="e2dd1-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="e2dd1-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e2dd1-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e2dd1-121">新しい <strong>Field</strong> オブジェクトのデータ型を決定する定数。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-121">A constant that determines the data type of the new <strong>Field</strong> object.</span></span> <span data-ttu-id="e2dd1-122">有効なデータ型については、<strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e2dd1-123"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="e2dd1-123"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="e2dd1-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="e2dd1-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="e2dd1-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e2dd1-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e2dd1-126">テキストを含む <strong>Field</strong> オブジェクトの最大サイズをバイト単位で示す整数。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="e2dd1-127">サイズの有効な値については、<strong><a href="field-size-property-dao.md">Size</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-127">See the <a href="field-size-property-dao.md"><strong>Size</strong></a> property for valid size values.</span></span> <span data-ttu-id="e2dd1-128">この引数は数値フィールドおよび固定幅フィールドでは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="e2dd1-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="e2dd1-129">Return value</span></span>

<span data-ttu-id="e2dd1-130">Field</span><span class="sxs-lookup"><span data-stu-id="e2dd1-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="e2dd1-131">注釈</span><span class="sxs-lookup"><span data-stu-id="e2dd1-131">Remarks</span></span>

<span data-ttu-id="e2dd1-p104">**CreateField** メソッドを使用して、新しいフィールドを作成し、そのフィールドの名前、データ型、およびサイズを指定できます。**CreateField** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-p104">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="e2dd1-136">引数 type および引数 Size は、**TableDef** オブジェクトの **Field** オブジェクトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-136">The  type and  Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="e2dd1-137">**Field** オブジェクトが **Index** または **Relation** オブジェクトに関連付けられている場合、これらの引数は無視されます。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="e2dd1-138">Name が示すオブジェクトが既にコレクションのメンバーである場合に **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-138">If  name refers to an object that is already a member of the collection, a run-time error occurs when you use the  Append  method.</span></span>

<span data-ttu-id="e2dd1-p106">**Fields** コレクションから **Field** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスを作成した後は、 **TableDef** オブジェクトの **Fields** コレクションから **Field** オブジェクトを削除できません。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-p106">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="e2dd1-141">\*\*リンクの提供元: \*\*[UtterAccess](https://www.utteraccess.com) コミュニティ。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-141">**Link provided by:** Community Member Icon The [UtterAccess](https://www.utteraccess.com) community</span></span> <span data-ttu-id="e2dd1-142">UtterAccess は非常に優れた Microsoft Access wiki およびヘルプ フォーラムです。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-142">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="e2dd1-143">DAO を使用して既存のテーブルにハイパーリンク フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="e2dd1-143">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="e2dd1-144">例</span><span class="sxs-lookup"><span data-stu-id="e2dd1-144">Example</span></span>

<span data-ttu-id="e2dd1-p108">次の例は、集計フィールドを作成する方法を示します。 CreateField メソッドで、" **FullName**" という名前のフィールドを作成します。次に、 Expression プロパティを、フィールドの値を計算する式に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-p108">The following example shows how to create a calculated field. The CreateField method creates a field named **FullName**. The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="e2dd1-148">**サンプル コードの提供元:** [Microsoft Access 2010 Programmer's Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)。</span><span class="sxs-lookup"><span data-stu-id="e2dd1-148">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

