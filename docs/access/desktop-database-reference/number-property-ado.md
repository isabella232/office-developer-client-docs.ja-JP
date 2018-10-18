---
<span data-ttu-id="23fb8-101"><<<<<<< ヘッド タイトル: 数値プロパティ (ADO) TOCTitle: 数値プロパティ (ADO) === タイトル: 番号のプロパティ (ADO) TOCTitle: プロパティ (ADO) の番号</span><span class="sxs-lookup"><span data-stu-id="23fb8-101"><<<<<<< HEAD title: Number Property (ADO) TOCTitle: Number Property (ADO) ======= title: Number property (ADO) TOCTitle: Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="23fb8-102">マスターの ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID: 48547243 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="23fb8-102">master ms:assetid: b5103af5-356b-ec74-cd62-86e59467d491 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249868(v=office.15) ms:contentKeyID: 48547243 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="23fb8-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="23fb8-103"><<<<<<< HEAD</span></span>
# <a name="number-property-ado"></a><span data-ttu-id="23fb8-104">Number プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="23fb8-104">Number Property (ADO)</span></span>
=======
# <a name="number-property-ado"></a><span data-ttu-id="23fb8-105">Number プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="23fb8-105">Number property (ADO)</span></span>
>>>>>>> <span data-ttu-id="23fb8-106">master</span><span class="sxs-lookup"><span data-stu-id="23fb8-106">master</span></span>


<span data-ttu-id="23fb8-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="23fb8-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="23fb8-108">[Error](error-object-ado.md) オブジェクトを一意に識別する数値を示します。</span><span class="sxs-lookup"><span data-stu-id="23fb8-108">Indicates the number that uniquely identifies an [Error](error-object-ado.md) object.</span></span>

<span data-ttu-id="23fb8-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="23fb8-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="23fb8-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="23fb8-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="23fb8-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="23fb8-111">Return value</span></span>
>>>>>>> <span data-ttu-id="23fb8-112">master</span><span class="sxs-lookup"><span data-stu-id="23fb8-112">master</span></span>

<span data-ttu-id="23fb8-113">**ErrorValueEnum** 定数のいずれかに対応する長整数型 ( [Long](errorvalueenum.md) ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="23fb8-113">Returns a **Long** value that may correspond to one of the [ErrorValueEnum](errorvalueenum.md) constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="23fb8-114">解説</span><span class="sxs-lookup"><span data-stu-id="23fb8-114">Remarks</span></span>

<span data-ttu-id="23fb8-p101">**Number** プロパティは、発生したエラーを調べるために使用します。プロパティの値は、エラー条件に対応した一意な数値です。</span><span class="sxs-lookup"><span data-stu-id="23fb8-p101">Use the **Number** property to determine which error occurred. The value of the property is a unique number that corresponds to the error condition.</span></span>

<span data-ttu-id="23fb8-117">[Errors](errors-collection-ado.md)コレクションは、いずれかの 16 進形式 (例: 0x80004005) または長整数型 (例: 2147467259) で HRESULT を返します。</span><span class="sxs-lookup"><span data-stu-id="23fb8-117">The [Errors](errors-collection-ado.md) collection returns an HRESULT in either hexadecimal format (for example, 0x80004005) or long value (for example, 2147467259).</span></span> <span data-ttu-id="23fb8-118">これらの Hresult は、OLE DB または偶数の OLE 自体など、基になるコンポーネントで発生する可能性がします。</span><span class="sxs-lookup"><span data-stu-id="23fb8-118">These HRESULTs can be raised by underlying components, such as OLE DB or even OLE itself.</span></span> <span data-ttu-id="23fb8-119">これらの数値の詳細については、の第 16 章を参照してください、 *OLE DB プログラマ リファレンスです*。</span><span class="sxs-lookup"><span data-stu-id="23fb8-119">For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

