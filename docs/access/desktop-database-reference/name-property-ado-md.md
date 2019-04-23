---
title: Name プロパティ (ADO MD)
TOCTitle: Name property (ADO MD)
ms:assetid: 31ea6dad-c464-3af7-4b7a-086900656c2c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249093(v=office.15)
ms:contentKeyID: 48544065
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e4e27870a0c1dbb38b7c0be31c439a95f6aae671
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288659"
---
# <a name="name-property-ado-md"></a><span data-ttu-id="c9eec-102">Name プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="c9eec-102">Name property (ADO MD)</span></span>


<span data-ttu-id="c9eec-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c9eec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c9eec-104">オブジェクトの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="c9eec-104">Indicates the name of an object.</span></span>

## <a name="return-values"></a><span data-ttu-id="c9eec-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="c9eec-105">Return values</span></span>

<span data-ttu-id="c9eec-106">文字列型 (**String**) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="c9eec-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9eec-107">注釈</span><span class="sxs-lookup"><span data-stu-id="c9eec-107">Remarks</span></span>

<span data-ttu-id="c9eec-p101">オブジェクトの **Name** プロパティを序数参照で取得できます。その後は、名前を使用して直接オブジェクトを参照できます。たとえば、cdf.CubeDefs(0).Name によって "Bobs Video Store" を取得すると、この [CubeDef](cubedef-object-ado-md.md) を cdf.CubeDefs("Bobs Video Store") として参照できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c9eec-p101">You can retrieve the **Name** property of an object by an ordinal reference, after which you can refer to the object directly by name. For example, if cdf.CubeDefs(0).Name yields "Bobs Video Store", you can refer to this [CubeDef](cubedef-object-ado-md.md) as cdf.CubeDefs("Bobs Video Store").</span></span>

