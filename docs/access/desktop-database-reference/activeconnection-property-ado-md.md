---
<span data-ttu-id="ac75a-101"><<<<<<< ヘッド タイトル: ActiveConnection プロパティ (ADO MD) TOCTitle: ms:assetid の ActiveConnection プロパティ (ADO MD): d09f0f91-5e1d-01ed-4d83-eaf58ff718a2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15) ms:contentKeyID: 48547845 ms.date: 2015/09/18 mtps_バージョン: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ac75a-101"><<<<<<< HEAD title: ActiveConnection Property (ADO MD) TOCTitle: ActiveConnection Property (ADO MD) ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15) ms:contentKeyID: 48547845 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="ac75a-102">ActiveConnection プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ac75a-102">ActiveConnection Property (ADO MD)</span></span>

<span data-ttu-id="ac75a-103">=== タイトル: ActiveConnection プロパティ (ADO MD) TOCTitle: ActiveConnection プロパティ (ADO MD) ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15) ms:contentKeyID: 48547845 ms.date: 2018/10/17 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="ac75a-103">======= title: ActiveConnection property (ADO MD) TOCTitle: ActiveConnection property (ADO MD) ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15) ms:contentKeyID: 48547845 ms.date: 10/17/2018 mtps_version: v=office.15</span></span>
---

# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="ac75a-104">ActiveConnection プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ac75a-104">ActiveConnection property (ADO MD)</span></span>
>>>>>>> <span data-ttu-id="ac75a-105">master</span><span class="sxs-lookup"><span data-stu-id="ac75a-105">master</span></span>

<span data-ttu-id="ac75a-106">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac75a-106">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ac75a-107">現在のセルセットまたはカタログが、現在どの ADO [Connection](connection-object-ado.md) オブジェクトに属しているのかを示します。</span><span class="sxs-lookup"><span data-stu-id="ac75a-107">Indicates to which ADO [Connection](connection-object-ado.md) object the current cellset or catalog currently belongs.</span></span>

<span data-ttu-id="ac75a-108"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="ac75a-108"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="ac75a-109">設定値と戻り値</span><span class="sxs-lookup"><span data-stu-id="ac75a-109">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="ac75a-110">設定値および戻り値</span><span class="sxs-lookup"><span data-stu-id="ac75a-110">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="ac75a-111">master</span><span class="sxs-lookup"><span data-stu-id="ac75a-111">master</span></span>

<span data-ttu-id="ac75a-p101">接続を定義する文字列、または **Connection** オブジェクトを含むバリアント型 ( **Variant** ) を設定または取得します。既定値は Empty 値です。</span><span class="sxs-lookup"><span data-stu-id="ac75a-p101">Sets or returns a **Variant** that contains a string defining a connection or **Connection** object. The default is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac75a-114">解説</span><span class="sxs-lookup"><span data-stu-id="ac75a-114">Remarks</span></span>

<span data-ttu-id="ac75a-p102">このプロパティには、有効な ADO **Connection** オブジェクト、または有効な接続文字列を設定します。接続文字列を設定すると、この定義を使用した新規の **Connection** オブジェクトがプロバイダーによって作成され、接続が開かれます。</span><span class="sxs-lookup"><span data-stu-id="ac75a-p102">You can set this property to a valid ADO **Connection** object or to a valid connection string. When this property is set to a connection string, the provider creates a new **Connection** object using this definition and opens the connection.</span></span>

<span data-ttu-id="ac75a-117">**Open** メソッドの [ActiveConnection](open-method-ado-md.md) 引数を使用して [Cellset](cellset-object-ado-md.md) オブジェクトを開くと、引数の値が **ActiveConnection** プロパティに継承されます。</span><span class="sxs-lookup"><span data-stu-id="ac75a-117">If you use the **ActiveConnection** argument of the [Open](open-method-ado-md.md) method to open a [Cellset](cellset-object-ado-md.md) object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="ac75a-p103">**Catalog** オブジェクトの [ActiveConnection](catalog-object-ado-md.md) プロパティを **Nothing** に設定すると、 [CubeDefs](cubedefs-collection-ado-md.md) コレクションおよび関連付けられたすべての [Dimension](dimension-object-ado-md.md)、[Hierarchy](hierarchy-object-ado-md.md)、[Level](level-object-ado-md.md)、および [Member](member-object-ado-md.md) オブジェクトを含む、関連付けられたデータが解放されます。 **Catalog** を開くために使用した **Connection** オブジェクトを閉じると、 **ActiveConnection** プロパティを **Nothing** に設定した場合と同じ効果があります。</span><span class="sxs-lookup"><span data-stu-id="ac75a-p103">Setting the **ActiveConnection** property of a [Catalog](catalog-object-ado-md.md) object to **Nothing** releases the associated data, including data in the [CubeDefs](cubedefs-collection-ado-md.md) collection and any related [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md) objects. Closing a **Connection** object that was used to open a **Catalog** has the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

