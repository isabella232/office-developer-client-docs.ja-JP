---
title: 'チュートリアル: コードを含む基本的なフォーム テンプレートの作成'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- フォーム テンプレート [infopath 2007], 管理対象コードの作成,管理対象コードのフォーム テンプレート [InfoPath 2007], フォーム テンプレートの作成 [InfoPath 2007], チュートリアル,InfoPath 2007, チュートリアル
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: Microsoft InfoPath の場合は、Visual Basic または C# でビジネス ロジックを記述できます。これを実行するには、フォーム テンプレートを InfoPath のデザイン モードで開き、いずれかのユーザー インターフェイス コマンドを使用してイベント ハンドラーを追加します。これにより、コードを記述するための Visual Studio 2012 開発環境が開きます。
ms.openlocfilehash: cc09856750ced28d35c8da172a08a31c4e3cd4a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299735"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a>チュートリアル: コードを含む基本的なフォーム テンプレートの作成

Microsoft InfoPath の場合は、Visual Basic または C# でビジネス ロジックを記述できます。これを実行するには、フォーム テンプレートを InfoPath のデザイン モードで開き、いずれかのユーザー インターフェイス コマンドを使用してイベント ハンドラーを追加します。これにより、コードを記述するための Visual Studio 2012 開発環境が開きます。既定では、Visual Studio 2012 を使用して作成したフォーム テンプレート プロジェクトは、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供されるマネージ コード オブジェクト モデルに対して動作します。 
  
このチュートリアルでは、最初に、Visual Studio 2012 開発環境で C# または Visual Basic を使用して、単純な Hello World アプリケーションを作成する方法を示します。チュートリアルの最後には、[User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) クラスの [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) プロパティを使用して現在のユーザー名を取得し、[ **テキスト ボックス**] コントロールにその値を設定する方法を示すコード サンプルがあります。 
  
## <a name="prerequisites"></a>前提条件

Visual Studio 2012 開発環境を使用してこのチュートリアルを完了するには、以下が必要です。
  
- Microsoft InfoPath がインストールされた Visual Studio 2012。
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a>Visual Studio Tools for Applications の Hello World

以下のチュートリアルでは、Visual Studio 2012 開発環境で [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) クラスの [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) イベントのイベント ハンドラーを記述することによって、[ **ボタン**] コントロールに関連付けられた単純な警告ダイアログ ボックスを表示する方法を学びます。 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a>新しいプロジェクトを作成してプログラミング言語を指定する

1. InfoPath デザイン モードを起動して、[ **空白 (InfoPath エディター)**] フォーム テンプレートをダブルクリックします。 
    
