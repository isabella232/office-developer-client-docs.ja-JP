---
title: Microsoft OLE DB Provider for Microsoft Indexing Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 7070fc6a7eeb9b2a41a15e2deaa24adb3bb7ba05
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611960"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a>Microsoft OLE DB Provider for Microsoft Indexing Service


**適用先**: Access 2013、Office 2013

Microsoft OLE DB Provider for Microsoft Indexing Service は、Microsoft Indexing Service によってインデックス付けされたファイル システムおよび Web データへのプログラムによる読み取り専用アクセスを提供します。 ADO アプリケーションでは、SQL クエリを使用してコンテンツおよびファイルのプロパティ情報を取得できます。

このプロバイダーはフリースレッドであり、Unicode に対応しています。

## <a name="connection-string-parameters"></a>接続文字列のパラメーター

このプロバイダーに接続するには、[ConnectionString](connectionstring-property-ado.md) プロパティの **Provider=** 引数を次のように設定します。

```vb 
 
MSIDXS 
```

[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。

## <a name="typical-connection-string"></a>標準的な接続文字列

このプロバイダーの標準的な接続文字列を次に示します。

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

この文字列は、次に示すキーワードで構成されています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>キーワード</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Provider</strong></p></td>
<td><p>OLE DB Provider for Microsoft Indexing Service を指定します。通常、この接続文字列ではこのキーワードのみを指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Data Source</strong></p></td>
<td><p>インデックス サービスのカタログ名を指定します。このキーワードを指定しない場合は、既定のシステム カタログが使用されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Locale Identifier</strong></p></td>
<td><p>ユーザーの言語に関する設定を指定する一意の 32 ビット番号 (1033 など) を指定します。これらの設定は、日付と時刻の形式、アルファベット順の並べ替え方法、文字列の比較方法などを示します。このキーワードを指定しない場合は、既定のシステム ロケール識別子が使用されます。</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>コマンド テキスト

インデックス サービスの SQL クエリの構文は、SQL-92 **SELECT** ステートメントおよびその **FROM** 句と **WHERE** 句の拡張機能で構成されます。クエリの結果は、OLE DB の行セットを通じて返され、ADO で利用して、 [Recordset](recordset-object-ado.md) オブジェクトとして操作できます。

正確に一致する語句の検索、ワイルドカードを使用したパターン検索や語幹検索を実行できます。検索ロジックでは、真偽判定、語の重要度、または他の語との類似性を基準にすることができます。"フリー テキスト" による検索も可能で、正確に一致する語ではなく、意味の一致するものを探すことができます。

このプロバイダーはストアド プロシージャの呼び出しや単純なテーブル名 (たとえば、[CommandType](commandtype-property-ado.md) が常に **adCmdText** である場合など) を受け付けません。

## <a name="recordset-behavior"></a>Recordset の動作

次の表は、このプロバイダーで開かれた **Recordset** オブジェクトで利用可能な機能の一覧です。 静的カーソルの種類 (**adOpenStatic**) のみを使用できます。

プロバイダーの構成による **Recordset** の動作の詳細については、 [Supports](supports-method-ado.md) メソッドを実行し、 [Recordset](properties-collection-ado.md) の **Properties** コレクションを列挙して、プロバイダー固有の動的プロパティが存在するかどうかを確認してください。

標準的な ADO **Recordset** のプロパティの利用可能性は、次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロパティ</p></th>
<th><p>可用性</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">ブックマーク</a>*</p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>常に <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>常に <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>常に <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>利用不可</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>読み取り/書き込み</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>読み取り専用</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">状態</a></p></td>
<td><p>読み取り専用</p></td>
</tr>
</tbody>
</table>


\*この機能を Recordset に存在するには、プロバイダーでブックマークを有効にする必要 **があります**。

標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Method</p></th>
<th><p>利用可能ですか?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate </a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">削除</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">開く</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-method-ado.md">再同期</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="odd">
<td><p><a href="supports-method-ado.md">サポート</a></p></td>
<td><p>必要</p></td>
</tr>
<tr class="even">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>いいえ</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>関連項目

Microsoft OLE DB Provider for Microsoft Indexing Service の実装方法および機能の詳細については、「Microsoft OLE DB Programmer's Reference」を参照してください。

