---
title: IsolationLevel プロパティ (ADO)
TOCTitle: IsolationLevel property (ADO)
ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15)
ms:contentKeyID: 48543493
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76978d33fc5f82c9b1f8137b64a663e7e95f2204
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883058"
---
# <a name="isolationlevel-property-ado"></a><span data-ttu-id="b815e-102">IsolationLevel プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="b815e-102">IsolationLevel property (ADO)</span></span>


<span data-ttu-id="b815e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="b815e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b815e-104">[Connection](connection-object-ado.md) オブジェクトの分離レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="b815e-104">Indicates the level of isolation for a [Connection](connection-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="b815e-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="b815e-105">Settings and return values</span></span>

<span data-ttu-id="b815e-p101">[IsolationLevelEnum](isolationlevelenum.md) の値を設定または取得します。既定値は **adXactChaos** です。</span><span class="sxs-lookup"><span data-stu-id="b815e-p101">Sets or returns an [IsolationLevelEnum](isolationlevelenum.md) value. The default is **adXactChaos**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b815e-108">解説</span><span class="sxs-lookup"><span data-stu-id="b815e-108">Remarks</span></span>

<span data-ttu-id="b815e-p102">**IsolationLevel** プロパティでは、 **Connection** オブジェクトの分離レベルを設定します。設定値は、次に [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) メソッドを呼び出すまで有効になりません。要求した分離レベルを使用できない場合、プロバイダーはその次に高い分離レベルを返します。</span><span class="sxs-lookup"><span data-stu-id="b815e-p102">Use the **IsolationLevel** property to set the isolation level of a **Connection** object. The setting does not take effect until the next time you call the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) method. If the level of isolation you request is unavailable, the provider may return the next greater level of isolation.</span></span>

<span data-ttu-id="b815e-112">**IsolationLevel** プロパティは読み取り/書き込み可能です。</span><span class="sxs-lookup"><span data-stu-id="b815e-112">The **IsolationLevel** property is read/write.</span></span>

<span data-ttu-id="b815e-113">**リモート データ サービスの使用法**クライアント側の Connection オブジェクトで使用すると、 **IsolationLevel**プロパティは**adXactUnspecified**にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="b815e-113">**Remote Data Service Usage**When used on a client-side Connection object, the **IsolationLevel** property can be set only to **adXactUnspecified**.</span></span>

<span data-ttu-id="b815e-p103">ユーザーは、クライアント側のキャッシュ上の接続されていない **Recordset** オブジェクトで作業するため、マルチユーザーの場合は問題になることがあります。たとえば、2 人のユーザーが同じレコードを更新しようとした際、リモート データ サービスは単純に先に操作を行ったユーザーの更新を受け付けます。2 番目のユーザーの更新要求はエラーになって失敗します。</span><span class="sxs-lookup"><span data-stu-id="b815e-p103">Because users are working with disconnected **Recordset** objects on a client-side cache, there may be multiuser issues. For instance, when two different users try to update the same record, Remote Data Service simply allows the user who updates the record first to "win." The second user's update request will fail with an error.</span></span>

