---
title: エラー (アクセス デスクトップ データベース参照)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 056ec0b34991348728898b4c0fc4a1a516a9913f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700984"
---
# <a name="errors"></a><span data-ttu-id="8e1fa-102">エラー</span><span class="sxs-lookup"><span data-stu-id="8e1fa-102">Errors</span></span>

<span data-ttu-id="8e1fa-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8e1fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8e1fa-104">ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="8e1fa-104">Any operation involving ADO objects can generate one or more provider errors.</span></span> <span data-ttu-id="8e1fa-105">エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **Connection** オブジェクトの **Errors** コレクションに追加されます。</span><span class="sxs-lookup"><span data-stu-id="8e1fa-105">As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object.</span></span> <span data-ttu-id="8e1fa-106">ADO アプリケーションで警告およびエラーの処理の詳細についてを参照してください[第 6 章: エラー処理](chapter-6-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="8e1fa-106">For details about handling warnings and errors in your ADO application, see [Chapter 6: Error handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="8e1fa-p102">アプリケーション エラーは別の機構で発生する場合があります。たとえば Visual Basic では、 **Err** オブジェクトにアプリケーション レベルのエラーが格納されます。</span><span class="sxs-lookup"><span data-stu-id="8e1fa-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

