---
title: DataTypeEnum (Access デスクトップデータベースリファレンス)
TOCTitle: DataTypeEnum
ms:assetid: a8ab7616-552f-ed5f-ed55-95254cfb374a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249780(v=office.15)
ms:contentKeyID: 48546904
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6ffba234ed1c5dc56138a665d6dd07038f55da7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294443"
---
# <a name="datatypeenum"></a>DataTypeEnum

**適用先:** Access 2013、Office 2013

Specifies the data type of a [Field](field-object-ado.md), [Parameter](parameter-object-ado.md), or [Property](property-object-ado.md). The corresponding OLE DB type indicator is shown in parentheses in the description column of the following table. ole db のデータ型の詳細については、「 *ole db プログラマリファレンス*」を参照してください。

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adarray<br />
</strong>(ADOX には適用されません)。</p></td>
<td><p>0x2000</p></td>
<td><p>常に別のデータ型定数と組み合わされ、そのデータ型の配列を示すフラグ値です。</p></td>
</tr>
<tr class="even">
<td><p><strong>adbigint</strong></p></td>
<td><p>1280</p></td>
<td><p>8 バイトの符号付き整数を示します (DBTYPE_I8)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adbinary</strong></p></td>
<td><p>128</p></td>
<td><p>バイナリ値を示します (DBTYPE_BYTES)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adboolean</strong></p></td>
<td><p>#</p></td>
<td><p>ブール値を示します (DBTYPE_BOOL)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adbstr</strong></p></td>
<td><p>~</p></td>
<td><p>null で終わる文字列 (Unicode) を示します (DBTYPE_BSTR)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adchapter</strong></p></td>
<td><p>136</p></td>
<td><p>子行セットの行を識別する 4 バイト チャプター値を示します (DBTYPE_HCHAPTER)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adchar</strong></p></td>
<td><p>129</p></td>
<td><p>文字列値を示します (DBTYPE_STR)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adcurrency</strong></p></td>
<td><p>シックス</p></td>
<td><p>通貨値を示します (DBTYPE_CY)。通貨型は小数点以下 4 桁の固定小数点の数値です。スケールが 10,000 の、8 バイトの符号付き整数で格納します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>addate</strong></p></td>
<td><p>7</p></td>
<td><p>日付値を示します (DBTYPE_DATE)。日付は倍精度浮動小数点数型 (Double) で格納され、整数部分は 1899 年 12 月 30 日からの日数を、小数部分は時刻を表します。</p></td>
</tr>
<tr class="even">
<td><p><strong>addbdate</strong></p></td>
<td><p>133</p></td>
<td><p>日付値 (yyyymmdd) を示します (DBTYPE_DBDATE)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>addbtime</strong></p></td>
<td><p>134</p></td>
<td><p>時刻値 (hhmmss) を示します (DBTYPE_DBTIME)。</p></td>
</tr>
<tr class="even">
<td><p><strong>addbtimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>日付/タイム スタンプ (yyyymmddhhmmss および 10 億分の 1 桁までの分数) を示します (DBTYPE_DBTIMESTAMP)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adDecimal</strong></p></td>
<td><p>第</p></td>
<td><p>固定精度およびスケールの正確な数値を示します (DBTYPE_DECIMAL)。</p></td>
</tr>
<tr class="even">
<td><p><strong>addouble</strong></p></td>
<td><p>5</p></td>
<td><p>倍精度浮動小数点値を示します (DBTYPE_R8)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adEmpty</strong></p></td>
<td><p>.0</p></td>
<td><p>値を指定しません (DBTYPE_EMPTY)。</p></td>
</tr>
<tr class="even">
<td><p><strong>aderror</strong></p></td>
<td><p>個</p></td>
<td><p>32 ビット エラー コードを示します (DBTYPE_ERROR)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfiletime</strong></p></td>
<td><p>64</p></td>
<td><p>1601 年 1 月 1 日からの時間を 100 ナノ秒単位で示す 64 ビット値を示します (DBTYPE_FILETIME)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adguid</strong></p></td>
<td><p>72</p></td>
<td><p>グローバル一意識別子 (GUID) を示します (DBTYPE_GUID)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIDispatch</strong></p></td>
<td><p>i-9</p></td>
<td><p>COM オブジェクトの <strong>IDispatch</strong> インターフェイスへのポインターを示します (DBTYPE_IDISPATCH)。</p><p><strong>注</strong>: 現在、このデータ型は ADO ではサポートされていません。 使用すると予期しない結果になることがあります。</p>
</td>
</tr>
<tr class="even">
<td><p><strong>adinteger</strong></p></td>
<td><p>1/3</p></td>
<td><p>4 バイトの符号付き整数を示します (DBTYPE_I4)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adIUnknown</strong></p></td>
<td><p>スリー</p></td>
<td><p>COM オブジェクトの <strong>IUnknown</strong> インターフェイスへのポインターを示します (DBTYPE_IUNKNOWN)。</p><p><strong>注</strong>: 現在、このデータ型は ADO ではサポートされていません。 使用すると予期しない結果になることがあります。
</p></td>
</tr>
<tr class="even">
<td><p><strong>adlongvarbinary</strong></p></td>
<td><p>205</p></td>
<td><p>ロング バイナリ値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adlongvarchar</strong></p></td>
<td><p>201</p></td>
<td><p>長い文字列値を示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adlongvarwchar</strong></p></td>
<td><p>203</p></td>
<td><p>長い、null で終わる Unicode 文字列値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p>固定精度およびスケールの正確な数値を示します (DBTYPE_NUMERIC)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adpropvariant</strong></p></td>
<td><p>138</p></td>
<td><p>オートメーション PROPVARIANT を示します (DBTYPE_PROP_VARIANT)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adsingle</strong></p></td>
<td><p>2/4</p></td>
<td><p>単精度浮動小数点値を示します (DBTYPE_R4)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adsmallint</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>2 バイトの符号付き整数を示します (DBTYPE_I2)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adtinyint</strong></p></td>
<td><p>16</p></td>
<td><p>1 バイトの符号付き整数を示します (DBTYPE_I1)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adアン signedbigint</strong></p></td>
<td><p>21</p></td>
<td><p>8 バイトの符号なし整数を示します (DBTYPE_UI8)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adアン signedint</strong></p></td>
<td><p>年</p></td>
<td><p>4 バイトの符号なし整数を示します (DBTYPE_UI4)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adアン signedsmallint</strong></p></td>
<td><p>個</p></td>
<td><p>2 バイトの符号なし整数を示します (DBTYPE_UI2)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adアン signedtinyint</strong></p></td>
<td><p>インチ</p></td>
<td><p>1 バイトの符号なし整数を示します (DBTYPE_UI1)。</p></td>
</tr>
<tr class="even">
<td><p><strong>aduserdefined 独自の方法</strong></p></td>
<td><p>132</p></td>
<td><p>ユーザー定義の変数を示します (DBTYPE_UDT)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>い</strong></p></td>
<td><p>204</p></td>
<td><p>バイナリ値を示します (<strong>Parameter</strong> オブジェクトのみ)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p>文字列値を示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVariant</strong></p></td>
<td><p>個</p></td>
<td><p>オートメーション バリアント型 (<strong>Variant</strong>) を示します (DBTYPE_VARIANT)。</p><p><strong>注</strong>: 現在、このデータ型は ADO ではサポートされていません。 使用すると予期しない結果になることがあります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adVarNumeric</strong></p></td>
<td><p>139</p></td>
<td><p>数値を示します (<strong>Parameter</strong> オブジェクトのみ)。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>null で終わる Unicode 文字列を示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adwchar</strong></p></td>
<td><p>130</p></td>
<td><p>null で終わる Unicode 文字列を示します (DBTYPE_WSTR)。</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>ADO/WFC と同等

パッケージ: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>定数</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums (データ形式)</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums DBTIME</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums のタイムスタンプ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の10進型</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。エラー</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。整数</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums (longvarbinary)</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums。 longvarchar</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。 longvarwchar</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums variant</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。アン signedbigint</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums/signedint</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums/signedsmallint</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums (アン)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums (VARBINARY)</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums。 varnumeric</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums。</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums</p></td>
</tr>
</tbody>
</table>

