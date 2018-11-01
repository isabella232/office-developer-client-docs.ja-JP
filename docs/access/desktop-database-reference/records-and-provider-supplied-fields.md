---
title: レコードおよびプロバイダー提供のフィールド
TOCTitle: Records and Provider-Supplied Fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: cf0e13569e902cd8665cd2a023ba1707d63f51a6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887461"
---
# <a name="records-and-provider-supplied-fields"></a><span data-ttu-id="7120e-102">レコードおよびプロバイダー提供のフィールド</span><span class="sxs-lookup"><span data-stu-id="7120e-102">Records and Provider-Supplied Fields</span></span>


<span data-ttu-id="7120e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="7120e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7120e-104">[Record](record-object-ado.md) オブジェクトが開かれると、そのソースは、開かれた [Connection](recordset-object-ado.md) オブジェクトと共に動作する、開かれた [Recordset](connection-object-ado.md) のカレント行、絶対 URL、または相対 URL になることができます。</span><span class="sxs-lookup"><span data-stu-id="7120e-104">When a [Record](record-object-ado.md) object is opened, its source can be the current row of an open [Recordset](recordset-object-ado.md), an absolute URL, or a relative URL in conjunction with an open [Connection](connection-object-ado.md) object.</span></span>

<span data-ttu-id="7120e-105">**Record** が **Recordset** から開かれる場合は、 **Record** オブジェクトの [Fields](fields-collection-ado.md) コレクションには、 **Recordset** からのすべてのフィールドに加えて、基になるプロバイダーによって追加されたフィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="7120e-105">If the **Record** is opened from a **Recordset**, the **Record** object [Fields](fields-collection-ado.md) collection will contain all the fields from the **Recordset**, plus any fields added by the underlying provider.</span></span>

<span data-ttu-id="7120e-p101">プロバイダーは、 **Record** の補完機能として作用する追加フィールドを挿入することができます。その結果、 **Record** には、 **Recordset** 全体、または **Recordset** の別の行から派生した **Record** にはない固有のフィールドが存在するようになります。</span><span class="sxs-lookup"><span data-stu-id="7120e-p101">The provider may insert additional fields that serve as supplementary characteristics of the **Record**. As a result, a **Record** may have unique fields not in the **Recordset** as a whole or any **Record** derived from another row of the **Recordset**.</span></span>

<span data-ttu-id="7120e-108">などの電子メールのデータ ソースから派生した**レコード セット**のすべての行からとして、このような列がある、および、件名します。</span><span class="sxs-lookup"><span data-stu-id="7120e-108">For example, all rows of a **Recordset** derived from an e-mail data source might have columns such as From, To, and Subject.</span></span> <span data-ttu-id="7120e-109">**レコード**は、**レコード セット**が同じフィールドを持つことから派生します。</span><span class="sxs-lookup"><span data-stu-id="7120e-109">A **Record** derived from that **Recordset** will have the same fields.</span></span> <span data-ttu-id="7120e-110">ただし、**レコード**には、その**レコード**の添付ファイル] と [Cc (カーボン コピー) などで表される特定のメッセージに固有の他のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="7120e-110">However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).</span></span>

<span data-ttu-id="7120e-111">**Record** オブジェクトと **Recordset** オブジェクトのカレント行には同じフィールドがありますが、 **Record** オブジェクトと **Recordset** オブジェクトには異なるメソッドとプロパティがあるので、この 2 つは別のものです。</span><span class="sxs-lookup"><span data-stu-id="7120e-111">Although the **Record** object and current row of the **Recordset** have the same fields, they are different because **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="7120e-p103">**Record** オブジェクトと **Recordset** オブジェクトに共通して存在しているフィールドは、いずれかのオブジェクトで変更することができます。ただし、基になるプロバイダーがフィールドを "Null" に設定できたとしても、 **Record** オブジェクトでフィールドを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="7120e-p103">A field held in common by the **Record** and **Recordset** can be modified on either object. However, the field cannot be deleted on the **Record** object, although the underlying provider may support setting the field to null.</span></span>

