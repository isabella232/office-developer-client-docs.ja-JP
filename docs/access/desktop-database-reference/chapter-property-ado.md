---
<span data-ttu-id="f2319-101"><<<<<<< ヘッド タイトル: 章プロパティ (ADO) TOCTitle: 章プロパティ (ADO) === タイトル: チャプター プロパティ (ADO) TOCTitle: チャプター プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2319-101"><<<<<<< HEAD title: Chapter Property (ADO) TOCTitle: Chapter Property (ADO) ======= title: Chapter property (ADO) TOCTitle: Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2319-102">マスターの ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="f2319-102">master ms:assetid: d7c9478e-487f-7023-1dd8-5313433dbc5e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250085(v=office.15) ms:contentKeyID: 48548014 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="f2319-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="f2319-103"><<<<<<< HEAD</span></span>
# <a name="chapter-property-ado"></a><span data-ttu-id="f2319-104">Chapter プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2319-104">Chapter Property (ADO)</span></span>
=======
# <a name="chapter-property-ado"></a><span data-ttu-id="f2319-105">チャプター プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="f2319-105">Chapter property (ADO)</span></span>
>>>>>>> <span data-ttu-id="f2319-106">master</span><span class="sxs-lookup"><span data-stu-id="f2319-106">master</span></span>


<span data-ttu-id="f2319-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2319-107">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="f2319-108">OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトから取得するか、または、OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="f2319-108">Gets or sets an OLE DB **Chapter** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="f2319-109">使用すると**に\_章\*\*\*\*章**オブジェクトを設定する行のサブセットになって、ADO**レコード セット**オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="f2319-109">When you use **put\_Chapter** to set the **Chapter** object, a subset of rows is turned into an ADO **Recordset** object.</span></span> <span data-ttu-id="f2319-110">これにより、 **Rowset**オブジェクトのカレント チャプターが設定されます。</span><span class="sxs-lookup"><span data-stu-id="f2319-110">This sets the current chapter of the **Rowset** object.</span></span> <span data-ttu-id="f2319-111">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="f2319-111">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2319-112">構文</span><span class="sxs-lookup"><span data-stu-id="f2319-112">Syntax</span></span>

<span data-ttu-id="f2319-113">HRESULT get\_章 (\[、戻り値を\]長\*plChapter)。</span><span class="sxs-lookup"><span data-stu-id="f2319-113">HRESULT get\_Chapter(\[out, retval\] long\* plChapter);</span></span>

<span data-ttu-id="f2319-114">HRESULT に\_の章 (\[に\]長 lChapter)。</span><span class="sxs-lookup"><span data-stu-id="f2319-114">HRESULT put\_Chapter(\[in\] long lChapter);</span></span>

## <a name="parameters"></a><span data-ttu-id="f2319-115">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2319-115">Parameters</span></span>

  - <span data-ttu-id="f2319-116">*plChapter*</span><span class="sxs-lookup"><span data-stu-id="f2319-116">*plChapter*</span></span>

  - <span data-ttu-id="f2319-117">チャプターのハンドルへのポインターです。</span><span class="sxs-lookup"><span data-stu-id="f2319-117">Pointer to the handle of a chapter.</span></span>

  - <span data-ttu-id="f2319-118">*LChapter*</span><span class="sxs-lookup"><span data-stu-id="f2319-118">*LChapter*</span></span>

  - <span data-ttu-id="f2319-119">チャプターのハンドルです。</span><span class="sxs-lookup"><span data-stu-id="f2319-119">Handle of a chapter.</span></span>

<span data-ttu-id="f2319-120"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="f2319-120"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="f2319-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="f2319-121">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="f2319-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="f2319-122">Return values</span></span>
>>>>>>> <span data-ttu-id="f2319-123">master</span><span class="sxs-lookup"><span data-stu-id="f2319-123">master</span></span>

<span data-ttu-id="f2319-124">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="f2319-124">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f2319-125">対象</span><span class="sxs-lookup"><span data-stu-id="f2319-125">Applies To</span></span>

[<span data-ttu-id="f2319-126">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="f2319-126">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

