---
<span data-ttu-id="9877f-101"><<<<<<< ヘッド タイトル: CacheSize プロパティ (ADO) TOCTitle: CacheSize プロパティ (ADO) === タイトル: CacheSize プロパティ (ADO) TOCTitle: CacheSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="9877f-101"><<<<<<< HEAD title: CacheSize Property (ADO) TOCTitle: CacheSize Property (ADO) ======= title: CacheSize property (ADO) TOCTitle: CacheSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9877f-102">マスターの ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15) ms:contentKeyID: 48544491 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="9877f-102">master ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15) ms:contentKeyID: 48544491 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9877f-103"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9877f-103"><<<<<<< HEAD</span></span>
# <a name="cachesize-property-ado"></a><span data-ttu-id="9877f-104">CacheSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="9877f-104">CacheSize Property (ADO)</span></span>
=======
# <a name="cachesize-property-ado"></a><span data-ttu-id="9877f-105">CacheSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="9877f-105">CacheSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="9877f-106">master</span><span class="sxs-lookup"><span data-stu-id="9877f-106">master</span></span>


<span data-ttu-id="9877f-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="9877f-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9877f-108">ローカル メモリにキャッシュされる [Recordset](recordset-object-ado.md) オブジェクトのレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="9877f-108">Indicates the number of records from a [Recordset](recordset-object-ado.md) object that are cached locally in memory.</span></span>

<span data-ttu-id="9877f-109"><<<<<<< 見出し</span><span class="sxs-lookup"><span data-stu-id="9877f-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="9877f-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="9877f-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="9877f-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="9877f-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="9877f-112">master</span><span class="sxs-lookup"><span data-stu-id="9877f-112">master</span></span>

<span data-ttu-id="9877f-p101">0 より大きい長整数型 ( **Long** ) の値を設定または取得します。既定値は 1 です。</span><span class="sxs-lookup"><span data-stu-id="9877f-p101">Sets or returns a **Long** value that must be greater than 0. Default is 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="9877f-115">解説</span><span class="sxs-lookup"><span data-stu-id="9877f-115">Remarks</span></span>

<span data-ttu-id="9877f-p102">**CacheSize** プロパティを使用すると、プロバイダーからローカル メモリに一度に取り込むレコード数を制御できます。たとえば、 **CacheSize** が 10 の場合、 **Recordset** オブジェクトが初めて開かれた後に、最初の 10 のレコードがプロバイダーによってローカル メモリに取り込まれます。 **Recordset** オブジェクト内を移動すると、プロバイダーはローカル メモリのバッファーからデータを返します。キャッシュ内の最後のレコードより後ろのレコードに移動すると、プロバイダーはすぐに次の 10 のレコードをデータ ソースからキャッシュに取り込みます。</span><span class="sxs-lookup"><span data-stu-id="9877f-p102">Use the **CacheSize** property to control how many records to retrieve at one time into local memory from the provider. For example, if the **CacheSize** is 10, after first opening the **Recordset** object, the provider retrieves the first 10 records into local memory. As you move through the **Recordset** object, the provider returns the data from the local memory buffer. As soon as you move past the last record in the cache, the provider retrieves the next 10 records from the data source into the cache.</span></span>

> [!NOTE]
> <span data-ttu-id="9877f-p103">[!メモ] **CacheSize** は、プロバイダー固有のプロパティ **Maximum Open Rows** ( **Recordset** オブジェクトの **Properties** コレクション内) に基づいています。 **CacheSize** を **Maximum Open Rows** より大きい値に設定することはできません。プロバイダーが開くことのできる行の数を変更するには、 **Maximum Open Rows** を設定します。</span><span class="sxs-lookup"><span data-stu-id="9877f-p103">**CacheSize** is based on the **Maximum Open Rows** provider-specific property (in the **Properties** collection of the **Recordset** object). You cannot set **CacheSize** to a value greater than **Maximum Open Rows**. To modify the number of rows which can be opened by the provider, set **Maximum Open Rows**.</span></span>

<span data-ttu-id="9877f-p104">**CacheSize** の値は、 **Recordset** オブジェクトの存続期間中に調整できますが、この値を変更しても、それ以降にデータ ソースから取得されてキャッシュに格納されるレコードの数にしか反映されません。このプロパティの値を変更しただけでは、現在のキャッシュ内の内容は変わりません。</span><span class="sxs-lookup"><span data-stu-id="9877f-p104">The value of **CacheSize** can be adjusted during the life of the **Recordset** object, but changing this value only affects the number of records in the cache after subsequent retrievals from the data source. Changing the property value alone will not change the current contents of the cache.</span></span>

<span data-ttu-id="9877f-125">取り込まれるレコード数が **CacheSize** で指定された数よりも少ない場合は、残りのレコードが返され、エラーは発生しません。</span><span class="sxs-lookup"><span data-stu-id="9877f-125">If there are fewer records to retrieve than **CacheSize** specifies, the provider returns the remaining records and no error occurs.</span></span>

<span data-ttu-id="9877f-126">**CacheSize** を 0 に設定することは許可されておらず、エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="9877f-126">A **CacheSize** setting of zero is not allowed and returns an error.</span></span>

<span data-ttu-id="9877f-p105">キャッシュから取得したレコードには、他のユーザーが平行してソース データに加えた変更は反映されていません。すべてのキャッシュ データを強制的に更新するには、[Resync](resync-method-ado.md) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="9877f-p105">Records retrieved from the cache don't reflect concurrent changes that other users made to the source data. To force an update of all the cached data, use the [Resync](resync-method-ado.md) method.</span></span>

<span data-ttu-id="9877f-p106">**CacheSize** を 1 より大きい値に設定した場合は、レコードの取得後に削除が発生していると、移動メソッド ([Move](move-method-ado.md)、[MoveFirst、MoveLast、MoveNext、および MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) で削除済みのレコードに移動する可能性があります。いったん最初の取得を行うと、削除された行のデータ値にアクセスしようとしない限り、以降の削除がデータ キャッシュに反映されることはありません。一方、**CacheSize** を 1 に設定した場合は、削除された行は取得できないため、この問題を排除できます。</span><span class="sxs-lookup"><span data-stu-id="9877f-p106">If **CacheSize** is set to a value greater than one, the navigation methods ([Move](move-method-ado.md), [MoveFirst, MoveLast, MoveNext, and MovePrevious](movefirst-movelast-movenext-and-moveprevious-methods-ado.md)) may result in navigation to a deleted record, if deletion occurs after the records were retrieved. After the initial fetch, subsequent deletions will not be reflected in your data cache until you attempt to access a data value from a deleted row. However, setting **CacheSize** to one eliminates this issue since deleted rows cannot be fetched.</span></span>

