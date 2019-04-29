---
title: ビューを操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- ビュー クラス [infopath 2007],InfoPath 2007,ビューを操作する,ビュー [InfoPath 2007]
localization_priority: Normal
ms.assetid: 947b33c3-2acc-45d2-a89d-a712b6bc53df
description: InfoPath フォーム テンプレートで作業する場合、フォームのビューにアクセスし、ビューに含まれるデータにさまざまな操作を行うコードを書くことができます。Microsoft.Office.InfoPath 名前空間によって提供される InfoPath オブジェクト モデルでは、View クラスのメンバーを使用して、フォームのビューにアクセスできます。
ms.openlocfilehash: 829375a87513634ef0b38b6d92de9f33a605e89f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406298"
---
# <a name="work-with-views"></a>ビューを操作する

InfoPath フォーム テンプレートで作業する場合、フォームのビューにアクセスし、ビューに含まれるデータにさまざまな操作を行うコードを書くことができます。[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath オブジェクト モデルでは、 [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスのメンバーを使用して、フォームのビューにアクセスできます。 
  
## <a name="overview-of-the-view-class"></a>View クラスの概要

[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、InfoPath ビューを操作できます。 
  
> [!NOTE]
> [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスのメソッドとプロパティは [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) イベント中には利用できません。 
  
|**名前**|**説明**|
|:-----|:-----|
|[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.DisableAutoUpdate.aspx) メソッド  <br/> |フォームの基になる XML ドキュメントと、それに関連付けられているビューが自動的に同期しないようにします。  <br/> |
|[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.EnableAutoUpdate.aspx) メソッド  <br/> |フォームの基になる XML ドキュメントと、それに関連付けられているビューが自動的に同期するようにします。  <br/> |
|[ExecuteAction(ActionType)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) メソッド  <br/> |ビューで現在選択されているデータに基づいて、フォームの基になる XML ドキュメントに対して編集コマンドを実行します。  <br/> |
|[ExecuteAction(ActionType, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ExecuteAction.aspx) メソッド  <br/> |指定したフィールドまたはグループに基づいて、フォームの基になる XML ドキュメントに対して編集コマンドを実行します。  <br/> |
|[Export](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Export.aspx) メソッド  <br/> |指定された形式のファイルにビューをエクスポートします。  <br/> |
|[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ForceUpdate.aspx) メソッド  <br/> |フォームの基になる XML ドキュメントと、それに関連付けられているビューを強制的に同期させます。  <br/> |
|[GetContextNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド  <br/> |指定したノードから開始する、返された XML ノードに対して反復処理を行うための **XPathNodeIterator** オブジェクトへの参照を取得します。  <br/> |
|[GetContextNodes(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) メソッド  <br/> |指定したフィールドまたはグループにバインドされているコントロール内にある、現在の選択範囲内の返された XML ノードに対して反復処理を行うための **XPathNodeIterator** オブジェクトへの参照を取得します。  <br/> |
|[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) メソッド  <br/> |ビューで現在選択されている項目内のすべての XML ノードに対して反復処理を行うための **XPathNodeIterator** オブジェクトへの参照を取得します。  <br/> |
|[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド  <br/> |指定した開始 XML ノードに基づいて、ビュー内の一定範囲内のノードを選択します。  <br/> |
|[SelectNodes(XPathNavigator, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド  <br/> |指定した開始 XML ノードと終了 XML ノードに基づいて、ビュー内の一定範囲内のノードを選択します。  <br/> |
|[SelectNodes(XPathNavigator, XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッド  <br/> |指定した開始 XML ノード、終了 XML ノード、および指定されたコントロールに基づいて、ビュー内の一定範囲のノードを選択します。  <br/> |
|[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッド  <br/> |このメソッドに渡された **XPathNavigator** オブジェクトで指定されるノードにバインドされた編集可能なコントロールに格納されているテキストを選択します。  <br/> |
|[SelectText(XPathNavigator, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッド  <br/> |このメソッドに渡された **XPathNavigator** オブジェクトで指定されるノードにバインドされた編集可能なコントロールに格納されているテキスト、および指定されたコントロールを選択します。  <br/> |
|[ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ShowMailItem.aspx) メソッド  <br/> |現在のビューが含まれる電子メール メッセージを作成します。  <br/> |
|[ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.ViewInfo.aspx) プロパティ  <br/> |ビューに関連付けられている [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) オブジェクトへの参照を取得します。  <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) プロパティ  <br/> |ビューに関連付けられている [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクトへの参照を取得します。  <br/> |
   
> [!NOTE]
> InfoPath オブジェクト モデルには、[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) クラスと [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) クラスもあります。これらを使用して、フォームに実装されているすべてのビューに関する情報を取得できます。 
  
## <a name="using-the-view-class"></a>View クラスを使用する

[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスにアクセスするには、 [this](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) (C#) または [Me](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (Visual Basic) キーワードを使用してアクセスする **XmlForm** クラスの **CurrentView** プロパティを使用します。ビューの名前にアクセスするには、ビューに関連付けられている [ViewInfo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfo.aspx) オブジェクトにアクセスする必要があります。次の例では、現在アクティブなビューの名前をメッセージ ボックスに表示する方法を示しています。 
  
```cs
MessageBox.Show("Current view name: " + 
   this.CurrentView.ViewInfo.Name);
```

```vb
MessageBox.Show("Current view name: " &amp; _
   Me.CurrentView.ViewInfo.Name)
```

すべての InfoPath フォーム テンプレートには、少なくとも 1 つの既定のビューがありますが、InfoPath ではフォームの基になる XML ドキュメントの複数のビューを作成することもできます。複数のビューがある場合、[ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) を使用して、フォーム テンプレートに実装されたすべてのビューで作業できます。フォーム テンプレートの [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) にアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx) クラスの [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを使用します。現在アクティブなビューをプログラムで変更するには、次のコード サンプルで示すように [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.SwitchView.aspx) の [SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) メソッドを使用します。 
  
```cs
this.ViewInfos.SwitchView("MySecondView");
```

```vb
Me.ViewInfos.SwitchView("MySecondView")
```

ビューを切り替える前の例は、フォームが開かれた後にのみ動作します。[Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) イベント中の既定のビューを設定するには、次の例で示すように、 [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.Initial.aspx) クラスの [Initial](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) プロパティを使用します。ただし、この値は、フォームが保存され、もう一度開かれた後にのみ有効になることに注意してください。 
  
```cs
this.ViewInfos.Initial = this.ViewInfos["MyInitialView"];
```

```vb
Me.ViewInfos.Initial = Me.ViewInfos["MyInitialView"];
```

## <a name="selecting-controls-in-a-view"></a>ビューでコントロールを選択する

InfoPath では、現在のビューでプログラムからコントロールを選択するために、[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) クラスの 2 つのメソッド、 [SelectText()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) と [SelectNodes()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) が用意されており、両方ともオーバーロードされます。 [SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッドはデータ入力用のコントロール ( **テキスト ボックス**など) に使用され、 **SelectNodes** メソッドは構造用のコントロール ( **省略可能セクション**など) に使用されます。ビューで特定のコントロールを選択するには、ノードとオプションでコントロールの ViewContext ID を指定する必要があります。ViewContext ID は、複数のコントロールがデータ ソース内の同じノードにバインドされている場合に必須となります。ViewContext ID 情報は、フォームのデザイン時に InfoPath により提供されます。
  
コントロールの ViewContext ID は、コントロールのプロパティ ダイアログ ボックスの **[詳細設定]** タブに表示されます。これを確認するには、コントロールを右クリックし、[_コントロール名_ **プロパティ**] をクリックして、**[詳細設定]** タブをクリックします。これで、コントロールの ViewContext ID が **[詳細設定]** タブの **[コード]** セクションに表示されます。 
  
## <a name="when-to-use-selecttext-and-selectnodes"></a>SelectText および SelectNodes の使用方法

[SelectText(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) メソッドを使用して、以下のデータ入力用のコントロールをプログラムから選択できます。 
  
- テキスト ボックス
    
- リッチ テキスト ボックス
    
- 日付の選択
    
[SelectNodes(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) メソッドを使用して、以下の構造用のコントロールをプログラムから選択できます。 
  
- 省略可能セクション
    
- 選択肢セクション
    
- 繰り返しセクション (項目)
    
- 繰り返しテーブル (行)
    
- 繰り返し再帰セクション (項目)
    
- 箇条書き、段落番号、および標準リスト
    
- 横方向の繰り返しテーブル
    
以下のコントロールは、プログラムから選択またはフォーカスの設定を行うことはできません。
  
- ドロップダウン リスト ボックス
    
- リスト ボックス
    
- チェック ボックス
    
- オプション ボタン
    
- ボタン
    
- 画像 (リンクまたは埋め込み)
    
- インク描画
    
- Hyperlink
    
- 式ボックス
    
- 縦書きラベル
    
- ActiveX セクション
    
- 横方向領域
    
## <a name="using-the-selecttext-and-selectnodes-methods"></a>SelectText および SelectNodes メソッドを使用する

次の例では、1 つのパラメーター  [xmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) を持つ **SelectText** メソッドの _SelectText(XPathNavigator)_ オーバーロードを使用して、"my:field1" にバインドされている **テキスト ボックス**を選択しています。 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode);
```

複数のコントロールが "my:field1" にバインドされている場合は、個別のコントロールを選択するための追加の  [viewContext](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) パラメーターを提供する **SelectText** メソッドの _SelectText(XPathNavigator, String)_ オーバーロードを使用する必要があります。次の例では、"my:field1" にバインドされている 2 つの **テキスト ボックス** コントロールがあることを想定しています。1 番目のコントロールの ViewContext ID は "CTRL1" で、2 番目のコントロールの ViewContext ID は "CTRL8" です。2 番目のコントロールが選択されています。 
  
```cs
// Create XPathNavigator and select field.
XPathNavigator textNode = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:field1", NamespaceManager);
// Select text in specified field.
CurrentView.SelectText(textNode, "CTRL8");
```

次の例では、1 つのパラメーター  [startNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) のみを持つ **SelectNodes** メソッドの _SelectNodes(XPathNavigator)_ オーバーロードを使用して、繰り返しグループ "my:employee" にバインドされている繰り返しテーブル内の最初の行を選択しています。 
  
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
```

繰り返しテーブル内の複数の行を選択することもできます。次の例では、繰り返しグループ "my:employee" にバインドされている繰り返しテーブル内の最初の 3 行が、 [startNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)パラメーターと  **endNode** パラメーターを持つ _SelectNodes_ メソッドの _SelectNodes(XPathNavigator, XPathNavigator, String)_ オーバーロードを使用して選択されています。 
  
```cs
// Create XPathNavigators to specify range of nodes.
XPathNavigator repeatingTableRow1 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:employee[1]", NamespaceManager);
XPathNavigator repeatingTableRow3 = 
   CreateNavigator().SelectSingleNode(
   "/my:myFields/my:employees/my:myemployee[3]", NamespaceManager);
// Select range of nodes in specified XPathNavigators.
CurrentView.SelectNodes(repeatingTableRow1, repeatingTableRow3);
```


