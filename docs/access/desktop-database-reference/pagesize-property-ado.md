---
<span data-ttu-id="a730a-101"><<<<<<< ヘッド タイトル: PageSize プロパティ (ADO) TOCTitle: PageSize プロパティ (ADO) === タイトル: PageSize プロパティ (ADO) TOCTitle: PageSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a730a-101"><<<<<<< HEAD title: PageSize Property (ADO) TOCTitle: PageSize Property (ADO) ======= title: PageSize property (ADO) TOCTitle: PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a730a-102">マスターの ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a730a-102">master ms:assetid: da56edd8-8947-aeff-2ef5-a8535c66575b ms:mtpsurl: https://msdn.microsoft.com/library/JJ250099(v=office.15) ms:contentKeyID: 48548079 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a730a-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a730a-103"><<<<<<< HEAD</span></span>
# <a name="pagesize-property-ado"></a><span data-ttu-id="a730a-104">PageSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a730a-104">PageSize Property (ADO)</span></span>
=======
# <a name="pagesize-property-ado"></a><span data-ttu-id="a730a-105">PageSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a730a-105">PageSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a730a-106">master</span><span class="sxs-lookup"><span data-stu-id="a730a-106">master</span></span>


<span data-ttu-id="a730a-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a730a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a730a-108">[Recordset](recordset-object-ado.md) の 1 ページを構成するレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="a730a-108">Indicates how many records constitute one page in the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="a730a-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a730a-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="a730a-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="a730a-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="a730a-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="a730a-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="a730a-112">master</span><span class="sxs-lookup"><span data-stu-id="a730a-112">master</span></span>

<span data-ttu-id="a730a-p101">1 ページのレコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 10 です。</span><span class="sxs-lookup"><span data-stu-id="a730a-p101">Sets or returns a **Long** value that indicates how many records are on a page. The default is 10.</span></span>

## <a name="remarks"></a><span data-ttu-id="a730a-115">解説</span><span class="sxs-lookup"><span data-stu-id="a730a-115">Remarks</span></span>

<span data-ttu-id="a730a-116"><<<<<<< ヘッドは、データの論理ページを構成するレコード数を決定するのには**PageSize**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a730a-116"><<<<<<< HEAD Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="a730a-117">ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。</span><span class="sxs-lookup"><span data-stu-id="a730a-117">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="a730a-118">これは、Web サーバーで、ユーザーが一度に特定の数のレコードを表示しながら、データのページ間を移動できるようにする場合に便利です。</span><span class="sxs-lookup"><span data-stu-id="a730a-118">This is useful in Web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
<span data-ttu-id="a730a-119">=== データの論理ページを構成するレコード数を決定するのには、 **PageSize**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a730a-119">======= Use the **PageSize** property to determine how many records make up a logical page of data.</span></span> <span data-ttu-id="a730a-120">ページ サイズを設定すると、 [AbsolutePage](absolutepage-property-ado.md) プロパティを使用して、特定のページの最初のレコードに移動できます。</span><span class="sxs-lookup"><span data-stu-id="a730a-120">Establishing a page size allows you to use the [AbsolutePage](absolutepage-property-ado.md) property to move to the first record of a particular page.</span></span> <span data-ttu-id="a730a-121">これは、機能は、同時にレコード数を表示、データのページにユーザーを許可すると、web サーバーのシナリオで便利です。</span><span class="sxs-lookup"><span data-stu-id="a730a-121">This is useful in web server scenarios when you want to allow the user to page through data, viewing a certain number of records at a time.</span></span>
>>>>>>> <span data-ttu-id="a730a-122">master</span><span class="sxs-lookup"><span data-stu-id="a730a-122">master</span></span>

<span data-ttu-id="a730a-123">このプロパティはいつでも設定でき、その値は、特定のページの最初のレコードの位置を計算するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a730a-123">This property can be set at any time, and its value will be used for calculating the location of the first record of a particular page.</span></span>

