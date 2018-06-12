---
title: 'チュートリアル: 作成し、InfoPath オブジェクト モデルを使用して基本的なフォーム テンプレートのデバッグ'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], walkthroughs,form templates [InfoPath 2007], creating InfoPath 2003-compatible,InfoPath 2003-compatible form templates, walkthroughs
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: ここでは、Microsoft.Office.Interop.InfoPath.SemiTrust 名前空間から提供される InfoPath 2003 互換オブジェクト モデルを使用する基本的な InfoPath マネージ コード フォーム テンプレートを作成する手順を順をおって説明します。
ms.openlocfilehash: 3939cfcfdf2a8683fe614c5f49cc8b2719484ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799219"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a>チュートリアル: 作成し、InfoPath オブジェクト モデルを使用して基本的なフォーム テンプレートのデバッグ

ここでは、[Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) 名前空間から提供される InfoPath 2003 互換オブジェクト モデルを使用する基本的な InfoPath マネージ コード フォーム テンプレートを作成する手順を順をおって説明します。 
  
## <a name="hello-world"></a>Hello World

次の例では、InfoPath 2003 互換オブジェクト モデルの [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) メソッドを使用して簡単な警告ダイアログ ボックスを表示する方法を説明します。 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a>InfoPath 2003 互換オブジェクト モデルを使用する新しい InfoPath フォーム テンプレートを作成する

1. [InfoPath 2003 オブジェクト モデルを使用してフォーム テンプレートの作成](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)で説明したように、InfoPath 2003 と互換性のあるオブジェクト モデルで動作する新しいフォーム テンプレートを作成します。
    
2. フォーム テンプレート プロジェクトを HelloWorld という名前で保存します。 
    
   プロジェクト システムがコード ファイルとプロジェクト ファイルを作成し、InfoPath のデザイン モードで空白のフォーム テンプレートを開きます。これでイベント ハンドラーを追加する準備ができました。
    
### <a name="add-a-button-with-an-onclick-event-handler"></a>OnClick イベント ハンドラーを設定したボタンを追加する

1. [ **ホーム**] タブの [ **コントロール**] セクションで、[ **ボタン**] コントロールをクリックして、ビューに挿入します。 
    
2. 挿入したコントロールを右クリックして、[ **ボタンのプロパティ**] をクリックします。
    
3. [ **ラベル**] を Alert に変更します。
    
4. [ **ID**] を AlertID に変更します。
    
5. [ **フォームのコードを編集**] をクリックします。
    
   [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) イベントのイベント ハンドラー スケルトンが作成され、Visual Studio 2012 のコード エディターにフォーカスが移動します。 イベント ハンドラーの使用方法の詳細については、[追加のイベント ハンドラーを使用して InfoPath 2003 オブジェクト モデル](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)を参照してください。 
    
   これでボタンのイベント ハンドラーにフォーム コードを追加する準備ができました。
    
### <a name="add-form-code-to-the-event-handler"></a>イベント ハンドラーにフォーム コードを追加する

