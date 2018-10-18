---
<span data-ttu-id="d46b5-101"><<<<<<< ヘッド タイトル: ConnectionString プロパティ (ADO) TOCTitle: ConnectionString プロパティ (ADO) === タイトル: ConnectionString プロパティ (ADO) TOCTitle: ConnectionString プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d46b5-101"><<<<<<< HEAD title: ConnectionString Property (ADO) TOCTitle: ConnectionString Property (ADO) ======= title: ConnectionString property (ADO) TOCTitle: ConnectionString property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d46b5-102">マスターの ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15) ms:contentKeyID: 48547627 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="d46b5-102">master ms:assetid: c67a7daf-258f-d99d-6475-a4aa98d1e99d ms:mtpsurl: https://msdn.microsoft.com/library/JJ249968(v=office.15) ms:contentKeyID: 48547627 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="d46b5-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d46b5-103"><<<<<<< HEAD</span></span>
# <a name="connectionstring-property-ado"></a><span data-ttu-id="d46b5-104">ConnectionString プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d46b5-104">ConnectionString Property (ADO)</span></span>
=======
# <a name="connectionstring-property-ado"></a><span data-ttu-id="d46b5-105">ConnectionString プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="d46b5-105">ConnectionString property (ADO)</span></span>
>>>>>>> <span data-ttu-id="d46b5-106">master</span><span class="sxs-lookup"><span data-stu-id="d46b5-106">master</span></span>


<span data-ttu-id="d46b5-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="d46b5-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="d46b5-108">データ ソースとの接続を確立するために使用される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-108">Indicates the information used to establish a connection to a data source.</span></span>

<span data-ttu-id="d46b5-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="d46b5-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="d46b5-110">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="d46b5-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="d46b5-111">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="d46b5-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="d46b5-112">master</span><span class="sxs-lookup"><span data-stu-id="d46b5-112">master</span></span>

<span data-ttu-id="d46b5-113">文字列型 ( **String** ) の値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-113">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d46b5-114">解説</span><span class="sxs-lookup"><span data-stu-id="d46b5-114">Remarks</span></span>

<span data-ttu-id="d46b5-115">**ConnectionString**プロパティを使用すると、一連のセミコロンで区切られた*引数\*\*の値を =* ステートメントを含む詳細な接続文字列を渡すことによってデータ ソースを指定します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-115">Use the **ConnectionString** property to specify a data source by passing a detailed connection string containing a series of *argument* *= value* statements separated by semicolons.</span></span>

<span data-ttu-id="d46b5-p101">ADO では、 **ConnectionString** プロパティに対して 5 種類の引数がサポートされます。その他の引数は ADO で処理されずに直接プロバイダーに渡されます。ADO でサポートされる引数を次に示します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-p101">ADO supports five arguments for the **ConnectionString** property; any other arguments pass directly to the provider without any processing by ADO. The arguments ADO supports are as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d46b5-118">引数</span><span class="sxs-lookup"><span data-stu-id="d46b5-118">Argument</span></span></p></th>
<th><p><span data-ttu-id="d46b5-119">説明</span><span class="sxs-lookup"><span data-stu-id="d46b5-119">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d46b5-120"><em>Provider=</em></span><span class="sxs-lookup"><span data-stu-id="d46b5-120"><em>Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="d46b5-121">接続に使用するプロバイダーの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-121">Specifies the name of a provider to use for the connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46b5-122"><em>ファイル名 =</em></span><span class="sxs-lookup"><span data-stu-id="d46b5-122"><em>File Name=</em></span></span></p></td>
<td><p><span data-ttu-id="d46b5-123">設定済みの接続情報を格納したプロバイダー固有のファイル (たとえば、持続的なデータ ソース オブジェクト) の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-123">Specifies the name of a provider-specific file (for example, a persisted data source object) containing preset connection information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46b5-124"><em>リモート プロバイダー =</em></span><span class="sxs-lookup"><span data-stu-id="d46b5-124"><em>Remote Provider=</em></span></span></p></td>
<td><p><span data-ttu-id="d46b5-p102">クライアント側の接続を開くときに使用するプロバイダーの名前を指定します (Remote Data Service のみ)。</span><span class="sxs-lookup"><span data-stu-id="d46b5-p102">Specifies the name of a provider to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46b5-127"><em>リモート サーバー =</em></span><span class="sxs-lookup"><span data-stu-id="d46b5-127"><em>Remote Server=</em></span></span></p></td>
<td><p><span data-ttu-id="d46b5-p103">クライアント側の接続を開くときに使用するサーバーのパス名を指定します (リモート データ サービスのみ)。</span><span class="sxs-lookup"><span data-stu-id="d46b5-p103">Specifies the path name of the server to use when opening a client-side connection. (Remote Data Service only.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46b5-130"><em>URL=</em></span><span class="sxs-lookup"><span data-stu-id="d46b5-130"><em>URL=</em></span></span></p></td>
<td><p><span data-ttu-id="d46b5-131">接続文字列を、ファイルやディレクトリなどのリソースを識別する絶対 URL として指定します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-131">Specifies the connection string as an absolute URL identifying a resource, such as a file or directory.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d46b5-132">**ConnectionString** プロパティを設定して [Connection](connection-object-ado.md) オブジェクトを開いた後、ADO によって定義された引数名がプロバイダーの対応する引数名にマップされるなど、プロバイダーによってプロパティの内容が変更される場合があります。</span><span class="sxs-lookup"><span data-stu-id="d46b5-132">After you set the **ConnectionString** property and open the [Connection](connection-object-ado.md) object, the provider may alter the contents of the property, for example, by mapping the ADO-defined argument names to their provider equivalents.</span></span>

<span data-ttu-id="d46b5-133">**ConnectionString**プロパティは、 **Open**メソッドの呼び出し中に、現在の**接続文字列**プロパティをオーバーライドするために、 [Open](open-method-ado-connection.md)メソッドの*ConnectionString*引数に対して使用する値を自動的に継承します。</span><span class="sxs-lookup"><span data-stu-id="d46b5-133">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument of the [Open](open-method-ado-connection.md) method, so you can override the current **ConnectionString** property during the **Open** method call.</span></span>

<span data-ttu-id="d46b5-134">*ファイル名*引数には、関連付けられているプロバイダーをロードするのには ADO が発生するため、*プロバイダー*と*ファイル名*の両方の引数を渡すことはできません。</span><span class="sxs-lookup"><span data-stu-id="d46b5-134">Because the *File Name* argument causes ADO to load the associated provider, you cannot pass both the *Provider* and *File Name* arguments.</span></span>

<span data-ttu-id="d46b5-135">**ConnectionString** プロパティは、接続が閉じているときは読み取り/書き込み可能で、開いているときは読み取り専用になります。</span><span class="sxs-lookup"><span data-stu-id="d46b5-135">The **ConnectionString** property is read/write when the connection is closed and read-only when it is open.</span></span>

<span data-ttu-id="d46b5-p104">**ConnectionString** プロパティにおいて重複している引数は無視されます。引数の最後のインスタンスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="d46b5-p104">Duplicates of an argument in the **ConnectionString** property are ignored. The last instance of any argument is used.</span></span>

<span data-ttu-id="d46b5-138">**リモート データ サービスの使用法**使用すると、クライアント側の**Connection**オブジェクトの**ConnectionString**プロパティは*リモート プロバイダー*と*リモート サーバー*のパラメーターのみを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="d46b5-138">**Remote Data Service Usage**When used on a client-side **Connection** object, the **ConnectionString** property can include only the *Remote Provider* and *Remote Server* parameters.</span></span>

