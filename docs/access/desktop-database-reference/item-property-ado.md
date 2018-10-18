---
<span data-ttu-id="2352c-101"><<<<<<< ヘッド タイトル: アイテムのプロパティ (ADO) TOCTitle: アイテムのプロパティ (ADO) === タイトル: Item プロパティ (ADO) TOCTitle: Item プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="2352c-101"><<<<<<< HEAD title: Item Property (ADO) TOCTitle: Item Property (ADO) ======= title: Item property (ADO) TOCTitle: Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2352c-102">マスターの ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="2352c-102">master ms:assetid: 793c305f-0e5b-a529-e21f-b7ab0843ed49 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249499(v=office.15) ms:contentKeyID: 48545767 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2352c-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="2352c-103"><<<<<<< HEAD</span></span>
# <a name="item-property-ado"></a><span data-ttu-id="2352c-104">Item プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="2352c-104">Item Property (ADO)</span></span>
=======
# <a name="item-property-ado"></a><span data-ttu-id="2352c-105">Item プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="2352c-105">Item property (ADO)</span></span>
>>>>>>> <span data-ttu-id="2352c-106">master</span><span class="sxs-lookup"><span data-stu-id="2352c-106">master</span></span>

<span data-ttu-id="2352c-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="2352c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2352c-108">コレクションの特定のメンバーをその名前または序数で示します。</span><span class="sxs-lookup"><span data-stu-id="2352c-108">Indicates a specific member of a collection, by name or ordinal number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2352c-109">構文</span><span class="sxs-lookup"><span data-stu-id="2352c-109">Syntax</span></span>

<span data-ttu-id="2352c-110">*オブジェクト*を設定する = *コレクション*です。項目 (インデックス)</span><span class="sxs-lookup"><span data-stu-id="2352c-110">Set*object* = *collection*.Item ( Index )</span></span>

<span data-ttu-id="2352c-111"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="2352c-111"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="2352c-112">戻り値</span><span class="sxs-lookup"><span data-stu-id="2352c-112">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="2352c-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="2352c-113">Return value</span></span>
>>>>>>> <span data-ttu-id="2352c-114">master</span><span class="sxs-lookup"><span data-stu-id="2352c-114">master</span></span>

<span data-ttu-id="2352c-115">オブジェクトへの参照を返します。</span><span class="sxs-lookup"><span data-stu-id="2352c-115">Returns an object reference.</span></span>

## <a name="parameters"></a><span data-ttu-id="2352c-116">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2352c-116">Parameters</span></span>

- <span data-ttu-id="2352c-117">*Index*</span><span class="sxs-lookup"><span data-stu-id="2352c-117">*Index*</span></span>

- <span data-ttu-id="2352c-118">コレクション内のオブジェクトの名前または序数に評価されるバリアント型 ( **Variant** ) の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="2352c-118">A **Variant** expression that evaluates either to the name or to the ordinal number of an object in a collection.</span></span>

## <a name="remarks"></a><span data-ttu-id="2352c-119">解説</span><span class="sxs-lookup"><span data-stu-id="2352c-119">Remarks</span></span>

<span data-ttu-id="2352c-120">コレクションから特定のオブジェクトを取得するのにには、 **Item**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="2352c-120">Use the **Item** property to return a specific object in a collection.</span></span> <span data-ttu-id="2352c-121">**項目**は、 *Index*引数に対応するコレクション内でオブジェクトを検索することはできません、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2352c-121">If **Item** cannot find an object in the collection corresponding to the *Index* argument, an error occurs.</span></span> <span data-ttu-id="2352c-122">また、いくつかのコレクションをサポートしていない名前付きオブジェクトです。これらのコレクションでは、序数参照を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2352c-122">Also, some collections don't support named objects; for these collections, you must use ordinal number references.</span></span>

<span data-ttu-id="2352c-123">**Item** プロパティはすべてのコレクションの既定プロパティなので、次のいずれの構文形式でも同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="2352c-123">The **Item** property is the default property for all collections; therefore, the following syntax forms are interchangeable:</span></span>

```vb
    collection.Item (Index)
    collection (Index)
```
