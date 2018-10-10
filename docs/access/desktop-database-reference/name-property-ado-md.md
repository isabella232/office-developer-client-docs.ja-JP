---
title: Name プロパティ (ADO MD)
TOCTitle: Name Property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0cc7a89e0d6b9cdaed2c54d3269b61280ce3306c
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476999"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="896ab-102">Name プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="896ab-102">Name Property (ADO MD)</span></span>


<span data-ttu-id="896ab-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="896ab-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="896ab-104">オブジェクトの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="896ab-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="896ab-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="896ab-105">Return Values</span></span>

<span data-ttu-id="896ab-106">文字列型 ( **String** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="896ab-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="896ab-107">解説</span><span class="sxs-lookup"><span data-stu-id="896ab-107">Remarks</span></span>

<span data-ttu-id="896ab-p101">オブジェクトの **Name** プロパティを序数参照で取得できます。その後は、名前を使用して直接オブジェクトを参照できます。たとえば、cdf.CubeDefs(0).Name によって "Bobs Video Store" を取得すると、この [CubeDef](cubedef-object-ado-md.md) を cdf.CubeDefs("Bobs Video Store") として参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="896ab-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>
