---
title: エラー (アクセス デスクトップ データベース参照)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3908a4b882a78360d3fd30ede0d4b9e406d03be5
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873881"
---
# <a name="errors"></a><span data-ttu-id="79741-102">エラー</span><span class="sxs-lookup"><span data-stu-id="79741-102">Errors</span></span>


<span data-ttu-id="79741-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="79741-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="79741-p101">ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **Connection** オブジェクトの **Errors** コレクションに追加されます。ADO アプリケーションで警告およびエラーを処理する方法の詳細については、「 [6 章: エラー処理](chapter-6-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="79741-p101">Any operation involving ADO objects can generate one or more provider errors. As each error occurs, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object. For details about handling warnings and errors in your ADO application, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

<span data-ttu-id="79741-p102">アプリケーション エラーは別の機構で発生する場合があります。たとえば Visual Basic では、 **Err** オブジェクトにアプリケーション レベルのエラーが格納されます。</span><span class="sxs-lookup"><span data-stu-id="79741-p102">Application errors can be raised by a separate mechanism. For example, in Visual Basic, the **Err** object will contain application-level errors.</span></span>