<span data-ttu-id="ac75a-120">**Catalog** オブジェクトの **ActiveConnection** プロパティによって参照されている接続の既定のデータベースを変更すると、 **Catalog** の内容が無効になります。</span><span class="sxs-lookup"><span data-stu-id="ac75a-120">Changing the default database of the connection referenced by the **ActiveConnection** property of a **Catalog** object invalidates the contents of the **Catalog**.</span></span>

<span data-ttu-id="ac75a-121">開いている **Cellset** オブジェクトの **ActiveConnection** プロパティを変更しようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="ac75a-121">An error will occur if you attempt to change the **ActiveConnection** property for an open **Cellset** object.</span></span>

<span data-ttu-id="ac75a-122"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="ac75a-122"><<<<<<< HEAD</span></span>

> [!NOTE]
> <P><span data-ttu-id="ac75a-p104">[!メモ] Visual Basic では、 <STRONG>ActiveConnection</STRONG> プロパティを <STRONG>Connection</STRONG> オブジェクトに設定する場合、必ず <STRONG>Set</STRONG> キーワードを使用してください。 <STRONG>Set</STRONG> キーワードを省略すると、 <STRONG>ActiveConnection</STRONG> プロパティに、実際には、 <STRONG>Connection</STRONG> オブジェクトの既定のプロパティである <STRONG>ConnectionString</STRONG> と同じものを設定していることになります。このコードは動作しますが、データ ソースへの追加の接続が作成されるため、パフォーマンスに悪い影響を与えることがあります。</span><span class="sxs-lookup"><span data-stu-id="ac75a-p104">In Visual Basic, remember to use the <STRONG>Set</STRONG> keyword when setting the <STRONG>ActiveConnection</STRONG> property to a <STRONG>Connection</STRONG> object. If you omit the <STRONG>Set</STRONG> keyword, you will actually be setting the <STRONG>ActiveConnection</STRONG> property equal to the <STRONG>Connection</STRONG> object's default property, <STRONG>ConnectionString</STRONG>. The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span></P>


=======
> [!NOTE]
> <span data-ttu-id="ac75a-p105">[!メモ] Visual Basic では、 **ActiveConnection** プロパティを **Connection** オブジェクトに設定する場合、必ず **Set** キーワードを使用してください。 **Set** キーワードを省略すると、 **ActiveConnection** プロパティに、実際には、 **Connection** オブジェクトの既定のプロパティである **ConnectionString** と同じものを設定していることになります。このコードは動作しますが、データ ソースへの追加の接続が作成されるため、パフォーマンスに悪い影響を与えることがあります。</span><span class="sxs-lookup"><span data-stu-id="ac75a-p105">In Visual Basic, remember to use the **Set** keyword when setting the **ActiveConnection** property to a **Connection** object. If you omit the **Set** keyword, you will actually be setting the **ActiveConnection** property equal to the **Connection** object's default property, **ConnectionString**. The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span>
>>>>>>> <span data-ttu-id="ac75a-129">master</span><span class="sxs-lookup"><span data-stu-id="ac75a-129">master</span></span>

<span data-ttu-id="ac75a-p106">MSOLAP データ プロバイダーを使用する場合、接続文字列内でデータ ソースをサーバー名に設定し、初期カタログにデータ ソースのカタログの名前を設定します。サーバーに接続されていないキューブ ファイルに接続するには、その .CUB ファイルのある場所へのフル パスを設定します。どちらの場合でも、プロバイダーにはプロバイダー名を設定します。たとえば、次の文字列を設定すると、MSOLAP プロバイダーを使用して Servername という名前のサーバーにある Bobs Video Store という名前のカタログに接続されます。</span><span class="sxs-lookup"><span data-stu-id="ac75a-p106">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source. To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file. In either case, set the provider to the provider name. For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:</span></span>

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

<span data-ttu-id="ac75a-134">次の文字列は、c: の場所にローカル キューブ ファイルに接続する\\MSDASDK\\のサンプル\\ole db\\olap\\データ\\bobsvid.cub。</span><span class="sxs-lookup"><span data-stu-id="ac75a-134">The following string connects to a local cube file at the location C:\\MSDASDK\\samples\\oledb\\olap\\data\\bobsvid.cub:</span></span>

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

