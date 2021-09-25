---
title: Cancel メソッド (ADO)
TOCTitle: Cancel method (ADO)
ms:assetid: 747edc04-a5cc-3631-2d0b-82e7e41a76b7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249476(v=office.15)
ms:contentKeyID: 48545662
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231032
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 8b8836ddc9e47334bb706050472088bbb585df6e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59558654"
---
# <a name="cancel-method-ado"></a>Cancel メソッド (ADO)

**適用先:** Access 2013、Office 2013

保留中の非同期メソッド呼び出しの実行を取り消します。

## <a name="syntax"></a>構文

*object*.キャンセル

## <a name="remarks"></a>注釈

非同期メソッド呼び出し (つまり、**adAsyncConnect**、**adAsyncExecute**、または **adAsyncFetch** オプションを指定して呼び出されたメソッド) の実行を中止するには、**Cancel** メソッドを使用します。

次の表は、特定の種類のオブジェクトに対して **Cancel** メソッドを使用したときに中止される操作です。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><br />
<em>object</em> の値</p></th>
<th><p>最後の非同期呼び出しが中止されるメソッド</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="command-object-ado.md">Command</a></p></td>
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute</a></p></td>
</tr>
<tr class="even">
<td><p><a href="connection-object-ado.md">Connection</a></p></td>
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute</a> または <a href="open-method-ado-connection.md">Open</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Record</a></p></td>
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a>、<a href="deleterecord-method-ado.md">DeleteRecord</a>、<a href="moverecord-method-ado.md">MoveRecord</a>、または <a href="open-method-ado-record.md">Open</a></p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p><a href="open-method-ado-recordset.md">開く</a></p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p><a href="open-method-ado-stream.md">開く</a></p></td>
</tr>
</tbody>
</table>

