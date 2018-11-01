---
title: ActiveX データ オブジェクト (ADO) のプロパティ
TOCTitle: ADO Properties
ms:assetid: 04f08f22-6327-c603-229e-d06a9f1c0d83
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248809(v=office.15)
ms:contentKeyID: 48543020
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4571f250891d02f8053e63aae7b94d674f61ca71
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876401"
---
# <a name="ado-properties"></a><span data-ttu-id="e7f6e-102">ADO プロパティ</span><span class="sxs-lookup"><span data-stu-id="e7f6e-102">ADO Properties</span></span>


<span data-ttu-id="e7f6e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-104"><a href="absolutepage-property-ado.md">AbsolutePage</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-104"><a href="absolutepage-property-ado.md">AbsolutePage</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-105">カレント レコードがあるページを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-105">Indicates on which page the current record resides.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-106"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-106"><a href="absoluteposition-property-ado.md">AbsolutePosition</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-107"><strong>Recordset</strong> オブジェクト内のカレント レコードの位置を表す値を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-107">Indicates the ordinal position of a <strong>Recordset</strong> object's current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-108"><a href="activecommand-property-ado.md">ActiveCommand</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-108"><a href="activecommand-property-ado.md">ActiveCommand</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-109">関連付けられた <strong>Recordset</strong> オブジェクトを作成した <strong>Command</strong> オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-109">Indicates the <strong>Command</strong> object that created the associated <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-110"><a href="activeconnection-property-ado.md">ActiveConnection</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-110"><a href="activeconnection-property-ado.md">ActiveConnection</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-111">指定された <strong>Command</strong> オブジェクト、 <strong>Recordset</strong> オブジェクト、または <strong>Record</strong> オブジェクトが現在属している <strong>Connection</strong> オブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-111">Indicates to which <strong>Connection</strong> object the specified <strong>Command</strong>, <strong>Recordset</strong>, or <strong>Record</strong> object currently belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-112"><a href="actualsize-property-ado.md">ActualSize</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-112"><a href="actualsize-property-ado.md">ActualSize</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-113">フィールドの値の実際の長さを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-113">Indicates the actual length of a field's value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-114"><a href="attributes-property-ado.md">Attributes</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-114"><a href="attributes-property-ado.md">Attributes</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-115">オブジェクトの 1 つまたは複数の属性を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-115">Indicates one or more characteristics of an object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-116"><a href="bof-eof-properties-ado.md">Bof プロパティと EOF</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-116"><a href="bof-eof-properties-ado.md">BOF and EOF</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-117"><strong>Bof プロパティ</strong>-現在のレコードの位置が<strong>Recordset</strong>オブジェクトの最初のレコードより前にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-117"><strong>BOF</strong> — indicates that the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="e7f6e-118"><strong>EOF</strong> : カレント レコードの位置が<strong>Recordset</strong>オブジェクトの最後のレコードの後にあることを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-118"><strong>EOF</strong> — indicates that the current record position is after the last record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-119"><a href="bookmark-property-ado.md">Bookmark</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-119"><a href="bookmark-property-ado.md">Bookmark</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-120"><strong>Recordset</strong> オブジェクトでカレント レコードを一意に識別するブックマークを示します。または、 <strong>Recordset</strong> オブジェクトのカレント レコードを、有効なブックマークで識別されるレコードに設定します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-120">Indicates a bookmark that uniquely identifies the current record in a <strong>Recordset</strong> object or sets the current record in a <strong>Recordset</strong> object to the record identified by a valid bookmark.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-121"><a href="cachesize-property-ado.md">CacheSize</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-121"><a href="cachesize-property-ado.md">CacheSize</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-122">ローカル メモリにキャッシュされる <strong>Recordset</strong> オブジェクトのレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-122">Indicates the number of records from a <strong>Recordset</strong> object that are cached locally in memory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-123"><a href="chapter-property-ado.md">章</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-123"><a href="chapter-property-ado.md">Chapter</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-124">OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトから取得するか、または、OLE DB Chapter オブジェクトを ADORecordsetConstruction オブジェクトに設定します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-124">Gets or sets an OLE DB <strong>Chapter</strong> object from/on an <strong>ADORecordsetConstruction</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-125"><a href="charset-property-ado.md">文字セット</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-125"><a href="charset-property-ado.md">CharSet</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-126">テキスト <strong>Stream</strong> の内容を変換する文字セットを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-126">Indicates the character set into which the contents of a text <strong>Stream</strong> should be translated.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-127"><a href="commandtext-property-ado.md">CommandText</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-127"><a href="commandtext-property-ado.md">CommandText</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-128">プロバイダーに対して発行するコマンド文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-128">Indicates the text of a command to be issued against a provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-129"><a href="commandtimeout-property-ado.md">CommandTimeout</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-129"><a href="commandtimeout-property-ado.md">CommandTimeout</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-130">実行しようとしたコマンドを中止して、エラーを生成するまでの待機時間を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-130">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-131"><a href="commandtype-property-ado.md">CommandType</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-131"><a href="commandtype-property-ado.md">CommandType</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-132"><strong>Command</strong> オブジェクトの型を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-132">Indicates the type of a <strong>Command</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-133"><a href="connectionstring-property-ado.md">ConnectionString プロパティ (ADO)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-133"><a href="connectionstring-property-ado.md">ConnectionString Property</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-134">データ ソースとの接続を確立するために使用される情報を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-134">Indicates the information used to establish a connection to a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-135"><a href="connectiontimeout-property-ado.md">ConnectionTimeout</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-135"><a href="connectiontimeout-property-ado.md">ConnectionTimeout</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-136">接続操作を中止して、エラーを生成するまでの待機時間を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-136">Indicates how long to wait while establishing a connection before terminating the attempt and generating an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-137"><a href="count-property-ado.md">Count</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-137"><a href="count-property-ado.md">Count</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-138">コレクション内のオブジェクト数を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-138">Indicates the number of objects in a collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-139"><a href="cursorlocation-property-ado.md">CursorLocation</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-139"><a href="cursorlocation-property-ado.md">CursorLocation</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-140">カーソル サービスの場所を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-140">Indicates the location of the cursor service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-141"><a href="cursortype-property-ado.md">カーソル。</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-141"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-142"><strong>Recordset</strong> オブジェクトで使用されているカーソルの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-142">Indicates the type of cursor used in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-143"><a href="datamember-property-ado.md">データ メンバー</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-143"><a href="datamember-property-ado.md">DataMember</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-144"><strong>DataSource</strong> プロパティによって参照されるオブジェクトから取得するデータ メンバーの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-144">Indicates the name of the data member that will be retrieved from the object referenced by the <strong>DataSource</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-145"><a href="datasource-property-ado.md">DataSource</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-145"><a href="datasource-property-ado.md">DataSource</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-146"><strong>Recordset</strong> オブジェクトとして表されるデータを持つオブジェクトを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-146">Indicates an object that contains data to be represented as a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-147"><a href="defaultdatabase-property-ado.md">DefaultDatabase</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-147"><a href="defaultdatabase-property-ado.md">DefaultDatabase</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-148"><strong>Connection</strong> オブジェクトの既定のデータベースを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-148">Indicates the default database for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-149"><a href="definedsize-property-ado.md">DefinedSize</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-149"><a href="definedsize-property-ado.md">DefinedSize</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-150"><strong>Field</strong> オブジェクトのデータ容量を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-150">Indicates the data capacity of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-151"><a href="description-property-ado.md">説明</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-151"><a href="description-property-ado.md">Description</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-152"><strong>Error</strong> オブジェクトを記述します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-152">Describes an <strong>Error</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-153"><a href="direction-property-ado.md">Direction</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-153"><a href="direction-property-ado.md">Direction</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-154"><strong>Parameter</strong> が、入力パラメーターと出力パラメーターのいずれか、またはその両方を表すのか、あるいはストアド プロシージャからの戻り値であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-154">Indicates whether the <strong>Parameter</strong> represents an input parameter, an output parameter, or both, or if the parameter is the return value from a stored procedure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-155"><a href="editmode-property-ado.md">EditMode</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-155"><a href="editmode-property-ado.md">EditMode</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-156">現在のレコードの編集ステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-156">Indicates the editing status of the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-157"><a href="eos-property-ado.md">EOS</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-157"><a href="eos-property-ado.md">EOS</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-158">現在の位置がストリームの末尾にあるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-158">Indicates whether the current position is at the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-159"><a href="filter-property-ado.md">Filter</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-159"><a href="filter-property-ado.md">Filter</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-160"><strong>Recordset</strong> のデータに対するフィルターを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-160">Indicates a filter for data in a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-161"><a href="helpcontext-helpfile-properties-ado.md">HelpContext、HelpFile</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-161"><a href="helpcontext-helpfile-properties-ado.md">HelpContext and HelpFile</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-162"><strong>Error</strong> オブジェクトに関連するヘルプ ファイルおよびヘルプ トピックを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-162">Indicates the help file and topic associated with an <strong>Error</strong> object.</span></span> <span data-ttu-id="e7f6e-163"><strong>HelpContextID</strong>: ヘルプ ファイルのトピックのコンテキスト ID を長整数型 ( <strong>Long</strong> ) の値で返します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-163"><strong>HelpContextID</strong> — returns a context ID, as a <strong>Long</strong> value, for a topic in a Help file.</span></span> <span data-ttu-id="e7f6e-164"><strong>HelpFile</strong>: ヘルプ ファイルへの完全なパスに評価される文字列型 ( <strong>String</strong> ) の値を返します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-164"><strong>HelpFile</strong> — returns a <strong>String</strong> value that evaluates to a fully resolved path to a Help file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-165"><a href="index-property-ado.md">Index</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-165"><a href="index-property-ado.md">Index</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-166"><strong>Recordset</strong> オブジェクトに対して現在有効なインデックスの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-166">Indicates the name of the index currently in effect for a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-167"><a href="isolationlevel-property-ado.md">IsolationLevel</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-167"><a href="isolationlevel-property-ado.md">IsolationLevel</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-168"><strong>Connection</strong> オブジェクトの分離レベルを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-168">Indicates the level of isolation for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-169"><a href="item-property-ado.md">Item</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-169"><a href="item-property-ado.md">Item</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-170">コレクションの特定のメンバーをその名前または序数で示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-170">Indicates a specific member of a collection, by name or ordinal number.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-171"><a href="lineseparator-property-ado.md">LineSeparator</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-171"><a href="lineseparator-property-ado.md">LineSeparator</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-172">テキスト <strong>Stream</strong> オブジェクトの行区切り文字として使用するバイナリ文字を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-172">Indicates the binary character to be used as the line separator in text <strong>Stream</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-173"><a href="locktype-property-ado.md">ロック。</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-173"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-174">編集時にレコードに適用されるロックの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-174">Indicates the type of locks placed on records during editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-175"><a href="marshaloptions-property-ado.md">スレッド</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-175"><a href="marshaloptions-property-ado.md">MarshalOptions</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-176">どのレコードがサーバーにマーシャリングされるかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-176">Indicates which records are to be marshaled back to the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-177"><a href="maxrecords-property-ado.md">MaxRecords</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-177"><a href="maxrecords-property-ado.md">MaxRecords</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-178">クエリから <strong>Recordset</strong> に返す最大レコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-178">Indicates the maximum number of records to return to a <strong>Recordset</strong> from a query.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-179"><a href="mode-property-ado.md">Mode</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-179"><a href="mode-property-ado.md">Mode</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-180"><strong>Connection</strong> オブジェクト、 <strong>Record</strong> オブジェクト、または <strong>Stream</strong> オブジェクトで使用可能なデータ変更権限を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-180">Indicates the available permissions for modifying data in a <strong>Connection</strong>, <strong>Record</strong>, or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-181"><a href="name-property-ado.md">Name</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-181"><a href="name-property-ado.md">Name</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-182">オブジェクトの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-182">Indicates the name of an object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-183"><a href="nativeerror-property-ado.md">以下</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-183"><a href="nativeerror-property-ado.md">NativeError</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-184">指定された <strong>Error</strong> オブジェクトでプロバイダー固有のエラー コードを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-184">Indicates the provider-specific error code for a given <strong>Error</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-185"><a href="number-property-ado.md">数値</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-185"><a href="number-property-ado.md">Number</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-186"><strong>Error</strong> オブジェクトを一意に識別する数値を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-186">Indicates the number that uniquely identifies an <strong>Error</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-187"><a href="numericscale-property-ado.md">NumericScale</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-187"><a href="numericscale-property-ado.md">NumericScale</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-188"><strong>Parameter</strong> オブジェクトまたは <strong>Field</strong> オブジェクトの数値の桁数を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-188">Indicates the scale of numeric values in a <strong>Parameter</strong> or <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-189"><a href="originalvalue-property-ado.md">OriginalValue</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-189"><a href="originalvalue-property-ado.md">OriginalValue</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-190">変更が行われる前のレコードに存在していた <strong>Field</strong> の値を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-190">Indicates the value of a <strong>Field</strong> that existed in the record before any changes were made.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-191"><a href="pagecount-property-ado.md">PageCount</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-191"><a href="pagecount-property-ado.md">PageCount</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-192"><strong>Recordset</strong> オブジェクトに含まれるデータのページ数を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-192">Indicates how many pages of data the <strong>Recordset</strong> object contains.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-193"><a href="pagesize-property-ado.md">PageSize</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-193"><a href="pagesize-property-ado.md">PageSize</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-194"><strong>Recordset</strong> の 1 ページを構成するレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-194">Indicates how many records constitute one page in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-195"><a href="parentrow-property-ado.md">ParentRow</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-195"><a href="parentrow-property-ado.md">ParentRow</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-196">OLE DB <strong>Row</strong> オブジェクトのコンテナーを <strong>ADORecordConstruction</strong> オブジェクトに設定し、行の親が ADO <strong>Record</strong> オブジェクトに変換されるようにします。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-196">Sets the container of an OLE DB <strong>Row</strong> object on an <strong>ADORecordConstruction</strong> object, so that the parent of the row is turned into an ADO <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-197"><a href="parenturl-property-ado.md">ParentURL</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-197"><a href="parenturl-property-ado.md">ParentURL</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-198">現在の <strong>Record</strong> オブジェクトの親 <strong>Record</strong> を示す絶対 URL 文字列を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-198">Indicates an absolute URL string that points to the parent <strong>Record</strong> of the current <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-199"><a href="position-property-ado.md">Position</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-199"><a href="position-property-ado.md">Position</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-200"><strong>Stream</strong> オブジェクト内の現在の位置を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-200">Indicates the current position within a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-201">Precision<a href="precision-property-ado.md"></a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-201"><a href="precision-property-ado.md">Precision</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-202"><strong>Parameter</strong> オブジェクト内の数値または数値型の <strong>Field</strong> オブジェクトの精度を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-202">Indicates the degree of precision for numeric values in a <strong>Parameter</strong> object or for numeric <strong>Field</strong> objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-203"><a href="prepared-property-ado.md">準備</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-203"><a href="prepared-property-ado.md">Prepared</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-204">コンパイルされたバージョンのコマンドを実行前に保存するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-204">Indicates whether to save a compiled version of a command before execution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-205"><a href="provider-property-ado.md">Provider</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-205"><a href="provider-property-ado.md">Provider</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-206"><strong>Connection</strong> オブジェクトのプロバイダー名を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-206">Indicates the name of the provider for a <strong>Connection</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-207"><a href="recordcount-property-ado.md">RecordCount</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-207"><a href="recordcount-property-ado.md">RecordCount</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-208"><strong>Recordset</strong> オブジェクト内のレコード数を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-208">Indicates the number of records in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-209"><a href="recordtype-property-ado.md">RecordType</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-209"><a href="recordtype-property-ado.md">RecordType</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-210"><strong>Record</strong> オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-210">Indicates the type of <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-211"><a href="row-property-ado.md">Row</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-211"><a href="row-property-ado.md">Row</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-212"><strong>ADORecordConstruction</strong> オブジェクトの OLE DB <strong>Row</strong> オブジェクトを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-212">Gets or sets an OLE DB <strong>Row</strong> object from/on an <strong>ADORecordConstruction</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-213"><a href="rowposition-property-ado.md">RowPosition</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-213"><a href="rowposition-property-ado.md">RowPosition</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-214"><strong>ADORecordsetConstruction</strong> オブジェクトの OLE DB <strong>RowPosition</strong> オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-214">Gets or sets an OLE DB <strong>RowPosition</strong> object from/on an <strong>ADORecordsetConstruction</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-215"><a href="rowset-property-ado.md">行セット</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-215"><a href="rowset-property-ado.md">Rowset</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-216"><strong>ADORecordsetConstruction</strong> オブジェクトの OLE DB <strong>Rowset</strong> オブジェクトを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-216">Gets or sets an OLE DB <strong>Rowset</strong> object from/on an <strong>ADORecordsetConstruction</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-217"><a href="size-property-ado.md">Size</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-217"><a href="size-property-ado.md">Size</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-218"><strong>Parameter</strong> オブジェクトの最大サイズをバイト数または文字数で示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-218">Indicates the maximum size, in bytes or characters, of a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-219"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">サイズ (ADO ストリーム)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-219"><a href="https://msdn.microsoft.com/library/jj250128(v=office.15)">Size (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-220">ストリームの合計サイズをバイト数で示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-220">Indicates the total size of the stream in number of bytes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-221"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-221"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-222"><strong>Recordset</strong> の並べ替えに使用するフィールド名、および各フィールドの並べ替え順序が昇順か降順かを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-222">Indicates one or more field names on which the <strong>Recordset</strong> is sorted, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-223"><a href="source-property-ado-error.md">ソース (ADO エラー)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-223"><a href="source-property-ado-error.md">Source (ADO Error)</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-224">エラーの発生源のオブジェクトまたはアプリケーションの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-224">Indicates the name of the object or application that originally generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-225"><a href="source-property-ado-record.md">ソース (ADO Record)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-225"><a href="source-property-ado-record.md">Source (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-226"><strong>Record</strong> オブジェクトによって表されるエンティティを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-226">Indicates the entity represented by the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-227"><a href="source-property-ado-recordset.md">ソース (ADO レコード セット)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-227"><a href="source-property-ado-recordset.md">Source (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-228"><strong>Recordset</strong> オブジェクトのデータのソースを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-228">Indicates the source for the data in a <strong>Recordset</strong> object</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-229"><a href="sqlstate-property-ado.md">SQLState</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-229"><a href="sqlstate-property-ado.md">SQLState</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-230">特定の <strong>Error</strong> オブジェクトの SQL 状態を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-230">Indicates the SQL state for a given <strong>Error</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-231"><a href="state-property-ado.md">State</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-231"><a href="state-property-ado.md">State</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-232">対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-232">Indicates for all applicable objects whether the state of the object is open or closed.</span></span> <span data-ttu-id="e7f6e-233">非同期メソッドを実行しているすべての対象オブジェクトについて、そのオブジェクトが現在、接続、実行、または取得のどの状態であるかを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-233">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-234"><a href="status-property-ado-field.md">状態 (ADO フィールド)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-234"><a href="status-property-ado-field.md">Status (ADO Field)</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-235"><strong>Field</strong> オブジェクトのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-235">Indicates the status of a <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-236"><a href="status-property-ado-recordset.md">状態 (ADO レコード セット)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-236"><a href="status-property-ado-recordset.md">Status (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-237">一括更新またはその他の一括操作に関して現在のレコードのステータスを示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-237">Indicates the status of the current record with respect to batch updates or other bulk operations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-238"><a href="stayinsync-property-ado.md">StayInSync</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-238"><a href="stayinsync-property-ado.md">StayInSync</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-239">親の行の位置が変更されたときに、基になる子のレコード (つまり、この<em>章</em>) への参照が変更されたかどうかを階層<strong>レコード セット</strong>オブジェクト内に示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-239">Indicates, in a hierarchical <strong>Recordset</strong> object, whether the reference to the underlying child records (that is, the <em>chapter</em>) changes when the parent row position changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-240"><a href="type-property-ado.md">型</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-240"><a href="type-property-ado.md">Type</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-241"><strong>Parameter</strong> オブジェクト、 <strong>Field</strong> オブジェクト、または <strong>Property</strong> オブジェクトの操作の種類またはデータ型を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-241">Indicates the operational type or data type of a <strong>Parameter</strong>, <strong>Field</strong>, or <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-242"><a href="type-property-ado-stream.md">型 (ADO ストリーム)</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-242"><a href="type-property-ado-stream.md">Type (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-243"><strong>Stream</strong> (バイナリまたはテキスト) に格納されているデータの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-243">Indicates the type of data contained in the <strong>Stream</strong> (binary or text).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-244"><a href="underlyingvalue-property-ado.md">UnderlyingValue</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-244"><a href="underlyingvalue-property-ado.md">UnderlyingValue</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-245">データベース内の <strong>Field</strong> オブジェクトの現在の値を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-245">Indicates a <strong>Field</strong> object's current value in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7f6e-246"><a href="value-property-ado.md">値</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-246"><a href="value-property-ado.md">Value</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-247"><strong>Field</strong> オブジェクト、 <strong>Parameter</strong> オブジェクト、または <strong>Property</strong> オブジェクトに割り当てられた値を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-247">Indicates the value assigned to a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7f6e-248"><a href="version-property-ado.md">Version</a></span><span class="sxs-lookup"><span data-stu-id="e7f6e-248"><a href="version-property-ado.md">Version</a></span></span></p></td>
<td><p><span data-ttu-id="e7f6e-249">ADO のバージョン番号を示します。</span><span class="sxs-lookup"><span data-stu-id="e7f6e-249">Indicates the ADO version number.</span></span></p></td>
</tr>
</tbody>
</table>

