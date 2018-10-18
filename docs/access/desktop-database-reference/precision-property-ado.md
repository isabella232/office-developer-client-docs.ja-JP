---
<span data-ttu-id="8ed31-101"><<<<<<< ヘッド タイトル: Precision プロパティ (ADO) TOCTitle: Precision プロパティ (ADO) === タイトル: Precision プロパティ (ADO) TOCTitle: Precision プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ed31-101"><<<<<<< HEAD title: Precision Property (ADO) TOCTitle: Precision Property (ADO) ======= title: Precision property (ADO) TOCTitle: Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8ed31-102">マスターの ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: 48547685 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="8ed31-102">master ms:assetid: c9d54d78-d5a5-caf8-d635-259d1fcc0595 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249983(v=office.15) ms:contentKeyID: 48547685 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="8ed31-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="8ed31-103"><<<<<<< HEAD</span></span>
# <a name="precision-property-ado"></a><span data-ttu-id="8ed31-104">Precision プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ed31-104">Precision Property (ADO)</span></span>
=======
# <a name="precision-property-ado"></a><span data-ttu-id="8ed31-105">精度のプロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="8ed31-105">Precision property (ADO)</span></span>
>>>>>>> <span data-ttu-id="8ed31-106">master</span><span class="sxs-lookup"><span data-stu-id="8ed31-106">master</span></span>


<span data-ttu-id="8ed31-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8ed31-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8ed31-108">[Parameter](parameter-object-ado.md) オブジェクト内の数値または数値型の [Field](field-object-ado.md) オブジェクトの精度を示します。</span><span class="sxs-lookup"><span data-stu-id="8ed31-108">Indicates the degree of precision for numeric values in a [Parameter](parameter-object-ado.md) object or for numeric [Field](field-object-ado.md) objects.</span></span>

<span data-ttu-id="8ed31-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="8ed31-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="8ed31-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="8ed31-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="8ed31-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="8ed31-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="8ed31-112">master</span><span class="sxs-lookup"><span data-stu-id="8ed31-112">master</span></span>

<span data-ttu-id="8ed31-113">値を表すために使用する最大桁数を示すバイト型 ( **Byte** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="8ed31-113">Sets or returns a **Byte** value that indicates the maximum number of digits used to represent values.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ed31-114">解説</span><span class="sxs-lookup"><span data-stu-id="8ed31-114">Remarks</span></span>

<span data-ttu-id="8ed31-115">数値型の **Parameter** オブジェクトまたは **Field** オブジェクトの値を表すために使用する最大桁数を調べるには、 **Precision** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="8ed31-115">Use the **Precision** property to determine the maximum number of digits used to represent values for a numeric **Parameter** or **Field** object.</span></span>

<span data-ttu-id="8ed31-116">**Parameter** オブジェクトでは、値の設定および取得が可能です。</span><span class="sxs-lookup"><span data-stu-id="8ed31-116">The value is read/write on a **Parameter** object.</span></span>

<span data-ttu-id="8ed31-p101">**Field** オブジェクトの場合は、 **Precision** は通常、値の取得のみ可能です。ただし、 **Record** の [Fields](fields-collection-ado.md) コレクションに追加された新規 [Field](record-object-ado.md) オブジェクトの場合、 **Field** の [Value](value-property-ado.md) プロパティが指定されており、データ プロバイダーが **Fields** コレクションの **Update** メソッドを呼び出して新規 [Field](update-method-ado.md) の追加に成功した場合にのみ、 **Precision** の値の設定および取得が可能になります。</span><span class="sxs-lookup"><span data-stu-id="8ed31-p101">For a **Field** object, **Precision** is normally read-only. However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Precision** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the data provider has successfully added the new **Field** by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

