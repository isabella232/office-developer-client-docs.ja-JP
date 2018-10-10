---
title: BeginTrans メソッド、CommitTrans メソッド、および RollbackTrans メソッド (ADO)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)
ms:assetid: 9a0415f0-9424-8d1c-4779-92e932292d46
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249694(v=office.15)
ms:contentKeyID: 48546529
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 69d3d7830204ec400e01b64bb11434c272da5c29
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477458"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-ado"></a><span data-ttu-id="58c99-102">BeginTrans メソッド、CommitTrans メソッド、および RollbackTrans メソッド (ADO)</span><span class="sxs-lookup"><span data-stu-id="58c99-102">BeginTrans, CommitTrans, and RollbackTrans Methods (ADO)</span></span>


<span data-ttu-id="58c99-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="58c99-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="58c99-104">これらのトランザクション メソッドは、[Connection](connection-object-ado.md) オブジェクト内のトランザクション処理を次のように管理します。</span><span class="sxs-lookup"><span data-stu-id="58c99-104">These transaction methods manage transaction processing within a [Connection](connection-object-ado.md) object as follows:</span></span>

  - <span data-ttu-id="58c99-105">**BeginTrans** は、新しいトランザクションを開始します。</span><span class="sxs-lookup"><span data-stu-id="58c99-105">**BeginTrans** — Begins a new transaction.</span></span>

  - <span data-ttu-id="58c99-p101">**CommitTrans** は、すべての変更を保存して現在のトランザクションを終了します。新しいトランザクションを開始する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="58c99-p101">**CommitTrans** — Saves any changes and ends the current transaction. It may also start a new transaction.</span></span>

  - <span data-ttu-id="58c99-p102">**RollbackTrans** は、現在のトランザクションの間に行われたすべての変更をキャンセルし、トランザクションを終了します。新しいトランザクションを開始する場合もあります。</span><span class="sxs-lookup"><span data-stu-id="58c99-p102">**RollbackTrans** — Cancels any changes made during the current transaction and ends the transaction. It may also start a new transaction.</span></span>

## <a name="syntax"></a><span data-ttu-id="58c99-110">構文</span><span class="sxs-lookup"><span data-stu-id="58c99-110">Syntax</span></span>

<span data-ttu-id="58c99-111">*レベル* = *オブジェクト*です。BeginTrans()</span><span class="sxs-lookup"><span data-stu-id="58c99-111">*level* = *object*.BeginTrans()</span></span>

<span data-ttu-id="58c99-112">*オブジェクト*です。BeginTrans</span><span class="sxs-lookup"><span data-stu-id="58c99-112">*object*.BeginTrans</span></span>

<span data-ttu-id="58c99-113">*オブジェクト*です。CommitTrans</span><span class="sxs-lookup"><span data-stu-id="58c99-113">*object*.CommitTrans</span></span>

<span data-ttu-id="58c99-114">*オブジェクト*です。RollbackTrans</span><span class="sxs-lookup"><span data-stu-id="58c99-114">*object*.RollbackTrans</span></span>

## <a name="return-value"></a><span data-ttu-id="58c99-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="58c99-115">Return Value</span></span>

<span data-ttu-id="58c99-116">**BeginTrans** は、トランザクションの入れ子レベルを示す長整数型 ( **Long** ) の変数を返す関数として呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="58c99-116">**BeginTrans** can be called as a function that returns a **Long** variable indicating the nesting level of the transaction.</span></span>

## <a name="parameters"></a><span data-ttu-id="58c99-117">パラメーター</span><span class="sxs-lookup"><span data-stu-id="58c99-117">Parameters</span></span>

  - <span data-ttu-id="58c99-118">*object*</span><span class="sxs-lookup"><span data-stu-id="58c99-118">*object*</span></span>

  - <span data-ttu-id="58c99-119">**Connection** オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="58c99-119">A **Connection** object.</span></span>

<span data-ttu-id="58c99-120">**Connection**</span><span class="sxs-lookup"><span data-stu-id="58c99-120">**Connection**</span></span>

<span data-ttu-id="58c99-p103">**Connection** オブジェクトでこれらのメソッドを使用すると、ソース データに対して行った一連の変更を、1 つの単位として保存または取り消すことができます。たとえば、銀行口座間でお金を移すには、一方の口座からその金額を引き出し、他方の口座に入金するという 2 つの操作が行われます。どちらかの更新が失敗すると、口座の残高が合わなくなります。開いているトランザクションでこのような変更を行うと、すべての変更が正しく処理されるか、またはまったく変更が行われないことが保証されます。</span><span class="sxs-lookup"><span data-stu-id="58c99-p103">Use these methods with a **Connection** object when you want to save or cancel a series of changes made to the source data as a single unit. For example, to transfer money between accounts, you subtract an amount from one and add the same amount to the other. If either update fails, the accounts no longer balance. Making these changes within an open transaction ensures that either all or none of the changes go through.</span></span>


