---
title: エラー (Access デスクトップデータベースリファレンス)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 056ec0b34991348728898b4c0fc4a1a516a9913f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293358"
---
# <a name="errors"></a><span data-ttu-id="fc9b9-102">エラー</span><span class="sxs-lookup"><span data-stu-id="fc9b9-102">Errors</span></span>

<span data-ttu-id="fc9b9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc9b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fc9b9-104">ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="fc9b9-104">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="fc9b9-105">エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **Connection** オブジェクトの **Errors** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="fc9b9-105">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object.</span></span> <span data-ttu-id="fc9b9-106">ADO アプリケーションでの警告とエラーの処理の詳細については、「 [6 章: エラー処理](chapter-6-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fc9b9-106">For details about handling warnings and errors in your ADO application, see [Chapter 6: Error handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="fc9b9-p102">アプリケーション エラーは別の機構で発生する場合があります。たとえば Visual Basic では、 **Err** オブジェクトにアプリケーション レベルのエラーが格納されます。</span><span class="sxs-lookup"><span data-stu-id="fc9b9-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

