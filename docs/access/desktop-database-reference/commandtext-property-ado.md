---
<span data-ttu-id="00239-101"><<<<<<< ヘッド タイトル: CommandText プロパティ (ADO) TOCTitle: CommandText プロパティ (ADO) === タイトル: CommandText プロパティ (ADO) TOCTitle: CommandText プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="00239-101"><<<<<<< HEAD title: CommandText Property (ADO) TOCTitle: CommandText Property (ADO) ======= title: CommandText property (ADO) TOCTitle: CommandText property (ADO)</span></span>
>>>>>>> <span data-ttu-id="00239-102">マスターの ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15) ms:contentKeyID: 48543234 ms.date: 2015/09/18 mtps_version: v=office.15 f1_keywords:</span><span class="sxs-lookup"><span data-stu-id="00239-102">master ms:assetid: 0debec1c-068f-0aea-fce8-e61aa39c5907 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248859(v=office.15) ms:contentKeyID: 48543234 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="00239-103">ado210.chm1231123 f1_categories。</span><span class="sxs-lookup"><span data-stu-id="00239-103">ado210.chm1231123 f1_categories:</span></span>
- <span data-ttu-id="00239-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="00239-104">Office.Version=v15</span></span>
---

<span data-ttu-id="00239-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="00239-105"><<<<<<< HEAD</span></span>
# <a name="commandtext-property-ado"></a><span data-ttu-id="00239-106">CommandText プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="00239-106">CommandText Property (ADO)</span></span>
=======
# <a name="commandtext-property-ado"></a><span data-ttu-id="00239-107">CommandText プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="00239-107">CommandText property (ADO)</span></span>
>>>>>>> <span data-ttu-id="00239-108">master</span><span class="sxs-lookup"><span data-stu-id="00239-108">master</span></span>


<span data-ttu-id="00239-109">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="00239-109">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="00239-110">プロバイダーに対して発行するコマンド文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="00239-110">Indicates the text of a command to be issued against a provider.</span></span>

<span data-ttu-id="00239-111"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="00239-111"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="00239-112">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="00239-112">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="00239-113">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="00239-113">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="00239-114">master</span><span class="sxs-lookup"><span data-stu-id="00239-114">master</span></span>

<span data-ttu-id="00239-p101">SQL ステートメント、テーブル名、相対 URL、またはストアド プロシージャの呼び出しなど、プロバイダーのコマンドを含む文字列型 ( **String** ) の値を設定または取得します。既定値は "" (長さ 0 の文字列) です。</span><span class="sxs-lookup"><span data-stu-id="00239-p101">Sets or returns a **String** value that contains a provider command, such as an SQL statement, a table name, a relative URL, or a stored procedure call. Default is "" (zero-length string).</span></span>

## <a name="remarks"></a><span data-ttu-id="00239-117">解説</span><span class="sxs-lookup"><span data-stu-id="00239-117">Remarks</span></span>

<span data-ttu-id="00239-p102">**Command** オブジェクトで表されるコマンド テキストを設定または取得するには、 [CommandText](command-object-ado.md) プロパティを使用します。通常は SQL ステートメントを使いますが、ストアド プロシージャの呼び出しなど、プロバイダーが認識する、他の種類のコマンド ステートメントでもかまいません。SQL ステートメントは、特定の文法またはプロバイダーのクエリ プロセッサがサポートするバージョンである必要があります。</span><span class="sxs-lookup"><span data-stu-id="00239-p102">Use the **CommandText** property to set or return the text of a command represented by a [Command](command-object-ado.md) object. Usually this will be an SQL statement, but can also be any other type of command statement recognized by the provider, such as a stored procedure call. An SQL statement must be of the particular dialect or version supported by the provider's query processor.</span></span>

<span data-ttu-id="00239-121"><<<<<<< **Command**オブジェクトの[Prepared](prepared-property-ado.md)プロパティが**True**に設定されている場合はヘッド、 **CommandText**プロパティを設定するときに、接続を開く**コマンド**オブジェクトがバインドされていると、ADO クエリ (の準備プロバイダーによって格納されているクエリのコンパイルされた形式では、) [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))や**Open**メソッドを呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="00239-121"><<<<<<< HEAD If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) or **Open** methods.</span></span>
<span data-ttu-id="00239-122">=== ADO クエリを準備場合は、 **Command**オブジェクトの[Prepared](prepared-property-ado.md)プロパティが**True**に設定し、**コマンド**オブジェクトの**CommandText**プロパティを設定すると、開かれた接続をバインド、(コンパイル済みのフォームは、プロバイダーによって格納されているクエリ) [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)や**Open**メソッドを呼び出すとします。</span><span class="sxs-lookup"><span data-stu-id="00239-122">======= If the [Prepared](prepared-property-ado.md) property of the **Command** object is set to **True** and the **Command** object is bound to an open connection when you set the **CommandText** property, ADO prepares the query (that is, a compiled form of the query that is stored by the provider) when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) or **Open** methods.</span></span>
>>>>>>> <span data-ttu-id="00239-123">master</span><span class="sxs-lookup"><span data-stu-id="00239-123">master</span></span>

<span data-ttu-id="00239-p104">[CommandType](commandtype-property-ado.md) プロパティの設定値によっては、 **CommandText** プロパティが変更される場合があります。 **CommandText** プロパティはいつでも読み出すことができ、ADO がコマンド実行中に使う実際のコマンド テキストの参照も可能です。</span><span class="sxs-lookup"><span data-stu-id="00239-p104">Depending on the [CommandType](commandtype-property-ado.md) property setting, ADO may alter the **CommandText** property. You can read the **CommandText** property at any time to see the actual command text that ADO will use during execution.</span></span>

<span data-ttu-id="00239-p105">ファイルやディレクトリなどのリソースを指定する相対 URL を設定したり取得したりするには、 **CommandText** プロパティを使います。リソースは、絶対 URL で明示的に指定された位置や、開かれた [Connection](connection-object-ado.md) オブジェクトで暗黙的に指定された位置に対して相対的です。</span><span class="sxs-lookup"><span data-stu-id="00239-p105">Use the **CommandText** property to set or return a relative URL that specifies a resource, such as a file or directory. The resource is relative to a location specified explicitly by an absolute URL, or implicitly by an open [Connection](connection-object-ado.md) object.</span></span>


> [!NOTE]
<span data-ttu-id="00239-128"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="00239-128"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="00239-p106">[!メモ] http 体系を使用している URL は、<A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A> を自動的に呼び出します。詳細については、「 <A href="absolute-and-relative-urls.md">絶対 URL と相対 URL</A>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00239-p106">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>. For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="00239-131">[!メモ] http 体系を使用している URL は、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="00239-131">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="00239-132">詳細については、[絶対と相対 Url](absolute-and-relative-urls.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00239-132">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="00239-133">master</span><span class="sxs-lookup"><span data-stu-id="00239-133">master</span></span>


