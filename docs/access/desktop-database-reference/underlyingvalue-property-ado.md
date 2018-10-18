---
<span data-ttu-id="81a1c-101"><<<<<<< ヘッド タイトル: UnderlyingValue プロパティ (ADO) TOCTitle: UnderlyingValue プロパティ (ADO) === タイトル: UnderlyingValue プロパティ (ADO) TOCTitle: UnderlyingValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="81a1c-101"><<<<<<< HEAD title: UnderlyingValue Property (ADO) TOCTitle: UnderlyingValue Property (ADO) ======= title: UnderlyingValue property (ADO) TOCTitle: UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="81a1c-102">マスターの ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15) ms:contentKeyID: 48548782 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="81a1c-102">master ms:assetid: f84f4c1c-2bd4-a725-3575-ed063ead13c8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250262(v=office.15) ms:contentKeyID: 48548782 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="81a1c-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="81a1c-103"><<<<<<< HEAD</span></span>
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="81a1c-104">UnderlyingValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="81a1c-104">UnderlyingValue Property (ADO)</span></span>
=======
# <a name="underlyingvalue-property-ado"></a><span data-ttu-id="81a1c-105">UnderlyingValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="81a1c-105">UnderlyingValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="81a1c-106">master</span><span class="sxs-lookup"><span data-stu-id="81a1c-106">master</span></span>


<span data-ttu-id="81a1c-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="81a1c-107">**Applies to**: Access 2013 | Office 2013</span></span>



<span data-ttu-id="81a1c-108">データベース内の [Field](field-object-ado.md) オブジェクトの現在の値を示します。</span><span class="sxs-lookup"><span data-stu-id="81a1c-108">Indicates a [Field](field-object-ado.md) object's current value in the database.</span></span>

<span data-ttu-id="81a1c-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="81a1c-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="81a1c-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="81a1c-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="81a1c-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="81a1c-111">Return value</span></span>
>>>>>>> <span data-ttu-id="81a1c-112">master</span><span class="sxs-lookup"><span data-stu-id="81a1c-112">master</span></span>

<span data-ttu-id="81a1c-113">**Field** の値を示すバリアント型 ( **Variant** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="81a1c-113">Returns a **Variant** value that indicates the value of the **Field**.</span></span>

## <a name="remarks"></a><span data-ttu-id="81a1c-114">解説</span><span class="sxs-lookup"><span data-stu-id="81a1c-114">Remarks</span></span>

<span data-ttu-id="81a1c-p101">データベースから現在のフィールド値を返すには、 **UnderlyingValue** プロパティを使用します。 **UnderlyingValue** プロパティ内のフィールド値は、トランザクションで参照できる値であり、別のトランザクションによる最近の更新の結果である可能性があります。この値は、 [Recordset](originalvalue-property-ado.md) に最初に返された値を反映する [OriginalValue](recordset-object-ado.md) プロパティとは異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="81a1c-p101">Use the **UnderlyingValue** property to return the current field value from the database. The field value in the **UnderlyingValue** property is the value that is visible to your transaction and may be the result of a recent update by another transaction. This may differ from the [OriginalValue](originalvalue-property-ado.md) property, which reflects the value that was originally returned to the [Recordset](recordset-object-ado.md).</span></span>

<span data-ttu-id="81a1c-p102">これは [Resync](resync-method-ado.md) メソッドを使用した場合と似ていますが、 **UnderlyingValue** プロパティは現在のレコードから特定のフィールドの値のみを返します。この値は、 [Resync](resync-method-ado.md) メソッドが [Value](value-property-ado.md) プロパティを置き換えるために使用する値と同じです。</span><span class="sxs-lookup"><span data-stu-id="81a1c-p102">This is similar to using the [Resync](resync-method-ado.md) method, but the **UnderlyingValue** property returns only the value for a specific field from the current record. This is the same value that the [Resync](resync-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="81a1c-120">このプロパティを **OriginalValue** プロパティと共に使用すると、一括更新で発生する競合を解消できます。</span><span class="sxs-lookup"><span data-stu-id="81a1c-120">When you use this property with the **OriginalValue** property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="81a1c-121">Record</span><span class="sxs-lookup"><span data-stu-id="81a1c-121">Record</span></span>

<span data-ttu-id="81a1c-122">[Record](record-object-ado.md) オブジェクトの場合、 [Update](update-method-ado.md) が呼び出される前に追加されたフィールドについては、このプロパティは空になります。</span><span class="sxs-lookup"><span data-stu-id="81a1c-122">For [Record](record-object-ado.md) objects, this property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

