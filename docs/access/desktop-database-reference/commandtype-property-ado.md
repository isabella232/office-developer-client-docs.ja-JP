---
<span data-ttu-id="aa086-101"><<<<<<< ヘッド タイトル: CommandType プロパティ (ADO) TOCTitle: CommandType プロパティ (ADO) === タイトル: CommandType プロパティ (ADO) TOCTitle: CommandType プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="aa086-101"><<<<<<< HEAD title: CommandType Property (ADO) TOCTitle: CommandType Property (ADO) ======= title: CommandType property (ADO) TOCTitle: CommandType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aa086-102">マスターの ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15) ms:contentKeyID: 48547663 ms.date: 2015/09/18 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="aa086-102">master ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15) ms:contentKeyID: 48547663 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="aa086-103">ado210.chm1231125 f1_categories。</span><span class="sxs-lookup"><span data-stu-id="aa086-103">ado210.chm1231125 f1_categories:</span></span>
- <span data-ttu-id="aa086-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="aa086-104">Office.Version=v15</span></span>
---

<span data-ttu-id="aa086-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="aa086-105"><<<<<<< HEAD</span></span>
# <a name="commandtype-property-ado"></a><span data-ttu-id="aa086-106">CommandType プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="aa086-106">CommandType Property (ADO)</span></span>
=======
# <a name="commandtype-property-ado"></a><span data-ttu-id="aa086-107">CommandType プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="aa086-107">CommandType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="aa086-108">master</span><span class="sxs-lookup"><span data-stu-id="aa086-108">master</span></span>


<span data-ttu-id="aa086-109">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa086-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aa086-110">[Command](command-object-ado.md) オブジェクトの型を示します。</span><span class="sxs-lookup"><span data-stu-id="aa086-110">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

<span data-ttu-id="aa086-111"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="aa086-111"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="aa086-112">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="aa086-112">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="aa086-113">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="aa086-113">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="aa086-114">master</span><span class="sxs-lookup"><span data-stu-id="aa086-114">master</span></span>

<span data-ttu-id="aa086-115">1 つまたは複数の [CommandTypeEnum](commandtypeenum.md) 値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="aa086-115">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>


> [!NOTE]
> <P><span data-ttu-id="aa086-p101">[!メモ] <STRONG>CommandType</STRONG> では、 <STRONG>adCmdFile</STRONG> または <STRONG>adCmdTableDirect</STRONG> の <STRONG>CommandTypeEnum</STRONG> 値を使用しないでください。これらの値は、 <A href="open-method-ado-recordset.md">Recordset</A> の <A href="requery-method-ado.md">Open</A> メソッドと <A href="recordset-object-ado.md">Requery</A> メソッドのオプションとしてのみ使用することができます。</span><span class="sxs-lookup"><span data-stu-id="aa086-p101">Do not use the <STRONG>CommandTypeEnum</STRONG> values of <STRONG>adCmdFile</STRONG> or <STRONG>adCmdTableDirect</STRONG> with <STRONG>CommandType</STRONG>. These values can only be used as options with the <A href="open-method-ado-recordset.md">Open</A> and <A href="requery-method-ado.md">Requery</A> methods of a <A href="recordset-object-ado.md">Recordset</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="aa086-118">解説</span><span class="sxs-lookup"><span data-stu-id="aa086-118">Remarks</span></span>

<span data-ttu-id="aa086-119">**CommandType** プロパティは、 [CommandText](commandtext-property-ado.md) プロパティの評価を最適化するために使用します。</span><span class="sxs-lookup"><span data-stu-id="aa086-119">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="aa086-120"><<<<<<< ヘッド場合は、 **CommandType**プロパティの値が**adCmdUnknown** (既定値) に等しい、ADO は、プロバイダーにするかどうかの呼び出しを行う必要があるためパフォーマンスが低下が発生する可能性があります**CommandText**プロパティでは、SQL ステートメント、ストアド プロシージャ、またはテーブル名です。</span><span class="sxs-lookup"><span data-stu-id="aa086-120"><<<<<<< HEAD If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name.</span></span> <span data-ttu-id="aa086-121">**CommandType**プロパティを設定を使用するコマンドの種類がわかっている場合は、関連するコードに直接移動するのには ADO に指示します。</span><span class="sxs-lookup"><span data-stu-id="aa086-121">If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code.</span></span> <span data-ttu-id="aa086-122">**CommandType**プロパティが**CommandText**プロパティのコマンドの種類に一致しない場合は、 [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))メソッドを呼び出すときにエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="aa086-122">If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>
<span data-ttu-id="aa086-123">=== ADO は、 **CommandText**プロパティが SQL ステートメントでは、かどうかを判断するのには、プロバイダーへの呼び出しを行う必要があるためパフォーマンスが低下が発生する可能性があります場合は、 **CommandType**プロパティの値が**adCmdUnknown** (既定値) をストアド プロシージャ、またはテーブル名です。</span><span class="sxs-lookup"><span data-stu-id="aa086-123">======= If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name.</span></span> <span data-ttu-id="aa086-124">**CommandType**プロパティを設定を使用するコマンドの種類がわかっている場合は、関連するコードに直接移動するのには ADO に指示します。</span><span class="sxs-lookup"><span data-stu-id="aa086-124">If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code.</span></span> <span data-ttu-id="aa086-125">**CommandType**プロパティが**CommandText**プロパティのコマンドの種類に一致しない場合は、 [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)メソッドを呼び出すときにエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="aa086-125">If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>
>>>>>>> <span data-ttu-id="aa086-126">master</span><span class="sxs-lookup"><span data-stu-id="aa086-126">master</span></span>

