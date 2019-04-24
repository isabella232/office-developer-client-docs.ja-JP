---
title: CreateField メソッド (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae322277dd1d357aceb3f9129110dded705f9eca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307064"
---
# <a name="relationcreatefield-method-dao"></a><span data-ttu-id="ccfac-102">CreateField メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="ccfac-102">Relation.CreateField method (DAO)</span></span>

<span data-ttu-id="ccfac-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccfac-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ccfac-104">新しい **[Field](field-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="ccfac-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfac-105">構文</span><span class="sxs-lookup"><span data-stu-id="ccfac-105">Syntax</span></span>

<span data-ttu-id="ccfac-106">*式*。CreateField (***名前***、***種類***、***サイズ***)</span><span class="sxs-lookup"><span data-stu-id="ccfac-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="ccfac-107">\*式\***Relation**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="ccfac-107">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="ccfac-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ccfac-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ccfac-109">名前</span><span class="sxs-lookup"><span data-stu-id="ccfac-109">Name</span></span></p></th>
<th><p><span data-ttu-id="ccfac-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="ccfac-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="ccfac-111">データ型</span><span class="sxs-lookup"><span data-stu-id="ccfac-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="ccfac-112">説明</span><span class="sxs-lookup"><span data-stu-id="ccfac-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccfac-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="ccfac-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="ccfac-114">Optional</span><span class="sxs-lookup"><span data-stu-id="ccfac-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="ccfac-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ccfac-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ccfac-116">新しい <strong>Field</strong> オブジェクトの一意の名前を表す文字列型 (String) の値。</span><span class="sxs-lookup"><span data-stu-id="ccfac-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="ccfac-117">有効な<strong>フィールド</strong>名の詳細については、 <strong><a href="connection-name-property-dao.md">Name</a></strong>プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccfac-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ccfac-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="ccfac-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="ccfac-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="ccfac-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="ccfac-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ccfac-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ccfac-121">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ccfac-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ccfac-122"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="ccfac-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="ccfac-123">Optional</span><span class="sxs-lookup"><span data-stu-id="ccfac-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="ccfac-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="ccfac-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="ccfac-125">このオブジェクトではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ccfac-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="ccfac-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="ccfac-126">Return value</span></span>

<span data-ttu-id="ccfac-127">Field</span><span class="sxs-lookup"><span data-stu-id="ccfac-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="ccfac-128">注釈</span><span class="sxs-lookup"><span data-stu-id="ccfac-128">Remarks</span></span>

<span data-ttu-id="ccfac-p102">**CreateField** メソッドを使用して、新しいフィールドを作成し、そのフィールドの名前、データ型、およびサイズを指定できます。**CreateField** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。新しいオブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ccfac-p102">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field. If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the new object, you can alter some but not all of its property settings. See the individual property topics for more details.</span></span>

<span data-ttu-id="ccfac-133">引数 type および引数 size は、 **TableDef**オブジェクトの**Field**オブジェクトにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="ccfac-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="ccfac-134">これらの引数は、 **Field** オブジェクトが **Index** オブジェクトまたは **Relation** オブジェクトに関連付けられている場合は無視されます。</span><span class="sxs-lookup"><span data-stu-id="ccfac-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="ccfac-135">name が既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ccfac-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="ccfac-p104">**Fields** コレクションから **Field** オブジェクトを削除するには、コレクションの **[Delete](fields-delete-method-dao.md)** メソッドを使用します。フィールドを参照するインデックスを作成した後は、 **TableDef** オブジェクトの **Fields** コレクションから **Field** オブジェクトを削除できません。</span><span class="sxs-lookup"><span data-stu-id="ccfac-p104">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection. You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