<span data-ttu-id="7120e-p104">**Record** が開かれた後に、プログラムでフィールドを追加することができます。また、追加したフィールドを削除することができますが、元の **Recordset** からフィールドを削除することはできません。</span><span class="sxs-lookup"><span data-stu-id="7120e-p104">After the **Record** is opened, you can programmatically add fields. You can also delete fields you have added, but you cannot delete fields from the original **Recordset**.</span></span>

<span data-ttu-id="7120e-p105">さらに、URL から **Record** オブジェクトを直接開くことができます。この場合、 **Record** に追加されるフィールドは、基になるプロバイダーによって異なります。現在ほとんどのプロバイダーでは、 **Record** で表されるエンティティを記述したフィールドのセットが追加されます。エンティティが単純ファイルなどのバイトのストリームから構成されている場合、通常は [Stream](stream-object-ado.md) オブジェクトを **Record** から開くことができます。</span><span class="sxs-lookup"><span data-stu-id="7120e-p105">You may also open the **Record** object directly from a URL. In this case, the fields added to the **Record** depend on the underlying provider. Currently, most providers add a set of fields that describe the entity represented by the **Record**. If the entity consists of a stream of bytes, such as a simple file, then a [Stream](stream-object-ado.md) object can usually be opened from the **Record**.</span></span>

## <a name="special-fields-for-document-source-providers"></a><span data-ttu-id="7120e-120">ドキュメント ソース プロバイダー用の特殊なフィールド</span><span class="sxs-lookup"><span data-stu-id="7120e-120">Special Fields for Document Source Providers</span></span>

<span data-ttu-id="7120e-121">プロバイダーでは、*ドキュメント ソース プロバイダー*と呼ばれる特別なクラスでは、フォルダーやドキュメントを管理します。</span><span class="sxs-lookup"><span data-stu-id="7120e-121">A special class of providers, called *document source providers*, manages folders and documents.</span></span> <span data-ttu-id="7120e-122">ドキュメント ソース プロバイダーがの代わりに、ドキュメントの特性を記述したフィールドの一意なセットでこれらのオブジェクトを作成するドキュメントを表す**Record**オブジェクトまたは**Recordset**オブジェクトがドキュメントのフォルダーを表すと、実際のドキュメント自体です。</span><span class="sxs-lookup"><span data-stu-id="7120e-122">When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself.</span></span> <span data-ttu-id="7120e-123">通常、1 つのフィールドには、ドキュメントを表す**ストリーム**への参照が含まれています。</span><span class="sxs-lookup"><span data-stu-id="7120e-123">Typically, one field contains a reference to the **Stream** that represents the document.</span></span>

<span data-ttu-id="7120e-124">これらのフィールドがリソースの **record** または **recordset** を形成していますが、これらのフィールドをサポートする特定のプロバイダーについてのフィールド一覧は、「 [付録 A: プロバイダー](appendix-a-providers.md)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="7120e-124">These fields constitute a resource **record** or **recordset** and are listed for the specific providers that support them in [Appendix A: Providers](appendix-a-providers.md).</span></span>

<span data-ttu-id="7120e-p107">リソースの **Record** または **Recordset** の **Fields** コレクションに 2 つの定数でインデックスを付けて、両方で共通して使用されるフィールドを取得します。 **Field** オブジェクトの [Value](value-property-ado.md) プロパティが、要求された内容を返します。</span><span class="sxs-lookup"><span data-stu-id="7120e-p107">Two constants index the **Fields** collection of a resource **Record** or **Recordset** to retrieve a pair of commonly used fields. The **Field** object [Value](value-property-ado.md) property returns the desired content.</span></span>

  - <span data-ttu-id="7120e-p108">**adDefaultStream** 定数でアクセスされたフィールドには、 **Record** オブジェクトまたは **Recordset** オブジェクトに関連付けられた既定のストリームが含まれます。プロバイダーは、既定のストリームをオブジェクトに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="7120e-p108">The field accessed with the **adDefaultStream** constant contains a default stream associated with the **Record** or **Recordset** object. The provider assigns a default stream to an object.</span></span>

  - <span data-ttu-id="7120e-129">**adRecordURL** 定数でアクセスされたフィールドには、ドキュメントを識別する絶対 URL が含まれます。</span><span class="sxs-lookup"><span data-stu-id="7120e-129">The field accessed with the **adRecordURL** constant contains the absolute URL that identifies the document.</span></span>