2. 使用するプログラミング言語を指定するために、[ **ファイル**] タブをクリックし、[ **フォームのオプション**] をクリックして、[ **カテゴリ**] の一覧の [ **プログラミング**] をクリックします。次に、[ **フォーム テンプレートのコード言語**] ドロップダウン リストから [ **Visual Basic**] または [ **C#**] を選択します。 
    
   > [!NOTE]
   > [ **フォーム テンプレートのコード言語**] ドロップダウン リスト内のその他のプログラミング言語オプションでは、以前のバージョンの InfoPath との互換性が提供されています。[ **C# (InfoPath 2007 互換)**] および [ **Visual Basic (InfoPath 2007 互換)**] オプションは、このトピック内の手順で機能します。[ **C# (InfoPath 2003 互換)**] および [ **Visual Basic (InfoPath 2003 互換)**] オプションを使用する場合は、「[[ウォークスルー] InfoPath 2003 オブジェクト モデルを使用して基本的なフォーム テンプレートを作成およびデバッグする方法](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)」を参照してください。 
  
    これで、[ **ボタン**] コントロールを追加して、イベント ハンドラーを作成できます。 
    
### <a name="add-a-button-control-and-event-handler"></a>ボタン コントロールとイベント ハンドラーを追加する

1. [ **コントロール**] グループの [ **ボタン**] コントロールをクリックして、ボタン コントロールをフォームに追加します。 
    
2. [ **ボタン**] コントロールをダブルクリックして、リボンの [ **プロパティ**] タブの [ **ラベル**] プロパティに「Hello」と入力し、[ **ユーザー設定コード**] をクリックします。入力を要求するメッセージが表示されたら、フォームに HelloWorld という名前を付けて保存します。
    
   これにより、[ **ボタン**] コントロールの [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) イベントのイベント ハンドラーにカーソルが置かれた状態で [ **Visual Studio Tools for Applications**] 環境が開きます。 
    
   これでボタンのイベント ハンドラーにフォーム コードを追加する準備ができました。 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a>イベント ハンドラーに "Hello World" コードを追加してフォームをプレビューする

1. イベント ハンドラー スケルトンに次のように入力します。
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   フォーム テンプレートのコードは次のようになります。
    
   ```cs
    using Microsoft.Office.InfoPath;
    using System;
    using System.Windows.Forms;
    using System.Xml;
    using System.Xml.XPath;
    namespace HelloWorld
    {
        public partial class FormCode
        {
            public void InternalStartup()
            {
            ((ButtonEvent)EventManager.ControlEvents["CTRL1_5"]).Clicked += new ClickedEventHandler(CTRL1_5_Clicked);
            }
            public void CTRL1_5_Clicked(object sender, ClickedEventArgs e)
            {
            MessageBox.Show("Hello World!");
            }
        }
    }
   ```

   ```vb
    Imports Microsoft.Office.InfoPath
    Imports System
    Imports System.Windows.Forms
    Imports System.Xml
    Imports System.Xml.XPath
    Namespace HelloWorld
        Public Class FormCode
            Private Sub InternalStartup(ByVal sender As Object, ByVal e As EventArgs) Handles Me.Startup
            AddHandler DirectCast(EventManager.ControlEvents("CTRL1_5"), ButtonEvent).Clicked, AddressOf CTRL1_5_Clicked
            End Sub
            Public Sub CTRL1_5_Clicked(ByVal sender As Object, ByVal e As ClickedEventArgs)
            MessageBox.Show("Hello World!")
            End Sub
        End Class
    End Namespace
   ```

2. InfoPath デザイン モード ウィンドウに切り替えます。
    
3. [ **ホーム**] タブの [ **プレビュー**] ボタンをクリックします。 
    
4. フォーム上の [Hello] ボタンをクリックします。 
    
   "Hello World!" という内容のメッセージ ボックスが表示されます。
    
   次の手順は、フォーム コードにデバッグ用のブレークポイントを追加する方法を示しています。
    
### <a name="debug-form-code"></a>フォーム コードをデバッグする

1. Visual Studio 2012 ウィンドウに戻ります。
    
2. 行の左にあるグレーのバーをクリックします。
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   赤い円が表示され、コード行が強調表示されます。これは、ランタイムがフォーム コードのこのブレークポイントで一時停止することを表しています。
    
3. [ **デバッグ**] メニューの [ **デバッグ開始**] をクリックします (または F5 キーを押します)。 
    
4. InfoPath の [ **プレビュー**] ウィンドウで、フォーム上の [Hello] ボタンをクリックします。 
    
5. Visual Studio 2012 コード エディターにフォーカスが移り、ブレークポイント行が強調表示されます。
    
6. [ **デバッグ**] メニューで [ **ステップ オーバー**] をクリックするか、または Shift キーを押しながら F8 キーを押して、コード内を順に移動します。 
    
7. イベント ハンドラー コードが実行され、"Hello World!" メッセージが表示されます。 
    
8. **[OK]** をクリックして Visual Studio 2012 コード エディターに戻り、**[デバッグ]** メニューの **[デバッグの停止]** をクリックします (または Ctrl+Alt+Break を押します)。 
    
## <a name="getting-the-current-users-name"></a>現在のユーザーの名前を取得する

次の例では、[User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) クラスの [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) プロパティを使用して現在のユーザーの名前を取得し、 **Loading** イベントのイベント ハンドラーを使用して、[ [テキスト ボックス](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx)] コントロールの値を挿入する方法を学びます。 
  
[ **テキスト ボックス**] コントロールへの値の設定は、[XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) クラスのインスタンスを使用して、そのコントロールのバインド先である XML ノードに現在のユーザーの名前を書き込んで行います。 
  
まず、[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) クラスの [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを呼び出して、フォームの基盤となる XML ドキュメントを表す [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) クラスのインスタンスを取得します。次に、 [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) オブジェクトが [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) メソッドを呼び出して、このメソッドが **XPathNavigator** オブジェクトを作成し、そのオブジェクトをフォームのメイン データ ソースのルート ノードに置きます。 
  
[XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) クラスの **SelectSingleNode** メソッドが呼び出され、フォームのデータ ソースの employee フィールドを選択します。最後に、 [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) メソッドが呼び出され、 [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) プロパティを使用してそのフィールドの値を設定します。 
  
マネージ コード フォーム テンプレートでの **System.Xml** の作業の詳細については、「[XPathNavigator クラスおよび XPathNodeIterator クラスを操作する](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)」を参照してください。
  
### <a name="add-a-loading-event-handler"></a>Loading イベント ハンドラーを追加する

1. 前の手順で作成した HelloWorld フォーム テンプレートを InfoPath デザイン モードで開きます。
    
2. [ **表示**] タブの [ **フィールドの表示**] を選択します。
    
3. [ **マイフィールド**] フォルダーを右クリックして [ **追加**] をクリックします。
    
4. [ **名前**] に「employee」と入力して、[ **OK**] をクリックします。
    
5. employee フィールドをビューにドラッグします。 
    
6. [ **開発**] タブの [ **Loading イベント**] をクリックします。
    
   これにより [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) イベントのイベント ハンドラーが作成され、コード エディターのフォーカスがそのイベント ハンドラーに移動します。 
    
7. コード エディターで、以下のように入力します。
    
   ```cs
    public void FormEvents_Loading(object sender, LoadingEventArgs e)
    {
        XPathNavigator dataSource;
        dataSource = this.MainDataSource.CreateNavigator();
        dataSource.SelectSingleNode(
            "/my:myFields/my:employee", NamespaceManager).SetValue(this.User.UserName);
    }
   ```
 
   ```vb
    Public Sub FormEvents_Loading(ByVal sender As Object, ByVal e As LoadingEventArgs)
        Dim dataSource As XPathNavigator
        dataSource = Me.MainDataSource.CreateNavigator
        dataSource.SelectSingleNode( _
            "/my:myFields/my:employee", NamespaceManager).SetValue(Me.User.UserName)
    End Sub
   ```

8. InfoPath フォーム デザイン ウィンドウに切り替え、[ **ホーム**] タブの [ **プレビュー**] ボタンをクリックしてフォームをプレビューします。 
    
   employee フィールドに現在のユーザー名が自動的に入力されます。 
    
## <a name="next-steps"></a>次の手順

- 他のコントロールとイベントのイベント ハンドラーの操作については、「[イベント ハンドラーを追加する](how-to-add-an-event-handler.md)」を参照してください。
    
- フォーム テンプレート内でのコードのプレビューとデバッグについては、「[コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-infopath-form-templates-with-code.md)」を参照してください。
    
- マネージ コード フォーム テンプレートを展開する方法については、「[コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)」を参照してください。
    
- マネージ コード フォーム テンプレートの InfoPath オブジェクト モデルと一般的なプログラミング タスクについては、「[InfoPath オブジェクト モデルと一般的な開発タスクについて](understanding-the-infopath-object-model-and-common-developer-tasks.md)」を参照してください。
    
## <a name="see-also"></a>関連項目

- [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

