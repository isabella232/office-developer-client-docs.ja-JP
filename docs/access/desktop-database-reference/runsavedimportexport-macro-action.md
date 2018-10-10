---
title: RunSavedImportExport マクロ アクション
TOCTitle: RunSavedImportExport Macro Action
ms:assetid: b2449c51-ee20-6e50-87f3-a45adc0b0dde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822018(v=office.15)
ms:contentKeyID: 48547165
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm3022
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0afff780714f8be943a2b0b7d744d6118fcacf88
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478536"
---
# <a name="runsavedimportexport-macro-action"></a>RunSavedImportExport マクロ アクション


**適用されます**Access 2013 |。Office 2013

**RunSavedImportExport** アクションを使用すると、インポート ウィザードまたはエクスポート ウィザードを使用して作成した保存済みのインポート定義またはエクスポート定義を実行できます。


> [!NOTE]
> <P>[!メモ] データベースが信頼されていない場合、このアクションは許可されません。マクロの有効化の詳細については、この記事の「 See Also」セクションのリンクを参照してください。</P>



## <a name="setting"></a>設定

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


## <a name="remarks"></a>解説

  - このマクロ アクションの動作は、Access で次の操作を実行した場合と同じです。
    
    1.  [ **外部データ**] タブで、[ **保存済みのインポート操作**] または [ **保存済みのエクスポート操作**] をクリックします。
    
    2.  [ **データ タスクの管理**] ダイアログ ボックスの [ **保存済みのインポート操作**] タブまたは [ **保存済みのエクスポート操作**] タブ (前の手順で選択した操作によります) で、実行する定義をクリックします。
    
    3.  [ **実行**] をクリックします。

  - **RunSavedImportExport** アクションを実行する前に、インポート元ファイルとエクスポート先ファイルが存在し、インポート元データのインポートの準備ができていることを確認して、この操作によってエクスポート先ファイルのデータが誤って上書きされないようにしてください。

  - インポート定義およびエクスポート定義の保存と実行の詳細については、「 **参照**」セクションのリンク先を参照してください。

  - 保存されているインポートまたはエクスポート定義のマクロを作成した後で**インポート エクスポート名を保存された**引数が削除された場合に選択するが表示されます、次のエラー メッセージ、マクロの実行時:**で指定したインデックスの仕様は存在しません。別のインデックスを指定します。'仕様の名前。' です。** 。

