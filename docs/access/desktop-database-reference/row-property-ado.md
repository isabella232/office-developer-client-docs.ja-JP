---
<span data-ttu-id="32657-101">タイトル: 行のプロパティを ActiveX データ オブジェクト (ADO) <<<<<<< ヘッド TOCTitle: 行プロパティ (ADO) === TOCTitle: 行のプロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="32657-101">title: Row Property - ActiveX Data Objects (ADO) <<<<<<< HEAD TOCTitle: Row Property (ADO) ======= TOCTitle: Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="32657-102">マスターの ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="32657-102">master ms:assetid: 1c2b0e27-7232-4b1c-826c-9dc15d758851 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248959(v=office.15) ms:contentKeyID: 48543562 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="32657-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="32657-103"><<<<<<< HEAD</span></span>
# <a name="row-property-ado"></a><span data-ttu-id="32657-104">Row プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="32657-104">Row Property (ADO)</span></span>
=======
# <a name="row-property-ado"></a><span data-ttu-id="32657-105">行プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="32657-105">Row property (ADO)</span></span>
>>>>>>> <span data-ttu-id="32657-106">master</span><span class="sxs-lookup"><span data-stu-id="32657-106">master</span></span>


<span data-ttu-id="32657-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="32657-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="32657-108">**ADORecordConstruction** オブジェクトの OLE DB **Row** オブジェクトを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="32657-108">Gets or sets an OLE DB **Row** object from/on an **ADORecordConstruction** object.</span></span> <span data-ttu-id="32657-109">使用すると**に\_行\*\*\*\*行**オブジェクトを設定するのには、行になって ADO**レコード**オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="32657-109">When you use **put\_Row** to set a **Row** object, a row is turned into an ADO **Record** object.</span></span> <span data-ttu-id="32657-110">値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="32657-110">Read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32657-111">構文</span><span class="sxs-lookup"><span data-stu-id="32657-111">Syntax</span></span>

<span data-ttu-id="32657-112">HRESULT get\_行 (\[、戻り値を\]IUnknown\* \* ppRow)。</span><span class="sxs-lookup"><span data-stu-id="32657-112">HRESULT get\_Row(\[out, retval\] IUnknown\*\* ppRow);</span></span>

<span data-ttu-id="32657-113">HRESULT に\_の行 (\[の\]IUnknown\* pRow)。</span><span class="sxs-lookup"><span data-stu-id="32657-113">HRESULT put\_Row(\[in\] IUnknown\* pRow);</span></span>

## <a name="parameters"></a><span data-ttu-id="32657-114">パラメーター</span><span class="sxs-lookup"><span data-stu-id="32657-114">Parameters</span></span>

  - <span data-ttu-id="32657-115">*ppRow*</span><span class="sxs-lookup"><span data-stu-id="32657-115">*ppRow*</span></span>

  - <span data-ttu-id="32657-116">OLE DB **Row** オブジェクトを指すポインター。</span><span class="sxs-lookup"><span data-stu-id="32657-116">Pointer to an OLE DB **Row** object.</span></span>

  - <span data-ttu-id="32657-117">*PRow*</span><span class="sxs-lookup"><span data-stu-id="32657-117">*PRow*</span></span>

  - <span data-ttu-id="32657-118">OLE DB **Row** オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="32657-118">An OLE DB **Row** object.</span></span>

<span data-ttu-id="32657-119"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="32657-119"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="32657-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="32657-120">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="32657-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="32657-121">Return values</span></span>
>>>>>>> <span data-ttu-id="32657-122">master</span><span class="sxs-lookup"><span data-stu-id="32657-122">master</span></span>

<span data-ttu-id="32657-123">このプロパティのメソッドなどの標準の HRESULT 値を返します。\_[ok] および E\_は失敗します。</span><span class="sxs-lookup"><span data-stu-id="32657-123">This property method returns the standard HRESULT values, including S\_OK and E\_FAIL.</span></span>

## <a name="applies-to"></a><span data-ttu-id="32657-124">対象</span><span class="sxs-lookup"><span data-stu-id="32657-124">Applies To</span></span>

[<span data-ttu-id="32657-125">ADORecordConstruction</span><span class="sxs-lookup"><span data-stu-id="32657-125">ADORecordConstruction</span></span>](adorecordconstruction-interface-ado.md)

