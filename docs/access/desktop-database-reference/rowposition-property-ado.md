---
<span data-ttu-id="e52de-101"><<<<<<< ヘッド タイトル: RowPosition プロパティ (ADO) TOCTitle: RowPosition プロパティ (ADO) === タイトル: RowPosition プロパティ (ADO) TOCTitle: RowPosition プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e52de-101"><<<<<<< HEAD title: RowPosition Property (ADO) TOCTitle: RowPosition Property (ADO) ======= title: RowPosition property (ADO) TOCTitle: RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e52de-102">マスターの ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e52de-102">master ms:assetid: b87f14b0-136b-0564-3e12-f9d5ecc4f7c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249887(v=office.15) ms:contentKeyID: 48547325 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e52de-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e52de-103"><<<<<<< HEAD</span></span>
# <a name="rowposition-property-ado"></a><span data-ttu-id="e52de-104">RowPosition プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e52de-104">RowPosition Property (ADO)</span></span>
=======
# <a name="rowposition-property-ado"></a><span data-ttu-id="e52de-105">RowPosition プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e52de-105">RowPosition property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e52de-106">master</span><span class="sxs-lookup"><span data-stu-id="e52de-106">master</span></span>


<span data-ttu-id="e52de-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e52de-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="e52de-108">**ADORecordsetConstruction** オブジェクトの OLE DB **RowPosition** オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e52de-108">Gets or sets an OLE DB **RowPosition** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="e52de-109">使用すると**に\_RowPosition** **RowPosition**オブジェクトを設定するには、結果の**Recordset**オブジェクトでは、現在の行を特定するのには**RowPosition**オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="e52de-109">When you use **put\_RowPosition** to set the **RowPosition** object, the resulting **Recordset** object uses the **RowPosition** object to determine the current row.</span></span>

<span data-ttu-id="e52de-110">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="e52de-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e52de-111">構文</span><span class="sxs-lookup"><span data-stu-id="e52de-111">Syntax</span></span>

<span data-ttu-id="e52de-112">HRESULT get\_RowPosition (\[、戻り値を\]IUnknown\* \* ppRowPos)。</span><span class="sxs-lookup"><span data-stu-id="e52de-112">HRESULT get\_RowPosition(\[out, retval\] IUnknown\*\* ppRowPos);</span></span>

<span data-ttu-id="e52de-113">HRESULT に\_RowPosition (\[の\]IUnknown\* pRowPos)。</span><span class="sxs-lookup"><span data-stu-id="e52de-113">HRESULT put\_RowPosition(\[in\] IUnknown\* pRowPos);</span></span>

## <a name="parameters"></a><span data-ttu-id="e52de-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e52de-114">Parameters</span></span>

  - <span data-ttu-id="e52de-115">*ppRowPos*</span><span class="sxs-lookup"><span data-stu-id="e52de-115">*ppRowPos*</span></span>

  - <span data-ttu-id="e52de-116">OLE DB **RowPosition** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="e52de-116">Pointer to an OLE DB **RowPosition** object.</span></span>

  - <span data-ttu-id="e52de-117">*PRowPos*</span><span class="sxs-lookup"><span data-stu-id="e52de-117">*PRowPos*</span></span>

  - <span data-ttu-id="e52de-118">OLE DB **RowPosition** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="e52de-118">An OLE DB **RowPosition** object.</span></span>

<span data-ttu-id="e52de-119"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e52de-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="e52de-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="e52de-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="e52de-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="e52de-121">Return values</span></span>
>>>>>>> <span data-ttu-id="e52de-122">master</span><span class="sxs-lookup"><span data-stu-id="e52de-122">master</span></span>

<span data-ttu-id="e52de-123">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="e52de-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="remarks"></a><span data-ttu-id="e52de-124">解説</span><span class="sxs-lookup"><span data-stu-id="e52de-124">Remarks</span></span>

<span data-ttu-id="e52de-p102">このプロパティを設定したときに、 **RowPosition** オブジェクトの **Rowset** オブジェクトと **Recordset** オブジェクトの **Rowset** オブジェクトが異なる場合、前者が後者よりも優先されます。同様の動作が **RowPosition** の現在の **Chapter** にも適用されます。</span><span class="sxs-lookup"><span data-stu-id="e52de-p102">When this property is set, if the **Rowset** object on the **RowPosition** object is different from the **Rowset** object on the **Recordset** object, the former overrides the latter. The same behavior applies to the current **Chapter** of the **RowPosition** as well.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e52de-127">対象</span><span class="sxs-lookup"><span data-stu-id="e52de-127">Applies To</span></span>

[<span data-ttu-id="e52de-128">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="e52de-128">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

