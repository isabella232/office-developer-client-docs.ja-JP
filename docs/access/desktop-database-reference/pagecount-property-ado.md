---
<span data-ttu-id="65e1a-101"><<<<<<< ヘッド タイトル: PageCount プロパティ (ADO) TOCTitle: PageCount プロパティ (ADO) === タイトル: PageCount プロパティ (ADO) TOCTitle: PageCount プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="65e1a-101"><<<<<<< HEAD title: PageCount Property (ADO) TOCTitle: PageCount Property (ADO) ======= title: PageCount property (ADO) TOCTitle: PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="65e1a-102">マスターの ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="65e1a-102">master ms:assetid: 9cd8bf5c-b1e7-a453-4629-9cba7e408f53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249712(v=office.15) ms:contentKeyID: 48546609 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="65e1a-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="65e1a-103"><<<<<<< HEAD</span></span>
# <a name="pagecount-property-ado"></a><span data-ttu-id="65e1a-104">PageCount プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="65e1a-104">PageCount Property (ADO)</span></span>
=======
# <a name="pagecount-property-ado"></a><span data-ttu-id="65e1a-105">PageCount プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="65e1a-105">PageCount property (ADO)</span></span>
>>>>>>> <span data-ttu-id="65e1a-106">master</span><span class="sxs-lookup"><span data-stu-id="65e1a-106">master</span></span>


<span data-ttu-id="65e1a-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="65e1a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="65e1a-108">[Recordset](recordset-object-ado.md) オブジェクトに含まれるデータのページ数を示します。</span><span class="sxs-lookup"><span data-stu-id="65e1a-108">Indicates how many pages of data the [Recordset](recordset-object-ado.md) object contains.</span></span>

<span data-ttu-id="65e1a-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="65e1a-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="65e1a-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="65e1a-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="65e1a-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="65e1a-111">Return value</span></span>
>>>>>>> <span data-ttu-id="65e1a-112">master</span><span class="sxs-lookup"><span data-stu-id="65e1a-112">master</span></span>

<span data-ttu-id="65e1a-113">**Recordset** のページ数を示す長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="65e1a-113">Returns a **Long** value that indicates the number of pages in the **Recordset**.</span></span>

## <a name="remarks"></a><span data-ttu-id="65e1a-114">解説</span><span class="sxs-lookup"><span data-stu-id="65e1a-114">Remarks</span></span>

<span data-ttu-id="65e1a-115">**PageCount**プロパティのデータ ページの数を決定するが、**レコード セット**オブジェクトでは使用します。</span><span class="sxs-lookup"><span data-stu-id="65e1a-115">Use the **PageCount** property to determine how many pages of data are in the **Recordset** object.</span></span> <span data-ttu-id="65e1a-116">*ページ*は、 [PageSize](pagesize-property-ado.md)プロパティの設定のと同じサイズのレコードのグループです。</span><span class="sxs-lookup"><span data-stu-id="65e1a-116">*Pages* are groups of records whose size equals the [PageSize](pagesize-property-ado.md) property setting.</span></span> <span data-ttu-id="65e1a-117">**PageSize**の値よりも少ないレコードがあるため、最後のページが完了しない場合でも、 **PageCount**の値に追加ページとしてカウントします。</span><span class="sxs-lookup"><span data-stu-id="65e1a-117">Even if the last page is incomplete because there are fewer records than the **PageSize** value, it counts as an additional page in the **PageCount** value.</span></span> <span data-ttu-id="65e1a-118">**Recordset**オブジェクトがこのプロパティをサポートしていない場合、値は**PageCount**は決められていないことを示す-1 になります。</span><span class="sxs-lookup"><span data-stu-id="65e1a-118">If the **Recordset** object does not support this property, the value will be -1 to indicate that the **PageCount** is indeterminable.</span></span>

<span data-ttu-id="65e1a-119">ページ機能の詳細については、 **PageSize** プロパティおよび [AbsolutePage](absolutepage-property-ado.md) プロパティのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="65e1a-119">See the **PageSize** and [AbsolutePage](absolutepage-property-ado.md) properties for more on page functionality.</span></span>