<span data-ttu-id="7120e-p109">ドキュメント ソース プロバイダーでは、 [Record](properties-collection-ado.md) オブジェクトと **Field** オブジェクトの **Properties** コレクションはサポートされません。 **Properties** コレクションの内容は、このようなオブジェクトに対しては Null です。</span><span class="sxs-lookup"><span data-stu-id="7120e-p109">A document source provider does not support the [Properties](properties-collection-ado.md) collection of **Record** and **Field** objects. The content of the **Properties** collection is null for such objects.</span></span>

<span data-ttu-id="7120e-p110">ドキュメント ソース プロバイダーで、ドキュメント ソース プロバイダーかどうかを識別する **Datasource Type** などのプロバイダー特有のプロパティを追加することができます。使用しているプロバイダーの種類を調べる方法の詳細については、そのプロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="7120e-p110">A document source provider may add a provider-specific property such as **Datasource Type** to identify whether it is a document source provider. For more information about how to determine your type of provider, see your provider documentation.</span></span>

## <a name="resource-recordset-columns"></a><span data-ttu-id="7120e-134">リソース レコードセットの列</span><span class="sxs-lookup"><span data-stu-id="7120e-134">Resource Recordset Columns</span></span>

<span data-ttu-id="7120e-135">*リソース レコード セット*は、次の列で構成されます。</span><span class="sxs-lookup"><span data-stu-id="7120e-135">A *resource recordset* consists of the following columns.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7120e-136">列名</span><span class="sxs-lookup"><span data-stu-id="7120e-136">Column name</span></span></p></th>
<th><p><span data-ttu-id="7120e-137">型</span><span class="sxs-lookup"><span data-stu-id="7120e-137">Type</span></span></p></th>
<th><p><span data-ttu-id="7120e-138">説明</span><span class="sxs-lookup"><span data-stu-id="7120e-138">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7120e-139">RESOURCE_PARSENAME</span><span class="sxs-lookup"><span data-stu-id="7120e-139">RESOURCE_PARSENAME</span></span></p></td>
<td><p><span data-ttu-id="7120e-140">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-140">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-p111">読み取り専用です。リソースの URL を示します。</span><span class="sxs-lookup"><span data-stu-id="7120e-p111">Read-only. Indicates the URL of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-143">RESOURCE_PARENTNAME</span><span class="sxs-lookup"><span data-stu-id="7120e-143">RESOURCE_PARENTNAME</span></span></p></td>
<td><p><span data-ttu-id="7120e-144">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-144">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-p112">読み取り専用です。親レコードの絶対 URL を示します。</span><span class="sxs-lookup"><span data-stu-id="7120e-p112">Read-only. Indicates the absolute URL of the parent record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-147">RESOURCE_ABSOLUTEPARSENAME</span><span class="sxs-lookup"><span data-stu-id="7120e-147">RESOURCE_ABSOLUTEPARSENAME</span></span></p></td>
<td><p><span data-ttu-id="7120e-148">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-148">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-p113">読み取り専用です。リソースの絶対 URL、つまり PARENTNAME と PARSENAME の連結を示します。</span><span class="sxs-lookup"><span data-stu-id="7120e-p113">Read-only. Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-151">RESOURCE_ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="7120e-151">RESOURCE_ISHIDDEN</span></span></p></td>
<td><p><span data-ttu-id="7120e-152">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="7120e-152">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="7120e-p114">リソースが非表示状態であれば True です。RESOURCE_ISHIDDEN が True の行を、行セットを作成するコマンドが明示的に選択しない限り、行は返されません。</span><span class="sxs-lookup"><span data-stu-id="7120e-p114">True if the resource is hidden. No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-155">RESOURCE_ISREADONLY</span><span class="sxs-lookup"><span data-stu-id="7120e-155">RESOURCE_ISREADONLY</span></span></p></td>
<td><p><span data-ttu-id="7120e-156">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="7120e-156">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="7120e-p115">リソースが読み取り専用であれば True です。DBBINDFLAG_WRITE でこのリソースを開こうとすると、DB_E_READONLY が設定され、失敗します。リソースが読み取り専用で開かれた場合でも、このプロパティは編集することができます。</span><span class="sxs-lookup"><span data-stu-id="7120e-p115">True if the resource is read-only. Attempts to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY. This property may be edited even when the resource has only been opened for reading.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-160">RESOURCE_CONTENTTYPE</span><span class="sxs-lookup"><span data-stu-id="7120e-160">RESOURCE_CONTENTTYPE</span></span></p></td>
<td><p><span data-ttu-id="7120e-161">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-161">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-162">ドキュメントの使用方法を示します-たとえば、法律家の書類です。</span><span class="sxs-lookup"><span data-stu-id="7120e-162">Indicates the likely use of the document — for example, a lawyer's brief.</span></span> <span data-ttu-id="7120e-163">ドキュメントの作成に使用される Office テンプレートに対応するこの可能性があります。&quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="7120e-163">This may correspond to the Office template used to create the document.&quot;&quot;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-164">RESOURCE_CONTENTCLASS</span><span class="sxs-lookup"><span data-stu-id="7120e-164">RESOURCE_CONTENTCLASS</span></span></p></td>
<td><p><span data-ttu-id="7120e-165">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-165">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-166">次のように形式を示すドキュメントの MIME の種類を示す&quot;と&quot;.'</span><span class="sxs-lookup"><span data-stu-id="7120e-166">Indicates the MIME type of the document, indicating the format such as &quot;text/html&quot;.'</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-167">RESOURCE_CONTENTLANGUAGE</span><span class="sxs-lookup"><span data-stu-id="7120e-167">RESOURCE_CONTENTLANGUAGE</span></span></p></td>
<td><p><span data-ttu-id="7120e-168">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-168">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-169">内容がどの言語で保存されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="7120e-169">Indicates the language in which the content is stored.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-170">RESOURCE_CREATIONTIME</span><span class="sxs-lookup"><span data-stu-id="7120e-170">RESOURCE_CREATIONTIME</span></span></p></td>
<td><p><span data-ttu-id="7120e-171">adFileTime</span><span class="sxs-lookup"><span data-stu-id="7120e-171">adFileTime</span></span></p></td>
<td><p><span data-ttu-id="7120e-p117">読み取り専用です。リソースが作成された時刻を含んだ FILETIME 構造を示します。時刻は、Coordinated Universal Time (UTC) 形式で報告されます。</span><span class="sxs-lookup"><span data-stu-id="7120e-p117">Read-only. Indicates a FILETIME structure containing the time the resource was created. The time is reported in Coordinated Universal Time (UTC) format.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-175">RESOURCE_LASTACCESSTIME</span><span class="sxs-lookup"><span data-stu-id="7120e-175">RESOURCE_LASTACCESSTIME</span></span></p></td>
<td><p><span data-ttu-id="7120e-176">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="7120e-176">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="7120e-p118">読み取り専用です。リソースが最後にアクセスされた時刻を含んだ FILETIME 構造を示します。時刻は UTC 形式です。プロバイダーでこの時刻メンバーがサポートされない場合、FILETIME メンバーは 0 です。</span><span class="sxs-lookup"><span data-stu-id="7120e-p118">Read-only. Indicates a FILETIME structure containing the time that the resource was last accessed. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-181">RESOURCE_LASTWRITETIME</span><span class="sxs-lookup"><span data-stu-id="7120e-181">RESOURCE_LASTWRITETIME</span></span></p></td>
<td><p><span data-ttu-id="7120e-182">AdFileTime</span><span class="sxs-lookup"><span data-stu-id="7120e-182">AdFileTime</span></span></p></td>
<td><p><span data-ttu-id="7120e-p119">読み取り専用です。リソースが最後に書き込まれた時刻を含んだ FILETIME 構造を示します。時刻は UTC 形式です。プロバイダーでこの時刻メンバーがサポートされない場合、FILETIME メンバーは 0 です。</span><span class="sxs-lookup"><span data-stu-id="7120e-p119">Read-only. Indicates a FILETIME structure containing the time that the resource was last written. The time is in UTC format. The FILETIME members are zero if the provider does not support this time member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-187">RESOURCE_STREAMSIZE</span><span class="sxs-lookup"><span data-stu-id="7120e-187">RESOURCE_STREAMSIZE</span></span></p></td>
<td><p><span data-ttu-id="7120e-188">asUnsignedBigInt</span><span class="sxs-lookup"><span data-stu-id="7120e-188">asUnsignedBigInt</span></span></p></td>
<td><p><span data-ttu-id="7120e-p120">読み取り専用です。リソースの既定のストリームのサイズをバイト数で示します。</span><span class="sxs-lookup"><span data-stu-id="7120e-p120">Read-only. Indicates the size of the resource's default stream, in bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-191">RESOURCE_ISCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="7120e-191">RESOURCE_ISCOLLECTION</span></span></p></td>
<td><p><span data-ttu-id="7120e-192">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="7120e-192">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="7120e-p121">読み取り専用です。リソースがディレクトリなどのコレクションであれば True です。リソースが単純ファイルの場合は False です。</span><span class="sxs-lookup"><span data-stu-id="7120e-p121">Read-only. True if the resource is a collection, such as a directory. False if the resource is a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span><span class="sxs-lookup"><span data-stu-id="7120e-196">RESOURCE_ISSTRUCTUREDDOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="7120e-197">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="7120e-197">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="7120e-p122">リソースが構造ドキュメントであれば True です。リソースが構造ドキュメントでない場合は False です。その場合は、コレクションまたは単純ファイルの可能性があります。</span><span class="sxs-lookup"><span data-stu-id="7120e-p122">True if the resource is a structured document. False if the resource is not a structured document. It could be a collection or a simple file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-201">DEFAULT_DOCUMENT</span><span class="sxs-lookup"><span data-stu-id="7120e-201">DEFAULT_DOCUMENT</span></span></p></td>
<td><p><span data-ttu-id="7120e-202">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-202">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-p123">読み取り専用です。このリソースがフォルダーの既定の単純ドキュメントまたは構造ドキュメントへの URL を含んでいることを示します。既定のストリームがリソースから要求されたときに使用されます。このプロパティは、単純ファイルの場合は空白です。</span><span class="sxs-lookup"><span data-stu-id="7120e-p123">Read-only. Indicates that this resource contains a URL to the default simple document of a folder or a structured document. Used when the default stream is requested from a resource. This property is blank for a simple file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-207">CHAPTERED_CHILDREN</span><span class="sxs-lookup"><span data-stu-id="7120e-207">CHAPTERED_CHILDREN</span></span></p></td>
<td><p><span data-ttu-id="7120e-208">AdChapter</span><span class="sxs-lookup"><span data-stu-id="7120e-208">AdChapter</span></span></p></td>
<td><p><span data-ttu-id="7120e-p124">読み取り専用です。オプションです。リソースの子を含む行セットのチャプターを示します (<em>OLE DB Provider for Internet Publishing</em> はこの列を使用しません)。</span><span class="sxs-lookup"><span data-stu-id="7120e-p124">Read-only. Optional. Indicates the chapter of the rowset containing the children of the resource. (The <em>OLE DB Provider for Internet Publishing</em> does not use this column.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7120e-213">RESOURCE_DISPLAYNAME</span><span class="sxs-lookup"><span data-stu-id="7120e-213">RESOURCE_DISPLAYNAME</span></span></p></td>
<td><p><span data-ttu-id="7120e-214">AdVarWChar</span><span class="sxs-lookup"><span data-stu-id="7120e-214">AdVarWChar</span></span></p></td>
<td><p><span data-ttu-id="7120e-p125">読み取り専用です。リソースの表示名を示します。</span><span class="sxs-lookup"><span data-stu-id="7120e-p125">Read-only. Indicates the display name of the resource.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7120e-217">RESOURCE_ISROOT</span><span class="sxs-lookup"><span data-stu-id="7120e-217">RESOURCE_ISROOT</span></span></p></td>
<td><p><span data-ttu-id="7120e-218">AdBoolean</span><span class="sxs-lookup"><span data-stu-id="7120e-218">AdBoolean</span></span></p></td>
<td><p><span data-ttu-id="7120e-p126">読み取り専用です。リソースがコレクションのルートまたは構造ドキュメントであれば True です。</span><span class="sxs-lookup"><span data-stu-id="7120e-p126">Read-only. True if the resource is the root of a collection or structured document.</span></span></p></td>
</tr>
</tbody>
</table>

