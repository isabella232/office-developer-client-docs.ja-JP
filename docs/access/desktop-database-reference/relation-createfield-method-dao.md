---
title: Relation.CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8de2072e96ec00cab96dac19bd1af5889acd883a
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999037"
---
# <a name="relationcreatefield-method-dao"></a><span data-ttu-id="d1674-102">Relation.CreateField メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="d1674-102">Relation.CreateField method (DAO)</span></span>

<span data-ttu-id="d1674-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d1674-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d1674-104">新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="d1674-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1674-105">構文</span><span class="sxs-lookup"><span data-stu-id="d1674-105">Syntax</span></span>

<span data-ttu-id="d1674-106">*式*です。CreateField (***名前***、***種類***、***サイズ***)</span><span class="sxs-lookup"><span data-stu-id="d1674-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="d1674-107">\*式\***Relation**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d1674-107">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d1674-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d1674-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d1674-109">名前</span><span class="sxs-lookup"><span data-stu-id="d1674-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d1674-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="d1674-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d1674-111">データ型</span><span class="sxs-lookup"><span data-stu-id="d1674-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d1674-112">説明</span><span class="sxs-lookup"><span data-stu-id="d1674-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1674-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="d1674-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d1674-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="d1674-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d1674-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="d1674-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d1674-p101">新しい <strong>Field</strong> オブジェクトの一意の名前を表す文字列型 (String) の値。有効な <strong>Field</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1674-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1674-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="d1674-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="d1674-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="d1674-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="d1674-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="d1674-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d1674-121">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d1674-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1674-122"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="d1674-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="d1674-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="d1674-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="d1674-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="d1674-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d1674-125">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="d1674-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="d1674-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="d1674-126">Return value</span></span>

<span data-ttu-id="d1674-127">Field</span><span class="sxs-lookup"><span data-stu-id="d1674-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="d1674-128">注釈</span><span class="sxs-lookup"><span data-stu-id="d1674-128">Remarks</span></span>

<span data-ttu-id="d1674-p102">**CreateField** メソッドを使用すると、新しいフィールドを作成して、そのフィールドの名前、データ型、およびサイズを指定できます。 **CreateField** を使用するときに 1 つ以上のオプションの引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトをコレクションに追加した後は、一部のプロパティ設定を変更できなくなります。詳細については、各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d1674-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="d1674-133">タイプとサイズの引数は、**テーブル定義**オブジェクト内の**Field**オブジェクトのみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="d1674-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="d1674-134">これらの引数は、 **Field** オブジェクトが **Index** オブジェクトまたは **Relation** オブジェクトに関連付けられている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="d1674-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="d1674-135">名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d1674-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="d1674-p104">**Field** オブジェクトを **Fields** コレクションから削除するには、そのコレクションで **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスの作成後は、その **Field** オブジェクトを **TableDef** オブジェクトの **Fields** コレクションから削除できません。</span><span class="sxs-lookup"><span data-stu-id="d1674-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

