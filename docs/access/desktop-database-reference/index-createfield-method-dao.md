---
title: Index.CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a3723beee3907cc209951c3494a2bde2a4c17bfa
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477282"
---
# <a name="indexcreatefield-method-dao"></a><span data-ttu-id="0901b-102">Index.CreateField メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="0901b-102">Index.CreateField Method (DAO)</span></span>


<span data-ttu-id="0901b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="0901b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0901b-104">新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="0901b-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="0901b-105">構文</span><span class="sxs-lookup"><span data-stu-id="0901b-105">Syntax</span></span>

<span data-ttu-id="0901b-106">*式*です。CreateField (***名前***、***種類***、***サイズ***)</span><span class="sxs-lookup"><span data-stu-id="0901b-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="0901b-107">\*式\***Index**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0901b-107">*expression* A variable that represents an **Index** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="0901b-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="0901b-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0901b-109">名前</span><span class="sxs-lookup"><span data-stu-id="0901b-109">Name</span></span></p></th>
<th><p><span data-ttu-id="0901b-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="0901b-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="0901b-111">データ型</span><span class="sxs-lookup"><span data-stu-id="0901b-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="0901b-112">説明</span><span class="sxs-lookup"><span data-stu-id="0901b-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0901b-113">名前</span><span class="sxs-lookup"><span data-stu-id="0901b-113">Name</span></span></p></td>
<td><p><span data-ttu-id="0901b-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="0901b-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="0901b-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="0901b-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0901b-p101">新しい <strong>Field</strong> オブジェクトの一意の名前を表す文字列型 (String) の値。有効な <strong>Field</strong> 名の詳細については、<strong><a href="connection-name-property-dao.md">Name</a></strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0901b-p101">A String that uniquely names the new <strong>Field</strong> object. See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0901b-118">種類</span><span class="sxs-lookup"><span data-stu-id="0901b-118">Type</span></span></p></td>
<td><p><span data-ttu-id="0901b-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="0901b-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="0901b-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="0901b-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0901b-121">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0901b-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0901b-122">サイズ</span><span class="sxs-lookup"><span data-stu-id="0901b-122">Size</span></span></p></td>
<td><p><span data-ttu-id="0901b-123">省略可能</span><span class="sxs-lookup"><span data-stu-id="0901b-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="0901b-124"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="0901b-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="0901b-125">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0901b-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="0901b-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="0901b-126">Return Value</span></span>

<span data-ttu-id="0901b-127">Field</span><span class="sxs-lookup"><span data-stu-id="0901b-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="0901b-128">注釈</span><span class="sxs-lookup"><span data-stu-id="0901b-128">Remarks</span></span>

<span data-ttu-id="0901b-p102">**CreateField** メソッドを使用すると、新しいフィールドを作成して、そのフィールドの名前、データ型、およびサイズを指定できます。 **CreateField** を使用するときに 1 つ以上のオプションの引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトをコレクションに追加した後は、一部のプロパティ設定を変更できなくなります。詳細については、各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="0901b-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="0901b-133">タイプとサイズの引数は、**テーブル定義**オブジェクト内の**Field**オブジェクトのみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="0901b-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="0901b-134">これらの引数は、 **Field** オブジェクトが **Index** オブジェクトまたは **Relation** オブジェクトに関連付けられている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="0901b-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="0901b-135">名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0901b-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="0901b-p104">**Field** オブジェクトを **Fields** コレクションから削除するには、そのコレクションで **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスの作成後は、その **Field** オブジェクトを **TableDef** オブジェクトの **Fields** コレクションから削除できません。</span><span class="sxs-lookup"><span data-stu-id="0901b-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

