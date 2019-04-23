---
title: LockNavigationPane マクロ アクション
TOCTitle: LockNavigationPane macro action
ms:assetid: abf7a989-c7cf-3efa-8df4-3c5b075d0e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821487(v=office.15)
ms:contentKeyID: 48546986
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm172454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 7f6ee19edaf2efdc03301e98e709db6dd69f101a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289872"
---
# <a name="locknavigationpane-macro-action"></a>LockNavigationPane マクロ アクション


**適用先:** Access 2013、Office 2013

" **LockNavigationPane** /ナビゲーションウィンドウのロック" アクションを使用すると、ナビゲーション ウィンドウに表示されているデータベース オブジェクトをユーザーが削除できないように設定できます。

## <a name="setting"></a>Setting

"LockNavigationPane/ナビゲーションウィンドウのロック" アクションの引数は次のとおりです。

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
<td><p>ナビゲーションウィンドウをロックするには [<strong>はい</strong>] を、ナビゲーションウィンドウのロックを解除するには [<strong>いいえ</strong>] を選択します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

Locking the Navigation Pane prevents you from deleting database objects or cutting database objects to the clipboard. 次の操作のいずれかを実行することはでき*ません*。

  - データベース オブジェクトをクリップボードにコピーする

  - クリップボードからデータベース オブジェクトを貼り付ける

  - ナビゲーション ウィンドウの表示と非表示を切り替える

  - ナビゲーション ウィンドウのレイアウトを変更する

  - ナビゲーション ウィンドウのセクションの表示と非表示を切り替える

To run the **LockNavigationPane** action in a VBA module, use the **LockNavigationPane** method of the **DoCmd** object.

