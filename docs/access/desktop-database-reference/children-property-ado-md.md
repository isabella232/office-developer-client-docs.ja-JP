---
title: Children プロパティ (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 57049e0e68e4620664687cd261881af953de189f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875211"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="5e6c7-102">Children プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="5e6c7-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="5e6c7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5e6c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e6c7-104">階層内で、現在の [Member](members-collection-ado-md.md) を親とする [Members](member-object-ado-md.md) コレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="5e6c7-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="5e6c7-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="5e6c7-105">Return values</span></span>

<span data-ttu-id="5e6c7-106">**Members** コレクションを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="5e6c7-106">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e6c7-107">解説</span><span class="sxs-lookup"><span data-stu-id="5e6c7-107">Remarks</span></span>

<span data-ttu-id="5e6c7-p101">**Children** プロパティには、現在の **Member** を階層内で親とする **Members** コレクションが含まれます。リーフ レベルの **Member** オブジェクトには **Members** コレクションに子メンバーがありません。このプロパティは、 **Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトでのみサポートされています。 **Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5e6c7-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

