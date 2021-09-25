---
title: LogEvent マクロ アクション
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5868f8c351bfacba2008b114f5df1596eb4a246f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602256"
---
# <a name="logevent-macro-action"></a>LogEvent マクロ アクション

**適用先**: Access 2013、Office 2013

The **LogEvent** action writes information to the **USysApplicationLog** system table.

> [!NOTE]
> "LogEvent/イベントのログ記録" アクションは、データ マクロでのみ使用できます。

## <a name="setting"></a>設定

"LogEvent/イベントのログ記録" アクションの引数は次のとおりです。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>引数</p></th>
<th><p>必須</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>説明</strong></p></td>
<td><p>いいえ</p></td>
<td><p>記録する条件を説明する文字列式を指定します。説明は 255 文字以内とします。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

The **LogEvent** action can be used to write status information to the **USysApplicationLog** system table that does not merit using the **[RaiseError](raiseerror-macro-action.md)** action to throw an error. For example, you could log changes to a specific field, or use the items written to the **USysApplicationLog** to assist you in debugging your macro.

When you use the **LogEvent** action to write to the **USysApplicationLog** table, the **Category** column is automatically set to **User**.

To see the **USysApplicationLog** table, use the following steps:

1.  [ **ファイル**] メニューの [ **オプション**] をクリックします。

2.  [ **Access のオプション**] ダイアログ ボックスで [ **カレント データベース**] タブをクリックします。

3.  [ **ナビゲーション**] セクションで [ **ナビゲーション オプション**] をクリックします。

4.  [ **ナビゲーション オプション**] ダイアログ ボックスで [ **システム オブジェクトの表示**] をクリックし、[ **OK**] をクリックします。

5.  [ **OK**] をクリックして [ **Access のオプション**] ダイアログ ボックスを終了します。

