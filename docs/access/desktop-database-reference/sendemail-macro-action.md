---
title: SendEmail マクロ アクション
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 191942c63bce2111c22f2fbc871513a3c30c7a40
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585341"
---
# <a name="sendemail-macro-action"></a>SendEmail マクロ アクション

**適用先**: Access 2013、Office 2013

**SendEmail アクションは** 電子メール メッセージを送信します。

> [!NOTE]
> **SendEmail** アクションは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

**SendEmail** アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>To/宛先</strong></p></td>
<td><p>はい</p></td>
<td><p>メッセージで [<strong>宛先</strong>] 行に含めるメッセージ受信者名。この引数 (および <em>Cc</em> 引数と <em>Bcc</em> 引数) で複数の受信者名を指定する場合は、セミコロン (;) で区切ります。</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc/CC</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メッセージの Cc (カーボン コピー) 行に名前を付け &quot; &quot; したいメッセージ受信者。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc/BCC</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メッセージの BCC (ブラインド カーボン コピー) 行に名前を付けしたい &quot; &quot; メッセージ受信者。</p></td>
</tr>
<tr class="even">
<td><p><strong>Subject/件名</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メッセージの件名。このテキストはメール メッセージの [ <strong>件名</strong> ] 行に表示されます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Body</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メール メッセージの本文に含めるテキスト。この引数を指定しない場合、メッセージにテキストが追加されません。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**SendEmail** アクションは、 **[After Delete](after-delete-macro-event.md)** マクロ イベント、 **[After Insert](after-insert-macro-event.md)** マクロ イベント、および **[After Update](after-update-macro-event.md)** マクロ イベントでのみ使用できます。

**SendEmail** アクションでは、メッセージを表示し、編集することはできません。

