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
ms.localizationpriority: medium
ms.openlocfilehash: cda7c774e6af9f40d529fe809c49506a57c73c2b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568474"
---
# <a name="setmenuitem-macro-action"></a>SetMenuItem マクロ アクション

**適用先:** Access 2013、Office 2013

You can use the **SetMenuItem** action to set the state of menu items (enabled or disabled, selected or unselected) on custom or global menus on the **Add-Ins** tab.

> [!NOTE]
> The **SetMenuItem** action works only with custom and global menus created by using menu macros. The **SetMenuItem** action is included in Microsoft Access only for compatibility with previous versions. It does not work with the command bar functionality. However, you can use the **Enabled** and **State** properties in a Visual Basic for Applications (VBA) module to disable or enable and select or unselect items on shortcut menus or custom or global menus.

## <a name="setting"></a>設定

"SetMenuItem/メニューの設定" アクションの引数は次のとおりです。

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
<td><p>状態を設定するコマンドを含むメニューのインデックス。 カスタム メニューまたはグローバル メニューの目的のメニューのインデックスに 0 から始まる整数値を入力します。 [マクロ ビルダー] ウィンドウの <strong>[アクション引数</strong> ] セクションの [ <strong>メニュー</strong> インデックス] ボックスにインデックス値を入力します。 インデックスは、カスタム またはグローバル メニューのメニュー マクロ内のメニューの位置を基準にしています (メニュー マクロ内のこのメニューの <strong>AddMenu</strong> アクションの位置は 0 からカウントされます)。 メニュー マクロで条件式を使用してカスタム メニュー項目を非表示または表示できるので、メニューの表示が多少異なる場合があります。 これは必須の引数です。 この引数でメニューを選択し、"Command Index/コマンド インデックス" 引数と "Subcommand Index/サブコマンド インデックス" 引数を空白にすると、メニュー名自体を有効または無効にすることができます。 ただし、メニュー名のチェックマークを付けたり外したりすることはできません (Access では、メニュー名の "Flag/フラグ" 引数の [チェックマーク表示] と [チェックマーク非表示] の設定は無視されます)。</p></td>
</tr>
<tr class="even">
<td><p><strong>Command Index/コマンド インデックス</strong></p></td>
<td><p>状態を設定するコマンドのインデックスを指定します。"Menu Index/メニュー インデックス" 引数で選択したメニューの該当コマンドのインデックスとして 0 以上の整数値を入力します。インデックスは、ユーザー設定のメニューやグローバル メニューで選択したメニューを定義するマクロ グループにおけるコマンドの位置 (マクロ グループ内でのコマンドのマクロを示す 0 から数えた位置) を基準としています。メニューのマクロ グループで条件式を使用するとユーザー設定のメニュー コマンドの表示と非表示を切り替えることができるため、メニューの表示は多少異なる場合があります。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Subcommand Index/サブコマンド インデックス</strong></p></td>
<td><p>状態を設定するサブコマンドのインデックスを指定します。これが適用されるのは、目的のコマンドにサブメニューが含まれる場合のみです。"Command Index/コマンド インデックス" 引数で選択したサブメニューの該当サブコマンドのインデックスとして 0 以上の整数値を入力します。インデックスは、ユーザー設定のメニューやグローバル メニューで選択したサブメニューを定義するマクロ グループにおけるサブコマンドの位置 (マクロ グループ内でのサブコマンドのマクロを示す 0 から数えた位置) を基準としています。</p></td>
</tr>
<tr class="even">
<td><p><strong>Flag</strong></p></td>
<td><p>コマンドまたはサブコマンドに設定する状態を指定します。コマンドを無効にして淡色表示にする場合は [<strong>淡色表示</strong>]、コマンドを有効にする場合は [<strong>通常表示</strong>]、コマンドの横にチェックマークを付けて選択つまり設定されていることを示す場合は [<strong>チェックマーク表示</strong>]、チェックマークを外す場合は [<strong>チェックマーク非表示</strong>] をクリックします。既定値は [<strong>通常表示</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

The **SetMenuItem** action works only on a custom or global menu. If the active window does not have a custom or global menu, running a macro containing the **SetMenuItem** action causes a run-time error.

このアクションを使用すると、メニュー コマンドおよびサブコマンドの状態は設定できますが、サブコマンドのサブコマンドの状態は設定できません。

To run the **SetMenuItem** action in a Visual Basic for Applications (VBA) module, use the **SetMenuItem** method of the **DoCmd** object.

