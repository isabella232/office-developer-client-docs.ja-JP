---
<span data-ttu-id="02be9-101"><<<<<<< ヘッド タイトル: ActiveCommand プロパティ (ADO) TOCTitle: ActiveCommand プロパティ (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 2015/09/18 mtps_version: v =office.15</span><span class="sxs-lookup"><span data-stu-id="02be9-101"><<<<<<< HEAD title: ActiveCommand Property (ADO) TOCTitle: ActiveCommand Property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="02be9-102">ActiveCommand プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="02be9-102">ActiveCommand Property (ADO)</span></span>

<span data-ttu-id="02be9-103">=== タイトル: ActiveCommand プロパティ (ADO) TOCTitle: ActiveCommand プロパティ (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 2018/10/17 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="02be9-103">======= title: ActiveCommand property (ADO) TOCTitle: ActiveCommand property (ADO) ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15) ms:contentKeyID: 48544459 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activecommand-property-ado"></a><span data-ttu-id="02be9-104">ActiveCommand プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="02be9-104">ActiveCommand property (ADO)</span></span>
>>>>>>> <span data-ttu-id="02be9-105">master</span><span class="sxs-lookup"><span data-stu-id="02be9-105">master</span></span>

<span data-ttu-id="02be9-106">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="02be9-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="02be9-107">関連付けられた [Recordset](command-object-ado.md) オブジェクトを作成した [Command](recordset-object-ado.md) オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="02be9-107">Indicates the [Command](command-object-ado.md) object that created the associated [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="02be9-108"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="02be9-108"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="02be9-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="02be9-109">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="02be9-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="02be9-110">Return value</span></span>
>>>>>>> <span data-ttu-id="02be9-111">master</span><span class="sxs-lookup"><span data-stu-id="02be9-111">master</span></span>

<span data-ttu-id="02be9-p101">**Command** オブジェクトが格納されたバリアント型 ( **Variant** ) の値を返します。既定は、Null オブジェクト参照です。</span><span class="sxs-lookup"><span data-stu-id="02be9-p101">Returns a **Variant** that contains a **Command** object. Default is a null object reference.</span></span>

## <a name="remarks"></a><span data-ttu-id="02be9-114">解説</span><span class="sxs-lookup"><span data-stu-id="02be9-114">Remarks</span></span>

<span data-ttu-id="02be9-115">**ActiveCommand** プロパティは、値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="02be9-115">The **ActiveCommand** property is read-only.</span></span>

<span data-ttu-id="02be9-116"><<<<<<< ヘッド場合は、**コマンド**オブジェクトに使用しなかった、現在の**レコード セット**を作成し、 **Null**オブジェクト参照が返されます。</span><span class="sxs-lookup"><span data-stu-id="02be9-116"><<<<<<< HEAD If a **Command** object was not used to create the current **Recordset**, then a **Null** object reference is returned.</span></span>
<span data-ttu-id="02be9-117">=== 現在の**レコード セット**を作成する**コマンド**オブジェクトが使用できない場合は、 **Null**オブジェクト参照が返されます。</span><span class="sxs-lookup"><span data-stu-id="02be9-117">======= If a **Command** object was not used to create the current **Recordset**, a **Null** object reference is returned.</span></span>
>>>>>>> <span data-ttu-id="02be9-118">master</span><span class="sxs-lookup"><span data-stu-id="02be9-118">master</span></span>

<span data-ttu-id="02be9-119">このプロパティは、作成された **Recordset** オブジェクトのみが与えられていて、関連付けられている **Command** オブジェクトを取得したい場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="02be9-119">Use this property to find the associated **Command** object when you are given only the resulting **Recordset** object.</span></span>

