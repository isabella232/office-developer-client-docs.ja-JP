---
<span data-ttu-id="e7e0e-101"><<<<<<< ヘッド タイトル: ParentURL プロパティ (ADO) TOCTitle: ParentURL プロパティ (ADO) === タイトル: ParentURL プロパティ (ADO) TOCTitle: ParentURL プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-101"><<<<<<< HEAD title: ParentURL Property (ADO) TOCTitle: ParentURL Property (ADO) ======= title: ParentURL property (ADO) TOCTitle: ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e7e0e-102">マスターの ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: 48548517 ms.date: 2015/09/18 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="e7e0e-102">master ms:assetid: ec7ec476-6f9e-8486-fe02-74995975df5c ms:mtpsurl: https://msdn.microsoft.com/library/JJ250200(v=office.15) ms:contentKeyID: 48548517 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e7e0e-103"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e7e0e-103"><<<<<<< HEAD</span></span>
# <a name="parenturl-property-ado"></a><span data-ttu-id="e7e0e-104">ParentURL プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-104">ParentURL Property (ADO)</span></span>
=======
# <a name="parenturl-property-ado"></a><span data-ttu-id="e7e0e-105">ParentURL プロパティ (ADO)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-105">ParentURL property (ADO)</span></span>
>>>>>>> <span data-ttu-id="e7e0e-106">master</span><span class="sxs-lookup"><span data-stu-id="e7e0e-106">master</span></span>

<span data-ttu-id="e7e0e-107">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7e0e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e7e0e-108">現在の [Record](record-object-ado.md) オブジェクトの親 **Record** を示す絶対 URL 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-108">Indicates an absolute URL string that points to the parent [Record](record-object-ado.md) of the current **Record** object.</span></span>

<span data-ttu-id="e7e0e-109"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e7e0e-109"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="e7e0e-110">戻り値</span><span class="sxs-lookup"><span data-stu-id="e7e0e-110">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="e7e0e-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="e7e0e-111">Return value</span></span>
>>>>>>> <span data-ttu-id="e7e0e-112">master</span><span class="sxs-lookup"><span data-stu-id="e7e0e-112">master</span></span>

<span data-ttu-id="e7e0e-113">親 **Record** の URL を示す文字列型 ( **String** ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-113">Returns a **String** value that indicates the URL of the parent **Record**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7e0e-114">解説</span><span class="sxs-lookup"><span data-stu-id="e7e0e-114">Remarks</span></span>

<span data-ttu-id="e7e0e-p101">**ParentURL** プロパティは、 **Record** オブジェクトを開くために使用されるソースに依存します。たとえば、 **ActiveConnection** プロパティによって参照されるディレクトリの相対パスを含むソースを使用して [Record](activeconnection-property-ado.md) を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-p101">The **ParentURL** property depends upon the source used to open the **Record** object. For example, the **Record** may be opened with a source containing a relative path name of a directory referenced by the [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

<span data-ttu-id="e7e0e-p102">ここで、"second" が "first" の下のフォルダーであるとします。 **Record** オブジェクトを開くには、次のようにします。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-p102">Suppose "second" is a folder contained under "first". Open the **Record** object with the following:</span></span>

```vb
    record.ActiveConnection = "https://first"
    record.Open "second"
```

<span data-ttu-id="e7e0e-119">**ParentURL**プロパティの値は、 **ParentURL**プロパティは、"https://first"、 **ActiveConnection**と同じです。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-119">Now, the value of the **ParentURL** property is **ParentURL** property is "https://first" , the same as **ActiveConnection**.</span></span>

<span data-ttu-id="e7e0e-120">ソースの絶対 URL を次のように、場合もあります"https://first/second"です。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-120">The source may also be an absolute URL such as, "https://first/second" .</span></span> <span data-ttu-id="e7e0e-121">**ParentURL**プロパティでは、"https://first"、上のレベルです。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-121">The **ParentURL** property is then "https://first" , the level above .</span></span> <span data-ttu-id="e7e0e-122">**ParentURL**プロパティでは、"https://first"、「秒」の上のレベルです。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-122">The **ParentURL** property is then "https://first" , the level above "second" .</span></span>

<span data-ttu-id="e7e0e-123">次のような場合、このプロパティは Null 値になります。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-123">This property may be a null value if:</span></span>

- <span data-ttu-id="e7e0e-124">現在のレコードに親がない場合 ( **Record** オブジェクトがディレクトリのルートを表す場合など)</span><span class="sxs-lookup"><span data-stu-id="e7e0e-124">There is no parent for the current object; for example, if the **Record** object represents the root of a directory.</span></span>

- <span data-ttu-id="e7e0e-125">**Record** オブジェクトが URL で指定できないエンティティである場合</span><span class="sxs-lookup"><span data-stu-id="e7e0e-125">The **Record** object represents an entity that cannot be specified with a URL.</span></span>

<span data-ttu-id="e7e0e-126">このプロパティは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-126">This property is read-only.</span></span>


> [!NOTE]
> - <span data-ttu-id="e7e0e-p104">[!メモ] このプロパティは、[Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) などのドキュメント ソース プロバイダーでのみサポートされます。詳細については、「 [レコードおよびプロバイダー提供のフィールド](records-and-provider-supplied-fields.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-p104">This property is only supported by document source providers, such as the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md). For more information, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>
> - <span data-ttu-id="e7e0e-129">[!メモ] http 体系を使用している URL は、Microsoft OLE DB Provider for Internet Publishing を自動的に呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-129">URLs using the http scheme will automatically invoke the Microsoft OLE DB Provider for Internet Publishing.</span></span> <span data-ttu-id="e7e0e-130">詳細については、「 [絶対 URL と相対 URL](absolute-and-relative-urls.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-130">For more information, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span> 
> - <span data-ttu-id="e7e0e-131">[!メモ] 現在のレコードに ADO **Recordset** のデータ レコードが含まれている場合、 **ParentURL** プロパティにアクセスすると、URL を取得できないことを示す実行時エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e7e0e-131">If the current record contains a data record from an ADO **Recordset**, accessing the **ParentURL** property causes a run-time error, indicating that no URL is possible.</span></span>


