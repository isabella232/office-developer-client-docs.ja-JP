---
title: "'QuitAccess/Accessの終了' マクロ アクション"
TOCTitle: QuitAccess Macro Action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5fa3b7ffc97f69b1ebc85799a8b2a27b6acc1d90
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476385"
---
# <a name="quitaccess-macro-action"></a>"QuitAccess/Accessの終了" マクロ アクション


**適用されます**Access 2013 |。Office 2013

**QuitAccess**アクションを使用すると、Microsoft Access を終了します。 **QuitAccess**アクションでは、Access の終了時にデータベース オブジェクトを保存するためのいくつかのオプションのいずれかの指定もできます。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定値

**QuitAccess**アクションには、次の引数があります。

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
<td><p><strong>Options</strong></p></td>
<td><p>Access の終了時の未保存のオブジェクトに対する処理を指定します。[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションにある [<strong>オプション</strong>] ボックスで、ダイアログ ボックスを表示してオブジェクトごとに保存するかどうかを指定する場合は [<strong>確認</strong>]、ダイアログ ボックスを表示せずにすべてのオブジェクトを保存する場合は [<strong>すべて保存</strong>]、オブジェクトを保存せずに終了する場合は [<strong>終了</strong>] をクリックします。既定値は [<strong>すべて保存</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**QuitAccess**アクション マクロで、次のすべてのアクションは実行されません。

このアクションを使用すると、フォームのカスタム メニュー コマンドまたはボタンを使用して**保存**] ダイアログ ボックスを表示しないで Access を終了します。 たとえば、マスター フォーム、ユーザー設定のワークスペースにオブジェクトを表示するために使用される場合もあります。 このフォームには、 **Quit**ボタン**すべてを保存**する設定**オプション**の引数を指定して**QuitAccess**アクションを含むマクロを実行する可能性があります。

/System オプションは、[**ファイル**] タブをクリックして、[**終了**] をクリックと同じ効果。 このコマンドをクリックすると、保存されていないオブジェクトがある場合、ダイアログ ボックスが表示か**QuitAccess**アクションの引数**のオプション**の**プロンプト**を使用する場合に表示されるものと同じです。

Access を終了したりオブジェクトを閉じたりするのにことがなく、指定したオブジェクトを保存するのには、マクロで**SaveObject**アクションを使用できます。

Visual Basic for Applications (VBA) モジュールに**QuitAccess**アクションを実行するには、 **DoCmd**オブジェクトの**Quit**メソッドを使用します。

