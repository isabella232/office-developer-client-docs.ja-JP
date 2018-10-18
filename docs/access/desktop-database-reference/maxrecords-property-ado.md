---
<span data-ttu-id="3369d-101"><<<<<<< ヘッド タイトル: MaxRecords プロパティ (ADO) TOCTitle: MaxRecords プロパティ (ADO) === タイトル: MaxRecords プロパティ (ADO) TOCTitle: MaxRecords プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3369d-101"><<<<<<< HEAD title: MaxRecords Property (ADO) TOCTitle: MaxRecords Property (ADO) ======= title: MaxRecords property (ADO) TOCTitle: MaxRecords property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3369d-102">マスターの ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: 48544475 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3369d-102">master ms:assetid: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: 48544475 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3369d-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="3369d-103"><<<<<<< HEAD</span></span>
# <a name="maxrecords-property-ado"></a><span data-ttu-id="3369d-104">MaxRecords プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3369d-104">MaxRecords Property (ADO)</span></span>
=======
# <a name="maxrecords-property-ado"></a><span data-ttu-id="3369d-105">MaxRecords プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3369d-105">MaxRecords property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3369d-106">master</span><span class="sxs-lookup"><span data-stu-id="3369d-106">master</span></span>


<span data-ttu-id="3369d-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3369d-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3369d-108">クエリから [Recordset](recordset-object-ado.md) に返す最大レコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="3369d-108">Indicates the maximum number of records to return to a [Recordset](recordset-object-ado.md) from a query.</span></span>

<span data-ttu-id="3369d-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="3369d-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="3369d-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="3369d-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="3369d-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="3369d-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="3369d-112">master</span><span class="sxs-lookup"><span data-stu-id="3369d-112">master</span></span>

<span data-ttu-id="3369d-p101">返される最大レコード数を示す長整数型 ( **Long** ) の値を設定または取得します。既定値は 0 (制限なし) です。</span><span class="sxs-lookup"><span data-stu-id="3369d-p101">Sets or returns a **Long** value that indicates the maximum number of records to return. Default is zero (no limit).</span></span>

## <a name="remarks"></a><span data-ttu-id="3369d-115">解説</span><span class="sxs-lookup"><span data-stu-id="3369d-115">Remarks</span></span>

<span data-ttu-id="3369d-p102">**MaxRecords** プロパティは、プロバイダーがデータ ソースから返すレコード数を制限するために使用します。このプロパティの既定値は 0 で、プロバイダーが要求されたすべてのレコードを返すことを意味します。</span><span class="sxs-lookup"><span data-stu-id="3369d-p102">Use the **MaxRecords** property to limit the number of records that the provider returns from the data source. The default setting of this property is zero, which means the provider returns all requested records.</span></span>

<span data-ttu-id="3369d-118">**MaxRecords** プロパティは、 **Recordset** が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="3369d-118">The **MaxRecords** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

