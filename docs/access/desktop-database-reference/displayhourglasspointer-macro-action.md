---
title: DisplayHourglassPointer マクロ アクション
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: c0c6708acde1c9a50ae9a30ff8b1fce57e392605
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59585733"
---
# <a name="displayhourglasspointer-macro-action"></a>DisplayHourglassPointer マクロ アクション


**適用先**: Access 2013、Office 2013

You can use the **DisplayHourglassPointer** action to change the mouse pointer to an image of an hourglass (or another icon you've chosen) while a macro is running. This action can provide a visual indication that the macro is running. This is especially useful when a macro action or the macro itself takes a long time to run.

## <a name="setting"></a>設定

"DisplayHourglassPointer/砂時計ポインターの表示" アクションの引数は次のとおりです。

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


## <a name="remarks"></a>注釈

このアクションは、" **Echo/エコー** " アクションでエコーをオフにした場合によく使用します。 エコーがオフの場合、Access はマクロが終了するまで画面の更新を中断します。

Access automatically resets the **Hourglass On** argument to **No** when the macro finishes running.

> [!NOTE]
> - Microsoft Windows では、Windows コントロール パネルの [**マウスのプロパティ**] ダイアログ ボックスで [**待ち状態**] に設定されたアイコンが使用されます。すべての Windows オペレーティング システムで、既定の設定は砂時計アイコンです。
> - 別のアイコンを選択することもできます。

Visual Basic for Applications (VBA) モジュールで "DisplayHourglassPointer/砂時計ポインターの表示" アクションを実行するには、DoCmd オブジェクトの Hourglass メソッドを使用します。

