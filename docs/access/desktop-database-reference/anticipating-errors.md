---
title: エラーの予測
TOCTitle: Anticipating errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 044f5ab8a76b6736ac45bc332d155f5ad5d801ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559060"
---
# <a name="anticipating-errors"></a>エラーの予測


**適用先:** Access 2013、Office 2013

エラーの防止は、エラーの処理以上に重要です。この最後のセクションでは、エラーが発生する可能性を抑えるために、アプリケーションで実現可能な予防策の一部を示します。

オブジェクトを使用して操作を実行しようとする前に、 **State** プロパティの値を確認して、オブジェクトの状態を確認します。たとえば、アプリケーションでグローバルな **Connection** を使用する場合は、 **Open** メソッドを呼び出す前に、その接続の **State** プロパティを確認して、既に開いているかどうか確認します。

- ユーザーからデータを受け取るプログラムでは、そのデータをデータ ストアに渡す前に、検証を実行するコードを用意する必要があります。データ ストア、プロバイダー、ADO、またはプログラミング言語からも、問題が通知されることはありません。ユーザーが入力するすべてのバイトを確認して、そのデータがフィールドの型と一致していること、および必須フィールドが空でないことを確認する必要があります。

データをデータ ストアに書き込もうとする前に、そのデータを確認します。最も簡単な方法は、 **WillMove** イベントまたは **WillUpdateRecordset** イベントを処理することです。ADO のイベントを処理する方法の詳細については、「 [7 章: ADO イベントを処理する](chapter-7-handling-ado-events.md)」を参照してください。

レコード ポインターを移動しようとする前に、 **Recordset** オブジェクトが **Recordset** の範囲を超えていないことを確認します。 **EOF** が True の場合に **MoveNext** を実行しようとしたり、 **BOF** が True の場合に **MovePrev** を実行しようとしたりすると、エラーが発生します。また、 **EOF** と **BOF** の両方が True の場合に、いずれかの **Move** メソッドを実行すると、エラーが生成されます。

また、 **Seek** や **Find** などの操作を空の **Recordset** に対して実行しようとしたときにも、エラーが発生します。

