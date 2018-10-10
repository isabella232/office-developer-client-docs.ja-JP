---
title: "\"GoToPage/ページの移動\" マクロ アクション"
TOCTitle: GoToPage Macro Action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
ms.openlocfilehash: dc7777535fdba5bcb1f6ace167e23e1294f13960
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477153"
---
# <a name="gotopage-macro-action"></a>"GoToPage/ページの移動" マクロ アクション


**適用されます**Access 2013 |。Office 2013

**GoToPage**アクションを使用すると、アクティブ フォームの指定したページの先頭のコントロールにフォーカスを移動します。 このアクションは、関連のある情報を改ページで分割しているフォームを作成した場合に使用できます。 たとえば、社員フォームの最初のページに個人情報、2 ページ目に会社情報、3 ページ目に売上情報があるとします。 **GoToPage**アクションを使用すると、目的のページに移動します。 また、タブ コントロールを使用すると、1 つのフォーム上で複数のページに情報を表示することもできます。

## <a name="setting"></a>設定値

**GoToPage**アクションには、次の引数があります。

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
<td><p><strong>ページ番号</strong></p></td>
<td><p>フォーカスを移動するページの数です。 マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの<strong>ページ番号</strong>ボックスにページ番号を入力します。 この引数を指定しないと、フォーカスはカレント ページにとどまります。 表示するページの部分を表示するのには、<strong>右</strong>と<strong>下</strong>の引数を使用できます。</p></td>
</tr>
<tr class="even">
<td><p><strong>Right</strong></p></td>
<td><p>ページで、スポットの水平方向の位置は、ウィンドウの左端に表示するウィンドウの左端から計測されます。 <strong></strong>引数を指定する場合に必要です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Down</strong></p></td>
<td><p>ページ上の場所の垂直方向の位置は、ウィンドウの上端に表示するウィンドウの上端から測定されます。 <strong>右</strong>の引数を指定する場合に必要です。</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><STRONG>右</STRONG>と<STRONG>下</STRONG>の引数は、インチまたはセンチメートル、Windows コントロール パネルの [地域の設定によって測定されます。</P>



## <a name="remarks"></a>解説

ページで指定された最初のコントロール (フォームのタブ オーダーで定義されている) を選択するのには、このアクションを使用できます。 **フォーカスを移動**を使用すると、フォーム上の特定のコントロールに移動できます。

Access ウィンドウよりも大きいページでは、フォームの**右**と**下**の引数を使用できます。 " **Page Number/ページ番号** " 引数を使用して目的のページに移動し、次に " **Right/右** " 引数と " **Down/下** " 引数を使ってページの必要な部分を表示します。 このとき、ウィンドウの左上隅から、引数で指定した間隔を置いた位置に、ページの左上隅が表示されます。

**GoToPage**アクションは、次の場合に使用できません。

  - 非表示のフォームのページにフォーカスを移動する場合

  - タブ コントロール内の別のページにフォーカスを移動する場合

Visual Basic for Applications (VBA) モジュールでは、 **GoToPage**アクションを実行するには、 **DoCmd**オブジェクトの**GoToPage**メソッドを使用します。

