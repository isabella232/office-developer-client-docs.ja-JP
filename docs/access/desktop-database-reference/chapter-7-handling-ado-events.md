---
title: '第 7 章: ADO イベントの処理'
TOCTitle: 'Chapter 7: Handling ADO events'
ms:assetid: 22924fe2-d00d-8a0c-52f5-2dc6039537ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249004(v=office.15)
ms:contentKeyID: 48543709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e7357cc60a3bddbf96c2abae39fecfb7107025e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699045"
---
# <a name="chapter-7-handling-ado-events"></a><span data-ttu-id="d783a-102">第 7 章: ADO イベントの処理</span><span class="sxs-lookup"><span data-stu-id="d783a-102">Chapter 7: Handling ADO events</span></span>

<span data-ttu-id="d783a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d783a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d783a-104">ADO イベント モデルでは、特定操作の開始前に、または終了後に、*イベント*、または、通知を発行する同期および非同期 ADO 操作をサポートします。</span><span class="sxs-lookup"><span data-stu-id="d783a-104">The ADO event model supports certain synchronous and asynchronous ADO operations that issue *events*, or notifications, before the operation starts or after it completes.</span></span> <span data-ttu-id="d783a-105">イベントは、実際には、アプリケーションで定義したイベント ハンドラーのルーチンの呼び出しです。</span><span class="sxs-lookup"><span data-stu-id="d783a-105">An event is actually a call to an event-handler routine that you define in your application.</span></span>

<span data-ttu-id="d783a-p102">操作開始前に発生するイベントのグループに対してハンドラー関数またはプロシージャを記述すると、その操作に渡されたパラメーターを確認または変更することができます。この操作はまだ実行されていないので、その操作を取り消すことも、そのまま実行して完了することもできます。</span><span class="sxs-lookup"><span data-stu-id="d783a-p102">If you provide handler functions or procedures for the group of events that occur before the operation starts, you can examine or modify the parameters that were passed to the operation. Because it has not been executed yet, you can either cancel the operation or allow it to complete.</span></span>

<span data-ttu-id="d783a-p103">操作完了後に発生するイベントのグループは、ADO を非同期で利用する場合に特に重要です。たとえば、アプリケーションで非同期の [Recordset.Open](open-method-ado-recordset.md) 操作を開始すると、操作の終了時に実行完了イベントによる通知を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="d783a-p103">The group of events that occur after an operation completes are especially important if you use ADO asynchronously. For example, an application that starts an asynchronous [Recordset.Open](open-method-ado-recordset.md) operation is notified by an execution complete event when the operation concludes.</span></span>

<span data-ttu-id="d783a-110">ADO イベント モデルを使用するとアプリケーションのオーバーヘッドが増加しますが、オブジェクトの [State](state-property-ado.md) プロパティをループで監視するなどの非同期操作を利用する他の方法に比べて、このモデルの方がはるかに柔軟性があります。</span><span class="sxs-lookup"><span data-stu-id="d783a-110">Using the ADO event model adds some overhead to your application but provides far more flexibility than other methods of dealing with asynchronous operations, such as monitoring the [State](state-property-ado.md) property of an object with a loop.</span></span>

<span data-ttu-id="d783a-111">この章では、次のトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="d783a-111">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="d783a-112">ADO イベント ハンドラーの概要</span><span class="sxs-lookup"><span data-stu-id="d783a-112">ADO event handler summary</span></span>](ado-event-handler-summary.md)
- [<span data-ttu-id="d783a-113">イベントの種類</span><span class="sxs-lookup"><span data-stu-id="d783a-113">Types of events</span></span>](types-of-events.md)
- [<span data-ttu-id="d783a-114">イベント パラメーター</span><span class="sxs-lookup"><span data-stu-id="d783a-114">Event parameters</span></span>](event-parameters.md)
- [<span data-ttu-id="d783a-115">イベント ハンドラーの共同作業の方法</span><span class="sxs-lookup"><span data-stu-id="d783a-115">How event handlers work together</span></span>](how-event-handlers-work-together.md)
- [<span data-ttu-id="d783a-116">(ADO) の言語によって、ADO イベントのインスタンス化</span><span class="sxs-lookup"><span data-stu-id="d783a-116">ADO event instantiation by language (ADO)</span></span>](ado-event-instantiation-by-language-ado.md)
