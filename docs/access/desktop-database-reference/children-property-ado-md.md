---
title: Children プロパティ (ADO MD)
TOCTitle: Children Property (ADO MD)
ms:assetid: 66eff203-68e5-a36d-eb2f-2e9faa80deb6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249400(v=office.15)
ms:contentKeyID: 48545352
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dbbae74ce8ce22255e97403fc3906dd50f36b38b
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605052"
---
# <a name="children-property-ado-md"></a><span data-ttu-id="4feda-102">Children プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4feda-102">Children Property (ADO MD)</span></span>


<span data-ttu-id="4feda-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="4feda-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="4feda-104">階層内で、現在の [Member](members-collection-ado-md.md) を親とする [Members](member-object-ado-md.md) コレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="4feda-104">Returns a [Members](members-collection-ado-md.md) collection for which the current [Member](member-object-ado-md.md) is the parent in the hierarchy.</span></span>

<span data-ttu-id="4feda-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="4feda-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="4feda-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="4feda-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="4feda-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="4feda-107">Return values</span></span>
>>>>>>> <span data-ttu-id="4feda-108">master</span><span class="sxs-lookup"><span data-stu-id="4feda-108">master</span></span>

<span data-ttu-id="4feda-109">**Members** コレクションを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="4feda-109">Returns a **Members** collection and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="4feda-110">解説</span><span class="sxs-lookup"><span data-stu-id="4feda-110">Remarks</span></span>

<span data-ttu-id="4feda-p101">**Children** プロパティには、現在の **Member** を階層内で親とする **Members** コレクションが含まれます。リーフ レベルの **Member** オブジェクトには **Members** コレクションに子メンバーがありません。このプロパティは、 **Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトでのみサポートされています。 **Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4feda-p101">The **Children** property contains a **Members** collection for which the current **Member** is the hierarchical parent. Leaf level **Member** objects have no child members in the **Members** collection. This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

