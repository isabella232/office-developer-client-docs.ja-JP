---
title: エラーを予測する
TOCTitle: Anticipating Errors
ms:assetid: f2368a03-d446-ab42-b505-d5f5a214c000
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250229(v=office.15)
ms:contentKeyID: 48548645
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f062eb86b45778cc7f25fb2d0d0588b82bdd78b3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478820"
---
# <a name="anticipating-errors"></a><span data-ttu-id="3d561-102">エラーを予測する</span><span class="sxs-lookup"><span data-stu-id="3d561-102">Anticipating Errors</span></span>


<span data-ttu-id="3d561-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3d561-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3d561-p101">エラーの防止は、エラーの処理以上に重要です。この最後のセクションでは、エラーが発生する可能性を抑えるために、アプリケーションで実現可能な予防策の一部を示します。</span><span class="sxs-lookup"><span data-stu-id="3d561-p101">Error prevention is at least as important as error handling. This final section contains a short list of precautions your application can take to help make errors less likely to occur.</span></span>

<span data-ttu-id="3d561-p102">オブジェクトを使用して操作を実行しようとする前に、 **State** プロパティの値を確認して、オブジェクトの状態を確認します。たとえば、アプリケーションでグローバルな **Connection** を使用する場合は、 **Open** メソッドを呼び出す前に、その接続の **State** プロパティを確認して、既に開いているかどうか確認します。</span><span class="sxs-lookup"><span data-stu-id="3d561-p102">Check the state of objects by checking the value in the **State** property before trying to perform an operation using those objects. For example, if your application uses a global **Connection**, check its **State** property to see if it is already open before calling the **Open** method.</span></span>

  - <span data-ttu-id="3d561-p103">ユーザーからデータを受け取るプログラムでは、そのデータをデータ ストアに渡す前に、検証を実行するコードを用意する必要があります。データ ストア、プロバイダー、ADO、またはプログラミング言語からも、問題が通知されることはありません。ユーザーが入力するすべてのバイトを確認して、そのデータがフィールドの型と一致していること、および必須フィールドが空でないことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d561-p103">Any program that accepts data from a user must include code to validate that data before sending it to the data store. You cannot rely on the data store, the provider, ADO, or even your programming language to notify you of problems. You must check every byte entered by your users, making sure that data is the correct type for its field and that required fields are not empty.</span></span>

<span data-ttu-id="3d561-p104">データをデータ ストアに書き込もうとする前に、そのデータを確認します。最も簡単な方法は、 **WillMove** イベントまたは **WillUpdateRecordset** イベントを処理することです。ADO のイベントを処理する方法の詳細については、「 [7 章: ADO イベントを処理する](chapter-7-handling-ado-events.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d561-p104">Check the data before you try to write any data to the data store. The easiest way to do so is to handle the **WillMove** event or the **WillUpdateRecordset** event. For a more complete discussion of handling ADO events, see [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md).</span></span>

<span data-ttu-id="3d561-p105">レコード ポインターを移動しようとする前に、 **Recordset** オブジェクトが **Recordset** の範囲を超えていないことを確認します。 **EOF** が True の場合に **MoveNext** を実行しようとしたり、 **BOF** が True の場合に **MovePrev** を実行しようとしたりすると、エラーが発生します。また、 **EOF** と **BOF** の両方が True の場合に、いずれかの **Move** メソッドを実行すると、エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="3d561-p105">Make sure that **Recordset** objects are not beyond the boundaries of the **Recordset** before attempting to move the record pointer. If you try to **MoveNext** when **EOF** is True or **MovePrev** when **BOF** is True, an error will occur. If you perform any of the **Move** methods when both **EOF** and **BOF** are True, an error will be generated.</span></span>

<span data-ttu-id="3d561-117">また、 **Seek** や **Find** などの操作を空の **Recordset** に対して実行しようとしたときにも、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="3d561-117">Errors also will occur if you try to perform operations such as **Seek** and **Find** on an empty **Recordset**.</span></span>
