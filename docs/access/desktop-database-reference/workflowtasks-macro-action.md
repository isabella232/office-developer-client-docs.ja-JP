---
title: WorkflowTasks マクロ アクション
TOCTitle: WorkflowTasks macro action
ms:assetid: 4b299681-b45b-f6d1-2cfe-ebf01712bfc1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193503(v=office.15)
ms:contentKeyID: 48544684
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm8454
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 921396edd480e06194d1c3dcbb683aa8556553e2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721858"
---
# <a name="workflowtasks-macro-action"></a>WorkflowTasks マクロ アクション


**適用されます**Access 2013、Office 2013。

**WorkflowTasks**アクションを使用するには、[**ワークフロー タスク**] ダイアログ ボックスを表示します。

## <a name="setting"></a>設定値

**WorkflowTasks**アクションには、次の引数があります。

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
<td><p><strong>Record Number/レコード番号</strong></p></td>
<td><p>リストの最初の項目の<strong>1</strong> 、2 番目の<strong>2</strong>項目というように、Microsoft SharePoint Foundation リスト内の項目の位置。 この引数に式を入力することもできます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

  - **WorkflowTasks**アクションは、 **[ワークフロー タスク**] ダイアログ ボックスを開きます。 このダイアログ ボックスは、指定した項目で使用可能なすべてのタスクを表示します。 SharePoint Foundation でリストに対してワークフローを定義する必要があります。

  - **WorkflowTasks**アクションは、リンクされた SharePoint Foundation リストが開かれ、選択した後にのみ使用できます。 開き、リンクされたリストを選択するには、 **OpenTable**のアクションを使用します。 リストが既に開いている場合は、 **SelectObject**アクションを使用して選択します。

  - **WorkflowTasks**アクションは、データシート ビューで開いている間にリンクされている SharePoint Foundation リスト内の任意のセルを右クリックし、**ワークフロー**、] をポイントして、**ワークフローのタスク**をクリックと同じです。

  - VBA モジュールでは、 **WorkflowTasks**アクションを実行するには、 **DoCmd**オブジェクトの**WorkflowTasks**メソッドを使用します。

