---
title: エラー (Access デスクトップ データベースリファレンス)
TOCTitle: Errors
ms:assetid: 42f5cab9-f32a-d789-10e8-8d73892427f6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249199(v=office.15)
ms:contentKeyID: 48544490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: c00628ff0bf1cdf6674647c3ef5bd57e3f8654e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597423"
---
# <a name="errors"></a>エラー

**適用先**: Access 2013、Office 2013

ADO オブジェクトに関係するすべての操作では、1 つ以上のプロバイダー エラーが発生する場合があります。 エラーが発生するたびに、1 つ以上の **Error** オブジェクトが **Connection** オブジェクトの **Errors** コレクションに追加されます。 ADO アプリケーションでの警告とエラーの処理の詳細については [、「Chapter 6: Error Handling」を参照してください](chapter-6-error-handling.md)。

アプリケーション エラーは別の機構で発生する場合があります。たとえば Visual Basic では、 **Err** オブジェクトにアプリケーション レベルのエラーが格納されます。

