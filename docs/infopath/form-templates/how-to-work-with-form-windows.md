---
title: フォーム ウィンドウを操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- windowscollection [infopath 2007],フォーム ウィンドウ [InfoPath 2007],Window クラス [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: 32ae2427-882b-45f8-8754-0e8c27fc23ba
description: InfoPath フォームをプログラムから操作するときは、フォームのウィンドウにアクセスするコードを記述し、ウィンドウに含まれるアイテムの一部をカスタマイズすることができます。Microsoft.Office.InfoPath 名前空間によって提供される InfoPath オブジェクト モデルでは、Window クラスを WindowCollection クラスと共に使用した、フォームのウィンドウへのアクセスがサポートされています。
ms.openlocfilehash: 7edb5f4e1530b64251ea89f0f41ad6926a11f2ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59568104"
---
# <a name="work-with-form-windows"></a>フォーム ウィンドウを操作する

InfoPath フォームをプログラムから操作するときは、フォームのウィンドウにアクセスするコードを記述し、ウィンドウに含まれるアイテムの一部をカスタマイズすることができます。[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供される InfoPath オブジェクト モデルでは、 [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) クラスを [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) クラスと共に使用した、フォームのウィンドウへのアクセスがサポートされています。 
  
> [!NOTE]
> フォームのウィンドウを操作するクラスは、[ **InfoPath エディター フォーム**] で作業しているときのみ使用できます。フォーム テンプレートの [ **互換性**] 設定が [ **Web ブラウザー フォーム**] の場合には、これらのクラスは使用できません。 
  
InfoPath には、次の 2 種類のウィンドウがあります。 
  
- ユーザーがフォームにデータを入力するときに使用する編集ウィンドウ。
    
- ユーザーがフォーム テンプレートをデザインするときに使用するデザイン ウィンドウ。
    
フォーム テンプレートのコードを書くときに便利な機能を備えているのは編集ウィンドウです。現在のウィンドウを表す [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクトを使用して、さまざまなプロパティとメソッドにアクセスし、フォーム編集の操作性をカスタマイズすることができます。 
  
## <a name="overview-of-the-windowscollection-class"></a>WindowsCollection クラスの概要

[WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) クラスには、次のプロパティがあります。フォーム テンプレートの開発者は、これらのプロパティを使用して、フォームに含まれている [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクトを管理できます。 
  
|**名前**|**説明**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Count.aspx) プロパティ  <br/> |コレクションに含まれている [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクトの数を取得します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.Item.aspx) プロパティ  <br/> |指定した [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクトへの参照を取得します。  <br/> |
   
## <a name="overview-of-the-window-class"></a>Window クラスの概要

[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) クラスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用することにより、InfoPath ウィンドウを操作できます。 これらのメソッドとプロパティのサポートは、操作対象のウィンドウの種類 ([WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx)) によって異なります。 メソッドとプロパティの中には、ウィンドウの種類がエディター (**WindowType.Editor**) でないと機能しないものがあります。 その他のメソッドとプロパティは、ウィンドウの種類がエディターでも、デザイナー (**WindowType.Designer**) でも機能します。 さらに、InfoPath オブジェクト モデルのすべてのメンバーと同様に、フォーム テンプレートから呼び出す際のメソッドとプロパティのサポートは、セキュリティ レベルおよびフォームのデプロイ方法によって異なります。
  
|**名前**|**説明**|**ウィンドウの種類のサポート**|
|:-----|:-----|:-----|
|[Activate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Activate.aspx) メソッド  <br/> |ウィンドウをアクティブ化し、ウィンドウにフォーカスを与えます。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Active.aspx) プロパティ  <br/> |ウィンドウが現在アクティブなウィンドウかどうかを示す **Boolean** 値を取得します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[Caption](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Caption.aspx) プロパティ  <br/> |[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクトによって表されるウィンドウのキャプション テキストを取得または設定します。  <br/> |**Editor** のみ  <br/> |
|[Close()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) メソッド  <br/> |未保存のフォームに対する変更や、未保存の変更内容があるフォームを保存するかどうかを確認し、ウィンドウを閉じます。  <br/> |**Editor** のみ  <br/> |
|[Close(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Close.aspx) メソッド  <br/> |ウィンドウを閉じます。オプションで、未保存のフォームや、未保存の変更内容があるフォームを保存せずに強制的に閉じます。  <br/> |**Editor** のみ  <br/> |
|[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) プロパティ  <br/> |ウィンドウに関連付けられている Microsoft Office **CommandBars** コレクションへの参照を取得します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[Height](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Height.aspx) プロパティ  <br/> |ウィンドウの高さ (ポイント単位) を取得または設定します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[Left](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Left.aspx) プロパティ  <br/> |ウィンドウの水平方向の位置 (ポイント単位) を取得または設定します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.MailEnvelope.aspx) プロパティ  <br/> |[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MailEnvelope.aspx) クラスへの参照を取得します。  <br/> |**Editor** のみ  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.TaskPanes.aspx) プロパティ  <br/> |[TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) コレクションへの参照を取得します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[Top](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Top.aspx) プロパティ  <br/> |ウィンドウの垂直方向の位置 (ポイント単位) を取得または設定します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[Width](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.Width.aspx) プロパティ  <br/> |ウィンドウの幅 (ポイント単位) を取得または設定します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowState.aspx) プロパティ  <br/> |ウィンドウの状態を [WindowState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowState.aspx) 値として取得または設定します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.WindowType.aspx) プロパティ  <br/> |ウィンドウの種類を [WindowType](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowType.aspx) 列挙値として取得します。  <br/> |**Designer** と **Editor** の両方  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.XmlForm.aspx) プロパティ  <br/> |ウィンドウに関連付けられた [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) オブジェクトへの参照を返します。  <br/> |**Editor** のみ  <br/> |
   
