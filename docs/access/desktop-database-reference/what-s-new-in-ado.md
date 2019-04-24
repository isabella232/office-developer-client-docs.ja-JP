---
title: ActiveX Data Objects (ADO) の新機能
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 593daf08da1b4ce435d17f2a6deedfa3e89dbd32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302612"
---
# <a name="whats-new-in-ado"></a><span data-ttu-id="1c2eb-102">ADO の新機能</span><span class="sxs-lookup"><span data-stu-id="1c2eb-102">What's new in ADO</span></span>

<span data-ttu-id="1c2eb-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="1c2eb-103">**Applies to**: Access 2013, Office 2013</span></span> 
 
<span data-ttu-id="1c2eb-104">ADO 2.5 リリースには、次に示す新機能および拡充されたマニュアルが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-104">The following new features and enhanced documentation are included in the ADO 2.5 release.</span></span> <span data-ttu-id="1c2eb-105">この一覧では、ADO、ADO MD、および ADOX を扱っています。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-105">This list covers ADO, ADO MD, and ADOX.</span></span>

## <a name="new-features"></a><span data-ttu-id="1c2eb-106">新機能</span><span class="sxs-lookup"><span data-stu-id="1c2eb-106">New features</span></span>

- <span data-ttu-id="1c2eb-107">**[レコードとストリーム](chapter-10-records-and-streams.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2eb-107">**[Records and streams](chapter-10-records-and-streams.md)**</span></span>

  <span data-ttu-id="1c2eb-108">このリリースの ADO には、ファイルシステム内のディレクトリやファイル、電子メールシステム内のフォルダーやメッセージなどを表す、または管理する[Record](record-object-ado.md)オブジェクトが導入されています。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-108">This release of ADO introduces the [Record](record-object-ado.md) object, which can represent and manage things like directories and files in a file system, and folders and messages in an email system.</span></span> <span data-ttu-id="1c2eb-109">**Record** は [Recordset](recordset-object-ado.md) の行を表すこともできますが、 **Record** オブジェクトと **Recordset** オブジェクトでは、メソッドおよびプロパティが異なります。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-109">A **Record** can also represent a row in a [Recordset](recordset-object-ado.md), although **Record** and **Recordset** objects have different methods and properties.</span></span>

  <span data-ttu-id="1c2eb-110">新しい [Stream](stream-object-ado.md) オブジェクトは、ファイルやメッセージのストリームを構成するバイトまたはテキストのバイナリ ストリームの読み取り、書き込み、および管理を行うための手段を提供します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-110">The new [Stream](stream-object-ado.md) object provides the means to read, write, and manage the binary stream of bytes or text that comprise a file or message stream.</span></span>

- <span data-ttu-id="1c2eb-111">**[URL の使用状況](absolute-and-relative-urls.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2eb-111">**[URL usage](absolute-and-relative-urls.md)**</span></span>

  <span data-ttu-id="1c2eb-p103">このリリースでは、データ ストア オブジェクトを指定するための接続文字列やコマンド テキストに代わる手段として、Uniform Resource Locator (URL) の使用が導入されました。URL は、既存の [Connection](connection-object-ado.md) オブジェクトや **Recordset** オブジェクトだけでなく、新しい **Record** オブジェクトや **Stream** オブジェクトでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-p103">This release also introduces the use of Uniform Resource Locators (URLs), as an alternative to connection strings and command text, to name data store objects. URLs may be used with the existing [Connection](connection-object-ado.md) and **Recordset** objects, as well as with the new **Record** and **Stream** objects.</span></span>

  <span data-ttu-id="1c2eb-114">With this release, ADO supports OLE DB providers that recognize their own URL schemes.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-114">With this release, ADO supports OLE DB providers that recognize their own URL schemes.</span></span> <span data-ttu-id="1c2eb-115">たとえば、Windows 2000 ファイルシステムにアクセスする[OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)\*\* は、既存の HTTP スキームを認識します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-115">For example, the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)*,* which accesses the Windows 2000 file system, recognizes the existing HTTP scheme.</span></span>

- <span data-ttu-id="1c2eb-116">**[ドキュメントソースプロバイダー用の特殊なフィールド](records-and-provider-supplied-fields.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2eb-116">**[Special fields for document source providers](records-and-provider-supplied-fields.md)**</span></span>

  <span data-ttu-id="1c2eb-117">*ドキュメントソース*プロバイダーと呼ばれる、プロバイダーの特別なクラスで、フォルダーとドキュメントを管理します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-117">A special class of providers, called *document source* providers, manage folders and documents.</span></span> <span data-ttu-id="1c2eb-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-118">When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document.</span></span> <span data-ttu-id="1c2eb-119">これらのフィールドは、\*リソース\***レコード**または**レコードセット**を構成します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-119">These fields constitute a *resource* **Record** or **Recordset**.</span></span>

## <a name="new-reference-topics"></a><span data-ttu-id="1c2eb-120">新しいリファレンストピック</span><span class="sxs-lookup"><span data-stu-id="1c2eb-120">New reference topics</span></span>

### <a name="properties"></a><span data-ttu-id="1c2eb-121">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c2eb-121">Properties</span></span>

<span data-ttu-id="1c2eb-122">このリリースでは、以下の新しいプロパティが組み込まれました。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-122">The following new properties are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c2eb-123">プロパティ</span><span class="sxs-lookup"><span data-stu-id="1c2eb-123">Property</span></span></p></th>
<th><p><span data-ttu-id="1c2eb-124">説明</span><span class="sxs-lookup"><span data-stu-id="1c2eb-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-125"><a href="charset-property-ado.md">Charset</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-125"><a href="charset-property-ado.md">Charset</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-126">テキスト <strong>Stream</strong> オブジェクトの変換後の文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-126">Indicates the character set into which the contents of a text <strong>Stream</strong> object should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-127"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-127"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-128">現在の位置がストリームの最後かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-128">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-129"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-130">テキスト <strong>Stream</strong> オブジェクトで行区切り文字として使用するバイナリ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-130">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-131"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-131"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-132"><strong>Connection</strong>、<strong>Record</strong>、または <strong>Stream</strong> オブジェクトでデータを変更するために使用できる権限を示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-132">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-133"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-133"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-134">現在の <strong>Record</strong> オブジェクトの親 <strong>Record</strong> を示す絶対 URL 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-134">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-135"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-135"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-136"><strong>Stream</strong> オブジェクト内の現在の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-136">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-137"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-137"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-138"><strong>Record</strong> オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-138">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-139"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Size</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-140">ストリームのサイズをバイト数で示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-140">Indicates the size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-141"><a href="source-property-ado-record.md">Source</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-141"><a href="source-property-ado-record.md">Source</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-142"><strong>Record</strong> オブジェクトによって表されるエンティティを示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-142">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-143"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-143"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-144">対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-144">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="1c2eb-145">非同期メソッドを実行しているオブジェクトで該当するものすべてについて、オブジェクトの現在の状態が接続中、実行中、または取得中のいずれであるかを示します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-145">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-146"><a href="type-property-ado-stream.md">Type</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-146"><a href="type-property-ado-stream.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-147"><strong>Stream</strong> オブジェクトに含まれるデータの種類を示します (バイナリまたはテキスト)。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-147">Indicates the type of data contained in the <strong>Stream</strong> object (binary or text).</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a><span data-ttu-id="1c2eb-148">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c2eb-148">Methods</span></span>

<span data-ttu-id="1c2eb-149">このリリースでは、以下の新しいメソッドが組み込まれました。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-149">The following new methods are included in this release.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1c2eb-150">メソッド</span><span class="sxs-lookup"><span data-stu-id="1c2eb-150">Method</span></span></p></th>
<th><p><span data-ttu-id="1c2eb-151">説明</span><span class="sxs-lookup"><span data-stu-id="1c2eb-151">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-152"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-153">ファイルまたはディレクトリとその内容を、別の場所にコピーします。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-153">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-154"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-154"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-155"><strong>stream</strong> <strong>オブジェクト</strong>内の指定された文字数またはバイト数 (<strong>型</strong>によって異なります) を別の<strong>stream</strong>オブジェクトにコピーします。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-155">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> <strong>object</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-156"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-157">ファイルまたはディレクトリとそのすべてのサブディレクトリを削除します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-157">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-158"><a href="flush-method-ado.md">揃え</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-158"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-159">ADO バッファーに残っている <strong>Stream</strong> オブジェクトの内容を、<strong>Stream</strong> オブジェクトに関連付けられた、基になるオブジェクトに反映します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-159">Forces the contents of the <strong>Stream</strong> object remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> object is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-160"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-160"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-161"><strong>Record</strong> で表されるディレクトリ内のファイルとサブディレクトリを表す行を含む <strong>Recordset</strong> を返します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-161">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record.</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-163">既存のファイルの内容を、<strong>Stream</strong> オブジェクトに読み込みます。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-163">Loads the contents of an existing file into a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-164"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-164"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-165">ファイルまたはディレクトリとその内容を、別の場所に移動します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-165">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-166"><a href="open-method-ado-record.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-166"><a href="open-method-ado-record.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-167">既存の <strong>Record</strong> オブジェクトを開きます。または、新しいファイルかディレクトリを作成します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-167">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-168"><a href="open-method-ado-stream.md">Open</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-168"><a href="open-method-ado-stream.md">Open</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-169">バイナリ データまたはテキスト データのストリームを操作するための <strong>Stream</strong> オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-169">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-170"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-170"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-171">バイナリ <strong>Stream</strong> オブジェクトから、指定されたバイト数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-171">Reads a specified number of bytes from a binary <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-172"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-172"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-173">テキスト <strong>Stream</strong> オブジェクトから、指定された文字数を読み取ります。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-173">Reads specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-174"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-174"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-175"><strong>Stream</strong> のバイナリの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-175">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-176"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-176"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-177">ストリームの末尾の位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-177">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-178"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-178"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-179">テキスト <strong>Stream</strong> オブジェクトを読み取るときに、1 行全体をスキップします。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-179">Skips one entire line when reading a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1c2eb-180"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-180"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-181">バイナリ データを <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-181">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1c2eb-182"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="1c2eb-182"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="1c2eb-183">指定されたテキスト文字列を <strong>Stream</strong> オブジェクトに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-183">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a><span data-ttu-id="1c2eb-184">新機能と強化されたドキュメント</span><span class="sxs-lookup"><span data-stu-id="1c2eb-184">New and enhanced documentation</span></span>

- <span data-ttu-id="1c2eb-185">**[コード例のトピック](ado-code-examples.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2eb-185">**[Code example topics](ado-code-examples.md)**</span></span>

  <span data-ttu-id="1c2eb-186">この例は、microsoft visual C++ および microsoft visual J++ で記述されたコード例を含むように展開されています。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-186">The examples have been expanded to contain code examples written in Microsoft Visual C++ and Microsoft Visual J++.</span></span> <span data-ttu-id="1c2eb-187">これらのコード例は、コピーしてエディターに貼り付けることができます。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-187">You can copy and paste these code examples into your editor.</span></span>

- <span data-ttu-id="1c2eb-188">**[プロバイダーのトピック](appendix-a-providers.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2eb-188">**[Provider topics](appendix-a-providers.md)**</span></span>

  <span data-ttu-id="1c2eb-189">[OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) と共に ADO を使用する方法を説明した新しいトピックが追加されました。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-189">A new topic is included that explains how to use ADO with the [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span>

- <span data-ttu-id="1c2eb-190">**[ADO を使ったプログラミング](appendix-c-programming-with-ado.md)**</span><span class="sxs-lookup"><span data-stu-id="1c2eb-190">**[Programming with ADO](appendix-c-programming-with-ado.md)**</span></span>

  <span data-ttu-id="1c2eb-191">この新しいセクションには、さまざまなプログラミング言語で ADO を使用するためのヒントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-191">This new section contains tips and tricks for using ADO with various programming languages.</span></span> <span data-ttu-id="1c2eb-192">このファイルには、ado および ado/WFC 用の Visual C++ 拡張機能のための既存の構文インデックスと、microsoft visual basic、microsoft visual basic Scripting Edition、microsoft JScript、microsoft visual C++、またはその他の開発者に固有の新しい情報が含まれています。Microsoft Visual J++。</span><span class="sxs-lookup"><span data-stu-id="1c2eb-192">It contains the existing syntax indexes for the Visual C++ Extensions for ADO and ADO/WFC, as well as new information specific to developers using Microsoft Visual Basic, Microsoft Visual Basic Scripting Edition, Microsoft JScript, Microsoft Visual C++, or Microsoft Visual J++.</span></span>

