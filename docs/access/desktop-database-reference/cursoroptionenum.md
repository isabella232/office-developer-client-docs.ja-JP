---
title: カーソル optionenum (Access デスクトップデータベースリファレンス)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7443e0cb29954fae9dfc193ffc6aa8dee9886089
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295199"
---
# <a name="cursoroptionenum"></a>CursorOptionEnum

**適用先:** Access 2013、Office 2013

[Supports](supports-method-ado.md) メソッドがテストする機能を表します。

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
<td><p><strong>adAddNew</strong></p></td>
<td><p>0x1000400</p></td>
<td><p>新しいレコードを追加する <a href="addnew-method-ado.md">AddNew</a> メソッドをサポートします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adapproxposition</strong></p></td>
<td><p>0x4000</p></td>
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a> プロパティと <a href="absolutepage-property-ado.md">AbsolutePage</a> プロパティをサポートします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adbookmark</strong></p></td>
<td><p>0x2000</p></td>
<td><p>特定のレコードへのアクセスを確保する <a href="bookmark-property-ado.md">Bookmark</a> プロパティをサポートします。</p></td>
</tr>
<tr class="even">
<td><p><strong>addelete</strong></p></td>
<td><p>0x1000800</p></td>
<td><p>レコードを削除する <a href="delete-method-ado-recordset.md">Delete</a> メソッドをサポートします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adfind</strong></p></td>
<td><p>0x80000</p></td>
<td><p><a href="recordset-object-ado.md">Recordset</a> 内の行の位置を確認する <a href="find-method-ado.md">Find</a> メソッドをサポートします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adHoldRecords</strong></p></td>
<td><p>0x100</p></td>
<td><p>保留中のすべての変更をコミットせずに、新たなレコードを格納するか、または次の格納位置を変更します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adindex</strong></p></td>
<td><p>0x100000</p></td>
<td><p>インデックスに名前を付ける <a href="index-property-ado.md">Index</a> プロパティをサポートします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adMovePrevious</strong></p></td>
<td><p>0x200</p></td>
<td><p>ブックマークを使用せずに現在のレコードの位置を後方に移動する <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> メソッドと <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> メソッド、および <a href="move-method-ado.md">Move</a> メソッドと <a href="getrows-method-ado.md">GetRows</a> メソッドをサポートします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adnotify</strong></p></td>
<td><p>0x40000</p></td>
<td><p>基になるデータ プロバイダーが通知をサポートしていることを示します (これにより <strong>Recordset</strong> イベントのサポートの有無が決まります)。</p></td>
</tr>
<tr class="even">
<td><p><strong>adresync</strong></p></td>
<td><p>0x20000</p></td>
<td><p>基になるデータベースのカーソルにある可視データを更新する <a href="resync-method-ado.md">Resync</a> メソッドをサポートします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adseek</strong></p></td>
<td><p>0x200000</p></td>
<td><p><strong>Recordset</strong> 内の行を検索する <a href="seek-method-ado.md">Seek</a> メソッドをサポートします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adUpdate</strong></p></td>
<td><p>0x1008000</p></td>
<td><p>既存のデータを変更する <a href="update-method-ado.md">Update</a> メソッドをサポートします。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUpdateBatch</strong></p></td>
<td><p>「その他」</p></td>
<td><p>複数の変更をグループとしてプロバイダーに送信するバッチ更新 (<a href="updatebatch-method-ado.md">UpdateBatch</a> メソッドと <a href="cancelbatch-method-ado.md">CancelBatch</a> メソッド) をサポートします。</p></td>
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
<td><p>AdoEnums オプション</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums のオプション。 approxposition</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums オプション。 BOOKMARK</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums を削除します。</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums オプション。検索</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums オプション。 HOLDRECORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums オプション。インデックス</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums オプション。 MOVEPREVIOUS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums オプションの通知</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums オプション。 RESYNC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums オプション。シーク</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums オプション</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums。 UPDATEBATCH</p></td>
</tr>
</tbody>
</table>

