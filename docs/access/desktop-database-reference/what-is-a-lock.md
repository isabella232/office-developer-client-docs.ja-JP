---
title: ロックとは (デスクトップ データベースの参照にアクセス)
TOCTitle: What is a Lock?
ms:assetid: 9ddc3198-1531-1d8f-153d-fc79847e388a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249721(v=office.15)
ms:contentKeyID: 48546636
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5e503fd15d9864cc6ab007de031493e321622246
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713423"
---
# <a name="what-is-a-lock"></a><span data-ttu-id="17ac6-103">ロックとは</span><span class="sxs-lookup"><span data-stu-id="17ac6-103">What is a lock?</span></span>


<span data-ttu-id="17ac6-104">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="17ac6-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17ac6-p102">ロックとは、マルチユーザー環境で DBMS が行へのアクセスを制限するプロセスです。行または列が排他的にロックされると、他のユーザーは、ロックが解除されるまでロックされたデータにアクセスできません。これにより、2 人のユーザーが 1 つの行の同じ列を同時に更新できないようにします。</span><span class="sxs-lookup"><span data-stu-id="17ac6-p102">Locking is the process by which a DBMS restricts access to a row in a multi-user environment. When a row or column is exclusively locked, other users are not permitted to access the locked data until the lock is released. This ensures that two users cannot simultaneously update the same column in a row.</span></span>

<span data-ttu-id="17ac6-p103">ロックは、リソースの観点から非常に負荷が高い可能性があるため、データの整合性を保持する必要がある場合にのみ使用します。インターネットに接続されたデータベースのように、毎秒数百または数千のユーザーが 1 つのレコードにアクセスしようとする可能性があるデータベースでは、不要なロックが直ちにアプリケーションのパフォーマンスの低下を招くことになります。</span><span class="sxs-lookup"><span data-stu-id="17ac6-p103">Locks can be very expensive from a resource perspective and should be used only when required to preserve data integrity. In a database where hundreds or thousands of users could be trying to access a record every second — such as a database connected to the Internet — unnecessary locking could quickly result in slower performance in your application.</span></span>

<span data-ttu-id="17ac6-110">適切なロック オプションを選択することで、データ ソースと ADO カーソル ライブラリが同時実行を管理する方法を制御できます。</span><span class="sxs-lookup"><span data-stu-id="17ac6-110">You can control how the data source and the ADO cursor library manage concurrency by choosing the appropriate locking option.</span></span>

<span data-ttu-id="17ac6-p104">プロバイダーが **Recordset** を開くときに使用するロックの種類は、 **LockType** プロパティを使用して事前に設定します。開いている **Recordset** オブジェクトで使用されているロックの種類は、このプロパティを取得することで確認できます。</span><span class="sxs-lookup"><span data-stu-id="17ac6-p104">Set the **LockType** property before opening a **Recordset** to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="17ac6-p105">プロバイダーによっては、すべての種類のロックをサポートしていない場合もあります。要求した **LockType** 設定がプロバイダーでサポートされていない場合は、別の種類のロックが代用されます。 **Recordset** オブジェクトで実際に使用できるロック機能を調べるには、 [adUpdate](supports-method-ado.md) および **adUpdateBatch** の **Supports** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="17ac6-p105">Providers might not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="17ac6-p106">**CursorLocation** プロパティが [adUseClient](cursorlocation-property-ado.md) に設定されている場合、 **adLockPessimistic** 設定はサポートされません。サポートされていない値を設定しても、エラーは発生せず、サポートされる最も近い種類の **LockType** が代わりに使用されます。</span><span class="sxs-lookup"><span data-stu-id="17ac6-p106">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="17ac6-118">**LockType** プロパティは、 **Recordset** が閉じている場合は読み取り/書き込み可能になっていますが、開いている場合は読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="17ac6-118">The **LockType** property is read/write when the **Recordset** is closed, and read-only when it is open.</span></span>

<span data-ttu-id="17ac6-119">このセクションには、次のトピックが含まれています。</span><span class="sxs-lookup"><span data-stu-id="17ac6-119">This section includes the following topic:</span></span>

- [<span data-ttu-id="17ac6-120">ロックの種類</span><span class="sxs-lookup"><span data-stu-id="17ac6-120">Types of Locks</span></span>](types-of-locks.md)

