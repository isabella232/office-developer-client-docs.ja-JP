---
<span data-ttu-id="eb374-101"><<<<<<< ヘッド タイトル: OriginalValue プロパティ (ADO) TOCTitle: OriginalValue プロパティ (ADO) === タイトル: OriginalValue プロパティ (ADO) TOCTitle: OriginalValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="eb374-101"><<<<<<< HEAD title: OriginalValue Property (ADO) TOCTitle: OriginalValue Property (ADO) ======= title: OriginalValue property (ADO) TOCTitle: OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="eb374-102">マスターの ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="eb374-102">master ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15) ms:contentKeyID: 48542974 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="eb374-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="eb374-103"><<<<<<< HEAD</span></span>
# <a name="originalvalue-property-ado"></a><span data-ttu-id="eb374-104">OriginalValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="eb374-104">OriginalValue Property (ADO)</span></span>
=======
# <a name="originalvalue-property-ado"></a><span data-ttu-id="eb374-105">OriginalValue プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="eb374-105">OriginalValue property (ADO)</span></span>
>>>>>>> <span data-ttu-id="eb374-106">master</span><span class="sxs-lookup"><span data-stu-id="eb374-106">master</span></span>

<span data-ttu-id="eb374-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb374-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="eb374-108">変更が行われる前のレコードに存在していた [Field](field-object-ado.md) の値を示します。</span><span class="sxs-lookup"><span data-stu-id="eb374-108">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

<span data-ttu-id="eb374-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="eb374-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="eb374-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="eb374-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="eb374-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="eb374-111">Return value</span></span>
>>>>>>> <span data-ttu-id="eb374-112">master</span><span class="sxs-lookup"><span data-stu-id="eb374-112">master</span></span>

<span data-ttu-id="eb374-113">変更前のフィールドの値を表すバリアント型 ( **Variant** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="eb374-113">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb374-114">解説</span><span class="sxs-lookup"><span data-stu-id="eb374-114">Remarks</span></span>

<span data-ttu-id="eb374-115">現在のレコードからフィールドの元の値を返すには、 **OriginalValue** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb374-115">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="eb374-116">*イミディ エイト更新モード*(でプロバイダーに変更を書き込みます、基になるデータ ソース[の更新](update-method-ado.md)メソッドを呼び出した後)、 **OriginalValue**プロパティは、変更する前に存在していたフィールドの値を返します (以後、最後の**Update**メソッドの呼び出し)。</span><span class="sxs-lookup"><span data-stu-id="eb374-116">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="eb374-117">これは、 [Value](value-property-ado.md)プロパティを置換するのには、 [CancelUpdate](cancelupdate-method-ado.md)メソッドを使用するのと同じ値です。</span><span class="sxs-lookup"><span data-stu-id="eb374-117">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="eb374-118">*バッチ更新モード*(をプロバイダー複数の変更をキャッシュし、 [UpdateBatch](updatebatch-method-ado.md)メソッドを呼び出した場合にのみ、基になるデータ ソースに書き込みます)、 **OriginalValue**プロパティは、いずれかの前に存在していたフィールドの値を返します(つまり、最後の**UpdateBatch**メソッドを呼び出す) ために変更します。</span><span class="sxs-lookup"><span data-stu-id="eb374-118">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call).</span></span> <span data-ttu-id="eb374-119">これは、 **Value**プロパティを置換するのには、 [CancelBatch](cancelbatch-method-ado.md)メソッドを使用するのと同じ値です。</span><span class="sxs-lookup"><span data-stu-id="eb374-119">This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property.</span></span> <span data-ttu-id="eb374-120">[UnderlyingValue](underlyingvalue-property-ado.md)プロパティを使用してこのプロパティを使用する場合は、バッチ更新で発生した競合を解決できます。</span><span class="sxs-lookup"><span data-stu-id="eb374-120">When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="eb374-121">Record</span><span class="sxs-lookup"><span data-stu-id="eb374-121">Record</span></span>

<span data-ttu-id="eb374-122">[Record](record-object-ado.md) オブジェクトの場合、 **Update** を呼び出す前に追加されたフィールドの [OriginalValue](update-method-ado.md) プロパティは空になります。</span><span class="sxs-lookup"><span data-stu-id="eb374-122">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

