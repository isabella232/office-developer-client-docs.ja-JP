---
title: Microsoft OLE DB Provider for Microsoft Active Directory Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c1555883ef8305225d6ddd1969d98de082288a6b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887538"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a>Microsoft OLE DB Provider for Microsoft Active Directory Service

**適用されます**Access 2013、Office 2013。

Microsoft Active Directory Service Interfaces (ADSI) プロバイダーを使用すると、ADO から ADSI をとおして異種ディレクトリ サービスに接続できます。これによって、ADO アプリケーションでは、Microsoft Windows NT 4.0 および Microsoft Windows 2000 のディレクトリ サービス、LDAP 準拠のディレクトリ サービス、および Novell Directory Services に対する読み取り専用アクセスが可能になります。ADSI 自体がプロバイダー モデルに基づいているので、新しいプロバイダーで別のディレクトリへのアクセスを提供する場合でも、ADO アプリケーションはシームレスにアクセスできます。ADSI プロバイダーはフリースレッドであり、Unicode に対応しています。

## <a name="connection-string-parameters"></a>接続文字列のパラメーター

このプロバイダーに接続するには、**ConnectionString** プロパティの [Provider](connectionstring-property-ado.md) 引数を次のように設定します。

```vb 
 
ADSDSOObject 
```

[Provider](provider-property-ado.md) プロパティを取得した場合も、この文字列が返されます。

## <a name="typical-connection-string"></a>標準的な接続文字列

このプロバイダーの標準的な接続文字列を次に示します。

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
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
<td><p>OLE DB Provider for Microsoft Active Directory Service を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>User ID</strong></p></td>
<td><p>ユーザー名を指定します。このキーワードを省略すると、現在のログオンが使用されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>ユーザー パスワードを指定します。このキーワードを省略すると、現在のログオンが使用されます。</p></td>
</tr>
</tbody>
</table>


**コマンド テキスト**

このプロバイダーで認識されるコマンド テキストの文字列は 4 つの値で構成され、その構文は次のとおりです。

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Root</em></p></td>
<td><p>検索を開始する <strong>ADsPath</strong> オブジェクト (つまり、検索のルート) を示します。</p></td>
</tr>
<tr class="even">
<td><p><em>Filter</em></p></td>
<td><p>RFC 1960 形式の検索フィルターを示します。</p></td>
</tr>
<tr class="odd">
<td><p><em>Attributes</em></p></td>
<td><p>返される属性をコンマ区切りの一覧で示します。</p></td>
</tr>
<tr class="even">
<td><p><em>スコープ</em></p></td>
<td><p>省略可能。 検索のスコープを指定する<strong>文字列</strong>です。 次のいずれか: 基本: ベース オブジェクト (検索のルート) のみを検索します。<br />
1 レベル-は、1 レベルのみを検索します。<br />
サブツリー-は、サブツリー全体を検索します。</p></td>
</tr>
</tbody>
</table>


次に例を示します。

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

このプロバイダーは、コマンド テキストとして SQL SELECT もサポートしています。次に例を示します。

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

このプロバイダーはストアド プロシージャの呼び出しや単純なテーブル名 (たとえば、[CommandType](commandtype-property-ado.md) が常に **adCmdText** である場合など) を受け付けません。コマンド テキストの要素の詳細については、Active Directory Service Interfaces のマニュアルを参照してください。

## <a name="recordset-behavior"></a>Recordset の動作

次の表は、このプロバイダーで開かれた [Recordset](recordset-object-ado.md) オブジェクトで利用可能な機能の一覧です。 静的カーソルの種類 (**adOpenStatic**) のみがあります。

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
<th><p>利用可能性</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>値の取得のみ</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>値の取得のみ</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>常に <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">カーソル。</a></p></td>
<td><p>常に <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>常に <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>値の取得のみ</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">ロック。</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">スレッド</a></p></td>
<td><p>利用不可</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>値の取得のみ</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>値の取得のみ</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>値の取得および設定</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>値の取得のみ</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>値の取得のみ</p></td>
</tr>
</tbody>
</table>


標準的な ADO **Recordset** のメソッドの利用可能性は、次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>メソッド</p></th>
<th><p>利用可能性</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Cancel</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">再同期</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">サポートしています</a></p></td>
<td><p>はい</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Update</a></p></td>
<td><p>いいえ</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>いいえ</p></td>
</tr>
</tbody>
</table>

