---
title: Axis オブジェクト (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720731"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="7f377-102">Axis オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7f377-102">Axis object (ADO MD)</span></span>


<span data-ttu-id="7f377-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7f377-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f377-104">1 つ以上の次元の選択されたメンバーを含む、セルセットの位置またはフィルターの軸を表します。</span><span class="sxs-lookup"><span data-stu-id="7f377-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f377-105">解説</span><span class="sxs-lookup"><span data-stu-id="7f377-105">Remarks</span></span>

<span data-ttu-id="7f377-106">**Axis** オブジェクトは、 [Axes](axes-collection-ado-md.md) コレクションに含めるか、または [Cellset](filteraxis-property-ado-md.md) の [FilterAxis](cellset-object-ado-md.md) プロパティによって返すことができます。</span><span class="sxs-lookup"><span data-stu-id="7f377-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="7f377-107">**Axis** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="7f377-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

- <span data-ttu-id="7f377-108">**Name** プロパティを使用して、 [Axis](name-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="7f377-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="7f377-109">**Positions** コレクションを使用して、 [Axis](positions-collection-ado-md.md) に沿った位置に反復処理を実行します。</span><span class="sxs-lookup"><span data-stu-id="7f377-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="7f377-110">**DimensionCount** プロパティを使用して、 [Axis](dimensioncount-property-ado-md.md) 上の次元の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f377-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

- <span data-ttu-id="7f377-111">標準の ADO **Properties** コレクションを使用して、 [Axis](properties-collection-ado.md) のプロバイダー固有の属性を取得します。</span><span class="sxs-lookup"><span data-stu-id="7f377-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

