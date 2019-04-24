---
title: StillExecuting プロパティ (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0e53c98f-17ac-3569-d780-540a6932013e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845245(v=office.15)
ms:contentKeyID: 48543245
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1195a45c3846cf79a45c16cda8e23bc95ef8156d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307568"
---
# <a name="recordsetstillexecuting-property-dao"></a><span data-ttu-id="7d3fb-102">StillExecuting プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="7d3fb-102">Recordset.StillExecuting property (DAO)</span></span>

<span data-ttu-id="7d3fb-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d3fb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="7d3fb-104">構文</span><span class="sxs-lookup"><span data-stu-id="7d3fb-104">Syntax</span></span>

<span data-ttu-id="7d3fb-105">*式*。StillExecuting</span><span class="sxs-lookup"><span data-stu-id="7d3fb-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="7d3fb-106">\*式\***Recordset**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="7d3fb-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d3fb-107">注釈</span><span class="sxs-lookup"><span data-stu-id="7d3fb-107">Remarks</span></span>

<span data-ttu-id="7d3fb-p101">**StillExecuting** プロパティを使用して、直前に呼び出した非同期の **Execute** メソッドまたは **OpenConnection** メソッド (つまり、 **dbRunAsync** オプションを指定して実行したメソッド) が完了しているかどうかを調べます。 **StillExecuting** プロパティが **True** の間は、返されたオブジェクトにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="7d3fb-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="7d3fb-p102">**StillExecuting** プロパティで **False** が取得された後で、関連付けられた **Connection** オブジェクトを返す **OpenConnection** メソッドを呼び出すと、そのオブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。</span><span class="sxs-lookup"><span data-stu-id="7d3fb-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="7d3fb-112">処理中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7d3fb-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

