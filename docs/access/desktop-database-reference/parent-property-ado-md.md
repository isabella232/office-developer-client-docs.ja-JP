---
title: Parent プロパティ (ADO MD)
TOCTitle: Parent Property (ADO MD)
ms:assetid: 62649da7-d35f-f11f-674c-28ce95abaf20
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249370(v=office.15)
ms:contentKeyID: 48545238
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7beba341a2374e1868c67c8f7b4fab73c71c0ba8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880300"
---
# <a name="parent-property-ado-md"></a><span data-ttu-id="09a7b-102">Parent プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="09a7b-102">Parent Property (ADO MD)</span></span>


<span data-ttu-id="09a7b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="09a7b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="09a7b-104">階層内の現在のメンバーの親であるメンバーを示します。</span><span class="sxs-lookup"><span data-stu-id="09a7b-104">Indicates the member that is the parent of the current member in a hierarchy.</span></span>

## <a name="return-values"></a><span data-ttu-id="09a7b-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="09a7b-105">Return values</span></span>

<span data-ttu-id="09a7b-106">[Member](member-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="09a7b-106">Returns a [Member](member-object-ado-md.md) object and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="09a7b-107">解説</span><span class="sxs-lookup"><span data-stu-id="09a7b-107">Remarks</span></span>

<span data-ttu-id="09a7b-p101">階層の最上位レベル (ルート) にあるメンバーには、親はありません。このプロパティは、**Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトでのみサポートされます。 **Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="09a7b-p101">A member that is at the top level of a hierarchy (the root) has no parent. This property is supported only on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

