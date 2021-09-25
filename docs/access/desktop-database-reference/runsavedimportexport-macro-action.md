---
title: RunSavedImportExport マクロ アクション
TOCTitle: RunSavedImportExport macro action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 697fd5e7c422be61f05cdb2ceaaa7f0f5e6ec4d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614935"
---
# <a name="runsavedimportexport-macro-action"></a>RunSavedImportExport マクロ アクション

**適用先**: Access 2013、Office 2013

**RunSavedImportExport** アクションを使用すると、インポート ウィザードまたはエクスポート ウィザードを使用して作成した保存済みのインポート定義またはエクスポート定義を実行できます。

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。

## <a name="setting"></a>Setting

**RunSavedImportExport** アクションの引数は次のとおりです。

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
<td><p><strong>Saved Import Export Name/保存済みのインポート/エクスポート操作の名前</strong></p></td>
<td><p>ドロップダウン リストから、保存済みのインポート定義またはエクスポート定義の名前を選択します。</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

- このマクロ アクションの動作は、Access で次の操作を実行した場合と同じです。
    
  1.  [ **外部データ**] タブで、[ **保存済みのインポート操作**] または [ **保存済みのエクスポート操作**] をクリックします。
    
  2.  [ **データ タスクの管理**] ダイアログ ボックスの [ **保存済みのインポート操作**] タブまたは [ **保存済みのエクスポート操作**] タブ (前の手順で選択した操作によります) で、実行する定義をクリックします。
    
  3.  [ **実行**] をクリックします。

- **RunSavedImportExport** アクションを実行する前に、インポート元ファイルとエクスポート先ファイルが存在し、インポート元データのインポートの準備ができていることを確認して、この操作によってエクスポート先ファイルのデータが誤って上書きされないようにしてください。

- インポート定義およびエクスポート定義の保存と実行の詳細については、「 **参照**」セクションのリンク先を参照してください。

- [保存されたインポート エクスポート名] 引数に選択した保存済みインポートまたはエクスポート仕様がマクロの作成後に削除されると、マクロの実行時に Access に次のエラー メッセージが表示されます。指定したインデックスを持つ仕様は存在しません。 **別のインデックスを指定します。'*****仕様名*****'。**

