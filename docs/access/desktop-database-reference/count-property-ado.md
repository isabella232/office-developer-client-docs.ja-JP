---
title: Count プロパティ (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295472"
---
# <a name="count-property-ado"></a><span data-ttu-id="30b4d-102">Count プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="30b4d-102">Count property (ADO)</span></span>


<span data-ttu-id="30b4d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="30b4d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30b4d-104">コレクション内のオブジェクト数を示します。</span><span class="sxs-lookup"><span data-stu-id="30b4d-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="30b4d-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="30b4d-105">Return value</span></span>

<span data-ttu-id="30b4d-106">長整数型 (**Long**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="30b4d-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30b4d-107">注釈</span><span class="sxs-lookup"><span data-stu-id="30b4d-107">Remarks</span></span>

<span data-ttu-id="30b4d-108">**Count** プロパティは、特定のコレクション内のオブジェクトの数を調べるために使います。</span><span class="sxs-lookup"><span data-stu-id="30b4d-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="30b4d-p101">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使う場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。Microsoft Visual Basic で **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For** **Each...Next** コマンドを使います。</span><span class="sxs-lookup"><span data-stu-id="30b4d-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="30b4d-111">**Count** が 0 の場合、コレクションにはオブジェクトが含まれていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="30b4d-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

