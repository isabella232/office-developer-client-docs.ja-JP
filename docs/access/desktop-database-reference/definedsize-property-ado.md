---
<span data-ttu-id="e1a0a-101"><<<<<<< ヘッド タイトル: DefinedSize プロパティ (ADO) TOCTitle: DefinedSize プロパティ (ADO) === タイトル: DefinedSize プロパティ (ADO) TOCTitle: DefinedSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e1a0a-101"><<<<<<< HEAD title: DefinedSize Property (ADO) TOCTitle: DefinedSize Property (ADO) ======= title: DefinedSize property (ADO) TOCTitle: DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e1a0a-102">マスターの ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e1a0a-102">master ms:assetid: 8d6db4c9-fbdc-9fcd-63f0-bd677c5ebcf6 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249619(v=office.15) ms:contentKeyID: 48546257 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e1a0a-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e1a0a-103"><<<<<<< HEAD</span></span>
# <a name="definedsize-property-ado"></a><span data-ttu-id="e1a0a-104">DefinedSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e1a0a-104">DefinedSize Property (ADO)</span></span>
=======
# <a name="definedsize-property-ado"></a><span data-ttu-id="e1a0a-105">DefinedSize プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e1a0a-105">DefinedSize property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e1a0a-106">master</span><span class="sxs-lookup"><span data-stu-id="e1a0a-106">master</span></span>


<span data-ttu-id="e1a0a-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1a0a-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e1a0a-108">[Field](field-object-ado.md) オブジェクトのデータ容量を示します。</span><span class="sxs-lookup"><span data-stu-id="e1a0a-108">Indicates the data capacity of a [Field](field-object-ado.md) object.</span></span>

<span data-ttu-id="e1a0a-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e1a0a-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="e1a0a-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e1a0a-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="e1a0a-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="e1a0a-111">Return value</span></span>
>>>>>>> <span data-ttu-id="e1a0a-112">master</span><span class="sxs-lookup"><span data-stu-id="e1a0a-112">master</span></span>

<span data-ttu-id="e1a0a-113">バイト数でフィールドの定義サイズを反映する長整数型 ( **Long** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="e1a0a-113">Returns a **Long** value that reflects the defined size of a field as a number of bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1a0a-114">解説</span><span class="sxs-lookup"><span data-stu-id="e1a0a-114">Remarks</span></span>

<span data-ttu-id="e1a0a-115">**DefinedSize** プロパティは、 **Field** オブジェクトのデータ容量を調べるために使います。</span><span class="sxs-lookup"><span data-stu-id="e1a0a-115">Use the **DefinedSize** property to determine the data capacity of a **Field** object.</span></span>

<span data-ttu-id="e1a0a-p101">**DefinedSize** プロパティと [ActualSize](actualsize-property-ado.md) プロパティは異なるものです。たとえば、宣言タイプが **adVarChar** で **DefinedSize** プロパティ値が 50 の、1 文字を格納した **Field** オブジェクトがあるとします。このオブジェクトが返す **ActualSize** プロパティ値は、1 文字をバイト数で表した長さです。</span><span class="sxs-lookup"><span data-stu-id="e1a0a-p101">The **DefinedSize** and [ActualSize](actualsize-property-ado.md) properties are different. For example, consider a **Field** object with a declared type of **adVarChar** and a **DefinedSize** property value of 50, containing a single character. The **ActualSize** property value it returns is the length in bytes of the single character.</span></span>

