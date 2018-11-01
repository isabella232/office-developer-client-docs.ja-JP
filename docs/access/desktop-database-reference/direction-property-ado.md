---
title: Direction プロパティ (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b9e34522a69b2e79f8ef44b912e2c0648c5b813d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881294"
---
# <a name="direction-property-ado"></a><span data-ttu-id="e7cbf-102">Direction プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e7cbf-102">Direction property (ADO)</span></span>


<span data-ttu-id="e7cbf-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e7cbf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7cbf-104">[Parameter](parameter-object-ado.md) が、入力パラメーター、出力パラメーター、または入出力両方のパラメーターを表しているか、あるいは、ストアド プロシージャからの戻り値であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7cbf-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="e7cbf-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="e7cbf-105">Settings and return values</span></span>

<span data-ttu-id="e7cbf-106">[ParameterDirectionEnum](parameterdirectionenum.md) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="e7cbf-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7cbf-107">解説</span><span class="sxs-lookup"><span data-stu-id="e7cbf-107">Remarks</span></span>

<span data-ttu-id="e7cbf-p101">**Direction** プロパティは、プロシージャとのパラメーターのやり取りの方法を指定するために使います。 **Direction** プロパティは読み取り/書き込み可能になっています。これにより、パラメーター情報を取得するために ADO がそれ以上プロバイダーを呼び出さないようにする場合に、この情報を設定したり、この情報を返さないプロバイダーを操作したりできます。</span><span class="sxs-lookup"><span data-stu-id="e7cbf-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="e7cbf-p102">プロバイダーの中には、ストアド プロシージャのパラメーターの入出力の方向を確認できないものがあります。その場合は、クエリを実行する前に **Direction** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e7cbf-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

