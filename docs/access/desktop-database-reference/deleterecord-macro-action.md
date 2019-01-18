---
title: DeleteRecord マクロ アクション
TOCTitle: DeleteRecord macro action
ms:assetid: c656a72c-c037-76a5-dc07-f6eccb6590dd
ms:mtpsurl: https://msdn.microsoft.com/library/Ff823132(v=office.15)
ms:contentKeyID: 48547624
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8fb20068052972696b09ea0d2165b344e97ea922
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725953"
---
# <a name="deleterecord-macro-action"></a>DeleteRecord マクロ アクション

**適用されます**Access 2013、Office 2013。

" **DeleteRecord/レコードの削除** " アクションを使用して、レコードを削除できます。

## <a name="setting"></a>設定

**CreateRecord** データ ブロックの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Record Alias/レコードの別名</strong></p></td>
<td><p>削除するレコードを識別する文字列です。 <em>別名</em>引数を指定しない場合は、現在のレコードが削除されます。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>備考

**LastCreateRecordIdentity** ローカル変数を使用して、 **CreateRecord** データ ブロックで一番新しく作成したレコードを操作できます。たとえば、次の構文では一番新しく作成したレコードを参照します。

`[LastCreateRecordIdentity]`

