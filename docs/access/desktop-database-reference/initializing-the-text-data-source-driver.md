---
title: テキスト データ ソース ドライバーの初期化
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 9fbe8bcde259f69086c511ec0343d345a15aa425
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594091"
---
# <a name="initializing-the-text-data-source-driver"></a>テキスト データ ソース ドライバーの初期化

**適用先**: Access 2013、Office 2013

テキスト データ ソースと HTML データ ソースの両方に同じデータベース ドライバーが使用されます。

テキスト データ ソース データベース ドライバーをインストールすると、セットアップ プログラムは、エンジンおよび ISAM Formats サブキーの Microsoft Windows レジストリに一連の既定値を書き込みます。 これらの設定は直接変更する必要があります。これらの設定を追加、削除、または変更するには、アプリケーションのセットアップ プログラムを使用します。 次のセクションでは、テキスト データ ソース データベース ドライバーの初期化と ISAM 形式の設定について説明します。

## <a name="text-data-source-initialization-settings"></a>テキスト データ ソースの初期化設定

Access **Connectivity Engine \\ ISAM Formats \\ Text** フォルダーには、テキスト データ ファイルへの外部アクセスに使用される Acetxt.dll ドライバーの初期化設定が含まれています。 通常、このキーのエントリの設定は次のようになっています。

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

Microsoft Access データベース エンジンで使用される、Text キーのエントリを次に示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Acetxt.dll の格納場所です。このフル パスはインストール時に決まります。値の型は REG_SZ 型です。</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>列のデータ型を推測する場合にスキャンする行の数です。0 に設定した場合はファイル全体が検索されます。既定値は 25 です。値の型は REG_DWORD 型です。</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>テーブルの 1 行目に列名があるかどうかを示すバイナリ値です。値 01 では、インポート時に列名が 1 行目に設定されます。</p></td>
</tr>
<tr class="even">
<td><p>CharacterSet</p></td>
<td><p>テキスト ページの格納方法を示すインジケーターです。設定可能な値は次のいずれかです。</p>
<p></p>
<ul>
<li><p>ANSI - ANSI コード ページで格納します。AnsiToUnicode および UnicodeToAnsi による変換が行われます</p></li>
<li><p>OEM - OEM コード ページで格納します。OemToUnicode および UnicodeToOem による変換が行われます。</p></li>
<li><p>Unicode - コード ページの変換は行われません。</p></li>
<li><p>&lt;10 進数&gt; - 特定の文字セットのコード ページ番号です。Unicode との変換が行われます。</p></li>
</ul>
<p></p>
<p>既定値は ANSI です。値の型は REG_SZ 型です。</p></td>
</tr>
<tr class="odd">
<td><p>形式</p></td>
<td><p>TabDelimited、CSVDelimited、Delimited (&lt;1 文字&gt;) のいずれかを指定できます。 区切り文字形式の 1 文字区切り文字は、二重引用符 ( ) を除く任意の 1 文字を指定できます &quot; 。 既定値は CSVDelimited です。 値の型は REG_SZ 型です。</p></td>
</tr>
<tr class="even">
<td><p>拡張機能</p></td>
<td><p>テキスト ベースのデータを探す場合に参照されるファイルの拡張子です。既定値は、txt、csv、tab、および asc です。値の型は REG_SZ 型です。</p></td>
</tr>
<tr class="odd">
<td><p>ExportCurrencySymbols</p></td>
<td><p>通貨フィールドをエクスポートする場合に、適切な通貨記号を追加するかどうかを示すバイナリ値です。値 01 は通貨記号を追加することを示し、値 00 は数値データのみをエクスポートすることを示します。既定値は 01 です。値の型は REG_BINARY 型です。</p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a>テキスト データ ソースの ISAM 形式

Access **Connectivity Engine \\ ISAM Formats \\ Text フォルダー** には、次のエントリが含まれます。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ名</p></th>
<th><p>型</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>テキスト</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>テキスト ファイル (*.txt、*.csv、*.tab、および *.asc)</p></td>
</tr>
<tr class="odd">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>テキスト ファイル (*.txt、*.csv、*.tab、および *.asc)</p></td>
</tr>
<tr class="even">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="odd">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>外部ファイルのデータをカレント データベースにインポートします。カレント データベースのデータを変更しても、外部ファイルのデータは変更されません。</p></td>
</tr>
<tr class="even">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>外部ファイルにリンクされているテーブルをカレント データベース内に作成します。カレント データベースのデータを変更すると、外部ファイルのデータも変更されます。</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>カレント データベースからテキスト ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。

