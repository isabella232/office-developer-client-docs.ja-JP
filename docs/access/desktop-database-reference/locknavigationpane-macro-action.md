---
title: "'LockNavigationPane/ナビゲーションウィンドウのロック' マクロ アクション"
TOCTitle: LockNavigationPane Macro Action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4e18b17c5d00095b61323511c20b95a355819eab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478825"
---
# <a name="locknavigationpane-macro-action"></a>"LockNavigationPane/ナビゲーションウィンドウのロック" マクロ アクション


**適用されます**Access 2013 |。Office 2013

" **LockNavigationPane** /ナビゲーションウィンドウのロック" アクションを使用すると、ナビゲーション ウィンドウに表示されているデータベース オブジェクトをユーザーが削除できないように設定できます。

## <a name="setting"></a>設定値

**LockNavigationPane**アクションには、次の引数があります。

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
<td><p><strong>Lock</strong></p></td>
<td><p><strong>はい</strong>ナビゲーション ウィンドウ] または [<strong>いいえ</strong>ナビゲーション ウィンドウのロックを解除をロックするを選択します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

ナビゲーション ウィンドウをロックすると、データベース オブジェクトまたはデータベース オブジェクトを切り取ってクリップボードを削除できなくなります。 *ない*次の操作のいずれかの操作を実行することを防ぐ。

  - データベース オブジェクトをクリップボードにコピーする

  - クリップボードからデータベース オブジェクトを貼り付ける

  - ナビゲーション ウィンドウの表示と非表示を切り替える

  - ナビゲーション ウィンドウのレイアウトを変更する

  - ナビゲーション ウィンドウのセクションの表示と非表示を切り替える

**LockNavigationPane**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**LockNavigationPane**メソッドを使用します。

