---
title: SendKeys マクロ アクション
TOCTitle: SendKeys macro action
ms:assetid: 3b06fcfc-ea64-c780-b5fc-6fc72853f524
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192656(v=office.15)
ms:contentKeyID: 48544275
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm183441
f1_categories:
- Office.Version=v15
ms.openlocfilehash: aa029e3a81670746cdc467ddf7578c5900b58b29
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929035"
---
# <a name="sendkeys-macro-action"></a>SendKeys マクロ アクション


**適用されます**Access 2013、Office 2013。

<table>
<thead>
<tr class="header">
<th><img src="media/access-alert-security.gif" title="セキュリティに関する注意" alt="Security note" /><strong>セキュリティ メモ</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>
      重要な情報または機密情報には <strong>SendKeys</strong> ステートメントまたは AutoKeys マクロを使用しないでください。悪意のあるユーザーがキー入力を途中で遮り、コンピューターおよびデータのセキュリティを侵害するおそれがあります。
</td>
</tr>
</tbody>
</table>


**SendKeys** アクションを使用すると、Microsoft Access やアクティブな Windows ベースのアプリケーションにキー操作を直接送信することができます。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定

**SendKeys** アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>アクションの引数</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Keystrokes/キー操作</strong></p></td>
<td><p>Access やアプリケーションで処理するキー操作を指定します。[マクロ ビルダー] ウィンドウの [ <strong>アクションの引数</strong>] セクションにある [ <strong>キー操作</strong>] ボックスに、キー操作を入力します。255 文字まで入力できます。この引数は省略できません。  </p></td>
</tr>
<tr class="even">
<td><p><strong>Wait/待機</strong></p></td>
<td><p>キー操作の処理が終わるまでマクロを一時中断するかどうかを指定します。中断する場合は [ <strong>はい</strong>]、中断しない場合は [ <strong>いいえ</strong>] をクリックします。既定値は [ <strong>いいえ</strong>] です。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**SendKeys** アクションで Access にキー操作を送信すると、Access ウィンドウに直接キー操作入力したときと同じように処理されます。

キー操作を指定するには、 **SendKeys** ステートメントと同じ構文を使用します。


> [!NOTE]
> <P>[!メモ] <STRONG>Keystrokes/キー操作</STRONG> 引数に不適切な構文、スペルを誤った文字列、または送り先のウィンドウにとって不適切な値が含まれる場合は、エラーが発生します。</P>



このアクションは、ダイアログ ボックスに情報を入力する場合 (特にマクロを中断せずにダイアログ ボックスに手動で入力する場合) に使用します。Access のアクションには、よく使用するダイアログ ボックスのオプションを自動的に選択する **PrintOut** アクションや **FindRecord** アクションなどがありますが、それ以外のダイアログ ボックスのオプションを選択するには **SendKeys** アクションを使います。


> [!NOTE]
> <UL>
> <LI>
> <P>[!メモ] ダイアログ ボックスによってマクロが中断されるので、ダイアログ ボックスを開くアクションの前に <STRONG>SendKeys</STRONG> アクションを配置し、 <STRONG>Wait/待機</STRONG> 引数を [ <STRONG>いいえ</STRONG> ] に設定する必要があります。</P>
> <LI>
> <P>Access やその他のアプリケーションにキー操作が到達するタイミングには注意が必要です。目的の処理を実行するために、<STRONG>SendKeys</STRONG> アクションを使わずに他の<STRONG>FindRecord</STRONG> アクションなどを使用してダイアログ ボックスのオプションを入力できる場合は、他のアクションを使用することをお勧めします。</P></LI></UL>



Access やその他の Windows ベースのアプリケーションに 255 文字を超えるキー操作を送る場合は、マクロで **SendKeys** アクションを複数回続けて使用します。

**SendKeys** アクションを使用してキー操作を送ると、対応する **KeyDown** 、 **KeyUp** 、 **KeyPress** イベントが発生します。ただし、ANSI 以外のキー操作 (ファンクション キーなど) を送っても **KeyPress** イベントは発生しません。

このアクションは Visual Basic for Applications (VBA) モジュールでは使用できません。 **SendKeys** ステートメントを代わりに使用してください。

