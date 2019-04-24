---
title: CreateDatabase メソッド (DAO)
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
localization_priority: Normal
ms.openlocfilehash: 13e41dcd182f720b3611108311db6cd56fb4847e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294366"
---
# <a name="dbenginecreatedatabase-method-dao"></a>CreateDatabase メソッド (DAO)

**適用先:** Access 2013、Office 2013

新しい **[Database](database-object-dao.md)** オブジェクトを作成し、そのデータベースをディスクに保存し、開かれた **Database** オブジェクトとして返します (Microsoft Access ワークスペースのみ)。 .

## <a name="syntax"></a>構文

*式*。CreateDatabase (***名前***、***ロケール***、***オプション***)

*式***DBEngine**オブジェクトを表す変数を取得します。

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
<td><p><em>名前</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><p>A String up to 255 characters long that is the name of the database file that you're creating. It can be the full path and file name. ネットワークでサポートされている場合は、server1\share1\dir1\db1 &quot; \\&quot;などのネットワークパスを指定することもできます。 You can only create Microsoft Access database files with this method.</p></td>
</tr>
<tr class="even">
<td><p><em>Locale</em></p></td>
<td><p>必須</p></td>
<td><p><strong>String</strong></p></td>
<td><ul>
<li><p>[設定] で指定された、データベースを作成する際の照合順序を表す文字列式。この引数を指定しないと、エラーが発生します。  </p></li>
<li><p>次に示すように、 <em>locale</em>引数の<strong></strong>定数に、(;p wd = &quot;&quot;で始まる) パスワード文字列を連結することによって、新しい Database オブジェクトのパスワードを作成することもできます。</p></li>
<li><p>dblangspanish &amp; &quot;語;p wd = NewPassword&quot;</p></li>
<li><p>既定の <em>locale</em> を使用し、パスワードを指定する場合は、単に <em>locale</em> 引数としてパスワード文字列を入力します。</p></li>
<li><p>&quot;;p wd = NewPassword&quot;</p></li>
<li><p>大文字、小文字、数字、記号を組み合わせた強力なパスワードを使用してください。これらの文字を混在させていないパスワードは脆弱なパスワードです。Y6dh!et5 は強力なパスワードです。House27 は脆弱なパスワードです。強力なパスワードでありながら、書き留めておかなくても覚えておくことができるパスワードを使用してください。  </p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><em>Option</em></p></td>
<td><p>Optional</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>1 つ以上のオプションを示す定数 (または定数の組み合わせ)。オプションを組み合わせるには、対応する定数を追加します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

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
<td><p><strong>dblanggeneral</strong></p></td>
<td><p>英語、ドイツ語、フランス語、ポルトガル語、イタリア語、現代スペイン語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblangarabic 語</strong></p></td>
<td><p>アラビア語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangchinesesimplified</strong></p></td>
<td><p>簡体字中国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblangchinesetraditional</strong></p></td>
<td><p>繁体字中国語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangcyrillic</strong></p></td>
<td><p>ロシア語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblangczech</strong></p></td>
<td><p>チェコ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangdutch 語</strong></p></td>
<td><p>オランダ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblanggreek 語</strong></p></td>
<td><p>ギリシャ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblanghebrew 語</strong></p></td>
<td><p>ヘブライ語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblanghungarian</strong></p></td>
<td><p>ハンガリー語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangicelandic 語</strong></p></td>
<td><p>アイスランド語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblangjapanese</strong></p></td>
<td><p>日本語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangkorean 語</strong></p></td>
<td><p>韓国語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblangnordic</strong></p></td>
<td><p>北欧諸国語 (Microsoft Jet データベース エンジン バージョン 1.0 のみ)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangnorwdan</strong></p></td>
<td><p>ノルウェー語およびデンマーク語</p></td>
</tr>
<tr class="even">
<td><p><strong>dblangpolish</strong></p></td>
<td><p>ポーランド語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangslovenian 語</strong></p></td>
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
<td><p><strong>dblangthai 語</strong></p></td>
<td><p>タイ語</p></td>
</tr>
<tr class="odd">
<td><p><strong>dblangturkish</strong></p></td>
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

