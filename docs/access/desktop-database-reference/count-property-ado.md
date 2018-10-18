---
<span data-ttu-id="a149d-101"><<<<<<< ヘッド タイトル: Count プロパティ (ADO) TOCTitle: Count プロパティ (ADO) === タイトル: Count プロパティ (ADO) TOCTitle: Count プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a149d-101"><<<<<<< HEAD title: Count Property (ADO) TOCTitle: Count Property (ADO) ======= title: Count property (ADO) TOCTitle: Count property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a149d-102">マスターの ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15) ms:contentKeyID: 48547253 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="a149d-102">master ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15) ms:contentKeyID: 48547253 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="a149d-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a149d-103"><<<<<<< HEAD</span></span>
# <a name="count-property-ado"></a><span data-ttu-id="a149d-104">Count プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a149d-104">Count Property (ADO)</span></span>
=======
# <a name="count-property-ado"></a><span data-ttu-id="a149d-105">Count プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="a149d-105">Count property (ADO)</span></span>
>>>>>>> <span data-ttu-id="a149d-106">master</span><span class="sxs-lookup"><span data-stu-id="a149d-106">master</span></span>


<span data-ttu-id="a149d-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="a149d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a149d-108">コレクション内のオブジェクト数を示します。</span><span class="sxs-lookup"><span data-stu-id="a149d-108">Indicates the number of objects in a collection.</span></span>

<span data-ttu-id="a149d-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="a149d-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="a149d-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="a149d-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="a149d-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="a149d-111">Return value</span></span>
>>>>>>> <span data-ttu-id="a149d-112">master</span><span class="sxs-lookup"><span data-stu-id="a149d-112">master</span></span>

<span data-ttu-id="a149d-113">長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="a149d-113">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a149d-114">解説</span><span class="sxs-lookup"><span data-stu-id="a149d-114">Remarks</span></span>

<span data-ttu-id="a149d-115">**Count** プロパティは、特定のコレクション内のオブジェクトの数を調べるために使います。</span><span class="sxs-lookup"><span data-stu-id="a149d-115">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="a149d-p101">コレクションのメンバーは 0 から順に番号が割り当てられるため、ループを使う場合は常に 0 から始めて、 **Count** プロパティより 1 小さい値で終わらせる必要があります。Microsoft Visual Basic で **Count** プロパティをチェックせずにコレクションのメンバーをループ処理するには、 **For** **Each...Next** コマンドを使います。</span><span class="sxs-lookup"><span data-stu-id="a149d-p101">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1. If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="a149d-118">**Count** が 0 の場合、コレクションにはオブジェクトが含まれていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="a149d-118">If the **Count** property is zero, there are no objects in the collection.</span></span>

