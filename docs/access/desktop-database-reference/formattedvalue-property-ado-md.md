---
title: FormattedValue プロパティ (ADO MD)
TOCTitle: FormattedValue Property (ADO MD)
ms:assetid: ea7962f2-b08b-52c9-34e5-c5490c72662f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250189(v=office.15)
ms:contentKeyID: 48548464
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b1c5efe469c7d22307590dec011366e2d76c1456
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875281"
---
# <a name="formattedvalue-property-ado-md"></a><span data-ttu-id="7cb46-102">FormattedValue プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="7cb46-102">FormattedValue Property (ADO MD)</span></span>


<span data-ttu-id="7cb46-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7cb46-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7cb46-104">セル値の書式付き表示を示します。</span><span class="sxs-lookup"><span data-stu-id="7cb46-104">Indicates the formatted display of a cell value.</span></span>

## <a name="return-values"></a><span data-ttu-id="7cb46-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="7cb46-105">Return values</span></span>

<span data-ttu-id="7cb46-106">文字列型 ( **String** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="7cb46-106">Returns a **String** and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="7cb46-107">解説</span><span class="sxs-lookup"><span data-stu-id="7cb46-107">Remarks</span></span>

<span data-ttu-id="7cb46-p101">**FormattedValue** プロパティを使用すると、 [Cell](value-property-ado-md.md) オブジェクトの [Value](cell-object-ado-md.md) プロパティの書式付き表示の値を取得できます。たとえば、セルの値が 1056.87 で、この値がドルの額を表している場合、 **FormattedValue** プロパティは $1,056.87 になります。</span><span class="sxs-lookup"><span data-stu-id="7cb46-p101">Use the **FormattedValue** property to obtain the formatted display value of the [Value](value-property-ado-md.md) property of a [Cell](cell-object-ado-md.md) object. For example, if the value of a cell was 1056.87, and this value represented a dollar amount, **FormattedValue** would be $1,056.87.</span></span>

