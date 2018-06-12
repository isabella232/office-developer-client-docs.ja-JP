---
title: InfoPath 2003 オブジェクト モデルを使用してビューに関する作業します。
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, views,views [InfoPath 2007], InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: feb1bfcb-1cb1-4d5c-bc84-df86a33a5934
description: InfoPath フォーム テンプレートの作業を行うときは、フォームのビューにアクセスし、ビューに格納されているデータに対してさまざまな操作を実行するためのコードを書くことができます。InfoPath 2003 互換のオブジェクト モデルでは、ViewObject インターフェイスのメンバーを使用してフォームのビューにアクセスできます。
ms.openlocfilehash: 1cbc472993ff18b26f31e3bc28b12a75e559644a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799130"
---
# <a name="work-with-views-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してビューに関する作業します。

InfoPath フォーム テンプレートの作業を行うときは、フォームのビューにアクセスし、ビューに格納されているデータに対してさまざまな操作を実行するためのコードを書くことができます。InfoPath 2003 互換のオブジェクト モデルでは、[ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスのメンバーを使用してフォームのビューにアクセスできます。 
  
## <a name="overview-of-the-viewobject-interface"></a>ViewObject インターフェイスの概要

[ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用して、InfoPath のビューを操作できます。 
  
> [!NOTE]
> [!メモ] [ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスのメソッドとプロパティは、 [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) イベント中には利用できません。 
  
|**名前**|**説明**|
|:-----|:-----|
|[DisableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.DisableAutoUpdate.aspx) メソッド  <br/> |XML Document Object Model (DOM) とビューの同期を無効にします。  <br/> |
|[EnableAutoUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.EnableAutoUpdate.aspx) メソッド  <br/> |XML DOM とビューの同期を有効にします。  <br/> |
|[ExecuteAction](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ExecuteAction.aspx) メソッド  <br/> |InfoPath の編集操作を実行します。  <br/> |
|[Export](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Export.aspx) メソッド  <br/> |指定した形式のファイルとしてビューをエクスポートします。  <br/> |
|[ForceUpdate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.ForceUpdate.aspx) メソッド  <br/> |XML DOM とビューを同期します。  <br/> |
|[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetContextNodes.aspx) メソッド  <br/> |指定した XML ノードとビュー コンテキストまたはビュー内の現在の選択範囲に基づいて、[XMLNodesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XMLNodesCollection.aspx) インターフェイスへの参照を返します。  <br/> |
|[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.GetSelectedNodes.aspx) メソッド  <br/> |ビュー内の現在の選択範囲に基づいて、 **XMLNodesCollection** インターフェイスへの参照を返します。  <br/> |
|[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectNodes.aspx) メソッド  <br/> |ビュー内の XML ノードの範囲を選択します。  <br/> |
|[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SelectText.aspx) メソッド  <br/> |ビュー内の指定した XML ノードに含まれるテキストを選択します。  <br/> |
|[SwitchView](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.SwitchView.aspx) メソッド  <br/> |InfoPath のフォームを、指定したビューに切り替えます。  <br/> |
|[Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Name.aspx) プロパティ  <br/> |現在のビューの名前を示す文字列値を返します。  <br/> |
|[Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) プロパティ  <br/> |ビューに関連付けられている [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) にアクセスする **WindowObject** インターフェイスへの参照を返します。  <br/> |
   
> [!NOTE]
> [!メモ] InfoPath 2003 互換オブジェクト モデルには、[ViewInfosCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfosCollection.aspx) インターフェイスもあります。これを使用して、フォーム内で実装されているすべてのビューに関する情報を取得できます。 
  
## <a name="using-the-viewobject-interface"></a>ViewObject インターフェイスを使用する

[ViewObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewObject.aspx) インターフェイスは、 [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.View.aspx) インターフェイス (フォーム コード クラスの  [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) メソッドで初期化される  `thisXDocument` 変数を通じてアクセス) の `_Startup` プロパティを通じてアクセスされます。たとえば、次のコード例では、 [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) インターフェイスの [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) メソッドを使用して、フォームの基になる XML ドキュメントに関連付けられている現在のビューの名前を示すメッセージ ボックスを表示する方法を示します。 
  
```cs
thisXDocument.UI.Alert("Current view name: " + 
   thisXDocument.View.Name);
```

```vb
thisXDocument.UI.Alert("Current view name: " &amp; _
   thisXDocument.View.Name)
```

すべての InfoPath フォームには既定のビューが 1 つ以上含まれますが、フォームの基になる XML ドキュメントのビューを複数作成することもできます。フォーム内に複数のビューがあるときは、 **View** オブジェクトを使用して、現在アクティブなビューを操作できます。現在アクティブなビューをプログラムによって変更するには、次のコード例に示すとおり、 **View** オブジェクトの **SwitchView** メソッドを使用します。 
  
```cs
thisXDocument.View.SwitchView("MySecondView");
```

```vb
thisXDocument.View.SwitchView("MySecondView")
```

ビューを切り替えるこの例は、フォームを開いた後にのみ動作します。 **OnLoad** イベントの発生中に既定のビューを設定するには、次の例に示すとおり、 [ViewInfoObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfo.IsDefault.aspx) インターフェイスの [IsDefault](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.ViewInfoObject.aspx) プロパティを使用します。 
  
```cs
thisXDocument.ViewInfos["MyDefaultView"].IsDefault = true;
```

```vb
thisXDocument.ViewInfos("MyDefaultView").IsDefault = True
```


