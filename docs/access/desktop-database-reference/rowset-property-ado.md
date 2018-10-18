---
<span data-ttu-id="3a63a-101"><<<<<<< ヘッド タイトル: 行セット プロパティ (ADO) TOCTitle: 行セット プロパティ (ADO) === タイトル: 行セットのプロパティ (ADO) TOCTitle: 行セットのプロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3a63a-101"><<<<<<< HEAD title: Rowset Property (ADO) TOCTitle: Rowset Property (ADO) ======= title: Rowset property (ADO) TOCTitle: Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3a63a-102">マスターの ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="3a63a-102">master ms:assetid: 1a1cb3ef-8f3c-30c1-3eb0-8618fdcacd53 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248946(v=office.15) ms:contentKeyID: 48543515 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="3a63a-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="3a63a-103"><<<<<<< HEAD</span></span>
# <a name="rowset-property-ado"></a><span data-ttu-id="3a63a-104">Rowset プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3a63a-104">Rowset Property (ADO)</span></span>
=======
# <a name="rowset-property-ado"></a><span data-ttu-id="3a63a-105">行セット プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="3a63a-105">Rowset property (ADO)</span></span>
>>>>>>> <span data-ttu-id="3a63a-106">master</span><span class="sxs-lookup"><span data-stu-id="3a63a-106">master</span></span>


<span data-ttu-id="3a63a-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="3a63a-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="3a63a-108">**ADORecordsetConstruction** オブジェクトの OLE DB **Rowset** オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="3a63a-108">Gets or sets an OLE DB **Rowset** object from/on an **ADORecordsetConstruction** object.</span></span> <span data-ttu-id="3a63a-109">Put を使用すると、\_、ADO**レコード セット**オブジェクトに、行セットの行セットが有効になっています。</span><span class="sxs-lookup"><span data-stu-id="3a63a-109">When you use put\_Rowset, the rowset is turned into an ADO **Recordset** object.</span></span>

<span data-ttu-id="3a63a-110">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="3a63a-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a63a-111">構文</span><span class="sxs-lookup"><span data-stu-id="3a63a-111">Syntax</span></span>

<span data-ttu-id="3a63a-112">HRESULT get\_行セット (\[、戻り値を\]IUnknown\* \* ppRowset)。</span><span class="sxs-lookup"><span data-stu-id="3a63a-112">HRESULT get\_Rowset(\[out, retval\] IUnknown\*\* ppRowset);</span></span>

<span data-ttu-id="3a63a-113">HRESULT に\_の行セット (\[の\]IUnknown\*ため)。</span><span class="sxs-lookup"><span data-stu-id="3a63a-113">HRESULT put\_Rowset(\[in\] IUnknown\* pRowset);</span></span>

## <a name="parameters"></a><span data-ttu-id="3a63a-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="3a63a-114">Parameters</span></span>

  - <span data-ttu-id="3a63a-115">*ppRowset*</span><span class="sxs-lookup"><span data-stu-id="3a63a-115">*ppRowset*</span></span>

  - <span data-ttu-id="3a63a-116">OLE DB **Rowset** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="3a63a-116">Pointer to an OLE DB **Rowset** object.</span></span>

  - <span data-ttu-id="3a63a-117">*PRowset*</span><span class="sxs-lookup"><span data-stu-id="3a63a-117">*PRowset*</span></span>

  - <span data-ttu-id="3a63a-118">OLE DB **Rowset** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="3a63a-118">An OLE DB **Rowset** object.</span></span>

<span data-ttu-id="3a63a-119"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="3a63a-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="3a63a-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="3a63a-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="3a63a-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="3a63a-121">Return values</span></span>
>>>>>>> <span data-ttu-id="3a63a-122">master</span><span class="sxs-lookup"><span data-stu-id="3a63a-122">master</span></span>

<span data-ttu-id="3a63a-123">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="3a63a-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="3a63a-124">対象</span><span class="sxs-lookup"><span data-stu-id="3a63a-124">Applies To</span></span>

[<span data-ttu-id="3a63a-125">ADORecordsetConstruction</span><span class="sxs-lookup"><span data-stu-id="3a63a-125">ADORecordsetConstruction</span></span>](adorecordsetconstruction-interface-ado.md)

