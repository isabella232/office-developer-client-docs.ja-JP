---
title: Direction プロパティ (ADO)
TOCTitle: Direction property (ADO)
ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15)
ms:contentKeyID: 48544823
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5885e89a3bce5d8b16ea855ce14689380655ad45
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293869"
---
# <a name="direction-property-ado"></a><span data-ttu-id="cb09b-102">Direction プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="cb09b-102">Direction property (ADO)</span></span>


<span data-ttu-id="cb09b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="cb09b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cb09b-104">[Parameter](parameter-object-ado.md) が、入力パラメーター、出力パラメーター、または入出力両方のパラメーターを表しているか、あるいは、ストアド プロシージャからの戻り値であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="cb09b-104">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="cb09b-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="cb09b-105">Settings and return values</span></span>

<span data-ttu-id="cb09b-106">[ParameterDirectionEnum](parameterdirectionenum.md) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="cb09b-106">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb09b-107">注釈</span><span class="sxs-lookup"><span data-stu-id="cb09b-107">Remarks</span></span>

<span data-ttu-id="cb09b-p101">**Direction** プロパティは、プロシージャとのパラメーターのやり取りの方法を指定するために使います。 **Direction** プロパティは読み取り/書き込み可能になっています。これにより、パラメーター情報を取得するために ADO がそれ以上プロバイダーを呼び出さないようにする場合に、この情報を設定したり、この情報を返さないプロバイダーを操作したりできます。</span><span class="sxs-lookup"><span data-stu-id="cb09b-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="cb09b-p102">プロバイダーの中には、ストアド プロシージャのパラメーターの入出力の方向を確認できないものがあります。その場合は、クエリを実行する前に **Direction** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb09b-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

