---
title: SendEmail マクロ アクション
TOCTitle: SendEmail Macro Action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: db82c2d0c8350d517044df5848f8c264b92e928d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477270"
---
# <a name="sendemail-macro-action"></a>SendEmail マクロ アクション


**適用されます**Access 2013 |。Office 2013

**SendEmail** マクロ アクションは、電子メール メッセージを送信します。


> [!NOTE]
> <P>[!メモ] <STRONG>SendEmail</STRONG> アクションは、データ マクロでのみ使用できます。</P>



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
<td><p>[メッセージの [<strong>宛先</strong>] 行を追加する名前を持つメッセージの受信者です。セミコロン (;) でこの引数に (および、 <em>Cc</em>と<em>Bcc</em>の引数) を指定した受信者の名前を区切ります。</p></td>
</tr>
<tr class="even">
<td><p><strong>Cc/CC</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メッセージの受信者、[cc] に入力する名前 (&quot;カーボン コピー&quot;)、メッセージ内の行です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bcc/BCC</strong></p></td>
<td><p>いいえ</p></td>
<td><p>メッセージの宛先、Bcc に入力する名前 (&quot;ブラインド カーボン コピー&quot;)、メッセージ内の行です。</p></td>
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


## <a name="remarks"></a>解説

**SendEmail** アクションは、 **[After Delete](after-delete-macro-event.md)** マクロ イベント、 **[After Insert](after-insert-macro-event.md)** マクロ イベント、および **[After Update](after-update-macro-event.md)** マクロ イベントでのみ使用できます。

**SendEmail** アクションでは、メッセージを表示し、編集することはできません。

