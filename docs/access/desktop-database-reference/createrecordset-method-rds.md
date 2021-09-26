---
title: CreateRecordset メソッド (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0665a57f3157fabceb954067d50d1583cb5bdfcb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626933"
---
# <a name="createrecordset-method-rds"></a>CreateRecordset メソッド (RDS)

**適用先**: Access 2013、Office 2013

空の、接続されていない [Recordset](recordset-object-ado.md) を作成します。

## <a name="syntax"></a>構文

*object*.CreateRecordset(*ColumnInfos*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Object* |[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトまたは [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*ColumnsInfos* |作成した **Recordset** の各列を定義する属性を、バリアント型 ( **Variant** ) の配列で指定します。 各列には、次の 4 つの必須属性と 1 つの省略可能な属性を持つ配列を定義します。 各列の配列は、 **Recordset** を定義する 1 つの配列にまとめられます。 属性の一覧については、次の表を参照してください。|

### <a name="variant-array-attributes"></a>バリアント配列の属性

|属性|説明|
|:--------|:----------|
|名前 |列のヘッダー名を指定します。|
|種類 |データ型の整数値を指定します。|
|Size |データ型にかかわらず、列の幅を文字数による整数値で指定します。|
|Nullability |ブール型の値を指定します。|
|スケール (オプション) |この属性は省略可能です。数値フィールドの小数値の桁数を定義します。この属性が省略された場合、小数点以下の桁数は 3 桁となり、4 桁以下は切り捨てられます。ただし、小数点以下の表示桁数が 3 桁になるだけで、精度には影響ありません。|

## <a name="remarks"></a>注釈

サーバー側のビジネス オブジェクトでは、株式相場のオペレーティング システム ファイルなど、OLE DB 以外のデータ プロバイダーのデータから、結果の **Recordset** を作成することができます。

次の表は、 [CreateRecordset](datatypeenum.md) メソッドでサポートされている **DataTypeEnum** 値の一覧です。一覧に示されている番号は、フィールドの定義に使用される参照番号です。

データ型は、固定長データ型または可変長データ型のいずれかです。固定長データ型では、サイズがあらかじめ決められていてもサイズの定義が要求されるため、サイズを -1 に定義する必要があります。可変長データ型では、1 ～ 32767 のサイズを指定できます。

可変長データ型では、次の表の「代入値」の欄に示されている値が強制的に使用されることがあります。代入値は、 **Recordset** が作成されて格納されるまでは参照できません。必要であれば、その後で、実際に使用されているデータ型を確認できます。

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>長さ</p></th>
<th><p>定数</p></th>
<th><p>番号</p></th>
<th><p>置換</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adTinyInt</strong></p></td>
<td><p>16 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adSmallInt</strong></p></td>
<td><p>2</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adInteger</strong></p></td>
<td><p>3</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adBigInt</strong></p></td>
<td><p>20</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedTinyInt</strong></p></td>
<td><p>17 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedSmallInt</strong></p></td>
<td><p>18 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedInt</strong></p></td>
<td><p>19</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adUnsignedBigInt</strong></p></td>
<td><p> 21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adSingle</strong></p></td>
<td><p>4 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDouble</strong></p></td>
<td><p>5</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adCurrency</strong></p></td>
<td><p>6 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>14 </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adNumeric</strong></p></td>
<td><p>131</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adBoolean</strong></p></td>
<td><p>11</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adError</strong></p></td>
<td><p>10</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adGuid</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adDate</strong></p></td>
<td><p>7 </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDBDate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adDBTime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDBTimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>7 </p></td>
</tr>
<tr class="odd">
<td><p>変数</p></td>
<td><p><strong>adBSTR</strong></p></td>
<td><p>8 </p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>変数</p></td>
<td><p><strong>adChar</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>変数</p></td>
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>変数</p></td>
<td><p><strong>adLongVarChar</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>変数</p></td>
<td><p><strong>adWChar</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>変数</p></td>
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>変数</p></td>
<td><p><strong>adLongVarWChar</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>変数</p></td>
<td><p><strong>adBinary</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>変数</p></td>
<td><p><strong>adVarBinary</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>変数</p></td>
<td><p><strong>adLongVarBinary</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>

