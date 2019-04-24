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
localization_priority: Normal
ms.openlocfilehash: adcc8a2a9462509f4b37d2dbdaf824387ae52a26
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309174"
---
# <a name="runsavedimportexport-macro-action"></a>RunSavedImportExport マクロ アクション

**適用先:** Access 2013、Office 2013

**RunSavedImportExport** アクションを使用すると、インポート ウィザードまたはエクスポート ウィザードを使用して作成した保存済みのインポート定義またはエクスポート定義を実行できます。

> [!NOTE]
> [!メモ] データベースが信頼されていない場合、このアクションは許可されません。

## <a name="setting"></a>設定値

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

- **保存**されたインポートまたはエクスポートに対して選択したエクスポート定義が、マクロの作成後に削除されると、マクロの実行時に次のエラーメッセージが表示されます。**指定されたインデックスを持つ仕様は、存在しません。別のインデックスを指定します。' * * * * * 仕様名 * *** * * * '。

