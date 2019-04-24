---
title: event理由列挙 (Access デスクトップデータベースリファレンス)
TOCTitle: EventReasonEnum
ms:assetid: 0639928e-d0ef-3db3-887e-f3da03913bc7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248815(v=office.15)
ms:contentKeyID: 48543047
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4948cd9a5f1436e4e1afc61bef87b63675e115ff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293330"
---
# <a name="eventreasonenum"></a>EventReasonEnum

**適用先:** Access 2013、Office 2013

イベントが発生した理由を表します。

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
<td><p><strong>adrsnaddnew</strong></p></td>
<td><p>1-d</p></td>
<td><p>新しいレコードが追加されました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrsnclose</strong></p></td>
<td><p>i-9</p></td>
<td><p><strong>Recordset</strong> が閉じられました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrsndelete</strong></p></td>
<td><p>pbm-2</p></td>
<td><p>レコードが削除されました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrsnfirstchange</strong></p></td>
<td><p>#</p></td>
<td><p>レコードに初めての変更が加えられました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrsnmove</strong></p></td>
<td><p>個</p></td>
<td><p><strong>Recordset</strong> 内のレコード ポインターが移動しました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrsnmovefirst</strong></p></td>
<td><p>個</p></td>
<td><p>レコード ポインターが <strong>Recordset</strong> の最初のレコードに移動しました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrsnmovelast</strong></p></td>
<td><p>約</p></td>
<td><p>レコード ポインターが <strong>Recordset</strong> の最後のレコードに移動しました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrsnmovenext</strong></p></td>
<td><p>スリー</p></td>
<td><p>レコード ポインターが <strong>Recordset</strong> の次のレコードに移動しました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnMovePrevious</strong></p></td>
<td><p>第</p></td>
<td><p>レコード ポインターが <strong>Recordset</strong> の前のレコードに移動しました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adrsnrequery</strong></p></td>
<td><p>7</p></td>
<td><p><a href="recordset-object-ado.md">Recordset</a> が再クエリされました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrsnresynch 同期</strong></p></td>
<td><p>~</p></td>
<td><p><strong>Recordset</strong> がデータベースと再同期しました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoAddNew</strong></p></td>
<td><p>5</p></td>
<td><p>新しいレコードの追加が取り消されました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adRsnUndoDelete</strong></p></td>
<td><p>シックス</p></td>
<td><p>レコードの削除が取り消されました。</p></td>
</tr>
<tr class="even">
<td><p><strong>adRsnUndoUpdate</strong></p></td>
<td><p>2/4</p></td>
<td><p>レコードの更新が取り消されました。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adrsnupdate</strong></p></td>
<td><p>1/3</p></td>
<td><p>既存のレコードが更新されました。</p></td>
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
<td><p>AdoEnums のイベント</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums を閉じます。</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の削除</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の変更</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の移動</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums のためのイベント</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums のためのイベント</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums のためのイベント</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums MOVEPREVIOUS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums の再クエリ</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の再同期</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums UNDOADDNEW</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums UNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums UNDOUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums の更新</p></td>
</tr>
</tbody>
</table>

