---
title: LockType プロパティ (ADO)
TOCTitle: LockType property (ADO)
ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15)
ms:contentKeyID: 48543589
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d12946a90d61a941bf5ef7d479970c8c96e074f9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289844"
---
# <a name="locktype-property-ado"></a><span data-ttu-id="fa3c6-102">LockType プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="fa3c6-102">LockType property (ADO)</span></span>


<span data-ttu-id="fa3c6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="fa3c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fa3c6-104">編集時にレコードに適用されるロックの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-104">Indicates the type of locks placed on records during editing.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="fa3c6-105">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="fa3c6-105">Settings and return values</span></span>

<span data-ttu-id="fa3c6-106">[LockTypeEnum](locktypeenum.md) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-106">Sets or returns a [LockTypeEnum](locktypeenum.md) value.</span></span> <span data-ttu-id="fa3c6-107">既定値は **adLockReadOnly** です。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-107">The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fa3c6-108">注釈</span><span class="sxs-lookup"><span data-stu-id="fa3c6-108">Remarks</span></span>

<span data-ttu-id="fa3c6-p102">プロバイダーが **Recordset** を開くときに使用するロックの種類は、 [LockType](recordset-object-ado.md) プロパティを使用して事前に設定します。開いている **Recordset** オブジェクトで使用されているロックの種類は、このプロパティを取得することで確認できます。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-p102">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="fa3c6-p103">プロバイダーによってはすべての種類のロックをサポートしていないものもあります。要求した **LockType** 設定をプロバイダーがサポートしていない場合は、他の種類のロックに置き換えられます。 **Recordset** オブジェクトで実際に使用可能なロック機能を調べるには、 [adUpdate](supports-method-ado.md) と **adUpdateBatch** で **Supports** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-p103">Providers may not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="fa3c6-p104">**CursorLocation** が [adUseClient](cursorlocation-property-ado.md) に設定されている場合、 **adLockPessimistic** 設定はサポートされません。サポートされていない値を設定してもエラーにはなりませんが、サポートされる **LockType** のうち、最も近いロックが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-p104">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="fa3c6-116">**LockType** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-116">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="fa3c6-117">**リモートデータサービスの使用状況**クライアント側の Recordset オブジェクトで使用する場合、 **LockType**プロパティは**adlockbatchoptimistic**にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="fa3c6-117">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

