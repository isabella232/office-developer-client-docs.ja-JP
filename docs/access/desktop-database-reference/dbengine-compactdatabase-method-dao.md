---
title: DBEngine.CompactDatabase メソッド (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e898a089843774792b1ed48cea65086331a94ec6
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931219"
---
# <a name="dbenginecompactdatabase-method-dao"></a>DBEngine.CompactDatabase メソッド (DAO)

**適用されます**Access 2013 |。アクセス 2016

コピーし、閉じたデータベースを最適化およびそのバージョン、照合の順序、および暗号化を変更するオプションを使用します。 します (Microsoft Access ワークスペースのみ)。

> [!NOTE]
> 操作、更新、および SQL クエリを [SQL 更新ステートメント (CurrentDb.Execute [更新])] などの暗号化されたリンク テーブルを使用している場合は、暗号化キーを指定する必要があります。 また、リンク テーブルでは、暗号化キーの 19 文字制限があります。 このトピックの最後に**暗号化されたリンク テーブル**のセクションを参照してください。

## <a name="syntax"></a>構文

*式*です。CompactDatabase (***SrcName***、 ***DstName***、 ***DstLocale***、***オプション***、***パスワード***)

*式***DBEngine**オブジェクトを返すオブジェクト式を指定します。

### <a name="parameters"></a>パラメーター

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>名前</p></th>
<th><p>必須/オプション</p></th>
<th><p>データ型</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SrcName</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>既存の閉じているデータベースを識別します。 できます、完全なパスとファイル名の場合は、次のように&quot;C:\db1.mdb&quot;。 ファイル名に拡張子が含まれる場合、それも指定する必要があります。 ネットワークでサポートされている場合は、指定することもネットワーク パスでは、次のように&quot; \\server1\share1\dir1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p>DstName</p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>作成中の最適化されたデータベースのファイル名およびそのパス。ネットワーク パスを指定することもできます。この引数を使用して、SrcName と同じデータベース ファイルを指定することはできません。</p></td>
</tr>
<tr class="odd">
<td><p>DstLocale</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>「解説」に指定されているように、DstName の作成のための照合順序を指定する文字列式。</p>
<ul>
<li><p>この引数を省略すると、DstName のロケールは SrcName と同じになります。</p></li>
<li><p>パスワード文字列を連結することによって、DstName のパスワードを作成することもできます (で始まる&quot;; pwd =&quot;) を次のように、DstLocale の引数の定数: dbLangSpanish &amp; &quot;; pwd = NewPassword&quot;。</p></li>
<li><p>SrcName (既定値) と同じ DstLocale を使用していますが、新しいパスワードを指定する場合は、DstLocale のパスワード文字列を入力するだけで: &quot;; pwd = NewPassword&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>選択肢</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>省略可能。解説に指定されているように、1 つ以上のオプションを示す定数または定数の組み合わせ。対応する定数を加算すると、オプションを組み合わせることができます。</p></td>
</tr>
<tr class="odd">
<td><p>password</p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>データベースが暗号化されている場合に、暗号化キーを含む文字列式です。 文字列&quot;; pwd =&quot;実際のパスワードを付ける必要があります。 パスワード設定を DstLocale に含めると、この設定は無視されます。</p>

> [!NOTE]
> これは非推奨のパラメーターでありでサポートされていません。ACCDB 形式です。 暗号化します。ACCDB ファイルを使用して、"pwd ="オプション文字列。 [!メモ] パスワードには、大文字、小文字、数字、記号を組み合わせた複雑なものを使用してください。 これらの文字を混在させたものになっていないパスワードは強固とはいえません。 たとえば、Y6dh!et5 は安全性の高いパスワードです。 House27 は推測されやすいパスワードです。 また、高い安全性を保ちながらも、書き留めておかなくても覚えておくことができるパスワードを使用してください。


</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

次の定数のいずれかを DstLocale 引数に使用して、テキストの文字列比較を行う **CollatingOrder** プロパティを指定できます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>照合順序</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>英語、ドイツ語、フランス語、ポルトガル語、イタリア語、現代スペイン語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>アラビア語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>簡体字中国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>繁体字中国語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangCyrillic</strong></p></td>
<td><p>ロシア語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>チェコ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>オランダ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>ギリシャ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>ヘブライ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>ハンガリー語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>アイスランド語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>日本語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>韓国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>北欧諸国語 (Microsoft Jet データベース エンジン バージョン 1.0 のみ)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>ノルウェー語およびデンマーク語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>ポーランド語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>スロベニア語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>古スペイン語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>スウェーデン語およびフィンランド語</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>タイ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>トルコ語</p></td>
</tr>
</tbody>
</table>

<br/>

引数 options に以下のいずれかの定数を使用すると、最適化する際に暗号化するか、または解読するかを指定できます。

> [!NOTE]
> 定数 dbEncrypt と dbDecrypt は非推奨しでサポートされていません。ACCDB ファイル形式です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>最適化中にデータベースを暗号化します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecrypt</strong></p></td>
<td><p>最適化中にデータベースを解読します。</p></td>
</tr>
</tbody>
</table>

<br/>

暗号化の定数を省略するか、または **dbDecrypt** と **dbEncrypt** の両方を指定すると、DstName の暗号化の設定は SrcName と同じになります。

引数 options に次のいずれかの定数を使用すると、最適化されたデータベースのデータの形式のバージョンを指定できます。この定数は、DstName のデータ形式のバージョンだけに影響し、フォーム、レポートなどの Microsoft Access によって定義されたオブジェクトのバージョンには影響しません。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>最適化に Microsoft Jet データベース エンジン バージョン 1.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>最適化に Microsoft Jet データベース エンジン バージョン 1.1 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>最適化に Microsoft Jet データベース エンジン バージョン 2.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>最適化に Microsoft Jet データベース エンジン バージョン 3.0 のファイル形式 (バージョン 3.5 互換) を使用するデータベースを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>最適化に Microsoft Jet データベース エンジン バージョン 4.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>最適化に Microsoft Access データベース エンジン バージョン 12.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
</tbody>
</table>

<br/>

指定できるバージョン定数は 1 つだけです。バージョン定数を省略すると、DstName には SrcName と同じバージョンが指定されます。DstName は、SrcName と同じかまたはそれ以降のバージョンのみに最適化できます。

データベースのデータを変更するに従って、データベースのファイルは断片化され、必要以上のディスク容量を使用する可能性があります。 **CompactDatabase** メソッドを定期的に実行すると、データベースを最適化してファイルの断片化を解消できます。一般的に、最適化されたデータベースは小さく、実行速度も向上します。データベースをコピーして最適化する間に、照合順序、暗号化、およびデータ形式のバージョンを変更することもできます。

データベースを最適化する前に SrcName を閉じる必要があります。マルチユーザー環境では、最適化中に他のユーザーは SrcName を開くことはできません。SrcName が閉じていないか、または排他的に使用できない場合は、エラーが発生します。

**CompactDatabase** メソッドはデータベースのコピーを作成するので、元のデータベースとデータベースのコピーに対して十分なディスク容量が必要です。十分なディスク空き容量がない場合、最適化の操作は失敗します。複製する DstName のデータベースは、SrcName と同じディスクに保存する必要はありません。データベースの最適化が正常に終了した後に、元の SrcName ファイルを削除し、最適化された DstName ファイルを元のファイル名に変更できます。

**CompactDatabase** メソッドは、SrcName に指定されているデータベースから DstName に指定されているデータベースにすべてのデータおよびセキュリティ アクセス許可の設定をコピーします。

> [!NOTE]
> [!メモ] **CompactDatabase** メソッドは Microsoft Access オブジェクトを変換できないので、 **CompactDatabase** メソッドを使用してこのようなオブジェクトを含むデータベースを変換しないでください。

## <a name="encrypted-linked-tables"></a>暗号化されたリンク テーブル

暗号化されたパスワードは、使用するデータベースのファイル形式に依存します。Access 2003 (.mdb) 以前のデータベースを使用している場合、データベースを保護するために 1 つのパスワードがあり、データベースを暗号化するために別のパスワードがあります。Access 2007 (.accdb) 以降 (.mdb) のデータベースでは、データベースを暗号化して保護するには 1 つのパスワードのみを使用します。2 つのパスワードを使用するオプションはなくなりました。

> [!NOTE]
> Access 2007 (.accdb) データベースの場合、パスワードは暗号化キーです。

コマンド ボタンには、次のサンプル VBA コードを使用できます。

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

次のコード例は、CompactDatabase を使用して、パスワード (暗号化キー) を使用し、最適化されたデータベース内のテーブルにリンクする方法を示しています。 パスワードを入力する必要があることに注意してください。

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
