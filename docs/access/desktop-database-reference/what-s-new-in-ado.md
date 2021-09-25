---
title: データ オブジェクト (ADO) ActiveX新機能
TOCTitle: What's new in ADO
ms:assetid: fd3d0f9c-e9df-d130-13e3-757620e9400c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250297(v=office.15)
ms:contentKeyID: 48548905
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 042ede650e6658ef346177491f95e976839c96e2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568321"
---
# <a name="whats-new-in-ado"></a>ADO の新機能

**適用先:** Access 2013、Office 2013 
 
ADO 2.5 リリースには、次に示す新機能および拡充されたマニュアルが含まれています。この一覧では、ADO、ADO MD、および ADOX を扱っています。

## <a name="new-features"></a>新機能

- **[レコードとストリーム](chapter-10-records-and-streams.md)**

  ADO のこのリリースでは [、ファイル](record-object-ado.md) システム内のディレクトリやファイル、電子メール システム内のフォルダーやメッセージを表し、管理できる Record オブジェクトが導入されています。 **Record** は [Recordset](recordset-object-ado.md) の行を表すこともできますが、 **Record** オブジェクトと **Recordset** オブジェクトでは、メソッドおよびプロパティが異なります。

  新しい [Stream](stream-object-ado.md) オブジェクトは、ファイルやメッセージのストリームを構成するバイトまたはテキストのバイナリ ストリームの読み取り、書き込み、および管理を行うための手段を提供します。

- **[URL の使用法](absolute-and-relative-urls.md)**

  このリリースでは、データ ストア オブジェクトを指定するための接続文字列やコマンド テキストに代わる手段として、Uniform Resource Locator (URL) の使用が導入されました。URL は、既存の [Connection](connection-object-ado.md) オブジェクトや **Recordset** オブジェクトだけでなく、新しい **Record** オブジェクトや **Stream** オブジェクトでも使用できます。

  With this release, ADO supports OLE DB providers that recognize their own URL schemes. たとえば[、OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md)(2000 Windows ファイル システムにアクセスする) は、既存の HTTP スキームを認識します。

- **[ドキュメント ソース プロバイダーの特別なフィールド](records-and-provider-supplied-fields.md)**

  ドキュメント ソース プロバイダーと呼ばれる特別なクラスの *プロバイダーは、* フォルダーとドキュメントを管理します。 When a **Record** object represents a document, or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document. これらのフィールドは、リソース *レコードまたは* **Recordset を****構成します**。

## <a name="new-reference-topics"></a>新しいリファレンス トピック

### <a name="properties"></a>プロパティ

このリリースでは、以下の新しいプロパティが組み込まれました。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロパティ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="charset-property-ado.md">Charset</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトの変換後の文字セットを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>現在の位置がストリームの最後かどうかを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトで行区切り文字として使用するバイナリ文字を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p><strong>Connection</strong>、<strong>Record</strong>、または <strong>Stream</strong> オブジェクトでデータを変更するために使用できる権限を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>現在の <strong>Record</strong> オブジェクトの親 <strong>Record</strong> を示す絶対 URL 文字列を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p><strong>Stream</strong> オブジェクト内の現在の位置を示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p><strong>Record</strong> オブジェクトの種類を示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">サイズ</a></p></td>
<td><p>ストリームのサイズをバイト数で示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-record.md">Source</a></p></td>
<td><p><strong>Record</strong> オブジェクトによって表されるエンティティを示します。</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>対象になるすべてのオブジェクトについて、オブジェクトの状態が開いているか、閉じているかを示します。 非同期メソッドを実行しているオブジェクトで該当するものすべてについて、オブジェクトの現在の状態が接続中、実行中、または取得中のいずれであるかを示します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado-stream.md">種類</a></p></td>
<td><p><strong>Stream</strong> オブジェクトに含まれるデータの種類を示します (バイナリまたはテキスト)。</p></td>
</tr>
</tbody>
</table>

### <a name="methods"></a>Methods

このリリースでは、以下の新しいメソッドが組み込まれました。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>メソッド</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>ファイルまたはディレクトリとその内容を、別の場所にコピーします。</p></td>
</tr>
<tr class="even">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Stream オブジェクトの指定した文字数またはバイト数<strong>(Type</strong>に応じて) を別の<strong>Stream</strong> <strong>オブジェクト</strong><strong>にコピー</strong>します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>ファイルまたはディレクトリとそのすべてのサブディレクトリを削除します。</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">フラッシュ</a></p></td>
<td><p>ADO バッファーに残っている <strong>Stream</strong> オブジェクトの内容を、<strong>Stream</strong> オブジェクトに関連付けられた、基になるオブジェクトに反映します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p><strong>Record</strong> で表されるディレクトリ内のファイルとサブディレクトリを表す行を含む <strong>Recordset</strong> を返します。</p></td>
</tr>
<tr class="even">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>既存のファイルの内容を、<strong>Stream</strong> オブジェクトに読み込みます。</p></td>
</tr>
<tr class="odd">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>ファイルまたはディレクトリとその内容を、別の場所に移動します。</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-record.md">開く</a></p></td>
<td><p>既存の <strong>Record</strong> オブジェクトを開きます。または、新しいファイルかディレクトリを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">開く</a></p></td>
<td><p>バイナリ データまたはテキスト データのストリームを操作するための <strong>Stream</strong> オブジェクトを開きます。</p></td>
</tr>
<tr class="even">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>バイナリ <strong>Stream</strong> オブジェクトから、指定されたバイト数を読み取ります。</p></td>
</tr>
<tr class="odd">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトから、指定された文字数を読み取ります。</p></td>
</tr>
<tr class="even">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p><strong>Stream</strong> のバイナリの内容をファイルに保存します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>ストリームの末尾の位置を設定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>テキスト <strong>Stream</strong> オブジェクトを読み取るときに、1 行全体をスキップします。</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>バイナリ データを <strong>Stream</strong> オブジェクトに書き込みます。</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>指定されたテキスト文字列を <strong>Stream</strong> オブジェクトに書き込みます。</p></td>
</tr>
</tbody>
</table>


## <a name="new-and-enhanced-documentation"></a>新しいドキュメントと拡張ドキュメント

- **[コード例のトピック](ado-code-examples.md)**

  この例は、microsoft Visual J++と Microsoft Visual J++ で記述されたコード例Microsoft Visual C++拡張されています。 これらのコード例は、コピーしてエディターに貼り付けることができます。

- **[プロバイダーのトピック](appendix-a-providers.md)**

  [OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) と共に ADO を使用する方法を説明した新しいトピックが追加されました。

- **[ADO を使ったプログラミング](appendix-c-programming-with-ado.md)**

  この新しいセクションには、さまざまなプログラミング言語で ADO を使用するためのヒントが含まれます。 ADO および ADO/WFC の Visual C++ 拡張機能の既存の構文インデックスと、Microsoft Visual Basic、Microsoft Visual Basic スクリプト エディション、Microsoft JScript、Microsoft Visual C++、または Microsoft Visual J++ を使用する開発者に固有の新しい情報が含まれる。

