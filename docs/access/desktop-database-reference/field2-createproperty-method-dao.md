---
title: Field2.CreateProperty メソッド (DAO)
TOCTitle: CreateProperty Method
ms:assetid: bdbd6bec-216f-138e-78df-9c3221692aa4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822737(v=office.15)
ms:contentKeyID: 48547446
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cf35138a4782e1f16d230ba120bf5482a9a8ce40
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722705"
---
# <a name="field2createproperty-method-dao"></a><span data-ttu-id="039c7-102">Field2.CreateProperty メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="039c7-102">Field2.CreateProperty method (DAO)</span></span>

<span data-ttu-id="039c7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="039c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="039c7-104">新しいユーザー定義の **[Property](property-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="039c7-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="039c7-105">構文</span><span class="sxs-lookup"><span data-stu-id="039c7-105">Syntax</span></span>

<span data-ttu-id="039c7-106">*式*です。CreateProperty (***名前***、***型***、***値***、 ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="039c7-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="039c7-107">\*式\***Field2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="039c7-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="039c7-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="039c7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="039c7-109">名前</span><span class="sxs-lookup"><span data-stu-id="039c7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="039c7-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="039c7-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="039c7-111">データ型</span><span class="sxs-lookup"><span data-stu-id="039c7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="039c7-112">説明</span><span class="sxs-lookup"><span data-stu-id="039c7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="039c7-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="039c7-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="039c7-114">省略可能</span><span class="sxs-lookup"><span data-stu-id="039c7-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="039c7-115"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="039c7-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="039c7-p101">新しい <strong>Property</strong> オブジェクトの一意の名前を表す文字列型 ( <strong>String</strong> ) の値。有効な <strong>Property</strong> 名の詳細については、 <strong>Name</strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="039c7-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="039c7-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="039c7-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="039c7-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="039c7-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="039c7-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="039c7-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="039c7-p102">新しい <strong>Property</strong> オブジェクトのデータ型を定義する定数。有効なデータ型については、 <strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="039c7-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="039c7-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="039c7-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="039c7-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="039c7-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="039c7-125"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="039c7-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="039c7-p103">初期プロパティ値を格納しているバリアント型 ( <strong>Variant</strong> ) の値。詳細については、 <strong><a href="field-value-property-dao.md">Value</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="039c7-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="039c7-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="039c7-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="039c7-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="039c7-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="039c7-130"><strong>Variant (バリアント型)</strong></span><span class="sxs-lookup"><span data-stu-id="039c7-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="039c7-131"><strong>バリアント型</strong>(<strong>ブール型</strong>のサブタイプ)<strong>プロパティ</strong>は、DDL オブジェクトであるかどうかを示す。</span><span class="sxs-lookup"><span data-stu-id="039c7-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="039c7-132">既定値は <strong>False</strong> です。</span><span class="sxs-lookup"><span data-stu-id="039c7-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="039c7-133">DDL が<strong>True</strong>の場合は、ユーザーが変更または<strong>dbSecWriteDef</strong>権限を持たない<strong>プロパティ</strong>オブジェクトを削除できません。</span><span class="sxs-lookup"><span data-stu-id="039c7-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="039c7-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="039c7-134">Return value</span></span>

<span data-ttu-id="039c7-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="039c7-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="039c7-136">注釈</span><span class="sxs-lookup"><span data-stu-id="039c7-136">Remarks</span></span>

<span data-ttu-id="039c7-137">ユーザー定義の **Property** オブジェクトを作成できるのは、持続的なオブジェクトの **[Properties](properties-collection-dao.md)** コレクション内だけです。</span><span class="sxs-lookup"><span data-stu-id="039c7-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="039c7-p105">**CreateProperty** の使用時に省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトの追加後は、一部のプロパティの設定は変更できません。詳細については、 **Name**、 **Type**、および **Value** の各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="039c7-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="039c7-141">名は、既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="039c7-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="039c7-p106">ユーザー定義の **Property** オブジェクトをコレクションから削除するには、 **[Properties](fields-delete-method-dao.md)** コレクションの **[Delete](properties-collection-dao.md)** メソッドを使用します。組み込みのプロパティは削除できません。</span><span class="sxs-lookup"><span data-stu-id="039c7-p106">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection. You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="039c7-144">DDL 引数を省略した場合のデフォルト値は False (DDL 以外)。</span><span class="sxs-lookup"><span data-stu-id="039c7-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="039c7-145">対応する DDL プロパティは公開されていないので、DDL から DDL 以外に変更する **Property** オブジェクトを削除し、再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="039c7-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


