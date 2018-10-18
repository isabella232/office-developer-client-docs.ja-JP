---
<span data-ttu-id="61bd7-101"><<<<<<< ヘッド タイトル: モード プロパティ (ADO) TOCTitle: モード プロパティ (ADO) === タイトル: Mode プロパティ (ADO) TOCTitle: Mode プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="61bd7-101"><<<<<<< HEAD title: Mode Property (ADO) TOCTitle: Mode Property (ADO) ======= title: Mode property (ADO) TOCTitle: Mode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="61bd7-102">マスターの ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15) ms:contentKeyID: 48545227 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="61bd7-102">master ms:assetid: 62086f4f-8624-16c4-dae1-a17475d1864d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249365(v=office.15) ms:contentKeyID: 48545227 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="61bd7-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="61bd7-103"><<<<<<< HEAD</span></span>
# <a name="mode-property-ado"></a><span data-ttu-id="61bd7-104">Mode プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="61bd7-104">Mode Property (ADO)</span></span>
=======
# <a name="mode-property-ado"></a><span data-ttu-id="61bd7-105">Mode プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="61bd7-105">Mode property (ADO)</span></span>
>>>>>>> <span data-ttu-id="61bd7-106">master</span><span class="sxs-lookup"><span data-stu-id="61bd7-106">master</span></span>


<span data-ttu-id="61bd7-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="61bd7-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="61bd7-108">[Connection](connection-object-ado.md) オブジェクト、 [Record](record-object-ado.md) オブジェクト、または [Stream](stream-object-ado.md) オブジェクトで使用可能なデータ変更権限を示します。</span><span class="sxs-lookup"><span data-stu-id="61bd7-108">Indicates the available permissions for modifying data in a [Connection](connection-object-ado.md), [Record](record-object-ado.md), or [Stream](stream-object-ado.md) object.</span></span>

<span data-ttu-id="61bd7-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="61bd7-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="61bd7-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="61bd7-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="61bd7-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="61bd7-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="61bd7-112">master</span><span class="sxs-lookup"><span data-stu-id="61bd7-112">master</span></span>

<span data-ttu-id="61bd7-p101">[ConnectModeEnum](connectmodeenum.md) の値を設定または取得します。**Connection** の既定値は **adModeUnknown** です。**Record** オブジェクトの既定値は **adModeRead** です。基になるソースに関連付けられている **Stream** (URL により、ソース、または **Record** の既定 **Stream** として開かれたもの) の既定値は、**adModeRead** です。基になるソースに関連付けられていない (メモリ内でインスタンス化された) **Stream** の既定値は **adModeUnknown** です。</span><span class="sxs-lookup"><span data-stu-id="61bd7-p101">Sets or returns a [ConnectModeEnum](connectmodeenum.md) value. The default value for a **Connection** is **adModeUnknown**. The default value for a **Record** object is **adModeRead**. The default value for a **Stream** associated with an underlying source (opened with a URL as the source, or as the default **Stream** of a **Record**) is **adModeRead**. The default value for a **Stream** not associated with an underlying source (instantiated in memory) is **adModeUnknown**.</span></span>

## <a name="remarks"></a><span data-ttu-id="61bd7-118">解説</span><span class="sxs-lookup"><span data-stu-id="61bd7-118">Remarks</span></span>

<span data-ttu-id="61bd7-p102">**Mode** プロパティは、プロバイダーが現在の接続で使用しているアクセス権を設定または取得するために使用します。 **Mode** プロパティは、 **Connection** オブジェクトが閉じているときにのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="61bd7-p102">Use the **Mode** property to set or return the access permissions in use by the provider on the current connection. You can set the **Mode** property only when the **Connection** object is closed.</span></span>

<span data-ttu-id="61bd7-p103">**Stream** オブジェクトでは、アクセス モードを指定しない場合、 **Stream** オブジェクトを開くときに使うソースのモードが継承されます。たとえば、 **Record** オブジェクトから **Stream** を開くと、既定では **Record** と同じモードで開きます。</span><span class="sxs-lookup"><span data-stu-id="61bd7-p103">For a **Stream** object, if the access mode is not specified, it is inherited from the source used to open the **Stream** object. For example, if a **Stream** is opened from a **Record** object, by default it is opened in the same mode as the **Record**.</span></span>

<span data-ttu-id="61bd7-123">このプロパティは、オブジェクトが閉じているときは読み取り/書き込み可能で、オブジェクトが開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="61bd7-123">This property is read/write while the object is closed and read-only while the object is open.</span></span>

<span data-ttu-id="61bd7-124">**リモート データ サービスの使用法**クライアント側の Connection オブジェクトで使用すると、[**モード**] プロパティは**adModeUnknown**にのみ設定できます。</span><span class="sxs-lookup"><span data-stu-id="61bd7-124">**Remote Data Service Usage**When used on a client-side Connection object, the **Mode** property can only be set to **adModeUnknown**.</span></span>

