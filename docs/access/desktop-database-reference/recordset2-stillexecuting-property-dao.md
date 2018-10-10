---
title: Recordset2.StillExecuting プロパティ (DAO)
TOCTitle: StillExecuting Property
ms:assetid: f051c350-0451-44fe-0e47-b152bae4b481
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836546(v=office.15)
ms:contentKeyID: 48548601
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 13feba35a2c635319b96955046edc2ce1d799d58
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477021"
---
# <a name="recordset2stillexecuting-property-dao"></a><span data-ttu-id="abbfd-102">Recordset2.StillExecuting プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="abbfd-102">Recordset2.StillExecuting Property (DAO)</span></span>


<span data-ttu-id="abbfd-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="abbfd-103">**Applies to**: Access 2013 | Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="abbfd-104">構文</span><span class="sxs-lookup"><span data-stu-id="abbfd-104">Syntax</span></span>

<span data-ttu-id="abbfd-105">*式*です。StillExecuting</span><span class="sxs-lookup"><span data-stu-id="abbfd-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="abbfd-106">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="abbfd-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="abbfd-107">注釈</span><span class="sxs-lookup"><span data-stu-id="abbfd-107">Remarks</span></span>

<span data-ttu-id="abbfd-p101">**StillExecuting** プロパティを使用して、直前に呼び出した非同期の **Execute** メソッドまたは **OpenConnection** メソッド (つまり、 **dbRunAsync** オプションを指定して実行したメソッド) が完了しているかどうかを調べます。 **StillExecuting** プロパティが **True** の間は、返されたオブジェクトにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="abbfd-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="abbfd-p102">**StillExecuting** プロパティで **False** が取得された後で、関連付けられた **Connection** オブジェクトを返す **OpenConnection** メソッドを呼び出すと、そのオブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。</span><span class="sxs-lookup"><span data-stu-id="abbfd-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="abbfd-112">処理中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="abbfd-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

