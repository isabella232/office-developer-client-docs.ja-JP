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
localization_priority: Normal
ms.openlocfilehash: f4574abc86e6eacd38721e601d26c8b8fbf0a0d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314106"
---
# <a name="activex-control-custom-properties-dialog-box"></a>ActiveX コントロールのカスタム プロパティ ダイアログ ボックス

**適用先:** Access 2013、Office 2013

ActiveX コントロールのプロパティを設定するときに、そのコントロールのカスタム プロパティ ダイアログ ボックスを使うこともできます。カスタム プロパティ ダイアログ ボックスは、デザイン ビューで ActiveX コントロールのプロパティを設定する場合、Microsoft Access のプロパティ シートのプロパティの一覧に代わる機能を提供します。

> [!NOTE]
> [!メモ] ここでの説明は Microsoft Access データベース環境で使用する ActiveX コントロールにのみ有効です。

## <a name="two-ways-to-set-properties"></a>プロパティを設定する2つの方法

カスタム プロパティ ダイアログ ボックスは、ActiveX コントロールを使用するアプリケーションで、Access のプロパティ シートのようなプロパティ シートが提供されていないことがあるために用意されています。カスタム プロパティ ダイアログ ボックスは、ホスト アプリケーションで提供されるインターフェイスに関係なく、キー コントロール プロパティを設定するインターフェイスを提供します。

ActiveX コントロールのプロパティには、次の 2 つのプロパティ シートの両方で設定できるものがあります。

- Microsoft Office Access のプロパティ シート
- ActiveX コントロールのカスタム プロパティ ダイアログ ボックス

デザイン ビューでプロパティを設定するときに、カスタム プロパティ ダイアログ ボックスしか使用できない場合もあります。それは、プロパティの設定に必要なインターフェイスが、Microsoft Office Access のプロパティ シートでは機能しない場合です。たとえば、カレンダー コントロールの **GridFont** プロパティは複数の引数を持ちますが、Microsoft Office Access のプロパティ シートでは 1 つのプロパティに対して複数の引数を設定できません。

## <a name="finding-the-custom-properties-dialog-box"></a>カスタムプロパティダイアログボックスの検索

すべての ActiveX コントロールがカスタム プロパティ ダイアログ ボックスを提供するわけではありません。 コントロールがカスタム プロパティ ダイアログ ボックスを提供するかどうかを確認するには、そのコントロールの Microsoft Office Access プロパティ シートで " **Custom** /カスタムコントロール" プロパティを確認します。 プロパティのリストに**custom**という名前が含まれている場合、コントロールはカスタムプロパティダイアログボックスを提供します。

## <a name="using-the-custom-properties-dialog-box"></a>カスタムプロパティダイアログボックスを使用する

access のプロパティシートで [**カスタム**プロパティ] ボックスを選択したら、プロパティボックスの右側にある [ **.** ..] ボタンをクリックして、コントロールのカスタムプロパティダイアログボックスを表示します。これは、多くの場合、タブ付きダイアログボックスとして表示されます。 Choose the tab that contains the interface for setting the properties that you want to set.

1つのタブで変更を行った後、[**適用**] ボタン (指定されている場合) を選択することで、それらの変更をすぐに適用することができます。 他のタブを選択して、必要に応じて他のプロパティを設定できます。 [カスタムプロパティ] ダイアログボックスで行ったすべての変更を承認するには、[ **OK** ] をクリックします。 プロパティの設定を変更せずに、access のプロパティシートに戻るには、[**キャンセル**] をクリックします。

[カスタムプロパティ] ダイアログボックスを表示するには、[**編集**] メニューの [ActiveX コントロール**オブジェクト**] コマンド (たとえば、[**カレンダーコントロールオブジェクト**]) の**プロパティ**サブコマンドを選択するか、または [同じサブコマンドを選択します。ActiveX コントロールのショートカットメニュー。 また、Access プロパティ シートに表示される ActiveX コントロール用のプロパティの中には、カレンダー コントロールの **GridFontColor** プロパティのように、プロパティ ボックスの右側に [ **ビルド** ] ボタンが表示されるプロパティもあります。 [**ビルド**] ボタンをクリックすると、[カスタムプロパティ] ダイアログボックスが表示され、適切なタブ (たとえば、**色**) が選択されます。

