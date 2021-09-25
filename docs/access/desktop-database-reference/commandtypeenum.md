---
title: CommandTypeEnum (Access デスクトップ データベースリファレンス)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: df4cd648d900e62fc699f1cd96286bd196c4eeb9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565787"
---
# <a name="commandtypeenum"></a>CommandTypeEnum

**適用先:** Access 2013、Office 2013

コマンド引数の解釈方法を表します。

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
<td><p><strong>adCmdUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>コマンドの種類の引数を指定しません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdText</strong></p></td>
<td><p>1</p></td>
<td><p><a href="commandtext-property-ado.md">CommandText</a> を、コマンドまたはストアド プロシージャのテキスト定義として評価します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTable</strong></p></td>
<td><p>2</p></td>
<td><p><strong>CommandText</strong> を、内部的に生成された SQL クエリから返された列のみで構成されるテーブル名として評価します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdStoredProc</strong></p></td>
<td><p>4 </p></td>
<td><p><strong>CommandText</strong> をストアド プロシージャ名として評価します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdUnknown</strong></p></td>
<td><p>8 </p></td>
<td><p>既定値。<strong>CommandText</strong> プロパティのコマンドの種類が不明であることを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adCmdFile</strong></p></td>
<td><p>256</p></td>
<td><p><strong>CommandText</strong> を、保存された <a href="recordset-object-ado.md">Recordset</a> のファイル名として評価します。<strong>Recordset</strong>.<a href="open-method-ado-recordset.md">Open</a> または <a href="requery-method-ado.md">Requery</a> と組み合わせてのみ使用できます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCmdTableDirect</strong></p></td>
<td><p>512</p></td>
<td><p><strong>CommandText</strong> を、すべての列が返されたテーブル名として評価します。 <strong>Recordset.Open</strong> または <strong>Requery</strong> と組み合わせてのみ使用できます。 <a href="seek-method-ado.md">Seek</a> メソッドを使用する場合、<strong>Recordset</strong> は <strong>adCmdTableDirect</strong> を指定して開く必要があります。 この値は、<a href="executeoptionenum.md">ExecuteOptionEnum</a> の値 <strong>adAsyncExecute</strong> と組み合わせて使用できません。</p></td>
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
<td><p>AdoEnums.CommandType.UNSPECIFIED</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.TEXT</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.STOREDPROC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.UNKNOWN</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CommandType.FILE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CommandType.TABLEDIRECT</p></td>
</tr>
</tbody>
</table>