## <a name="html-import-isam-formats"></a>HTML インポート ISAM 形式

Access **Connectivity Engine \\ ISAM Formats \\ HTML Import フォルダー** には、次のエントリが含まれます。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ名</p></th>
<th><p>型</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>テキスト</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML ファイル (*.ht*)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextImport</p></td>
<td><p>REG_SZ</p></td>
<td><p>外部ファイルのデータをカレント データベースにインポートします。カレント データベースのデータを変更しても、外部ファイルのデータは変更されません。</p></td>
</tr>
<tr class="odd">
<td><p>ResultTextLink</p></td>
<td><p>REG_SZ</p></td>
<td><p>外部ファイルにリンクされているテーブルをカレント データベース内に作成します。カレント データベースのデータを変更すると、外部ファイルのデータも変更されます。</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。

## <a name="html-export-isam-formats"></a>HTML エクスポート ISAM 形式

Access **Connectivity Engine \\ ISAM Formats \\ HTML Export フォルダー** には、次のエントリが含まれます。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ名</p></th>
<th><p>型</p></th>
<th><p>値</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>テキスト</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>HTML ファイル (*.htm)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>カレント データベースからテキスト ファイルにデータをエクスポートします。既存のファイルにエクスポートする場合、ファイル内のデータは上書きされます。</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] Windows レジストリの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a>テキストおよび HTML データSchema.iniファイルをカスタマイズする

テキスト データと HTML データの読み取り、インポート、またはエクスポートを行うには、Schema.ini ファイルを作成してその中にテキストの ISAM 情報を追加する必要があります。Schema.ini には、テキスト ファイルの書式化方法、インポート時の読み取り方法、ファイルへの既定のエクスポート書式など、データ ソースの仕様を記述します。次の例では、固定長のファイルである Filename.txt に対するレイアウトを示しています。

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

同様に、区切り記号付きファイルの書式は次のように指定します。

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

データを区切り記号付きテキスト ファイルにエクスポートする場合は、そのファイルに対して同様に次の書式を指定します。

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

My Special Export の例では、特定のエクスポート オプションについて説明しています。接続時にはさまざまなエクスポート オプションを指定できます。また、この最後の例は、接続時に必要に応じて渡すことのできるデータ ソース名 (DSN) にも対応しています。この 3 つの書式セクションは、すべて同じ .ini ファイルに追加できます。

