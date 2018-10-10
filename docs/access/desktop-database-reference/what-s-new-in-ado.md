---
title: ActiveX データ オブジェクト (ADO) の新機能
TOCTitle: What's New in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 86d3c151ac77ab4138afcd84ee2a14d94dd07aef
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477181"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="ee50b-102">ADO の新機能</span><span class="sxs-lookup"><span data-stu-id="ee50b-102">What's New in ADO</span></span>


<span data-ttu-id="ee50b-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="ee50b-103">**Applies to**: Access 2013 | Office 2013</span></span> 
 

<span data-ttu-id="ee50b-p101">ADO 2.5 リリースには、次に示す新機能および拡充されたマニュアルが含まれています。この一覧では、ADO、ADO MD、および ADOX を扱っています。</span><span class="sxs-lookup"><span data-stu-id="ee50b-p101">The following new features and enhanced documentation are included in the ADO 2.5 release. This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="ee50b-106">新機能</span><span class="sxs-lookup"><span data-stu-id="ee50b-106">New Features</span></span>

<span data-ttu-id="ee50b-107">**[レコードとストリーム](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="ee50b-107">**[Records and Streams](chapter-10-records-and-streams.md)**</span></span>

<span data-ttu-id="ee50b-p102">このリリースの ADO では、[Record](record-object-ado.md) オブジェクトが導入されており、ファイル システムのディレクトリやファイル、および電子メール システムのフォルダーやメッセージのような要素を表して管理できます。 **Record** は [Recordset](recordset-object-ado.md) の行を表すこともできますが、 **Record** オブジェクトと **Recordset** オブジェクトでは、メソッドおよびプロパティが異なります。</span><span class="sxs-lookup"><span data-stu-id="ee50b-p102">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an e-mail system. A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

<span data-ttu-id="ee50b-110">新しい [Stream](stream-object-ado.md) オブジェクトは、ファイルやメッセージのストリームを構成するバイトまたはテキストのバイナリ ストリームの読み取り、書き込み、および管理を行うための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

<span data-ttu-id="ee50b-111">**[URL の使用](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="ee50b-111">**[URL Usage](absolute-and-relative-urls.md)**</span></span>

<span data-ttu-id="ee50b-p103">このリリースでは、データ ストア オブジェクトを指定するための接続文字列やコマンド テキストに代わる手段として、Uniform Resource Locator (URL) の使用が導入されました。URL は、既存の [Connection](connection-object-ado.md) オブジェクトや **Recordset** オブジェクトだけでなく、新しい **Record** オブジェクトや **Stream** オブジェクトでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="ee50b-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

<span data-ttu-id="ee50b-114">このリリースでは、ADO では、独自の URL スキームを認識する OLE DB プロバイダーがサポートしています。</span><span class="sxs-lookup"><span data-stu-id="ee50b-114">With this release, ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="ee50b-115">などの[OLE DB プロバイダー](microsoft-ole-db-provider-for-internet-publishing.md)*,* 、Windows 2000 ファイル システムをアクセスするには、既存の HTTP スキームを認識します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-115">For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

<span data-ttu-id="ee50b-116">**[ドキュメント ソース プロバイダー用の特殊なフィールド](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="ee50b-116">**[Special Fields for Document Source Providers](records-and-provider-supplied-fields.md)**</span></span>

<span data-ttu-id="ee50b-117">プロバイダーでは、*ドキュメント ソース*プロバイダーと呼ばれる特別なクラスでは、フォルダーやドキュメントを管理します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="ee50b-118">ドキュメントを表す**Record**オブジェクトまたは**Recordset**オブジェクトがドキュメントのフォルダーを表す、ドキュメント ソース プロバイダーは、ドキュメントの特性を記述したフィールドの一意なセットでこれらのオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="ee50b-119">これらのフィールドは、\*リソース\***の Record**または**Recordset**を構成します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="ee50b-120">新しいリファレンス トピック</span><span class="sxs-lookup"><span data-stu-id="ee50b-120">New Reference Topics</span></span>

<span data-ttu-id="ee50b-121">このリリースでは、以下の新しいプロパティが組み込まれました。</span><span class="sxs-lookup"><span data-stu-id="ee50b-121">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee50b-122">プロパティ</span><span class="sxs-lookup"><span data-stu-id="ee50b-122">Property</span></span></p></th>
<th><p><span data-ttu-id="ee50b-123">説明</span><span class="sxs-lookup"><span data-stu-id="ee50b-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-124"><a href="charset-property-ado.md">文字セット</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-124"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-125">テキスト <strong>Stream</strong> オブジェクトの変換後の文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-125">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-126"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-126"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-127">現在の位置がストリームの末尾にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-127">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-128"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-128"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-129">テキスト <strong>Stream</strong> オブジェクトの行区切り文字として使用するバイナリ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-129">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-130"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-130"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-131"><strong>Connection</strong> オブジェクト、 <strong>Record</strong> オブジェクト、または <strong>Stream</strong> オブジェクトで使用可能なデータ変更権限を示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-131">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-132"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-132"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-133">現在の <strong>Record</strong> オブジェクトの親 <strong>Record</strong> を示す絶対 URL 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-133">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-134"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-134"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-135"><strong>Stream</strong> オブジェクト内の現在の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-135">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-136"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-136"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-137"><strong>Record</strong> オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-137">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-138"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-138"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-139">ストリームのサイズをバイト数で示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-139">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-140"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-140"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-141"><strong>Record</strong> オブジェクトによって表されるエンティティを示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-141">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-142"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-142"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-143">対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-143">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="ee50b-144">非同期メソッドを実行する対象になるすべてのオブジェクトについて、オブジェクトの状態が接続、実行、取得のいずれであるかを示します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-144">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-145"><a href="type-property-ado-stream.md">型</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-145"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-146"><strong>Stream</strong> オブジェクトに含まれるデータの種類を示します (バイナリまたはテキスト)。</span><span class="sxs-lookup"><span data-stu-id="ee50b-146">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ee50b-147">このリリースでは、以下の新しいメソッドが組み込まれました。</span><span class="sxs-lookup"><span data-stu-id="ee50b-147">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ee50b-148">メソッド</span><span class="sxs-lookup"><span data-stu-id="ee50b-148">Method</span></span></p></th>
<th><p><span data-ttu-id="ee50b-149">説明</span><span class="sxs-lookup"><span data-stu-id="ee50b-149">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-150"><a href="copyrecord-method-ado.md">定義</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-150"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-151">ファイルまたはディレクトリとその内容を、別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="ee50b-151">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-152"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-152"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-153"><strong>ストリーム</strong><strong>オブジェクト</strong>で、指定した文字数またはバイト (<strong>の種類</strong>) によって異なりますを別の<strong>Stream</strong>オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="ee50b-153">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-154"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-154"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-155">ファイルまたはディレクトリとそのすべてのサブディレクトリを削除します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-155">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-156"><a href="flush-method-ado.md">フラッシュ</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-156"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-157">ADO バッファーに残っている <strong>Stream</strong> オブジェクトの内容を、<strong>Stream</strong> オブジェクトに関連付けられた、基になるオブジェクトに反映します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-157">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-158"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-158"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-159"><strong>Record</strong> で表されるディレクトリ内のファイルとサブディレクトリを表す行を含む <strong>Recordset</strong> を返します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-159">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-160"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-160"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-161">既存のファイルの内容を、<strong>Stream</strong> オブジェクトに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ee50b-161">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-162"><a href="moverecord-method-ado.md">関係</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-162"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-163">ファイルまたはディレクトリとその内容を、別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-163">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-164"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-164"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-165">既存の <strong>Record</strong> オブジェクトを開きます。または、新しいファイルかディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-165">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-166"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-166"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-167">バイナリ データまたはテキスト データのストリームを操作するために <strong>Stream</strong> オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="ee50b-167">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-168"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-168"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-169">バイナリ型の <strong>Stream</strong> オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ee50b-169">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-170"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-170"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-171">文字列型の <strong>Stream</strong> オブジェクトから、指定された文字数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ee50b-171">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-172"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-172"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-173"><strong>Stream</strong> のバイナリの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-173">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-174"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-174"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-175">ストリームの末尾の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="ee50b-175">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-176"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-176"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-177">テキスト <strong>Stream</strong> オブジェクトを読み取るときに、1 行全体をスキップします。</span><span class="sxs-lookup"><span data-stu-id="ee50b-177">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ee50b-178"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-178"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-179">バイナリ データを <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="ee50b-179">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ee50b-180"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="ee50b-180"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="ee50b-181">指定されたテキスト文字列を <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="ee50b-181">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="ee50b-182">新規および拡充されたドキュメント</span><span class="sxs-lookup"><span data-stu-id="ee50b-182">New and Enhanced Documentation</span></span>

<span data-ttu-id="ee50b-183">**[コード例のトピック](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="ee50b-183">**[Code Example Topics](ado-code-examples.md)**</span></span>

<span data-ttu-id="ee50b-p107">例が拡充され、Microsoft Visual C++® および Microsoft Visual J++® で作成されたコード例が追加されました。これらのコード例は、コピーしてエディターに貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="ee50b-p107">The examples have been expanded to contain code examples written in Microsoft Visual C++® and Microsoft Visual J++®. You can copy and paste these code examples into your editor.</span></span>

<span data-ttu-id="ee50b-186">**[プロバイダーのトピック](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="ee50b-186">**[Provider Topics](appendix-a-providers.md)**</span></span>

<span data-ttu-id="ee50b-187">[OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) と共に ADO を使用する方法を説明した新しいトピックが追加されました。</span><span class="sxs-lookup"><span data-stu-id="ee50b-187">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

<span data-ttu-id="ee50b-188">**[ADO を使ったプログラミング](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="ee50b-188">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

<span data-ttu-id="ee50b-p108">この新しいセクションには、さまざまなプログラミング言語で ADO を使用するためのヒントが含まれます。ADO 用 Visual C++ Extensions と ADO/WFC の既存の構文インデックス、および Microsoft Visual Basic®、Microsoft Visual Basic® Scripting Edition、Microsoft JScript®、Microsoft Visual C++、または Microsoft Visual J++ を使用する開発者向けの新しい情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ee50b-p108">This new section contains tips and tricks for using ADO with various programming languages. It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic®, Microsoft Visual Basic® Scripting Edition, Microsoft JScript®, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

