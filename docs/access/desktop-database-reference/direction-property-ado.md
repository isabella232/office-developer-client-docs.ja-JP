---
<span data-ttu-id="42765-101"><<<<<<< ヘッド タイトル: 方向プロパティ (ADO) TOCTitle: 方向プロパティ (ADO) === タイトル: Direction プロパティ (ADO) TOCTitle: Direction プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="42765-101"><<<<<<< HEAD title: Direction Property (ADO) TOCTitle: Direction Property (ADO) ======= title: Direction property (ADO) TOCTitle: Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="42765-102">マスターの ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="42765-102">master ms:assetid: 51a94abb-7ce9-9adb-2b76-5391eb9f6863 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249262(v=office.15) ms:contentKeyID: 48544823 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="42765-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="42765-103"><<<<<<< HEAD</span></span>
# <a name="direction-property-ado"></a><span data-ttu-id="42765-104">Direction プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="42765-104">Direction Property (ADO)</span></span>
=======
# <a name="direction-property-ado"></a><span data-ttu-id="42765-105">Direction プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="42765-105">Direction property (ADO)</span></span>
>>>>>>> <span data-ttu-id="42765-106">master</span><span class="sxs-lookup"><span data-stu-id="42765-106">master</span></span>


<span data-ttu-id="42765-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="42765-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="42765-108">[Parameter](parameter-object-ado.md) が、入力パラメーター、出力パラメーター、または入出力両方のパラメーターを表しているか、あるいは、ストアド プロシージャからの戻り値であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="42765-108">Indicates whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, an input and an output parameter, or if the parameter is the return value from a stored procedure.</span></span>

<span data-ttu-id="42765-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="42765-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="42765-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="42765-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="42765-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="42765-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="42765-112">master</span><span class="sxs-lookup"><span data-stu-id="42765-112">master</span></span>

<span data-ttu-id="42765-113">[ParameterDirectionEnum](parameterdirectionenum.md) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="42765-113">Sets or returns a [ParameterDirectionEnum](parameterdirectionenum.md) value.</span></span>

## <a name="remarks"></a><span data-ttu-id="42765-114">解説</span><span class="sxs-lookup"><span data-stu-id="42765-114">Remarks</span></span>

<span data-ttu-id="42765-p101">**Direction** プロパティは、プロシージャとのパラメーターのやり取りの方法を指定するために使います。 **Direction** プロパティは読み取り/書き込み可能になっています。これにより、パラメーター情報を取得するために ADO がそれ以上プロバイダーを呼び出さないようにする場合に、この情報を設定したり、この情報を返さないプロバイダーを操作したりできます。</span><span class="sxs-lookup"><span data-stu-id="42765-p101">Use the **Direction** property to specify how a parameter is passed to or from a procedure. The **Direction** property is read/write; this allows you to work with providers that don't return this information or to set this information when you don't want ADO to make an extra call to the provider to retrieve parameter information.</span></span>

<span data-ttu-id="42765-p102">プロバイダーの中には、ストアド プロシージャのパラメーターの入出力の方向を確認できないものがあります。その場合は、クエリを実行する前に **Direction** プロパティを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42765-p102">Not all providers can determine the direction of parameters in their stored procedures. In these cases, you must set the **Direction** property before you execute the query.</span></span>

