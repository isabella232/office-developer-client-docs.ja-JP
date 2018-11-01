---
title: ChildCount プロパティ (ADO MD)
TOCTitle: ChildCount Property (ADO MD)
ms:assetid: ff1872f0-d5f6-174e-0473-7997a462ca81
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250309(v=office.15)
ms:contentKeyID: 48548956
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0ac5e65356e7ee66cda864bffc983ae1d394825b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879607"
---
# <a name="childcount-property-ado-md"></a><span data-ttu-id="87d7f-102">ChildCount プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="87d7f-102">ChildCount Property (ADO MD)</span></span>


<span data-ttu-id="87d7f-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="87d7f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="87d7f-104">階層内で、現在の [Member](member-object-ado-md.md) オブジェクトが親であるメンバーの数を示します。</span><span class="sxs-lookup"><span data-stu-id="87d7f-104">Indicates the number of members for which the current [Member](member-object-ado-md.md) object is the parent in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="87d7f-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="87d7f-105">Return values</span></span>

<span data-ttu-id="87d7f-106">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="87d7f-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="87d7f-107">解説</span><span class="sxs-lookup"><span data-stu-id="87d7f-107">Remarks</span></span>

<span data-ttu-id="87d7f-p101">**ChildCount** プロパティを使用して、 **Member** が持つ子の数の概算を取得します。 **Member** の子自体は、 [Children](children-property-ado-md.md) プロパティを使用して取得します。</span><span class="sxs-lookup"><span data-stu-id="87d7f-p101">Use the **ChildCount** property to return an estimate of how many children a **Member** has. The actual children of a **Member** can be returned by the [Children](children-property-ado-md.md) property.</span></span>

<span data-ttu-id="87d7f-p102">**Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトから取得される値は、最大で 65536 です。子の実際の数が 65536 を超える場合でも、取得される値は 65536 となります。そのため、 **ChildCount** が 65536 である場合、アプリケーションは子の数が 65536 または以上であると解釈する必要があります。</span><span class="sxs-lookup"><span data-stu-id="87d7f-p102">For **Member** objects from a [Position](position-object-ado-md.md) object, the maximum number returned is 65536. If the actual number of children exceeds 65536, the value returned will still be 65536. Therefore, the application should interpret a **ChildCount** of 65536 as equal to or greater than 65536 children.</span></span>

<span data-ttu-id="87d7f-p103">**Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトの場合、ADO コレクションの [Count](count-property-ado.md) プロパティを **Children** コレクションに使用して、子の正確な数を調べます。コレクション内にある子の数が多い場合、子の正確な数を確認するのに時間がかかることがあります。</span><span class="sxs-lookup"><span data-stu-id="87d7f-p103">For **Member** objects from a [Level](level-object-ado-md.md) object, use the ADO collection [Count](count-property-ado.md) property on the **Children** collection to determine the exact number of children. Determining the exact number of children may be slow if the number of children in the collection is large.</span></span>

