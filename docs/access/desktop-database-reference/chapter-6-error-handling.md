---
title: '第 6 章: エラー処理'
TOCTitle: 'Chapter 6: Error handling'
ms:assetid: 6ae7343b-b9e0-c4c3-f65c-110f903e573e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249420(v=office.15)
ms:contentKeyID: 48545440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 14d3dc4b291d96a47e0fb67c0e7d837463cd4bf2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296410"
---
# <a name="chapter-6-error-handling"></a><span data-ttu-id="d2ecb-102">第 6 章: エラー処理</span><span class="sxs-lookup"><span data-stu-id="d2ecb-102">Chapter 6: Error handling</span></span>

<span data-ttu-id="d2ecb-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2ecb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d2ecb-p101">ADO では、発生するエラーをさまざまな方法でアプリケーションに通知します。この章では、ADO の使用時に発生する可能性のあるエラーの種類、およびアプリケーションが通知を受ける方法について説明します。最後に、それらのエラーを処理する方法に関する提案を示します。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-p101">ADO uses several different methods to notify an application of errors that occur. This chapter discusses the types of errors that can occur when you are using ADO and how your application is notified. It concludes by making suggestions about how to handle those errors.</span></span>

## <a name="how-does-ado-report-errors"></a><span data-ttu-id="d2ecb-107">ADO でエラーが報告されるしくみ</span><span class="sxs-lookup"><span data-stu-id="d2ecb-107">How does ADO report errors?</span></span>

<span data-ttu-id="d2ecb-108">ADO では、次のようなさまざまな方法でエラーが通知されます。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-108">ADO notifies you about errors in several ways:</span></span>

- <span data-ttu-id="d2ecb-p102">ADO エラーが発生すると、実行時エラーが生成されます。ADO エラーの処理は、Visual Basic で **On Error** ステートメントを使用するなど、他の実行時エラーと同様の方法で行います。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-p102">ADO errors generate a run-time error. Handle an ADO error the same way you would any other run-time error, such as using an **On Error** statement in Visual Basic.</span></span>

- <span data-ttu-id="d2ecb-p103">プログラムが OLE DB からエラーを受け取る場合があります。OLE DB エラーの発生時にも、実行時エラーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-p103">Your program can receive errors from OLE DB. An OLE DB error generates a run-time error as well.</span></span>

- <span data-ttu-id="d2ecb-113">発生したエラーがデータ プロバイダーに固有のものである場合、データ ソースへのアクセスに使用された **Connection** オブジェクトの **Errors** コレクションに、1 つ以上の **Error** が追加されます。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-113">If the error is specific to your data provider, one or more **Error** objects are placed in the **Errors** collection of the **Connection** object that was used to access the data store when the error occurred.</span></span>

- <span data-ttu-id="d2ecb-p104">イベントを発生させた処理がエラーも発生させた場合、エラー情報が **Error** オブジェクトに追加され、パラメーターとしてイベントに渡されます。イベントの詳細については、「 [7 章: ADO イベントを処理する](chapter-7-handling-ado-events.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-p104">If the process that raised an event also produced an error, error information is placed in an **Error** object and passed as a parameter to the event. See [Chapter 7: Handling ADO Events](chapter-7-handling-ado-events.md) for more information about events.</span></span>

- <span data-ttu-id="d2ecb-p105">**Recordset** に関係するバッチ更新やその他の一括操作の処理時に発生した問題は、 **Recordset** の **Status** プロパティで示される場合があります。たとえば、スキーマの制約違反または権限不足は、 **RecordStatusEnum** 値で表される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-p105">Problems that occur when processing batch updates or other bulk operations involving a **Recordset** can be indicated by the **Status** property of the **Recordset**. For example, schema constraint violations or insufficient permissions can be specified by **RecordStatusEnum** values.</span></span>

- <span data-ttu-id="d2ecb-p106">現在のレコードに含まれる特定の **Field** に関する問題の発生も、 **Record** または **Recordset** の **Fields** コレクションに含まれる各 **Field** の **Status** プロパティによって示されます。たとえば、更新を完了できなかった場合や、データ型に互換性がない場合は、 **FieldStatusEnum** 値で表される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-p106">Problems that occur involving a particular **Field** in the current record are also indicated by the **Status** property of each **Field** in the **Fields** collection of the **Record** or **Recordset**. For example, updates that could not be completed or incompatible data types can be specified by **FieldStatusEnum** values.</span></span>

<span data-ttu-id="d2ecb-120">以降のセクションでは、これらの各通知方法について詳細に説明します。</span><span class="sxs-lookup"><span data-stu-id="d2ecb-120">The following sections describe each of these notification methods in more detail.</span></span>

- [<span data-ttu-id="d2ecb-121">ADO エラー</span><span class="sxs-lookup"><span data-stu-id="d2ecb-121">ADO errors</span></span>](ado-errors.md)
- [<span data-ttu-id="d2ecb-122">ADO エラー リファレンス</span><span class="sxs-lookup"><span data-stu-id="d2ecb-122">ADO error reference</span></span>](ado-error-reference.md)
- [<span data-ttu-id="d2ecb-123">プロバイダー エラー</span><span class="sxs-lookup"><span data-stu-id="d2ecb-123">Provider errors</span></span>](provider-errors.md)
- [<span data-ttu-id="d2ecb-124">フィールドに関連するエラー情報</span><span class="sxs-lookup"><span data-stu-id="d2ecb-124">Field-related error information</span></span>](field-related-error-information.md)
- [<span data-ttu-id="d2ecb-125">レコードセットに関連するエラー情報</span><span class="sxs-lookup"><span data-stu-id="d2ecb-125">Recordset-related error information</span></span>](recordset-related-error-information.md)
- [<span data-ttu-id="d2ecb-126">エラーの予測</span><span class="sxs-lookup"><span data-stu-id="d2ecb-126">Anticipating errors</span></span>](anticipating-errors.md)
- [<span data-ttu-id="d2ecb-127">他の言語でのエラー処理 (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2ecb-127">Handling errors in other languages (ADO)</span></span>](handling-errors-in-other-languages.md)
