---
title: "'SetProperty/プロパティの設定' マクロ アクション"
TOCTitle: SetProperty Macro Action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6d7aa1deb4bea90e8319cccc763a4e087dd53ef0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479015"
---
# <a name="setproperty-macro-action"></a>"SetProperty/プロパティの設定" マクロ アクション

**適用されます**Access 2013 |。Office 2013

**SetProperty**アクションを使用すると、フォームまたはレポート上のコントロールのプロパティを設定します。

## <a name="setting"></a>設定値

**SetProperty**アクションには、次の引数があります。

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
<td><p>コントロール名</p></td>
<td><p>フィールドまたはプロパティの値を設定するコントロールの名前を入力します。 コントロール名だけをしない完全な構文を使用します。 カレント フォームまたはカレント レポートのプロパティを設定する場合は、この引数を指定しないでください。</p></td>
</tr>
<tr class="even">
<td><p>プロパティ</p></td>
<td><p>設定するプロパティを選択します。 このアクションを使用して設定できるプロパティの一覧については、この資料の<strong>「解説」</strong>セクションを参照してください。</p></td>
</tr>
<tr class="odd">
<td><p>値</p></td>
<td><p>プロパティを設定する値を入力します。 プロパティの値を持つか、[はい] またはいいえ、 <strong>-1</strong>を使用して、[はい] を [いいえ] は<strong>0</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

- **SetProperty**操作を使用するには、コントロールの次のプロパティを設定するのには:**有効になっている**、**表示**、**ロックされている**、**左**、**上**、**幅**、**高さ****前景の色**、**背景色**、または**キャプション**です。

- 引数の***値***に無効な値を入力すると、エラーは発生しませんが、アクセスは、引数を解釈する方法によって、別の値にプロパティを変更する場合があります。

- フォームまたはレポートのプロパティを設定する対象のコントロールを含むを選択するアクションを実行した後にする場合にのみ、独立マクロ**SetProperty**操作を使用できます。 フォームまたはレポートが開いていない場合は、] を選択して、 **OpenForm**または**OpenReport**アクションを使用することができます。 フォームまたはレポートが既に開いている場合をオンに**します**を使用することができます。 プロパティを設定するのには、 **SetProperty**操作を使用できます。 オブジェクトを選択することは、プロパティを設定する対象のコントロールと同じフォームまたはレポート上のコントロールに埋め込まれているマクロで**SetProperty**操作を使用する場合に必要ではありません。

- VBA モジュールでは、 **SetProperty**アクションを実行するには、 **DoCmd**オブジェクトの**SetProperty**メソッドを使用します。

## <a name="example"></a>使用例

**MyTextBox** ] テキスト ボックスの表示/非表示を切り替えるには、SetProperty 操作を使用する例を次に示します。

**によって提供されるサンプル コード**を[Microsoft Access 2010 プログラマーズ リファレンス](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125)です。

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
