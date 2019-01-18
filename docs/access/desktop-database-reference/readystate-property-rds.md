---
title: ReadyState プロパティ (RDS)
TOCTitle: ReadyState property (RDS)
ms:assetid: e7b62205-a604-ef43-2f5d-9b51b46d2b5a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250175(v=office.15)
ms:contentKeyID: 48548412
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 71dd674e90e2438c616f0973c4f9948f1b20b1f1
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714781"
---
# <a name="readystate-property-rds"></a><span data-ttu-id="dc3c5-102">ReadyState プロパティ (RDS)</span><span class="sxs-lookup"><span data-stu-id="dc3c5-102">ReadyState property (RDS)</span></span>

<span data-ttu-id="dc3c5-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc3c5-104">[DataControl](datacontrol-object-rds.md) オブジェクトがデータを取得して [Recordset](recordset-object-ado.md) オブジェクトに格納するときの進行状況を示します。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-104">Indicates the progress of a [DataControl](datacontrol-object-rds.md) object as it retrieves data into its [Recordset](recordset-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="dc3c5-105">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="dc3c5-105">Settings and return values</span></span>

<span data-ttu-id="dc3c5-106">次のいずれかの値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-106">Sets or returns one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dc3c5-107">値</span><span class="sxs-lookup"><span data-stu-id="dc3c5-107">Value</span></span></p></th>
<th><p><span data-ttu-id="dc3c5-108">説明</span><span class="sxs-lookup"><span data-stu-id="dc3c5-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dc3c5-109"><strong>adcReadyStateLoaded</strong></span><span class="sxs-lookup"><span data-stu-id="dc3c5-109"><strong>adcReadyStateLoaded</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3c5-p101">現在のクエリが実行中で、行はまだ取得されていません。<strong>DataControl</strong> オブジェクトの <strong>Recordset</strong> は使用できません。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-p101">The current query is still executing and no rows have been fetched. The <strong>DataControl</strong> object's <strong>Recordset</strong> is not available for use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dc3c5-112"><strong>adcReadyStateInteractive</strong></span><span class="sxs-lookup"><span data-stu-id="dc3c5-112"><strong>adcReadyStateInteractive</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3c5-p102">現在のクエリによって取得された最初の行セットが <strong>DataControl</strong> オブジェクトの <strong>Recordset</strong> に格納され、使用できます。残りの行はまだ取得中です。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-p102">An initial set of rows retrieved by the current query has been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use. The remaining rows are still being fetched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dc3c5-115"><strong>adcReadyStateComplete</strong></span><span class="sxs-lookup"><span data-stu-id="dc3c5-115"><strong>adcReadyStateComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="dc3c5-116">現在のクエリによって取得されたすべての行が <strong>DataControl</strong> オブジェクトの <strong>Recordset</strong> に格納され、使用できます。
</span><span class="sxs-lookup"><span data-stu-id="dc3c5-116">All rows retrieved by the current query have been stored in the <strong>DataControl</strong> object's <strong>Recordset</strong> and are available for use.</span></span> <span data-ttu-id="dc3c5-117">エラーで処理が中止された場合や、<strong>Recordset</strong> オブジェクトが初期化されていない場合も、この状態になります。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-117">This state will also exist if an operation aborted due to an error, or if the <strong>Recordset</strong> object is not initialized.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="dc3c5-p104">[!メモ] これらの定数を使用するクライアント側の各実行可能ファイルで、使用する定数を宣言する必要があります。定数の宣言は、C:\Program Files\Common Files\System\MSADC フォルダーにある Adcvbs.inc ファイルからコピーして貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-p104">Each client-side executable file that uses these constants must provide declarations for them. You can cut and paste the constant declarations you want from the file Adcvbs.inc, located in the C:\Program Files\Common Files\System\MSADC folder.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc3c5-120">解説</span><span class="sxs-lookup"><span data-stu-id="dc3c5-120">Remarks</span></span>

<span data-ttu-id="dc3c5-p105">非同期クエリの処理中に [ReadyState](onreadystatechange-event-rds.md) プロパティの変更を監視するには、 **onReadyStateChange** イベントを使用します。この方法は、定期的にプロパティの値を確認するよりも効率的です。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-p105">Use the [onReadyStateChange](onreadystatechange-event-rds.md) event to monitor changes in the **ReadyState** property during an asynchronous query operation. This is more efficient than periodically checking the value of the property.</span></span>

<span data-ttu-id="dc3c5-123">[State](state-property-ado.md)プロパティを**取得のみ**、および**レコード セット**に変更**adStateExecuting**から**adcReadyStateComplete**、 **ReadyState**プロパティの変更、非同期操作中にエラーが発生した場合オブジェクト プロパティの[値](value-property-ado.md)のまま*何も*です。</span><span class="sxs-lookup"><span data-stu-id="dc3c5-123">If an error occurs during an asynchronous operation, the **ReadyState** property changes to **adcReadyStateComplete**, the [State](state-property-ado.md) property changes from **adStateExecuting** to **adStateClosed**, and the **Recordset** object [Value](value-property-ado.md) property remains *Nothing*.</span></span>

