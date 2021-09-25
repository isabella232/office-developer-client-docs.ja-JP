---
title: レコードとプロバイダー供給のフィールド
TOCTitle: Records and provider-supplied fields
ms:assetid: cde72d6a-b9b0-9636-581d-68239a3f522d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250022(v=office.15)
ms:contentKeyID: 48547776
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 77e913f87923cb4dc7f4d4ddde5bf63b944c6252
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593776"
---
# <a name="records-and-provider-supplied-fields"></a>レコードとプロバイダー供給のフィールド

**適用先**: Access 2013、Office 2013

[Record](record-object-ado.md) オブジェクトが開かれると、そのソースは、開かれた [Connection](recordset-object-ado.md) オブジェクトと共に動作する、開かれた [Recordset](connection-object-ado.md) のカレント行、絶対 URL、または相対 URL になることができます。

**Record** が **Recordset** から開かれる場合は、 **Record** オブジェクトの [Fields](fields-collection-ado.md) コレクションには、 **Recordset** からのすべてのフィールドに加えて、基になるプロバイダーによって追加されたフィールドが含まれます。

プロバイダーは、 **Record** の補完機能として作用する追加フィールドを挿入することができます。その結果、 **Record** には、 **Recordset** 全体、または **Recordset** の別の行から派生した **Record** にはない固有のフィールドが存在するようになります。

たとえば、電子メール データ ソースから派生した **Recordset** のすべての行に、From、To、Subject などの列が含まれます。 A **Record** derived from that **Recordset** will have the same fields. However, the **Record** may also have other fields unique to the particular message represented by that **Record**, such as Attachment and Cc (carbon copy).

**Record** オブジェクトと **Recordset** オブジェクトのカレント行には同じフィールドがありますが、 **Record** オブジェクトと **Recordset** オブジェクトには異なるメソッドとプロパティがあるので、この 2 つは別のものです。

**Record** オブジェクトと **Recordset** オブジェクトに共通して存在しているフィールドは、いずれかのオブジェクトで変更することができます。ただし、基になるプロバイダーがフィールドを "Null" に設定できたとしても、 **Record** オブジェクトでフィールドを削除することはできません。

**Record** が開かれた後に、プログラムでフィールドを追加することができます。また、追加したフィールドを削除することができますが、元の **Recordset** からフィールドを削除することはできません。

さらに、URL から **Record** オブジェクトを直接開くことができます。この場合、 **Record** に追加されるフィールドは、基になるプロバイダーによって異なります。現在ほとんどのプロバイダーでは、 **Record** で表されるエンティティを記述したフィールドのセットが追加されます。エンティティが単純ファイルなどのバイトのストリームから構成されている場合、通常は [Stream](stream-object-ado.md) オブジェクトを **Record** から開くことができます。

## <a name="special-fields-for-document-source-providers"></a>ドキュメント ソース プロバイダー用の特殊なフィールド

ドキュメント ソース プロバイダーと呼ばれる特別なクラスのプロバイダーは、フォルダーとドキュメントを管理します。 When a **Record** object represents a document or a **Recordset** object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself. Typically, one field contains a reference to the **Stream** that represents the document.

これらのフィールドがリソースの **record** または **recordset** を形成していますが、これらのフィールドをサポートする特定のプロバイダーについてのフィールド一覧は、「 [付録 A: プロバイダー](appendix-a-providers.md)」に記載されています。

リソースの **Record** または **Recordset** の **Fields** コレクションに 2 つの定数でインデックスを付けて、両方で共通して使用されるフィールドを取得します。 **Field** オブジェクトの [Value](value-property-ado.md) プロパティが、要求された内容を返します。

  - **adDefaultStream** 定数でアクセスされたフィールドには、 **Record** オブジェクトまたは **Recordset** オブジェクトに関連付けられた既定のストリームが含まれます。プロバイダーは、既定のストリームをオブジェクトに割り当てます。

  - **adRecordURL** 定数でアクセスされたフィールドには、ドキュメントを識別する絶対 URL が含まれます。

ドキュメント ソース プロバイダーでは、 [Record](properties-collection-ado.md) オブジェクトと **Field** オブジェクトの **Properties** コレクションはサポートされません。 **Properties** コレクションの内容は、このようなオブジェクトに対しては Null です。

ドキュメント ソース プロバイダーで、ドキュメント ソース プロバイダーかどうかを識別する **Datasource Type** などのプロバイダー特有のプロパティを追加することができます。使用しているプロバイダーの種類を調べる方法の詳細については、そのプロバイダーのマニュアルを参照してください。

