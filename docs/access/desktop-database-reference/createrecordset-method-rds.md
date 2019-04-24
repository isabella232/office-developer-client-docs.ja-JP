---
title: CreateRecordset メソッド (RDS)
TOCTitle: CreateRecordset method (RDS)
ms:assetid: 19524509-31da-9af1-4062-cd3c59b51278
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248940(v=office.15)
ms:contentKeyID: 48543497
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3dda0840617c32e9dceea3bd1baa362c5652a373
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295339"
---
# <a name="createrecordset-method-rds"></a>CreateRecordset メソッド (RDS)

**適用先:** Access 2013、Office 2013

空の、接続されていない [Recordset](recordset-object-ado.md) を作成します。

## <a name="syntax"></a>構文

*オブジェクト*。CreateRecordset (*columninfos*)

## <a name="parameters"></a>パラメーター

|パラメーター|説明|
|:--------|:----------|
|*Object* |[RDSServer.DataFactory](datafactory-object-rdsserver.md) オブジェクトまたは [RDS.DataControl](datacontrol-object-rds.md) オブジェクトを表すオブジェクト変数を指定します。|
|*コラムの「」の「コラム」* |作成した **Recordset** の各列を定義する属性を、バリアント型 ( **Variant** ) の配列で指定します。 各列には、次の 4 つの必須属性と 1 つの省略可能な属性を持つ配列を定義します。 各列の配列は、 **Recordset** を定義する 1 つの配列にまとめられます。 属性の一覧については、次の表を参照してください。|

### <a name="variant-array-attributes"></a>バリアント型 (Variant) 配列の属性

|属性|説明|
|:--------|:----------|
|名前 |列のヘッダー名を指定します。|
|型 |データ型の整数値を指定します。|
|サイズ |データ型にかかわらず、列の幅を文字数による整数値で指定します。|
|属性 |ブール型の値を指定します。|
|Scale (省略可能) |この属性は省略可能です。数値フィールドの小数値の桁数を定義します。この属性が省略された場合、小数点以下の桁数は 3 桁となり、4 桁以下は切り捨てられます。ただし、小数点以下の表示桁数が 3 桁になるだけで、精度には影響ありません。|

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
<th><p>Length</p></th>
<th><p>定数</p></th>
<th><p>番号</p></th>
<th><p>入れ替え</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adtinyint</strong></p></td>
<td><p>16</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adsmallint</strong></p></td>
<td><p>pbm-2</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adinteger</strong></p></td>
<td><p>1/3</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adbigint</strong></p></td>
<td><p>1280</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adアン signedtinyint</strong></p></td>
<td><p>インチ</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adアン signedsmallint</strong></p></td>
<td><p>個</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adアン signedint</strong></p></td>
<td><p>年</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adアン signedbigint</strong></p></td>
<td><p>21</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adsingle</strong></p></td>
<td><p>2/4</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>addouble</strong></p></td>
<td><p>5</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>adcurrency</strong></p></td>
<td><p>シックス</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adDecimal</strong></p></td>
<td><p>第</p></td>
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
<td><p><strong>adboolean</strong></p></td>
<td><p>#</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>aderror</strong></p></td>
<td><p>個</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>adguid</strong></p></td>
<td><p>72</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>addate</strong></p></td>
<td><p>7</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>addbdate</strong></p></td>
<td><p>133</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Fixed</p></td>
<td><p><strong>addbtime</strong></p></td>
<td><p>134</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Fixed</p></td>
<td><p><strong>addbtimestamp</strong></p></td>
<td><p>135</p></td>
<td><p>7</p></td>
</tr>
<tr class="odd">
<td><p>可変</p></td>
<td><p><strong>adbstr</strong></p></td>
<td><p>~</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>可変</p></td>
<td><p><strong>adchar</strong></p></td>
<td><p>129</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>可変</p></td>
<td><p><strong>adVarChar</strong></p></td>
<td><p>200</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>可変</p></td>
<td><p><strong>adlongvarchar</strong></p></td>
<td><p>201</p></td>
<td><p>200</p></td>
</tr>
<tr class="odd">
<td><p>可変</p></td>
<td><p><strong>adwchar</strong></p></td>
<td><p>130</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>可変</p></td>
<td><p><strong>adVarWChar</strong></p></td>
<td><p>202</p></td>
<td><p>130</p></td>
</tr>
<tr class="odd">
<td><p>可変</p></td>
<td><p><strong>adlongvarwchar</strong></p></td>
<td><p>203</p></td>
<td><p>130</p></td>
</tr>
<tr class="even">
<td><p>可変</p></td>
<td><p><strong>adbinary</strong></p></td>
<td><p>128</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>可変</p></td>
<td><p><strong>い</strong></p></td>
<td><p>204</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>可変</p></td>
<td><p><strong>adlongvarbinary</strong></p></td>
<td><p>205</p></td>
<td><p>204</p></td>
</tr>
</tbody>
</table>

