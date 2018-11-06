---
title: プロパティ オブジェクト (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 63df510830dee77ababc9ee1be53f0ae328ad8c3
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997120"
---
# <a name="property-object-dao"></a><span data-ttu-id="f8704-102">プロパティ オブジェクト (DAO)</span><span class="sxs-lookup"><span data-stu-id="f8704-102">Property object (DAO)</span></span>

<span data-ttu-id="f8704-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f8704-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f8704-104">**Property** オブジェクトは、DAO オブジェクトの組み込みまたはユーザー定義の特性を表します。</span><span class="sxs-lookup"><span data-stu-id="f8704-104">A **Property** object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8704-105">注釈</span><span class="sxs-lookup"><span data-stu-id="f8704-105">Remarks</span></span>

<span data-ttu-id="f8704-p101">**Connection** オブジェクトおよび **Error** オブジェクトを除くすべての DAO オブジェクトには、その DAO オブジェクトの組み込みプロパティに対応する **Property** オブジェクトを持つ **Properties** コレクションが含まれています。ユーザーは **Property** オブジェクトを定義して、DAO オブジェクトの **Properties** コレクションに追加することもできます。これらの **Property** オブジェクト (単にプロパティとも呼ばれる) により、オブジェクトのインスタンスに固有の属性が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f8704-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection which has **Property** objects corresponding to built-in properties of that DAO object. The user can also define **Property** objects and append them to the **Properties** collection of some DAO objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="f8704-109">次のオブジェクトに対し、ユーザー定義のプロパティを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="f8704-109">You can create user-defined properties for the following objects:</span></span>

- <span data-ttu-id="f8704-110">**Database**、 **Index**、 **QueryDef**、および **TableDef** の各オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f8704-110">**Database**, **Index**, **QueryDef**, and **TableDef** objects</span></span>

- <span data-ttu-id="f8704-111">**QueryDef** オブジェクトおよび **TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f8704-111">**Field** objects in **Fields** collections of **QueryDef** and **TableDef** objects</span></span>

<span data-ttu-id="f8704-112">ユーザー定義のプロパティを追加するには、一意の**名前**プロパティの設定値を持つ**プロパティ**オブジェクトを作成するのには、 **CreateProperty**メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f8704-112">To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting.</span></span> <span data-ttu-id="f8704-113">**プロパティ**新しいオブジェクトの**型**と**値**のプロパティを設定し、適切なオブジェクトの**Properties**コレクションに追加します。</span><span class="sxs-lookup"><span data-stu-id="f8704-113">Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object.</span></span> <span data-ttu-id="f8704-114">ユーザー定義のプロパティを追加するオブジェクトは、コレクションに既に追加されて必要があります。</span><span class="sxs-lookup"><span data-stu-id="f8704-114">The object to which you are adding the user-defined property must already be appended to a collection.</span></span> <span data-ttu-id="f8704-115">**Properties** コレクションに追加されていないユーザー定義の **Property** オブジェクトを参照したり、ユーザー定義の **Property** オブジェクトが含まれる **Properties** コレクションに、そのオブジェクトと同じ名前の **Property** オブジェクトを追加したりしようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8704-115">Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="f8704-116">**Properties** コレクションからユーザー定義のプロパティを削除することはできますが、組み込みプロパティは削除できません。</span><span class="sxs-lookup"><span data-stu-id="f8704-116">You can delete user-defined properties from the **Properties** collection, but you can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="f8704-p103">[!メモ] ユーザー定義の **Property** オブジェクトは、1 つのオブジェクトの特定のインスタンスにのみ関連付けられます。プロパティは、選択した種類のオブジェクトのすべてのインスタンスに定義されるわけではありません。</span><span class="sxs-lookup"><span data-stu-id="f8704-p103">A user-defined **Property** object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="f8704-p104">オブジェクトの **Properties** コレクションを使用して、オブジェクトの組み込みおよびユーザー定義のプロパティを列挙することができます。この操作を行うために、既存のプロパティの種類や属性 (**Name** プロパティや **Type** プロパティ) をあらかじめ知っている必要はありません。ただし、値の取得のみ可能なプロパティ (**Workspace** オブジェクトの **Password** プロパティなど) の読み取り、または不適切なコンテキストでのプロパティの読み取り/書き込み (**TableDef** オブジェクトの **Fields** コレクションの **Field** オブジェクトの **Value** プロパティの設定など) を実行しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f8704-p104">You can use the **Properties** collection of an object to enumerate the object's built-in and user-defined properties. You don't need to know beforehand exactly which properties exist or what their characteristics (**Name** and **Type** properties) are to manipulate them. However, if you try to read a write-only property, such as the **Password** property of a **Workspace** object, or try to read or write a property in an inappropriate context, such as the **Value** property setting of a **Field** object in the **Fields** collection of a **TableDef** object, an error occurs.</span></span>

<span data-ttu-id="f8704-122">**Property** オブジェクトには、次の 4 つの組み込みプロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="f8704-122">The **Property** object also has four built-in properties:</span></span>

- <span data-ttu-id="f8704-123">**Name** プロパティは、プロパティを一意に識別する文字列型 ( **String**) の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="f8704-123">The **Name** property, a **String** that uniquely identifies the property.</span></span>

- <span data-ttu-id="f8704-124">**Type** プロパティは、プロパティのデータ型を指定する整数型 ( **Integer**) の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="f8704-124">The **Type** property, an **Integer** that specifies the property data type.</span></span>

- <span data-ttu-id="f8704-125">**Value** プロパティは、プロパティの設定値を表すバリアント型 ( **Variant**) の値を格納します。</span><span class="sxs-lookup"><span data-stu-id="f8704-125">The **Value** property, a **Variant** that contains the property setting.</span></span>

- <span data-ttu-id="f8704-p105">**Inherited** プロパティは、そのプロパティが別のオブジェクトから継承されるかどうかを示すブール型 ( **Boolean**) の値を格納します。たとえば、 **Recordset** オブジェクトの **Fields** コレクションの **Field** オブジェクトは、基になる **TableDef** オブジェクトまたは **QueryDef** オブジェクトのプロパティを継承できます。</span><span class="sxs-lookup"><span data-stu-id="f8704-p105">The **Inherited** property, a **Boolean** that indicates whether the property is inherited from another object. For example, a **Field** object in a **Fields** collection of a **Recordset** object can inherit properties from the underlying **TableDef** or **QueryDef** object.</span></span>

<span data-ttu-id="f8704-128">コレクション内の組み込みの **Property** オブジェクトを、コレクションで付けられたインデックスまたは **Name** プロパティの設定値で参照するには、次のいずれかの構文を使います。</span><span class="sxs-lookup"><span data-stu-id="f8704-128">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="f8704-129">\* オブジェクト \***。プロパティ**(0)</span><span class="sxs-lookup"><span data-stu-id="f8704-129">\*object\***.Properties**(0)</span></span>

- <span data-ttu-id="f8704-130">\*オブジェクト \***。プロパティ**("\* 名 \*")</span><span class="sxs-lookup"><span data-stu-id="f8704-130">*object\***.Properties**("* name\*")</span></span>

- <span data-ttu-id="f8704-131">\*オブジェクト \***。プロパティ**\!\* 名 \*\]</span><span class="sxs-lookup"><span data-stu-id="f8704-131">*object\***.Properties**\!\[* name\*\]</span></span>

<span data-ttu-id="f8704-132">組み込みプロパティの場合、次の構文を使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f8704-132">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="f8704-133">*オブジェクト*です。*名*</span><span class="sxs-lookup"><span data-stu-id="f8704-133">*object*.*name*</span></span>

> [!NOTE]
> <span data-ttu-id="f8704-134">ユーザー定義のプロパティでは、使用してください、フル\*オブジェクト \***。プロパティ**("\* 名 \*") の構文です。</span><span class="sxs-lookup"><span data-stu-id="f8704-134">For a user-defined property, you must use the full *object\***.Properties**("* name\*") syntax.</span></span>

<span data-ttu-id="f8704-p106">同じ構文を使って、 **Property** オブジェクトの **Value** プロパティを参照することもできます。 **Property** オブジェクト自身と **Property** オブジェクトの **Value** プロパティのいずれを参照するかは、参照のコンテキストで決まります。</span><span class="sxs-lookup"><span data-stu-id="f8704-p106">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

