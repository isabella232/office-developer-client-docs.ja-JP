---
title: Number プロパティ (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5eb46d6fbeb677e6d0fe73223d74ae2ea42d368
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288575"
---
# <a name="number-property-ado"></a><span data-ttu-id="fa1c1-102">Number プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="fa1c1-102">Number property (ADO)</span></span>


<span data-ttu-id="fa1c1-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa1c1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa1c1-104">[Error](error-object-ado.md) オブジェクトを一意に識別する数値を示します。</span><span class="sxs-lookup"><span data-stu-id="fa1c1-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa1c1-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="fa1c1-105">Return value</span></span>

<span data-ttu-id="fa1c1-106">[ErrorValueEnum](errorvalueenum.md) 定数のいずれかに対応する長整数型 (**Long**) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="fa1c1-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa1c1-107">注釈</span><span class="sxs-lookup"><span data-stu-id="fa1c1-107">Remarks</span></span>

<span data-ttu-id="fa1c1-p101">**Number** プロパティは、発生したエラーを調べるために使用します。プロパティの値は、エラー条件に対応した一意な数値です。</span><span class="sxs-lookup"><span data-stu-id="fa1c1-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="fa1c1-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span><span class="sxs-lookup"><span data-stu-id="fa1c1-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="fa1c1-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span><span class="sxs-lookup"><span data-stu-id="fa1c1-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="fa1c1-112">これらの番号の詳細については、「 *OLE DB プログラマリファレンス*」の「16章」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fa1c1-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