1. **OnClick** イベント ハンドラーに次のコードを入力します。 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   コード行に含まれるピリオドを入力するたびに Microsoft IntelliSense のボックスが表示されます。イベント ハンドラー全体は次のようになります。
    
   ```cs
    [InfoPathEventHandler(MatchPath="AlertID", EventType=InfoPathEventType.OnClick)]
    public void AlertID_OnClick(DocActionEvent e)
    {
        thisXDocument.UI.Alert("Hello World!");
    }
   ```

   ```vb
    <InfoPathEventHandler(MatchPath:="AlertID", EventType:=InfoPathEventType.OnClick)>
    Public Sub AlertID_OnClick(ByVal e As DocActionEvent)
        thisXDocument.UI.Alert("Hello World!")
    End Sub
   ```

   > [!NOTE]
   > [!メモ] **Alert** メソッドを使用する代わりに、 **System.Windows.Forms** 名前空間の **MessageBox.Show** メソッドを使用してメッセージ ボックスを表示することもできます。それには、System.Windows.Forms アセンブリへの参照を追加し、コード ファイル先頭のディレクティブに  `using System.Windows.Forms;` または  `Imports System.Windows.Forms` を追加し、  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)` のようなコード行を入力する必要があります。
  
2. InfoPath のデザイン モード ウィンドウに切り替え、[ **ホーム**] タブの [ **プレビュー**] ボタンをクリックします。 
    
3. [ **プレビュー**] ウィンドウで [ **Alert**] をクリックします。 
    
   "Hello World!" という内容のメッセージ ボックスが表示されます。
    
   次の手順は、フォーム コードにデバッグ用のブレークポイントを追加する方法を示しています。
    
### <a name="debug-form-code"></a>フォーム コードをデバッグする

1. コード エディターで次の行の左にあるグレーのバーをクリックします。
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   赤い円が表示され、コード行が強調表示されます。これは、ランタイムがフォーム コードのこのブレークポイントで一時停止することを表しています。
    
2. [ **デバッグ**] メニューの [ **デバッグ開始**] をクリックします (または F5 キーを押します)。 
    
3. InfoPath の [ **プレビュー**] ウィンドウで [ **Alert**] をクリックします。 
    
   コード エディターにフォーカスが移動し、ブレークポイント行が強調表示されます。
    
4. [ **デバッグ**] メニューで [ **ステップ オーバー**] をクリックするか、または Shift キーを押しながら F8 キーを押して、コード内を順に移動します。 
    
   **Alert** メソッドのコードが実行され、InfoPath の [ **プレビュー**] ウィンドウに "Hello World!" という通知が表示されます。 
    
## <a name="getting-the-current-users-name"></a>現在のユーザーの名前を取得する

.NET Framework のクラスを使用すると、スクリプトでは簡単に利用できなかった機能を利用できます。この例では, .NET Framework のクラスを使用して現在のユーザーの名前を取得する方法を説明します。
  
### <a name="add-an-onload-event-handler"></a>OnLoad イベント ハンドラーを追加する

1. 前の例で作成した InfoPath HelloWorld プロジェクトを開きます。
    
2. [ **表示**] タブの [ **フィールドの表示**] をクリックします。
    
3. [ **マイフィールド**] ノードを右クリックし、[ **追加**] をクリックします。
    
4. **名前**種類の**従業員**、し、 **[ok]** をクリックします。
    
5. [ **employee**] ノードをビューにドラッグします。 
    
6. [ **開発**] タブの [ **OnLoad イベント**] をクリックします。
    
   これによって [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) イベントのイベント ハンドラーが作成され、コード エディターにフォーカスが移動します。フォームを読み込むたびに、このイベント ハンドラーのコードが呼び出されます。次の手順は、ユーザーの名前を取得するフォーム コードをイベント ハンドラーに追加する方法を示しています。 
    
### <a name="add-form-code"></a>フォーム コードを追加する

1. **OnLoad** イベント ハンドラーに次のコードを入力します。 
    
   ```cs
    // Store an XML DOM node as a local variable.
    IXMLDOMNode nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    if(nodeEmployee != null)
    {
        if(nodeEmployee.text == "")
        {
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName;
        }
    }
   ```

   ```vb
    // Store an XML DOM node as a local variable.
    Dim nodeEmployee As IXMLDOMNode
    nodeEmployee = thisXDocument.DOM.selectSingleNode("my:myFields/my:employee");
    If Not(nodeEmployee Is Nothing) Then
        If(nodeEmployee.text = "") Then
        // If the employee name is blank when the form is loaded, 
        // populate the employee node with the current user name.
        nodeEmployee.text = System.Environment.UserName
        End If
    End If
   ```

2. フォームをコンパイルおよびプレビューします。
    
   [employee] ボックスに自分のユーザー名が表示されます。 
    
マネージ コード フォーム テンプレートを展開する方法の詳細については、[コードを含む InfoPath フォーム テンプレートの展開](how-to-deploy-infopath-form-templates-with-code.md)を参照してください。 InfoPath オブジェクト モデルと、InfoPath 2003 互換オブジェクト モデルを使用するマネージ コード フォーム テンプレートでよく行うプログラミング作業については、「[InfoPath 2003 オブジェクト モデルを理解する](understanding-the-infopath-2003-object-model.md)」を参照してください。 
  
## <a name="see-also"></a>関連項目

- [InfoPath 2003 オブジェクト モデルを使用する初期化コードと後処理コード](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [InfoPath 2003 互換オブジェクト モデル](infopath-2003-compatible-object-models.md)
- [InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加します。](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

