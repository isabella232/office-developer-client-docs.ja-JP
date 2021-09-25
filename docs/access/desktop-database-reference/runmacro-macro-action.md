---
title: RunMacro マクロ アクション
TOCTitle: RunMacro macro action
ms:assetid: 25966f20-8160-0821-b88a-ed08b7786fdc
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191868(v=office.15)
ms:contentKeyID: 48543787
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm43195
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 861e6425ec7ab0da4f701fa7140c287ad24167d0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614956"
---
# <a name="runmacro-macro-action"></a>RunMacro マクロ アクション

**適用先**: Access 2013、Office 2013

**RunMacro** アクションを使用すると、マクロを実行できます。マクロ グループ内のマクロも実行できます。

このアクションは、次のような場合に使うと効果的です。

- マクロ内から別のマクロを実行する場合

- 特定の条件に基づいてマクロを実行する場合

- 独自のメニュー コマンドにマクロを割り当てる場合

## <a name="setting"></a>設定

"**RunMacro**/マクロの実行" アクションの引数は次のとおりです。

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
<td><p><strong>Macro Name/マクロ名</strong></p></td>
<td><p>The name of the macro to run. The <strong>Macro Name</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane shows all macros (and macro groups) in the current database. マクロ がマクロ グループ内にある場合は、マクロ グループ名としてリストのマクロ グループ名の下 <em>に表示されます</em>。<em>macroname</em>. This is a required argument. If you run a macro containing the <strong>RunMacro</strong> action in a library database, Microsoft Access looks for the macro with this name in the library database and doesn't look for it in the current database.</p></td>
</tr>
<tr class="even">
<td><p><strong>Repeat Count/実行回数</strong></p></td>
<td><p>マクロの最大実行回数を指定します。この引数および <strong>Repeat Expression/繰り返し条件式</strong> 引数を指定しない場合、マクロは 1 回だけ実行されます。  </p></td>
</tr>
<tr class="odd">
<td><p><strong>Repeat Expression/繰り返し条件式</strong></p></td>
<td><p><strong>True</strong> (–1) または <strong>False</strong> (0) に評価される式を指定します。式が <strong>False</strong> に評価される場合、マクロの実行は停止します。この式は、マクロを実行するたびに評価されます。</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>注釈

**Macro Name/マクロ名** 引数にマクロ グループ名を入力すると、マクロ グループ内の最初のマクロが実行されます。

このアクションの動作は、[ **データベース ツール**] タブの [ **マクロの実行**] をクリックし、マクロを選択して、[ **OK**] をクリックした場合と同じです。ただし、このコマンドではマクロを 1 回だけ実行するのに対し、 **RunMacro** アクションでは必要なだけ何回でもマクロを実行できます。

> [!TIP]
> [!ヒント] **Repeat Count/実行回数** 引数および **Repeat Expression/繰り返し条件式** 引数を使用すると、マクロの実行回数を指定できます。
> - どちらの引数も指定しない場合、マクロは 1 回だけ実行されます。
> - **Repeat Count/実行回数** を指定し、 **Repeat Expression/繰り返し条件式** 引数を指定しない場合、マクロは指定した回数だけ実行されます。
> - **Repeat Count/実行回数** 引数を指定せずに、 **Repeat Expression/繰り返し条件式** 引数に式を入力した場合、マクロは、式が **False** に評価されるまで実行されます。
> - 両方の引数に値を入力した場合、マクロは、 **Repeat Count/実行回数** 引数に指定した回数だけ実行されるか、 **Repeat Expression/繰り返し条件式** 引数が **False** に評価されるまで実行されます。これは、先に当てはまる方が適用されます。

**RunMacro** アクションを含むマクロを実行し、 **RunMacro** アクションに到達すると、呼び出されたマクロが実行されます。呼び出されたマクロの実行が終了すると、元のマクロに戻り、次のアクションが実行されます。

> [!NOTE]
> - 同じマクロ グループ内または別のマクロ グループ内のマクロを呼び出すことができます。
> - マクロはネストすることができます。たとえば、マクロ A からマクロ B を呼び出し、さらにマクロ B から別のマクロを呼び出すことができます。呼び出されたマクロの実行が終了すると、呼び出し元のマクロに戻り、次のアクションが実行されます。

Visual Basic for Applications (VBA) モジュールで **RunMacro** アクションを実行するには、 **DoCmd** オブジェクトの **RunMacro** メソッドを使用します。

