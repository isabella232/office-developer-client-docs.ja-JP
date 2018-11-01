---
title: エラーを予測する
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2ea388f44dbe9bdc572d439f5f0d00d6de7a06b1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876569"
---
# <a name="anticipating-errors"></a>エラーを予測する


**適用されます**Access 2013、Office 2013。

エラーの防止は、エラーの処理以上に重要です。この最後のセクションでは、エラーが発生する可能性を抑えるために、アプリケーションで実現可能な予防策の一部を示します。

オブジェクトを使用して操作を実行しようとする前に、 **State** プロパティの値を確認して、オブジェクトの状態を確認します。たとえば、アプリケーションでグローバルな **Connection** を使用する場合は、 **Open** メソッドを呼び出す前に、その接続の **State** プロパティを確認して、既に開いているかどうか確認します。

  - ユーザーからデータを受け取るプログラムでは、そのデータをデータ ストアに渡す前に、検証を実行するコードを用意する必要があります。データ ストア、プロバイダー、ADO、またはプログラミング言語からも、問題が通知されることはありません。ユーザーが入力するすべてのバイトを確認して、そのデータがフィールドの型と一致していること、および必須フィールドが空でないことを確認する必要があります。

データをデータ ストアに書き込もうとする前に、そのデータを確認します。最も簡単な方法は、 **WillMove** イベントまたは **WillUpdateRecordset** イベントを処理することです。ADO のイベントを処理する方法の詳細については、「 [7 章: ADO イベントを処理する](chapter-7-handling-ado-events.md)」を参照してください。

レコード ポインターを移動しようとする前に、 **Recordset** オブジェクトが **Recordset** の範囲を超えていないことを確認します。 **EOF** が True の場合に **MoveNext** を実行しようとしたり、 **BOF** が True の場合に **MovePrev** を実行しようとしたりすると、エラーが発生します。また、 **EOF** と **BOF** の両方が True の場合に、いずれかの **Move** メソッドを実行すると、エラーが生成されます。

また、 **Seek** や **Find** などの操作を空の **Recordset** に対して実行しようとしたときにも、エラーが発生します。

