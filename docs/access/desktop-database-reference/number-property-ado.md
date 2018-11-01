---
title: Number プロパティ (ADO)
TOCTitle: Number property (ADO)
ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15)
ms:contentKeyID: 48547243
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 72afba54062a3f103fe75939502c9f52eef4c44d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887199"
---
# <a name="number-property-ado"></a><span data-ttu-id="7f11b-102">Number プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="7f11b-102">Number property (ADO)</span></span>


<span data-ttu-id="7f11b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7f11b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7f11b-104">[Error](error-object-ado.md) オブジェクトを一意に識別する数値を示します。</span><span class="sxs-lookup"><span data-stu-id="7f11b-104">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="7f11b-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="7f11b-105">Return value</span></span>

<span data-ttu-id="7f11b-106">**ErrorValueEnum** 定数のいずれかに対応する長整数型 ( [Long](errorvalueenum.md) ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="7f11b-106">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f11b-107">解説</span><span class="sxs-lookup"><span data-stu-id="7f11b-107">Remarks</span></span>

<span data-ttu-id="7f11b-p101">**Number** プロパティは、発生したエラーを調べるために使用します。プロパティの値は、エラー条件に対応した一意な数値です。</span><span class="sxs-lookup"><span data-stu-id="7f11b-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="7f11b-110">[Errors](errors-collection-ado.md)コレクションは、いずれかの 16 進形式 (例: 0x80004005) または長整数型 (例: 2147467259) で HRESULT を返します。</span><span class="sxs-lookup"><span data-stu-id="7f11b-110">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="7f11b-111">これらの Hresult は、OLE DB または偶数の OLE 自体など、基になるコンポーネントで発生する可能性がします。</span><span class="sxs-lookup"><span data-stu-id="7f11b-111">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="7f11b-112">これらの数値の詳細については、の第 16 章を参照してください、 *OLE DB プログラマ リファレンスです*。</span><span class="sxs-lookup"><span data-stu-id="7f11b-112">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

