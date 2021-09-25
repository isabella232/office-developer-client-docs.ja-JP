---
title: ActiveX コントロールのカスタム プロパティ ダイアログ ボックス
TOCTitle: ActiveX control custom properties dialog box
description: カスタム プロパティ ダイアログ ボックスは、デザイン ビューで ActiveX コントロールのプロパティを設定する場合、Microsoft Access のプロパティ シートのプロパティの一覧に代わる機能を提供します。
ms:assetid: 124cf679-6efc-567a-84d1-8057dec93bde
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845396(v=office.15)
ms:contentKeyID: 48543338
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm4040
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 23b34df71d7bef984f16b32dd047aefb3f69d60a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588985"
---
# <a name="activex-control-custom-properties-dialog-box"></a>ActiveX コントロールのカスタム プロパティ ダイアログ ボックス

**適用先**: Access 2013、Office 2013

ActiveX コントロールのプロパティを設定するときに、そのコントロールのカスタム プロパティ ダイアログ ボックスを使うこともできます。カスタム プロパティ ダイアログ ボックスは、デザイン ビューで ActiveX コントロールのプロパティを設定する場合、Microsoft Access のプロパティ シートのプロパティの一覧に代わる機能を提供します。

> [!NOTE]
> [!メモ] ここでの説明は Microsoft Access データベース環境で使用する ActiveX コントロールにのみ有効です。

## <a name="two-ways-to-set-properties"></a>プロパティを設定する 2 つの方法

カスタム プロパティ ダイアログ ボックスは、ActiveX コントロールを使用するアプリケーションで、Access のプロパティ シートのようなプロパティ シートが提供されていないことがあるために用意されています。カスタム プロパティ ダイアログ ボックスは、ホスト アプリケーションで提供されるインターフェイスに関係なく、キー コントロール プロパティを設定するインターフェイスを提供します。

ActiveX コントロールのプロパティには、次の 2 つのプロパティ シートの両方で設定できるものがあります。

- Microsoft Office Access のプロパティ シート
- ActiveX コントロールのカスタム プロパティ ダイアログ ボックス

デザイン ビューでプロパティを設定するときに、カスタム プロパティ ダイアログ ボックスしか使用できない場合もあります。それは、プロパティの設定に必要なインターフェイスが、Microsoft Office Access のプロパティ シートでは機能しない場合です。たとえば、カレンダー コントロールの **GridFont** プロパティは複数の引数を持ちますが、Microsoft Office Access のプロパティ シートでは 1 つのプロパティに対して複数の引数を設定できません。

## <a name="finding-the-custom-properties-dialog-box"></a>[カスタム プロパティの検索] ダイアログ ボックス

すべての ActiveX コントロールがカスタム プロパティ ダイアログ ボックスを提供するわけではありません。 コントロールがカスタム プロパティ ダイアログ ボックスを提供するかどうかを確認するには、そのコントロールの Microsoft Office Access プロパティ シートで " **Custom** /カスタムコントロール" プロパティを確認します。 プロパティの一覧にカスタムという名前が含 **まれている** 場合、コントロールはカスタム プロパティ ダイアログ ボックスを提供します。

## <a name="using-the-custom-properties-dialog-box"></a>[カスタム プロパティ] ダイアログ ボックスの使用

Microsoft Access プロパティ シートで **[** カスタム] プロパティ ボックスを選択した後、プロパティ ボックスの右側にある [ビルド] ボタンを選択して、多くの場合、タブ付きダイアログ ボックスとして表示されるコントロールのカスタム プロパティ ダイアログ ボックスを表示します。 Choose the tab that contains the interface for setting the properties that you want to set.

1 つのタブで変更を行った後、多くの場合、[適用]ボタン (指定されている場合) を選択して、これらの変更をすぐに適用できます。 他のタブを選択して、必要に応じて他のプロパティを設定できます。 [カスタム プロパティ] ダイアログ ボックスで行われたすべての変更を承認するには **、[OK] ボタンを選択** します。 プロパティ設定を変更せずに Microsoft Access プロパティ シートに戻る場合は、[キャンセル] ボタン **を選択** します。

[編集] メニューの ActiveX コントロール オブジェクトコマンド (たとえば、Calendar Control  **Object)** の Properties サブコマンドを選択するか、ActiveX コントロールのショートカット メニューでこの同じサブコマンドを選択して、カスタム プロパティ ダイアログ ボックスを表示することもできます。 また、Access プロパティ シートに表示される ActiveX コントロール用のプロパティの中には、カレンダー コントロールの **GridFontColor** プロパティのように、プロパティ ボックスの右側に [ **ビルド** ] ボタンが表示されるプロパティもあります。 [ビルド] ボタン **を選択** すると、[カスタム プロパティ] ダイアログ ボックスが表示され、適切なタブ (色など) が **選択されます**。

