---
title: "\"DisplayHourglassPointer/砂時計ポインターの表示\" マクロ アクション"
TOCTitle: DisplayHourglassPointer Macro Action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4d9f370fdc1ea2100178a489ad1c81225cd05199
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874616"
---
# <a name="displayhourglasspointer-macro-action"></a>"DisplayHourglassPointer/砂時計ポインターの表示" マクロ アクション


**適用されます**Access 2013、Office 2013。

砂時計のマウス ポインターを変更するのには、 **DisplayHourglassPointer**アクションを使用することができます (または選択した別のアイコン)、マクロの実行中にします。 このアクションによって、マクロが実行中であることを視覚的に示すことができます。 マクロ アクションまたはマクロ自体の実行に時間がかかる場合に使用すると便利です。

## <a name="setting"></a>設定値

**DisplayHourglassPointer**アクションには、次の引数があります。

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
<td><p><strong>Hourglass On/表示</strong></p></td>
<td><p>[マクロ ビルダー] ウィンドウの [<strong>アクションの引数</strong>] セクションの [<strong>表示</strong>] ボックスで、砂時計のアイコンを表示する場合は [<strong>はい</strong>]、通常のマウス ポインターを表示する場合は [<strong>いいえ</strong>] をクリックします。既定値は [<strong>はい</strong>] です。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

このアクションは、" **Echo/エコー** " アクションでエコーをオフにした場合によく使用します。 エコーがオフの場合、アクセスは、マクロが終了するまで画面の更新を中断します。

自動的にリセット、**砂時計型インデント マーカーの**引数に [ **No**マクロの実行が完了するとします。

> [!NOTE]
> - Microsoft Windows では、Windows コントロール パネルの [**マウスのプロパティ**] ダイアログ ボックスで [**待ち状態**] に設定されたアイコンが使用されます。すべての Windows オペレーティング システムで、既定の設定は砂時計アイコンです。
> - 別のアイコンを選択することもできます。

Visual Basic for Applications (VBA) モジュールに**DisplayHourglassPointer**アクションを実行するには、 **DoCmd**オブジェクトの**Hourglass**メソッドを使用します。