> [!NOTE]
> <P><span data-ttu-id="58c99-p104">すべてのプロバイダーがトランザクションをサポートしているわけではありません。プロバイダー定義のプロパティ "<STRONG>Transaction DDL</STRONG>" が、<STRONG>Connection</STRONG> オブジェクトの <A href="properties-collection-ado.md">Properties</A> コレクションに含まれることを確認してください。このプロパティは、プロバイダーがトランザクションをサポートすることを示します。プロバイダーがトランザクションをサポートしない場合、いずれかのトランザクション メソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="58c99-p104">Not all providers support transactions. Verify that the provider-defined property "<STRONG>Transaction DDL</STRONG>" appears in the <STRONG>Connection</STRONG> object's <A href="properties-collection-ado.md">Properties</A> collection, indicating that the provider supports transactions. If the provider does not support transactions, calling one of these methods will return an error.</span></span></P>



<span data-ttu-id="58c99-128">いったん **BeginTrans** メソッドを呼び出すと、 **CommitTrans** メソッドまたは **RollbackTrans** メソッドを呼び出してトランザクションを終了するまで、変更がコミットされることはありません。</span><span class="sxs-lookup"><span data-stu-id="58c99-128">After you call the **BeginTrans** method, the provider will no longer instantaneously commit changes you make until you call **CommitTrans** or **RollbackTrans** to end the transaction.</span></span>

<span data-ttu-id="58c99-p105">入れ子になったトランザクションをサポートするプロバイダーの場合、開いているトランザクションで **BeginTrans** メソッドを呼び出すと、入れ子になった新しいトランザクションが開始されます。戻り値は、入れ子のレベルを示します。戻り値 "1" は最上位レベルのトランザクション (他のトランザクションの入れ子になっていないトランザクション) が開いたことを示し、"2" は第 2 レベルのトランザクション (最上位レベルのトランザクションの入れ子になっているトランザクション) が開いたことを示します ("3" 以下も同様です)。 **CommitTrans** メソッドまたは **RollbackTrans** メソッドを呼び出すと、最後に開いたトランザクションだけが処理されます。さらに上のレベルのトランザクションを処理するには、現在のトランザクションを閉じるか、またはロールバックする必要があります。</span><span class="sxs-lookup"><span data-stu-id="58c99-p105">For providers that support nested transactions, calling the **BeginTrans** method within an open transaction starts a new, nested transaction. The return value indicates the level of nesting: a return value of "1" indicates you have opened a top-level transaction (that is, the transaction is not nested within another transaction), "2" indicates that you have opened a second-level transaction (a transaction nested within a top-level transaction), and so forth. Calling **CommitTrans** or **RollbackTrans** affects only the most recently opened transaction; you must close or roll back the current transaction before you can resolve any higher-level transactions.</span></span>

<span data-ttu-id="58c99-p106">**CommitTrans** メソッドを呼び出すと、その接続で開いているトランザクションで行われた変更が保存され、トランザクションが終了します。 **RollbackTrans** メソッドを呼び出すと、開いているトランザクションで行われたすべての変更が元に戻され、トランザクションが終了します。開いているトランザクションが存在しない状態でいずれかのメソッドを呼び出すと、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="58c99-p106">Calling the **CommitTrans** method saves changes made within an open transaction on the connection and ends the transaction. Calling the **RollbackTrans** method reverses any changes made within an open transaction and ends the transaction. Calling either method when there is no open transaction generates an error.</span></span>

<span data-ttu-id="58c99-p107">**Connection** オブジェクトの [Attributes](attributes-property-ado.md) プロパティによっては、 **CommitTrans** メソッドまたは **RollbackTrans** メソッドを呼び出すと、新しいトランザクションが自動的に開始する場合があります。 **Attributes** プロパティが **adXactCommitRetaining** に設定されている場合は、 **CommitTrans** メソッドを呼び出すと、プロバイダーが新しいトランザクションを自動的に開始します。 **Attributes** プロパティが **adXactAbortRetaining** に設定されている場合は、 **RollbackTrans** メソッドを呼び出すと、プロバイダーが新しいトランザクションを自動的に開始します。</span><span class="sxs-lookup"><span data-stu-id="58c99-p107">Depending on the **Connection** object's [Attributes](attributes-property-ado.md) property, calling either the **CommitTrans** or **RollbackTrans** methods may automatically start a new transaction. If the **Attributes** property is set to **adXactCommitRetaining**, the provider automatically starts a new transaction after a **CommitTrans** call. If the **Attributes** property is set to **adXactAbortRetaining**, the provider automatically starts a new transaction after a **RollbackTrans** call.</span></span>

<span data-ttu-id="58c99-138">**リモート データ サービス**</span><span class="sxs-lookup"><span data-stu-id="58c99-138">**Remote Data Service**</span></span>

<span data-ttu-id="58c99-139">**BeginTrans** メソッド、 **CommitTrans** メソッド、および **RollbackTrans** メソッドは、クライアント側の **Connection** オブジェクトでは利用できません。</span><span class="sxs-lookup"><span data-stu-id="58c99-139">The **BeginTrans**, **CommitTrans**, and **RollbackTrans** methods are not available on a client-side **Connection** object.</span></span>
