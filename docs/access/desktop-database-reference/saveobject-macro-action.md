---
title: SaveObject マクロ アクション
TOCTitle: SaveObject macro action
ms:assetid: 85716dfc-f76f-ca47-cc40-f8f88162f85a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196789(v=office.15)
ms:contentKeyID: 48546060
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm116962
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: eb5ec32eadaf99732758860976aa59c4a29ef6c2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59593643"
---
# <a name="saveobject-macro-action"></a>SaveObject マクロ アクション

**適用先**: Access 2013、Office 2013

You can use the **SaveObject** action to save either a specified Access object or the active object if none is specified. You can also save the active object with a new name in some cases (this functions the same as the **Save As** command on the **Quick Access Toolbar**).

> [!NOTE]
> このアクションは、データベースが信頼されていない場合には許可されません。 

## <a name="setting"></a>Setting

"SaveObject/オブジェクトの保存" アクションの引数は次のとおりです。

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
<td><p><strong>オブジェクトの種類</strong></p></td>
<td><p>The type of object you want to save. Click <strong>Table</strong>, <strong>Query</strong>, <strong>Form</strong>, <strong>Report</strong>, <strong>Macro</strong>, <strong>Module</strong>, <strong>Data Access Page</strong>, <strong>Server View</strong>, <strong>Diagram</strong>, <strong>Stored Procedure</strong>, or <strong>Function</strong> in the <strong>Object Type</strong> box in the <strong>Action Arguments</strong> section of the Macro Builder pane. To select the active object, leave this argument blank. If you select an object type in this argument, you must select an existing object's name in the <strong>Object Name</strong> argument.  </p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name/オブジェクト名</strong></p></td>
<td><p>保存するオブジェクトの名前を指定します。[ <strong>オブジェクト名</strong>] ボックスには、データベース内のオブジェクトのうち、" <strong>Object Type/オブジェクトの種類</strong> " 引数で選択した種類のオブジェクトがすべて表示されます。" <strong>Object Type/オブジェクトの種類</strong> " 引数を指定せず、この引数も指定しないと、アクティブ オブジェクトが保存されます。この引数に新しい名前を入力すると、アクティブ オブジェクトが入力した名前で保存されます。 新しい名前を入力する場合は、Microsoft Access オブジェクトの名前付け規則に従う必要があります。  </p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>注釈

The **SaveObject** action works on all database objects that the user can explicitly open and save. The specified object must be open for the **SaveObject** action to have any effect on the object. This action has the same effect as selecting an object and then saving it by clicking **Save** on the **Quick Access Toolbar**. 

Leaving the **Object Type** argument blank and entering a new name in the **Object Name** argument has the same effect as clicking **Save As** on the **Quick Access Toolbar**, and entering a new name for the active object. Using the **SaveObject** action enables you to specify an object to save and to perform a **Save As** command from a macro.

> [!NOTE]
> You can't use the **SaveObject** action to save any of the following with a new name:
> - フォーム ビューまたはデータシート ビューのフォーム
> - 印刷プレビューのレポート
> - モジュール
> - データシート ビューまたは印刷プレビューのサーバー ビュー
> - ページ ビューのデータ アクセス ページ
> - データシート ビューまたは印刷プレビューのテーブル
> - データシート ビューまたは印刷プレビューのクエリ
> - データシート ビューまたは印刷プレビューのストアド プロシージャ

The **SaveObject** action, whether it's carried out in a macro run in the current database or in a library database, always saves the specified object or the active object in the database in which the object was created.

If you save the active object with a new name, but the name is the same as the name of an existing object of this type, a dialog box asks if you want to overwrite the existing object. If you've set the **Warnings On** argument of the **SetWarnings** action to **No**, the dialog box isn't displayed and the old object is automatically overwritten.

To run the **SaveObject** action in a Visual Basic for Applications (VBA) module, use the **Save** method of the **DoCmd** object.

