---
title: SendEmail マクロ アクション
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314652"
---
# <a name="sendemail-macro-action"></a>SendEmail マクロ アクション

**適用先:** Access 2013、Office 2013

**SendEmail**アクションは、電子メールメッセージを送信します。

> [!NOTE]
> **SendEmail** アクションは、データ マクロでのみ使用できます。

## <a name="setting"></a>Setting

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
<td><p>メッセージの Cc (&quot;カーボンコピー&quot;) 行に配置するメッセージの受信者名。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc/BCC</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メッセージの Bcc (&quot;ブラインドカーボンコピー&quot;) 行に配置するメッセージの受信者名を指定します。</p></td>
</tr>
<tr class="even">
<td><p><strong>Subject/件名</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メッセージの件名。このテキストはメール メッセージの [ <strong>件名</strong> ] 行に表示されます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Body/本文</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メール メッセージの本文に含めるテキスト。この引数を指定しない場合、メッセージにテキストが追加されません。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

**SendEmail** アクションは、 **[After Delete](after-delete-macro-event.md)** マクロ イベント、 **[After Insert](after-insert-macro-event.md)** マクロ イベント、および **[After Update](after-update-macro-event.md)** マクロ イベントでのみ使用できます。

**SendEmail** アクションでは、メッセージを表示し、編集することはできません。

