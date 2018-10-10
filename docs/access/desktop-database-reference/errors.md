---
title: エラー (アクセス デスクトップ データベース参照)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 38a89767de9fca317b3ed25fd81c7bf016a8ba46
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477423"
---
# <a name="errors"></a><span data-ttu-id="dc624-102">エラー</span><span class="sxs-lookup"><span data-stu-id="dc624-102">Errors</span></span>


<span data-ttu-id="dc624-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dc624-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dc624-p101">ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **Connection** オブジェクトの **Errors** コレクションに追加されます。ADO アプリケーションで警告およびエラーを処理する方法の詳細については、「 [6 章: エラー処理](chapter-6-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dc624-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object. For details about handling warnings and errors in your ADO application, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="dc624-p102">アプリケーション エラーは別の機構で発生する場合があります。たとえば Visual Basic では、 **Err** オブジェクトにアプリケーション レベルのエラーが格納されます。</span><span class="sxs-lookup"><span data-stu-id="dc624-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

