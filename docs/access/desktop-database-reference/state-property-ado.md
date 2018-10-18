---
<span data-ttu-id="58ba8-101"><<<<<<< ヘッド タイトル: 状態プロパティ (ADO) TOCTitle: 状態プロパティ (ADO) === タイトル: State プロパティ (ADO) TOCTitle: State プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="58ba8-101"><<<<<<< HEAD title: State Property (ADO) TOCTitle: State Property (ADO) ======= title: State property (ADO) TOCTitle: State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="58ba8-102">マスターの ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 2015/09/18 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="58ba8-102">master ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15) ms:contentKeyID: 48547053 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="58ba8-103">ado210.chm1231176 f1_categories。</span><span class="sxs-lookup"><span data-stu-id="58ba8-103">ado210.chm1231176 f1_categories:</span></span>
- <span data-ttu-id="58ba8-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="58ba8-104">Office.Version=v15</span></span>
---

<span data-ttu-id="58ba8-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="58ba8-105"><<<<<<< HEAD</span></span>
# <a name="state-property-ado"></a><span data-ttu-id="58ba8-106">State プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="58ba8-106">State Property (ADO)</span></span>
=======
# <a name="state-property-ado"></a><span data-ttu-id="58ba8-107">状態プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="58ba8-107">State property (ADO)</span></span>
>>>>>>> <span data-ttu-id="58ba8-108">master</span><span class="sxs-lookup"><span data-stu-id="58ba8-108">master</span></span>


<span data-ttu-id="58ba8-109">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="58ba8-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="58ba8-110">対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。</span><span class="sxs-lookup"><span data-stu-id="58ba8-110">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="58ba8-111">非同期メソッドを実行する対象になるすべてのオブジェクトについて、オブジェクトの状態が接続、実行、取得のいずれであるかを示します。</span><span class="sxs-lookup"><span data-stu-id="58ba8-111">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

<span data-ttu-id="58ba8-112"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="58ba8-112"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="58ba8-113">戻り値</span><span class="sxs-lookup"><span data-stu-id="58ba8-113">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="58ba8-114">戻り値</span><span class="sxs-lookup"><span data-stu-id="58ba8-114">Return value</span></span>
>>>>>>> <span data-ttu-id="58ba8-115">master</span><span class="sxs-lookup"><span data-stu-id="58ba8-115">master</span></span>

<span data-ttu-id="58ba8-p101">**ObjectStateEnum** の値になる長整数型 ( [Long](objectstateenum.md) ) の値を返します。既定値は **adStateClosed** です。</span><span class="sxs-lookup"><span data-stu-id="58ba8-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="58ba8-118">解説</span><span class="sxs-lookup"><span data-stu-id="58ba8-118">Remarks</span></span>

<span data-ttu-id="58ba8-119">**State** プロパティを使用して、特定のオブジェクトの現在の状態をいつでも調べることができます。</span><span class="sxs-lookup"><span data-stu-id="58ba8-119">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="58ba8-p102">オブジェクトの **State** プロパティは、値の組み合わせになる場合があります。たとえば、ステートメントが実行中である場合、このプロパティの値は **adStateOpen** と **adStateExecuting** の組み合わせになります。</span><span class="sxs-lookup"><span data-stu-id="58ba8-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="58ba8-122">**State** プロパティは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="58ba8-122">The **State** property is read-only.</span></span>

