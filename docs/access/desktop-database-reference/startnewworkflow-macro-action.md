---
title: "'StartNewWorkflow/新しいワークフローの開始' マクロ アクション"
TOCTitle: StartNewWorkflow Macro Action
ms:assetid: b3e81a11-b816-0eef-fc70-6d6da7a5a845
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822054(v=office.15)
ms:contentKeyID: 48547206
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm198223
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 6ba9d38caaa85ab9dd582abdbeb37aff5c7b340e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886495"
---
# <a name="startnewworkflow-macro-action"></a>"StartNewWorkflow/新しいワークフローの開始" マクロ アクション


**適用されます**Access 2013、Office 2013。

**StartNewWorkflow**アクションを使用すると、リンクされた Microsoft SharePoint Foundation リストに項目の新しいワークフローを開始します。

## <a name="setting"></a>設定値

**StartNewWorkflow**アクションには、次の引数があります。

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
<td><p>リストの最初の項目の<strong>1</strong> 、2 番目の<strong>2</strong>項目というように、SharePoint Foundation リスト内の項目の位置。 この引数に式を入力することもできます。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>解説

  - **StartNewWorkflow**アクションでは、**新しいワークフローの開始**] ダイアログ ボックスを開きます。 このダイアログ ボックスには、指定した項目で使用可能なすべてのワークフローが表示されます。 このアクションを使用して開始する前に、SharePoint Foundation でリストに対してワークフローを定義する必要があります。

  - **StartNewWorkflow**アクションは、リンクされた SharePoint リストが開かれ、選択した後にのみ使用できます。 開き、リンクされたリストを選択するには、 **OpenTable**のアクションを使用します。 リストが既に開いている場合は、 **SelectObject**アクションを使用して選択します。

  - **StartNewWorkflow**アクションには、データシート ビューで開いている間は、SharePoint リストにリンクされている任意のセルを右クリックし、**ワークフロー**、] をポイントし、[**新しいワークフローの開始**] をクリックと同じ効果があります。

  - **StartNewWorkflow**アクションは、VBA モジュールで実行するには、 **DoCmd**オブジェクトの**StartNewWorkflow**メソッドを使用します。

