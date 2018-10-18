---
<span data-ttu-id="d2c4e-101"><<<<<<< ヘッド タイトル: タイムアウト プロパティ (ADO) TOCTitle: タイムアウト プロパティ (ADO) === タイトル: タイムアウト プロパティ (ADO) TOCTitle: タイムアウト プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2c4e-101"><<<<<<< HEAD title: ConnectionTimeout Property (ADO) TOCTitle: ConnectionTimeout Property (ADO) ======= title: ConnectionTimeout property (ADO) TOCTitle: ConnectionTimeout property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d2c4e-102">マスターの ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: 48548589 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="d2c4e-102">master ms:assetid: efc39fd8-afce-5ac0-2fff-cbb55c1a444d ms:mtpsurl: https://msdn.microsoft.com/library/JJ250218(v=office.15) ms:contentKeyID: 48548589 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d2c4e-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d2c4e-103"><<<<<<< HEAD</span></span>
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="d2c4e-104">ConnectionTimeout プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2c4e-104">ConnectionTimeout Property (ADO)</span></span>
=======
# <a name="connectiontimeout-property-ado"></a><span data-ttu-id="d2c4e-105">タイムアウト プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d2c4e-105">ConnectionTimeout property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d2c4e-106">master</span><span class="sxs-lookup"><span data-stu-id="d2c4e-106">master</span></span>


<span data-ttu-id="d2c4e-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d2c4e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d2c4e-108">接続操作を中止して、エラーを生成するまでの待機時間を示します。</span><span class="sxs-lookup"><span data-stu-id="d2c4e-108">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span>

<span data-ttu-id="d2c4e-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d2c4e-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="d2c4e-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="d2c4e-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="d2c4e-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="d2c4e-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="d2c4e-112">master</span><span class="sxs-lookup"><span data-stu-id="d2c4e-112">master</span></span>

<span data-ttu-id="d2c4e-p101">接続が開くまでの待機時間を秒単位で示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 15 です。</span><span class="sxs-lookup"><span data-stu-id="d2c4e-p101">Sets or returns a **Long** value that indicates, in seconds, how long to wait for the connection to open. Default is 15.</span></span>

## <a name="remarks"></a><span data-ttu-id="d2c4e-115">解説</span><span class="sxs-lookup"><span data-stu-id="d2c4e-115">Remarks</span></span>

<span data-ttu-id="d2c4e-p102">ネットワーク トラフィックやサーバーの過度の使用が原因で接続を開く試みを中止する必要がある場合は、**Connection** オブジェクトで [ConnectionTimeout](connection-object-ado.md) プロパティを使用します。接続が開かれる前に **ConnectionTimeout** プロパティで設定した時間が経過した場合は、エラーが発生して接続の試みが取り消されます。このプロパティを 0 に設定した場合は、ADO は接続が開かれるまで無限に待機します。コードを書き込むプロバイダーが、 **ConnectionTimeout** 機能をサポートしていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="d2c4e-p102">Use the **ConnectionTimeout** property on a [Connection](connection-object-ado.md) object if delays from network traffic or heavy server use make it necessary to abandon a connection attempt. If the time from the **ConnectionTimeout** property setting elapses prior to the opening of the connection, an error occurs and ADO cancels the attempt. If you set the property to zero, ADO will wait indefinitely until the connection is opened. Make sure the provider to which you are writing code supports the **ConnectionTimeout** functionality.</span></span>

<span data-ttu-id="d2c4e-120">**ConnectionTimeout** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="d2c4e-120">The **ConnectionTimeout** property is read/write when the connection is closed and read-only when it is open.</span></span>

