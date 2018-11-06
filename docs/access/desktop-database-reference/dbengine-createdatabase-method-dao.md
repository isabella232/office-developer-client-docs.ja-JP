---
title: DBEngine.CreateDatabase メソッド (DAO)
TOCTitle: CreateDatabase Method
ms:assetid: d5821a4b-483a-b8fa-e929-5f036057d8c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835033(v=office.15)
ms:contentKeyID: 48547966
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052972
f1_categories:
- Office.Version=v15
ms.openlocfilehash: e9c77eabfc0689c6696c4ea6c8b4998b6b345458
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998351"
---
# <a name="dbenginecreatedatabase-method-dao"></a>DBEngine.CreateDatabase メソッド (DAO)

**適用されます**Access 2013、Office 2013。

新しい **[Database](database-object-dao.md)** オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた **Database** オブジェクトを取得します (Microsoft Access ワークスペースのみ)。

## <a name="syntax"></a>構文

*式*です。データベース (***名***、***ロケール***、***オプション***)

*式***DBEngine**オブジェクトを表す変数です。

## <a name="parameters"></a>パラメーター

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
<td><p><em>Name</em></p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><p>作成するデータベース ファイルの名前は、255 文字までの文字列です。 完全なパスとファイル名を指定できます。 ネットワークでサポートされている場合は、指定することもネットワーク パスでは、次のように&quot; \\server1\share1\dir1\db1&quot;。 のみ、このメソッドを使用して Microsoft Access データベース ファイルを作成できます。</p></td>
</tr>
<tr class="even">
<td><p><em>Locale</em></p></td>
<td><p>必須</p></td>
<td><p><strong>文字列型 (String)</strong></p></td>
<td><ul>
<li><p>[設定] で指定された、データベースを作成する際の照合順序を表す文字列式。この引数を指定しないと、エラーが発生します。  </p></li>
<li><p>パスワード文字列を連結して、新しい<strong>Database</strong>オブジェクトのパスワードを作成することもできます (で始まる&quot;; pwd =&quot; ) を次のように、引数<em>locale</em>の定数。</p></li>
<li><p>dbLangSpanish &amp; &quot;; pwd = NewPassword&quot;</p></li>
<li><p>既定の <em>locale</em> を使用し、パスワードを指定する場合は、単に <em>locale</em> 引数としてパスワード文字列を入力します。</p></li>
<li><p>&quot;pwd = NewPassword&quot;</p></li>
<li><p>大文字、小文字、数字、記号を組み合わせた強力なパスワードを使用してください。これらの文字を混在させていないパスワードは脆弱なパスワードです。Y6dh!et5 は強力なパスワードです。House27 は脆弱なパスワードです。強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。  </p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>省略可能</p></td>
<td><p><strong>バリアント型 (Variant)</strong></p></td>
<td><p>1 つ以上のオプションを示す定数 (または定数の組み合わせ)。オプションを組み合わせるには、対応する定数を追加します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

次の定数のいずれかを引数 locale に使用して、文字列比較を行うテキストの **[CollatingOrder](database-collatingorder-property-dao.md)** プロパティを指定できます。

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


次の定数 (複数可) を options 引数に使用して、データ形式のバージョン、およびデータベースを暗号化するかどうかを指定できます。

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
<td><p>暗号化されたデータベースを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Microsoft Jet データベース エンジン バージョン 1.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Microsoft Jet データベース エンジン バージョン 1.1 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Microsoft Jet データベース エンジン バージョン 2.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Microsoft Jet データベース エンジン バージョン 3.0 のファイル形式 (バージョン 3.5 と互換性がある) を使用するデータベースを作成します。</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Microsoft Jet データベース エンジン バージョン 4.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Microsoft Access データベース エンジン バージョン 12.0 のファイル形式を使用するデータベースを作成します。</p></td>
</tr>
</tbody>
</table>


暗号化の定数を省略した場合は、 **CreateDatabase** により暗号化されていないデータベースが作成されます。

**CreateDatabase** メソッドを使用して、新しい空のデータベースを作成して開き、 **Database** オブジェクトを取得します。このオブジェクトの構造と内容は、追加の DAO オブジェクトを使用して完成させる必要があります。既存のデータベースの部分的または完全なコピーを作成する場合は、 **[CompactDatabase](dbengine-compactdatabase-method-dao.md)** メソッドを使用してカスタマイズ可能なコピーを作成できます。