## <a name="using-the-windowscollection-and-window-classes"></a>WindowsCollection クラスおよび Window クラスを使用する

[WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) クラスには、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Windows.aspx) クラスの [Windows](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) プロパティを通じてアクセスできます。 [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) クラスを使用してフォームのウィンドウにアクセスするときは、インデクサーを使用するか (Visual C# の場合)、 **Item** プロパティに Long 型の整数を渡して (Visual Basic の場合)、 [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) オブジェクト インスタンスへの参照を取得します。たとえば、次のコードは、現在の InfoPath セッションの [WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) に含まれている最初の [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) オブジェクトへの参照を設定します。 
  
```cs
Window myWindow = this.Application.Windows[0];
```

```vb
Dim myWindow As Window = Me.Application.Windows(0)
```

現在開いているウィンドウには、[WindowCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.ActiveWindow.aspx) を介することなく、次のコード行に示すように [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) クラスの [ActiveWindow](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WindowCollection.aspx) プロパティを使用して直接アクセスすることができます。 
  
```cs
Window myWindow = this.Application.ActiveWindow;
```

```vb
Dim myWindow As Window = Me.Application.ActiveWindow
```

[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) クラスの [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.Window.aspx) プロパティを使用して [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) オブジェクトにアクセスすることもできます。このクラスは、フォームの基になる XML ドキュメントの操作に使われている現在のビューを表します。現在のビューを表す [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx) オブジェクトにアクセスするには、 [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) クラスの [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) プロパティを使用します。たとえば、次のコードは、現在のビューに関連付けられている [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) への参照を設定します。 
  
```cs
Window myWindow = this.CurrentView.Window;
```

```vb
Dim myWindow As Window = Me.CurrentView.Window
```

> [!NOTE]
> [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) クラスの一部のプロパティとメソッドは、編集ウィンドウでのみ使用できます。デザイン ウィンドウで使用すると、エラーが発生します。各ウィンドウの種類でサポートされるプロパティとメソッドの一覧については、前に示した表を参照してください。コードで [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) プロパティを使用すると、現在操作しているウィンドウの種類を確認できます。 
  

