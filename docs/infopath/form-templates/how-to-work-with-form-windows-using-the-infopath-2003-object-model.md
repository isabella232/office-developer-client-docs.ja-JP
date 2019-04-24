---
title: InfoPath 2003 オブジェクト モデルを使用してフォーム ウィンドウを操作する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2003 互換のフォーム テンプレート,フォーム ウィンドウ,フォーム ウィンドウ [InfoPath 2007], InfoPath 2003 互換のフォーム テンプレート
localization_priority: Normal
ms.assetid: fbcf3a04-ee0f-40a6-8edd-583ae203e2e1
description: InfoPath フォームをプログラムから操作するときは、フォームのウィンドウにアクセスするコードを記述し、ウィンドウに含まれるアイテムの一部をカスタマイズすることができます。InfoPath 2003 互換のオブジェクト モデルでは、WindowsCollection インターフェイスと WindowObject インターフェイスを関連させて使用することにより、フォームのウィンドウにアクセスできます。
ms.openlocfilehash: f8939fc562cf16c1bce0f6f88bba659e895254f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299896"
---
# <a name="work-with-form-windows-using-the-infopath-2003-object-model"></a>InfoPath 2003 オブジェクト モデルを使用してフォーム ウィンドウを操作する

InfoPath フォームをプログラムから操作するときは、フォームのウィンドウにアクセスするコードを記述し、ウィンドウに含まれるアイテムの一部をカスタマイズすることができます。InfoPath 2003 互換のオブジェクト モデルでは、[WindowsCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowObject.aspx) インターフェイスと [WindowObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.WindowsCollection.aspx) インターフェイスを関連させて使用することにより、フォームのウィンドウにアクセスできます。 
  
InfoPath には、次の 2 種類のウィンドウがあります。
  
- ユーザーがフォームにデータを入力するときに使用する編集ウィンドウ。
    
- ユーザーがフォーム テンプレートをデザインするときに使用するデザイン ウィンドウ。
    
フォーム テンプレートのコードを書くときに便利な機能を備えているのは編集ウィンドウです。参照する **WindowObject** インスタンスを使用して、さまざまなプロパティとメソッドにアクセスし、フォーム編集の操作性をカスタマイズすることができます。 
  
## <a name="overview-of-the-windowscollection-interface"></a>WindowsCollection インターフェイスの概要

**WindowsCollection** インターフェイスには、次のプロパティがあります。フォーム テンプレートの開発者は、これらのプロパティを使用して、フォーム テンプレートに含まれている **WindowObject** インスタンスを管理できます。 
  
|**[名前]**|**[説明]**|
|:-----|:-----|
|[Count](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Count.aspx) プロパティ  <br/> |コレクションに含まれている **Window** オブジェクトの数を返します。  <br/> |
|[Item](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Windows.Item.aspx) プロパティ  <br/> |指定された **Window** オブジェクトの参照を返します。  <br/> **注**: Visual C# では、**Item** プロパティを呼び出す代わりに、インデクサーを使用してコレクションにアクセスします。 例: `thisApplication.Windows[0].Caption`。           |
   
## <a name="overview-of-the-window-object"></a>Window オブジェクトの概要

**WindowObject** インターフェイスには、次のメソッドとプロパティがあります。フォームの開発者は、これらを使用して、InfoPath のウィンドウを操作できます。 これらのメソッドとプロパティのサポートは、操作対象のウィンドウの種類 ([XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx)) によって異なります。 メソッドとプロパティの中には、ウィンドウの種類がエディター (**XdWindowType.xdEditorWindow**) でないと機能しないものがあります。 その他のメソッドとプロパティは、ウィンドウの種類がエディターでも、デザイナー (**XdWindowType.xdDesignerWindow**) でも機能します。 さらに、InfoPath オブジェクト モデルのすべてのメンバーと同様に、フォーム テンプレートから呼び出す際のメソッドとプロパティのサポートは、セキュリティ レベルおよびフォームのデプロイ方法によって異なります。
  