Microsoft Access データベース エンジンで使用される、Schema.ini のエントリを次に示します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>エントリ</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>ColNameHeader</p></td>
<td><p>データの最初のレコードを列名に指定する <strong>True</strong> 、または <strong>False</strong> を設定できます。</p></td>
</tr>
<tr class="even">
<td><p>Format</p></td>
<td><p>TabDelimited、CSVDelimited、Delimited (&lt;1 文字&gt;)、FixedLength のいずれかを指定できます。 区切り文字で区切られたファイル形式に指定する区切り記号は、二重引用符 ( ) を除く任意の 1 文字を指定できます &quot; 。</p></td>
</tr>
<tr class="odd">
<td><p>FixedFormat</p></td>
<td><p>Format を FixedLength に指定した場合にのみ使用します。RaggedEdge は、行を復帰改行文字で終えるようにします。RaggedEdge は、行を復帰改行文字で終えるようにします。TrueFixedLength は、各行が決まった文字数になるようにします。復帰改行文字は、行の境界には存在せず、フィールドに埋め込まれていると見なされます。この設定がない場合、既定値は RaggedEdge です。</p></td>
</tr>
<tr class="even">
<td><p>MaxScanRows</p></td>
<td><p>列のデータ型を推測する場合にスキャンする行の数です。0 に設定した場合はファイル全体が検索されます。</p></td>
</tr>
<tr class="odd">
<td><p>CharacterSet</p></td>
<td><p>OEM、ANSI、UNICODE、または有効なコード ページの 10 進数の番号を設定できます。ソース ファイルの文字セットを示します。</p></td>
</tr>
<tr class="even">
<td><p>DateTimeFormat</p></td>
<td><p>日付と時刻を示す書式文字列を設定できます。このエントリは、インポートまたはエクスポート時にすべての "日付/時刻" フィールドを同じ書式で処理する場合に指定します。AM と PM を除くすべての Microsoft Jet データベース エンジンの書式がサポートされています。書式文字列を省略した場合は、Windows コントロール パネルで設定されている時刻の形式と日付の短い形式が使用されます。</p></td>
</tr>
<tr class="odd">
<td><p>CurrencySymbol</p></td>
<td><p>テキスト ファイルの通貨数値に使われる通貨記号を示します。ドル記号 ($) や Dm などがあります。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="even">
<td><p>CurrencyPosFormat</p></td>
<td><p>次のいずれかの値を設定できます: 空白のない通貨記号プレフィックス ($1)、空白のない通貨記号サフィックス (1$)、空白が 1 文字分ある通貨記号プレフィックス ($ 1)、Curren空白が 1 文字分ある通貨記号サフィックス (1 $)。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyDigits</p></td>
<td><p>通貨値の端数部分の桁数を指定します。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="even">
<td><p>CurrencyNegFormat</p></td>
<td><p>次のいずれかの値を指定できます。($1) –$1 $-1 $1 – (1$) –1$ 1–$1$– –1 $– –$ 1 1 $– $ 1 – $ 1 – $ 1 – $1 – $1 ( $ 1) ($ 1$) ドル記号は、この例の目的のために表示されますが、実際のプログラムの適切な CurrencySybol 値に置き換える必要があります。 このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="odd">
<td><p>CurrencyThousandSymbol</p></td>
<td><p>テキスト ファイルの通貨値を 3 桁ごとに区切る場合に使用する 1 文字の記号を示します。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="even">
<td><p>CurrencyDecimalSymbol</p></td>
<td><p>通貨値の整数部分と端数部分を区切るために使用する任意の 1 文字を設定できます。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="odd">
<td><p>DecimalSymbol</p></td>
<td><p>数値の整数部分と端数部分を区切るために使用する任意の 1 文字を設定できます。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="even">
<td><p>NumberDigits</p></td>
<td><p>数値の端数部分の桁数を示します。このエントリを省略した場合は、Windows コントロール パネルの既定値が使用されます。</p></td>
</tr>
<tr class="odd">
<td><p>NumberLeadingZeros</p></td>
<td><p>-1 を超え、1 未満の 10 進値の先頭に 0 を付けるかどうかを指定します。値は False (先頭に 0 を付けない) または True を指定できます。</p></td>
</tr>
<tr class="even">
<td><p>Col1, Col2, …</p></td>
<td><p>Lists the columns in the text file to be read. このエントリの形式は<em>、Coln</em> = <em>columnName</em>型 [Width ] columnName : 埋め込みスペースを含む列名を二重引用符で囲む <em>#</em> 必要があります。 <em></em> <em>type</em>: Can can bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime. Binary, OLE, Text, or Memo. さらに、次の ODBC テキスト ドライバーの種類がサポートされています。 Char (Text と同じ) Float (Double と同じ) 整数<em></em>(Short と同じ) LongChar (メモと同じ) 日付形式 メモ型の場合は、追加の書式マーカー [属性ハイパーリンク] を使用して、Microsoft Access でアクティブな URL である必要がある列を指定できます。 In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</p></td>
</tr>
<tr class="odd">
<td><p>TextDelimiter</p></td>
<td><p>特殊文字を含む文字列を区切るために使用する 1 つの文字を設定できます ("abc"、"xyz,pqr"、"hij" など)。 例: &quot;abc &quot; 、 xyz,pqr 、 hij このエントリが存在しない場合、既定の区切り記号は &quot; &quot; &quot; &quot; 二重引用符です。 このエントリが文字列 none &quot; の場合 &quot; 、文字は区切り文字として扱われます。</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> [!メモ] Schema.ini ファイルの設定を変更した場合は、新しい設定内容を有効にするために、データベース エンジンをいったん終了してから再起動する必要があります。


