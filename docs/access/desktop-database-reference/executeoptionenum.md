---
title: ExecuteOptionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: aeb1083c693e0848e30a0b9217ae709994daddb5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477747"
---
# <a name="executeoptionenum"></a>ExecuteOptionEnum


**適用されます**Access 2013 |。Office 2013

プロバイダーによるコマンドの実行方法を表します。

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
<td><p><strong>adAsyncExecute</strong></p></td>
<td><p>0x10</p></td>
<td><p>コマンドを非同期に実行することを示します。
 この値は、<a href="commandtypeenum.md">CommandTypeEnum</a> の値 <strong>adCmdTableDirect</strong> と組み合わせて使用できません。</p></td>
</tr>
<tr class="even">
<td><p><strong>adAsyncFetch</strong></p></td>
<td><p>0x20</p></td>
<td><p><a href="cachesize-property-ado.md">CacheSize</a> プロパティで指定した初期量の残りの行を非同期に取得することを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adAsyncFetchNonBlocking</strong></p></td>
<td><p>0x40</p></td>
<td><p>取得中にメイン スレッドがブロックされないことを示します。 要求された行が取得されていない場合、現在の行は、ファイルの末尾に自動的に移動します。 永続的に保存された <strong>Recordset</strong> を持つ <a href="stream-object-ado.md">Stream</a> から <a href="recordset-object-ado.md">Recordset</a> を開いた場合、<strong>adAsyncFetchNonBlocking</strong> は無効になり、操作は同期で実行され、ブロッキングが発生します。 <a href="commandtypeenum.md">adCmdTableDirect</a> オプションを使用して <strong>Recordset</strong> を開いた場合、<strong>adAsynchFetchNonBlocking</strong> は無効になります。</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteNoRecords</strong></p></td>
<td><p>0x80</p></td>
<td><p>コマンド テキストは、コマンドまたはストアド プロシージャ (たとえば、だけデータを挿入するコマンド) の行を返さないことを示します。 すべての行を取得する場合、破棄され、返されません。 <strong>adExecuteNoRecords</strong>は、<strong>コマンド</strong>または<strong>接続</strong>の<strong>Execute</strong>メソッドにオプションのパラメーターとしてだけ渡すことができます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adExecuteStream</strong></p></td>
<td><p>0x400</p></td>
<td><p>コマンドの実行結果がストリームとして返されることを示します。
 <strong>adExecuteStream</strong>は、<strong>コマンド</strong>の<strong>Execute</strong>メソッドにオプションのパラメーターとしてだけ渡すことができます。</p></td>
</tr>
<tr class="even">
<td><p><strong>adExecuteRecord</strong></p></td>
<td><p><br />
</p></td>
<td><p><strong>CommandText</strong> が、<strong>Record</strong> オブジェクトとして返される単一の行を返すコマンドまたはストアド プロシージャであることを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOptionUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>コマンドが指定されていないことを示します。</p></td>
</tr>
</tbody>
</table>


**ADO/WFC 等価**

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
<td><p>AdoEnums.ExecuteOption.ASYNCEXECUTE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCH</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.ExecuteOption.NORECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.ExecuteOption.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

