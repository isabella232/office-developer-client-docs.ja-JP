---
title: SetMenuItem マクロ アクション
TOCTitle: SetMenuItem macro action
ms:assetid: 503b3635-e721-1b99-3249-626e5dccdb8a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193803(v=office.15)
ms:contentKeyID: 48544789
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm16614
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 342b4c38b6a48ad36dc6d62ee34900e6f2057d42
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996868"
---
# <a name="setmenuitem-macro-action"></a>SetMenuItem マクロ アクション

**適用されます**Access 2013、Office 2013。

**SetMenuItem**アクションを使用すると、[**アドイン**] タブで、カスタムまたはグローバル メニューのメニュー項目の (有効または無効になっている、選択または選択されていない場合) の状態を設定します。

> [!NOTE]
> **SetMenuItem**アクションは、メニュー マクロで作成されたユーザー設定とグローバルのメニューでのみ動作します。 **SetMenuItem**アクションは、以前のバージョンとの互換性のための Microsoft Access に含まれます。 コマンド バーの機能は動作しません。 ただしを無効にするまたは有効にする選択するか、ショートカット メニュー上の項目の選択を解除するのには、Visual Basic for Applications (VBA) モジュールのプロパティを**有効に**し、**状態**またはユーザー設定やグローバル メニューを使用することができます。

## <a name="setting"></a>設定値

**SetMenuItem**アクションには、次の引数があります。

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
<td><p><strong>Menu Index/メニュー インデックス</strong></p></td>
<td><p>状態を設定するコマンドを含むメニューのインデックス。 カスタム メニューまたはグローバル メニューのメニューのインデックスを表す 0 から始まる整数値を入力します。 マクロ ビルダー] ウィンドウの<strong>メニューの [インデックス</strong>] ボックス [<strong>アクションの引数</strong>] セクションで、インデックスの値を入力します。 インデックスは、メニュー マクロに、カスタム メニューまたはグローバル メニュー (このメニューの<strong>メニューの追加</strong>アクション] メニューの 0 から数えた位置) のメニューの位置を基準にしています。 メニュー マクロで条件式を使用するにはカスタム メニュー項目を表示または非表示にするため、メニューの表示が若干異なる可能性があります。 この引数は省略できません。 場合はこの引数でメニューを選択し、<strong>インデックスのコマンド</strong>や<strong>サブコマンドのインデックス</strong>の引数を空白のままにするを有効にしたり、メニュー名自体を無効にできます。 ただし、選択または (アクセスを無視する] メニューの [名前の<strong>フラグ</strong>引数の設定<strong>を確認</strong>し<strong>をオフにします</strong>)] メニューの [名前の選択を解除することはできません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Command Index/コマンド インデックス</strong></p></td>
<td><p>状態を設定するコマンドのインデックス。 <strong>メニュー インデックス</strong>の引数で選択したメニューで目的のコマンドのインデックスを表す 0 から始まる整数値を入力します。 インデックスは、カスタム メニューまたはグローバル メニュー (0 から数えて、マクロ グループ内のこのコマンドのマクロの位置) を選択したメニューを定義するマクロ グループにおける対象コマンドの位置を基準にしています。 メニューのマクロ グループで条件式を使用するにはカスタム メニュー コマンドを表示または非表示にするため、メニューの表示が若干異なる可能性があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Subcommand Index/サブコマンド インデックス</strong></p></td>
<td><p>状態を設定するサブコマンドのインデックス。 これは、目的のコマンドにサブメニューがある場合にのみ適用されます。 <strong>コマンド インデックス</strong>引数で選択したサブメニューのサブコマンドのインデックスを表す 0 から始まる整数値を入力します。 インデックスは、カスタム メニューまたはグローバル メニュー (0 から数えて、マクロ グループ内のこのサブコマンドのマクロの位置) を選択したサブメニューを定義するマクロ グループにおける対象サブコマンドの位置を基準にしています。</p></td>
</tr>
<tr class="even">
<td><p><strong>Flag</strong></p></td>
<td><p>コマンドまたはサブコマンドに設定する状態を指定します。コマンドを無効にして淡色表示にする場合は [<strong>淡色表示</strong>]、コマンドを有効にする場合は [<strong>通常表示</strong>]、コマンドの横にチェックマークを付けて選択つまり設定されていることを示す場合は [<strong>チェックマーク表示</strong>]、チェックマークを外す場合は [<strong>チェックマーク非表示</strong>] をクリックします。既定値は [<strong>通常表示</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

**SetMenuItem**アクションは、カスタム メニューまたはグローバル メニューに対してのみ機能します。 作業中のウィンドウは、カスタム メニューまたはグローバル メニューを持たない場合は、 **SetMenuItem**アクションを含むマクロを実行すると実行時エラーが発生します。

このアクションを使用すると、メニュー コマンドおよびサブコマンドの状態は設定できますが、サブコマンドのサブコマンドの状態は設定できません。

**SetMenuItem**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **DoCmd**オブジェクトの**SetMenuItem**メソッドを使用します。

