---
title: Members コレクション (ADO MD)
TOCTitle: Members collection (ADO MD)
ms:assetid: 1389c554-e4f1-107d-22c6-7fe851d53d23
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248910(v=office.15)
ms:contentKeyID: 48543371
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: adc8ed771bcba6a4b6532b33b27980f8aab695c5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721326"
---
# <a name="members-collection-ado-md"></a><span data-ttu-id="eb478-102">Members コレクション (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="eb478-102">Members collection (ADO MD)</span></span>


<span data-ttu-id="eb478-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="eb478-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eb478-104">レベル、または軸上の位置からの [Member](member-object-ado-md.md) オブジェクトを含みます。</span><span class="sxs-lookup"><span data-stu-id="eb478-104">Contains the [Member](member-object-ado-md.md) objects from a level or a position along an axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb478-105">解説</span><span class="sxs-lookup"><span data-stu-id="eb478-105">Remarks</span></span>

<span data-ttu-id="eb478-106">**Members** コレクションには、以下の種類のメンバーを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="eb478-106">A **Members** collection is used to contain the following types of members:</span></span>

  - <span data-ttu-id="eb478-p101">キューブのレベルを構成するメンバーで、**Level** オブジェクトの [Members](level-object-ado-md.md) コレクションに含まれます。たとえば、「 [多次元スキーマおよびデータの概要](overview-of-multidimensional-schemas-and-data.md)」のサンプルでは、Countries レベルの 4 つのメンバーは、Canada、USA、UK、および Germany です。</span><span class="sxs-lookup"><span data-stu-id="eb478-p101">The members that make up a level in a cube. These are contained in the **Members** collection of a [Level](level-object-ado-md.md) object. For example, using the sample from [Overview of Multidimensional Schemas and Data](overview-of-multidimensional-schemas-and-data.md), the four members of the Countries level are Canada, USA, UK, and Germany.</span></span>

  - <span data-ttu-id="eb478-p102">階層内の特定のメンバーの子であるメンバー。このメンバーは、親 の [Member](children-property-ado-md.md) オブジェクトの **Children** プロパティによって取得できます。たとえば、上記と同じサンプルでは、Canada メンバーの 2 つの子は Canada-East と Canada-West です。</span><span class="sxs-lookup"><span data-stu-id="eb478-p102">The members that are the children of a specific member within a hierarchy. These members are returned by the [Children](children-property-ado-md.md) property of the parent **Member** object. For example, again using the same sample, the two children of the Canada member are Canada-East and Canada-West.</span></span>

  - <span data-ttu-id="eb478-p103">[cellset](cellset-object-ado-md.md) の軸上の特定の位置を定義するメンバー。たとえば、「 [多次元データを処理する](working-with-multidimensional-data.md)」のセルセットでは、x 軸上の最初の位置の 2 つのメンバーは Valentine と Seattle です。この 2 つのメンバーは、**Position** オブジェクトの [Members](position-object-ado-md.md) コレクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="eb478-p103">The members that define a specific position along an axis of a [cellset](cellset-object-ado-md.md). Using the cellset from [Working with Multidimensional Data](working-with-multidimensional-data.md) as an example, the two members of the first position on the x-axis are Valentine and Seattle. These members are contained by the **Members** collection of a [Position](position-object-ado-md.md) object.</span></span>

<span data-ttu-id="eb478-p104">**Members** は、標準の ADO コレクションです。このコレクションのプロパティとメソッドを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="eb478-p104">**Members** is a standard ADO collection. With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="eb478-118">[Count](count-property-ado.md) プロパティを使用して、コレクションの尾オブジェクトの数を取得します。</span><span class="sxs-lookup"><span data-stu-id="eb478-118">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="eb478-119">既定の [Item](item-property-ado.md) プロパティを使用して、コレクションからオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="eb478-119">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="eb478-120">[Refresh](refresh-method-ado.md) メソッドを使用して、プロバイダーからコレクションのオブジェクトを更新します。</span><span class="sxs-lookup"><span data-stu-id="eb478-120">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

