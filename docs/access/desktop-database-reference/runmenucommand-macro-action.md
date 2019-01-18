---
title: RunMenuCommand マクロ アクション
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698163"
---
# <a name="runmenucommand-macro-action"></a>RunMenuCommand マクロ アクション

**適用されます**Access 2013、Office 2013。

**RunMenuCommand**アクションを使用すると、組み込みの Access コマンドを実行します。

## <a name="setting"></a>設定値

**RunMenuCommand**アクションには、次のアクションの引数があります。

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
<td><p><strong>Command</strong></p></td>
<td><p>実行するコマンドの名前を指定します。[<strong>コマンド</strong>] ボックスには、Access の使用可能な組み込みのコマンドが五十音順で表示されます。この引数は省略できません。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>解説

**RunMenuCommand**アクションを使用すると、カスタム メニュー バー、グローバル メニュー バー、カスタム ショートカット メニューまたはグローバル ショートカット メニューから、Access コマンドを実行します。

マクロ内で条件付き書式**RunMenuCommand**アクションを使用するには一定の条件に従ってコマンドを実行します。

> [!NOTE]
> [**ファイル**] タブをクリックし、[**最近使用した**最近使用したデータベースを示しています。 **開く**をクリックする代わりにこれらのデータベースのいずれかをクリックすることができます。 データベースのこれらの項目は、**コマンド**の引数のドロップダウン リスト ボックスに表示されないし、 **RunMenuCommand**アクションを使用してマクロ内で使用できません。

以前のバージョンの Access から Access データベースを変換するときにいくつかのコマンドが利用できなくです。 コマンドでは、可能性がありますが名前が変更されて、別のメニューに移動または、Access で使用可能な不要になった場合があります。 **RunMenuCommand**アクションには、このようなコマンドの動作を**DoMenuItem**を変換できません。 マクロを開くと、このようなコマンドの**コマンド**の引数が空で、 **RunMenuCommand**アクションが表示されます。 マクロを編集、有効なコマンド引数を入力し、または**RunMenuCommand**アクションを削除する必要があります。

**RunMenuCommand**アクションを Visual Basic for Applications (VBA) のモジュールで実行するには、 **Application**オブジェクトの**RunCommand**メソッドを使用します。 (これは、 **DoCmd**オブジェクトの**RunCommand**メソッドと同等) です。