## <a name="resource-recordset-columns"></a>リソース レコードセットの列

"リソース レコードセット" は、次の列で構成されています。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>列名</p></th>
<th><p>種類</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>RESOURCE_PARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>読み取り専用です。リソースの URL を示します。</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_PARENTNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>読み取り専用です。親レコードの絶対 URL を示します。</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ABSOLUTEPARSENAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>読み取り専用です。リソースの絶対 URL、つまり PARENTNAME と PARSENAME の連結を示します。</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISHIDDEN</p></td>
<td><p>AdBoolean</p></td>
<td><p>リソースが非表示状態であれば True です。RESOURCE_ISHIDDEN が True の行を、行セットを作成するコマンドが明示的に選択しない限り、行は返されません。</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISREADONLY</p></td>
<td><p>AdBoolean</p></td>
<td><p>リソースが読み取り専用であれば True です。DBBINDFLAG_WRITE でこのリソースを開こうとすると、DB_E_READONLY が設定され、失敗します。リソースが読み取り専用で開かれた場合でも、このプロパティは編集することができます。</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTTYPE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>たとえば、法律家の書類などの、ドキュメントの使用方法を示します。 これは、ドキュメントの作成にOfficeテンプレートに対応する場合があります。&quot;&quot;</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CONTENTCLASS</p></td>
<td><p>AdVarWChar</p></td>
<td><p>テキスト/html などの形式を示す、ドキュメントの MIME の種類 &quot; を &quot; 示します 。'</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_CONTENTLANGUAGE</p></td>
<td><p>AdVarWChar</p></td>
<td><p>内容がどの言語で保存されるかを示します。</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_CREATIONTIME</p></td>
<td><p>adFileTime</p></td>
<td><p>読み取り専用です。リソースが作成された時刻を含んだ FILETIME 構造を示します。時刻は、Coordinated Universal Time (UTC) 形式で報告されます。</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_LASTACCESSTIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>読み取り専用です。リソースが最後にアクセスされた時刻を含んだ FILETIME 構造を示します。時刻は UTC 形式です。プロバイダーでこの時刻メンバーがサポートされない場合、FILETIME メンバーは 0 です。</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_LASTWRITETIME</p></td>
<td><p>AdFileTime</p></td>
<td><p>読み取り専用です。リソースが最後に書き込まれた時刻を含んだ FILETIME 構造を示します。時刻は UTC 形式です。プロバイダーでこの時刻メンバーがサポートされない場合、FILETIME メンバーは 0 です。</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_STREAMSIZE</p></td>
<td><p>asUnsignedBigInt</p></td>
<td><p>読み取り専用です。リソースの既定のストリームのサイズをバイト数で示します。</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_ISCOLLECTION</p></td>
<td><p>AdBoolean</p></td>
<td><p>読み取り専用です。リソースがディレクトリなどのコレクションであれば True です。リソースが単純ファイルの場合は False です。</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISSTRUCTUREDDOCUMENT</p></td>
<td><p>AdBoolean</p></td>
<td><p>リソースが構造ドキュメントであれば True です。リソースが構造ドキュメントでない場合は False です。その場合は、コレクションまたは単純ファイルの可能性があります。</p></td>
</tr>
<tr class="odd">
<td><p>DEFAULT_DOCUMENT</p></td>
<td><p>AdVarWChar</p></td>
<td><p>読み取り専用です。このリソースがフォルダーの既定の単純ドキュメントまたは構造ドキュメントへの URL を含んでいることを示します。既定のストリームがリソースから要求されたときに使用されます。このプロパティは、単純ファイルの場合は空白です。</p></td>
</tr>
<tr class="even">
<td><p>CHAPTERED_CHILDREN</p></td>
<td><p>AdChapter</p></td>
<td><p>読み取り専用です。オプションです。リソースの子を含む行セットのチャプターを示します (<em>OLE DB Provider for Internet Publishing</em> はこの列を使用しません)。</p></td>
</tr>
<tr class="odd">
<td><p>RESOURCE_DISPLAYNAME</p></td>
<td><p>AdVarWChar</p></td>
<td><p>読み取り専用です。リソースの表示名を示します。</p></td>
</tr>
<tr class="even">
<td><p>RESOURCE_ISROOT</p></td>
<td><p>AdBoolean</p></td>
<td><p>読み取り専用です。リソースがコレクションのルートまたは構造ドキュメントであれば True です。</p></td>
</tr>
</tbody>
</table>

