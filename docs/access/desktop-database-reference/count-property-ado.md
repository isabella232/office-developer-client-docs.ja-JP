---
title: Count プロパティ (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c710b02678940d898f910ef5215d879cd6ded163
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880860"
---
# <a name="count-property-ado"></a><span data-ttu-id="ae200-102">Count プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="ae200-102">Count property (ADO)</span></span>


<span data-ttu-id="ae200-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="ae200-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ae200-104">コレクション内のオブジェクト数を示します。</span><span class="sxs-lookup"><span data-stu-id="ae200-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="ae200-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="ae200-105">Return value</span></span>

<span data-ttu-id="ae200-106">長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="ae200-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae200-107">解説</span><span class="sxs-lookup"><span data-stu-id="ae200-107">Remarks</span></span>

<span data-ttu-id="ae200-108">**Count** プロパティは、特定のコレクション内のオブジェクトの数を調べるために使います。</span><span class="sxs-lookup"><span data-stu-id="ae200-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="ae200-p101">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使う場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。Microsoft Visual Basic で **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For** **Each...Next** コマンドを使います。</span><span class="sxs-lookup"><span data-stu-id="ae200-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="ae200-111">**Count** が 0 の場合、コレクションにはオブジェクトが含まれていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="ae200-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

