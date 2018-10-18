---
title: Description プロパティ (ADO MD)
TOCTitle: Description Property (ADO MD)
ms:assetid: 06d5e1d0-6ed7-fe14-3723-3790e225482a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248816(v=office.15)
ms:contentKeyID: 48543055
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7dd66e0288e20bcf38adefc2fcc30f1856ebf3e6
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606872"
---
# <a name="description-property-ado-md"></a><span data-ttu-id="a7b74-102">Description プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="a7b74-102">Description Property (ADO MD)</span></span>


<span data-ttu-id="a7b74-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a7b74-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a7b74-104">現在のオブジェクトを説明するテキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="a7b74-104">Returns a text explanation of the current object.</span></span>

<span data-ttu-id="a7b74-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a7b74-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="a7b74-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="a7b74-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="a7b74-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="a7b74-107">Return values</span></span>
>>>>>>> <span data-ttu-id="a7b74-108">master</span><span class="sxs-lookup"><span data-stu-id="a7b74-108">master</span></span>

<span data-ttu-id="a7b74-109">文字列型 ( **String** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="a7b74-109">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="a7b74-110">解説</span><span class="sxs-lookup"><span data-stu-id="a7b74-110">Remarks</span></span>

<span data-ttu-id="a7b74-p101">[Member](member-object-ado-md.md) オブジェクトでは、 **Description** プロパティはメジャー メンバーと数式メンバーのみに適用されます。これ以外のメンバーに対しては、 **Description** は空の文字列 ("") を返します。メンバーの種類の詳細については、「 [Type プロパティ (ADO MD)](type-property-ado-md.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7b74-p101">For [Member](member-object-ado-md.md) objects, **Description** applies only to measure and formula members. **Description** returns an empty string ("") for all other types of members. For more information about the various types of members, see the [Type](type-property-ado-md.md) property.</span></span>

<span data-ttu-id="a7b74-p102">このプロパティは、**Level** オブジェクトに属する [Member](level-object-ado-md.md) オブジェクトでのみサポートされています。 **Position** オブジェクトに属する [Member](position-object-ado-md.md) オブジェクトからこのプロパティが参照されると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a7b74-p102">This property is only supported on **Member** objects belonging to a [Level](level-object-ado-md.md) object. An error occurs when this property is referenced from **Member** objects belonging to a [Position](position-object-ado-md.md) object.</span></span>