|**[名前]**|**[説明]**|**ウィンドウの種類のサポート**|
|:-----|:-----|:-----|
|[Activate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Activate.aspx) メソッド  <br/> |現在アクティブなウィンドウを指定します。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[Active](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Active.aspx) プロパティ  <br/> |ウィンドウが現在アクティブなウィンドウかどうかを示す **Boolean** 値を返します。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[Caption](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Caption.aspx) プロパティ  <br/> |**Window** オブジェクトによって表されるウィンドウのキャプション テキストを返す、または設定する読み取り/書き込みプロパティ。  <br/> |**xdEditorWindow** のみ  <br/> |
|[Close](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Close.aspx) メソッド  <br/> |ウィンドウを閉じます。  <br/> |**xdEditorWindow** のみ  <br/> |
|[CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.CommandBars.aspx) プロパティ  <br/> |Microsoft Office **CommandBars** オブジェクトへの参照を返します。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[Height](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Height.aspx) プロパティ  <br/> |**Window** オブジェクトによって表されるウィンドウのポイント単位での高さを指定する Long 型整数の読み取り/書き込みプロパティ。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[Left](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Left.aspx) プロパティ  <br/> |**Window** オブジェクトによって表されるウィンドウのポイント単位での水平方向の位置を指定する Long 型整数の読み取り/書き込みプロパティ。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[MailEnvelope](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.MailEnvelope.aspx) プロパティ  <br/> |[MailEnvelopeObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.MailEnvelopeObject.aspx) オブジェクトへの参照を返します。  <br/> |**xdEditorWindow** のみ  <br/> |
|[TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.TaskPanes.aspx) プロパティ  <br/> |[TaskPanesCollection](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.TaskPanesCollection.aspx) コレクションへの参照を返します。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[Top](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Top.aspx) プロパティ  <br/> |**Window** オブジェクトによって表されるウィンドウのポイント単位での垂直方向の位置を指定する Long 型整数の読み取り/書き込みプロパティ。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[WindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowType.aspx) プロパティ  <br/> |[XdWindowType](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowType.aspx) 列挙に基づいて、ウィンドウの種類を表す数値を返します。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[Width](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.Width.aspx) プロパティ  <br/> |**Window** オブジェクトによって表されるウィンドウのポイント単位での幅を指定する Long 型整数の読み取り/書き込みプロパティ。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[WindowState](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.WindowState.aspx) プロパティ  <br/> |[Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdWindowState.aspx) オブジェクトによって表されるウィンドウの状態を返す、または設定する **XdWindowState** 型の読み取り/書き込みプロパティ。  <br/> |**xdDesignWindow** および **xdEditorWindow**  <br/> |
|[XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Window2.XDocument.aspx) プロパティ  <br/> |ウィンドウに関連付けられている [_XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument.aspx) オブジェクトへの参照を返します。  <br/> |**xdEditorWindow** のみ  <br/> |
   
## <a name="using-the-windowscollection-and-window-interfaces"></a>WindowsCollection インターフェイスおよび Window インターフェイスを使用する

**WindowsCollection** インターフェイスには、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Windows.aspx) インターフェイスの [Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) プロパティを通じてアクセスできます。 **WindowsCollection** インターフェイスを使用してフォームのウィンドウにアクセスするときは、インデクサーを使用するか (Visual C# の場合)、 **Item** プロパティに Long 型整数を渡して (Visual Basic の場合)、 **WindowObject** インターフェイス インスタンスへの参照を返します。たとえば、次のコードは、 **WindowsCollection** に含まれる最初の **WindowObject** への参照を設定します。
  
```cs
WindowObject objWindow = thisApplication.Windows[0];
```

```vb
Dim objWindow As WindowObject = thisApplication.Windows(0)
```

ただし、次のコードに示すとおり、 [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.ActiveWindow.aspx) インターフェイスの **ActiveWindow** プロパティを使用すると、 ** WindowsCollection ** を介することなく、現在開いているウィンドウに直接アクセスできます。
  
```cs
WindowObject objWindow = thisApplication.ActiveWindow;
```

```vb
Dim objWindow As WindowObject = thisApplication.ActiveWindow
```

> [!NOTE]
> InfoPath マネージ コード プロジェクトをデバッグするときは、デバッグ ウィンドウがアクティブなので、 **ActiveWindow** プロパティは常に **null** を返します。 
  
**WindowObject** は、 [View](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.Window.aspx) インターフェイスの [Window](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.View.aspx) プロパティを使用してアクセスすることもできます。このインターフェイスは、フォームの基になる XML ドキュメントに関連付けられています。 **XDocument** インターフェイスの **View** プロパティは、 **View** オブジェクトにアクセスするために使用します。たとえば、次のコードは、フォームの基になる XML ドキュメントのビューに関連付けられている **WindowObject** への参照を設定します。 
  
```cs
WindowObject objWindow = thisXDocument.View.Window;
```

```vb
Dim objWindow As WindowObject = thisXDocument.View.Window
```

> [!NOTE]
> **Window** オブジェクトの一部のプロパティとメソッドは、編集ウィンドウでのみ使用できます。デザイン ウィンドウで使用すると、エラーが発生します。各ウィンドウの種類でサポートされるプロパティとメソッドの一覧については、前に示した表を参照してください。コードで **WindowType** プロパティを使用すると、現在操作しているウィンドウの種類を確認できます。 
  

