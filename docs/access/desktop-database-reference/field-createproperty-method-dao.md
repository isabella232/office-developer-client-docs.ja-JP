---
title: CreateProperty メソッド (DAO)
TOCTitle: CreateProperty Method
ms:assetid: b3c1d303-7cab-89c3-8e90-f18a0445d304
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822050(v=office.15)
ms:contentKeyID: 48547202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9a88dce09798fa05aa602799f18a22e28d39c53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293141"
---
# <a name="fieldcreateproperty-method-dao"></a><span data-ttu-id="d16f4-102">CreateProperty メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="d16f4-102">Field.CreateProperty method (DAO)</span></span>


<span data-ttu-id="d16f4-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d16f4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d16f4-104">新しいユーザー定義の **[Property](property-object-dao.md)** オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="d16f4-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d16f4-105">構文</span><span class="sxs-lookup"><span data-stu-id="d16f4-105">Syntax</span></span>

<span data-ttu-id="d16f4-106">*式*。CreateProperty (***Name***、 ***Type***、 ***Value***、 ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="d16f4-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="d16f4-107">\*式\***Field**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d16f4-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d16f4-108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d16f4-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d16f4-109">名前</span><span class="sxs-lookup"><span data-stu-id="d16f4-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d16f4-110">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="d16f4-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d16f4-111">データ型</span><span class="sxs-lookup"><span data-stu-id="d16f4-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d16f4-112">説明</span><span class="sxs-lookup"><span data-stu-id="d16f4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d16f4-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="d16f4-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d16f4-114">Optional</span><span class="sxs-lookup"><span data-stu-id="d16f4-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d16f4-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d16f4-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d16f4-p101">新しい <strong>Property</strong> オブジェクトの一意の名前を表す文字列型 ( <strong>String</strong> ) の値。有効な <strong>Property</strong> 名の詳細については、 <strong>Name</strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="d16f4-p101">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object. See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d16f4-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="d16f4-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="d16f4-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="d16f4-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="d16f4-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d16f4-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d16f4-p102">新しい <strong>Property</strong> オブジェクトのデータ型を定義する定数。有効なデータ型については、 <strong><a href="field-type-property-dao.md">Type</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="d16f4-p102">A constant that defines the data type of the new <strong>Property</strong> object. See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d16f4-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="d16f4-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="d16f4-124">Optional</span><span class="sxs-lookup"><span data-stu-id="d16f4-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="d16f4-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d16f4-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d16f4-p103">初期プロパティ値を格納しているバリアント型 ( <strong>Variant</strong> ) の値。詳細については、 <strong><a href="field-value-property-dao.md">Value</a></strong> プロパティを参照してください。  </span><span class="sxs-lookup"><span data-stu-id="d16f4-p103">A <strong>Variant</strong> containing the initial property value. See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d16f4-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="d16f4-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="d16f4-129">Optional</span><span class="sxs-lookup"><span data-stu-id="d16f4-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="d16f4-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d16f4-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d16f4-131"><strong>Property</strong> が DDL オブジェクトであるかどうかを示す、サブタイプがブール型 (<strong>Boolean</strong>) であるバリアント型 (<strong>Variant</strong>) の値。</span><span class="sxs-lookup"><span data-stu-id="d16f4-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="d16f4-132">既定では <strong>False です</strong> 。</span><span class="sxs-lookup"><span data-stu-id="d16f4-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="d16f4-133">DDL が<strong>True</strong>の場合、ユーザーは、 <strong>dbsecwritedef</strong>権限を持っていない限り、この<strong>プロパティ</strong>オブジェクトを変更または削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="d16f4-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="d16f4-134">戻り値</span><span class="sxs-lookup"><span data-stu-id="d16f4-134">Return value</span></span>

<span data-ttu-id="d16f4-135">プロパティ</span><span class="sxs-lookup"><span data-stu-id="d16f4-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="d16f4-136">注釈</span><span class="sxs-lookup"><span data-stu-id="d16f4-136">Remarks</span></span>

<span data-ttu-id="d16f4-137">ユーザー定義の **Property** オブジェクトを作成できるのは、持続的なオブジェクトの **[Properties](properties-collection-dao.md)** コレクション内だけです。</span><span class="sxs-lookup"><span data-stu-id="d16f4-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="d16f4-p105">**CreateProperty** を使用するときに 1 つ以上の省略可能な引数を省略した場合は、新しいオブジェクトをコレクションに追加する前に、適切な代入ステートメントを使用して、対応するプロパティを設定またはリセットできます。オブジェクトをコレクションに追加した後は、一部のプロパティ設定を変更できなくなります。詳細については、 **Name**、 **Type**、および **Value** の各プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d16f4-p105">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection. After you append the object, you can alter some but not all of its property settings. See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="d16f4-141">name が既にコレクションのメンバーであるオブジェクトを参照している場合、 **[Append](fields-append-method-dao.md)** メソッドを使用すると、実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="d16f4-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="d16f4-142">ユーザー定義の **Property** オブジェクトをコレクションから削除するには、 **[Properties](fields-delete-method-dao.md)** コレクションの **Delete** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d16f4-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="d16f4-143">組み込みのプロパティは削除できません。</span><span class="sxs-lookup"><span data-stu-id="d16f4-143">You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="d16f4-144">ddl 引数を省略すると、既定では False (非 DDL) になります。</span><span class="sxs-lookup"><span data-stu-id="d16f4-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="d16f4-145">対応する DDL プロパティは公開されないため、 **Property** オブジェクトを DDL から非 DDL に変更する場合は、そのオブジェクトを削除して再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d16f4-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


