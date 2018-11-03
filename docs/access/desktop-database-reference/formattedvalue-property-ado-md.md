---
title: FormattedValue プロパティ (ADO MD)
TOCTitle: FormattedValue property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 547feea04a7e6d103f30071094070650705789be
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922112"
---
# <a name="formattedvalue-property-ado-md"></a><span data-ttu-id="77442-102">FormattedValue プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="77442-102">FormattedValue property (ADO MD)</span></span>


<span data-ttu-id="77442-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="77442-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="77442-104">セル値の書式付き表示を示します。</span><span class="sxs-lookup"><span data-stu-id="77442-104">Indicates the formatted display of a cell value.</span></span>

## <a name="return-values"></a><span data-ttu-id="77442-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="77442-105">Return values</span></span>

<span data-ttu-id="77442-106">文字列型 ( **String** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="77442-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="77442-107">解説</span><span class="sxs-lookup"><span data-stu-id="77442-107">Remarks</span></span>

<span data-ttu-id="77442-p101">**FormattedValue** プロパティを使用すると、 [Cell](value-property-ado-md.md) オブジェクトの [Value](cell-object-ado-md.md) プロパティの書式付き表示の値を取得できます。たとえば、セルの値が 1056.87 で、この値がドルの額を表している場合、 **FormattedValue** プロパティは $1,056.87 になります。</span><span class="sxs-lookup"><span data-stu-id="77442-p101">Use the **FormattedValue** property to obtain the formatted display value of the [Value](value-property-ado-md.md) property of a [Cell](cell-object-ado-md.md) object. For example, if the value of a cell was 1056.87, and this value represented a dollar amount, **FormattedValue** would be $1,056.87.</span></span>

