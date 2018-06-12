---
title: 'チュートリアル: コードを含む基本的なフォーム テンプレートを作成します。'
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- form templates [infopath 2007], creating managed code,managed code form templates [InfoPath 2007], creating,form templates [InfoPath 2007], walkthroughs,InfoPath 2007, walkthroughs
localization_priority: Normal
ms.assetid: 0f55c8be-8641-476a-b0c8-c88adb2ac2b9
description: Microsoft InfoPath では、InfoPath デザイナーでフォーム テンプレートを開くし使用してユーザー インターフェイスのコマンドのいずれかの Visual Studio 2012 の開発環境を開いて、イベント ハンドラーを追加するのには、Visual Basic または C# でのビジネス ロジックを記述できます。コードを記述します。
ms.openlocfilehash: 8c98d71c26f8e56c532b2a4467218c366072b2ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799237"
---
# <a name="walkthrough-create-a-basic-form-template-with-code"></a><span data-ttu-id="a3e54-104">チュートリアル: コードを含む基本的なフォーム テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-104">Walkthrough: Create a basic form template with code</span></span>

<span data-ttu-id="a3e54-p101">Microsoft InfoPath の場合は、Visual Basic または C# でビジネス ロジックを記述できます。これを実行するには、フォーム テンプレートを InfoPath のデザイン モードで開き、いずれかのユーザー インターフェイス コマンドを使用してイベント ハンドラーを追加します。これにより、コードを記述するための Visual Studio 2012 開発環境が開きます。既定では、Visual Studio 2012 を使用して作成したフォーム テンプレート プロジェクトは、[Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) 名前空間によって提供されるマネージ コード オブジェクト モデルに対して動作します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-p101">In Microsoft InfoPath, you can write business logic in Visual Basic or C# by opening a form template in the InfoPath designer, and then using one of the user interface commands to add an event handler, which will open the Visual Studio 2012 development environment for writing your code. By default, form template projects created using Visual Studio 2012 work against the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace.</span></span> 
  
<span data-ttu-id="a3e54-p102">このチュートリアルでは、最初に、Visual Studio 2012 開発環境で C# または Visual Basic を使用して、単純な Hello World アプリケーションを作成する方法を示します。チュートリアルの最後には、[User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) クラスの [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) プロパティを使用して現在のユーザー名を取得し、[ **テキスト ボックス**] コントロールにその値を設定する方法を示すコード サンプルがあります。</span><span class="sxs-lookup"><span data-stu-id="a3e54-p102">This walkthrough first shows you how to create a simple Hello World application using C# or Visual Basic in the Visual Studio 2012 development environment. The walkthrough concludes with a code sample that shows you how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the current user's name and populate a **Text Box** control with that value.</span></span> 
  
## <a name="prerequisites"></a><span data-ttu-id="a3e54-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="a3e54-109">Prerequisites</span></span>

<span data-ttu-id="a3e54-110">Visual Studio 2012 開発環境を使用してこのチュートリアルを完了するには、以下が必要です。</span><span class="sxs-lookup"><span data-stu-id="a3e54-110">In order to complete this walkthrough using the Visual Studio 2012 development environment, you will need:</span></span>
  
- <span data-ttu-id="a3e54-111">Microsoft InfoPath がインストールされた Visual Studio 2012。</span><span class="sxs-lookup"><span data-stu-id="a3e54-111">Microsoft InfoPath with Visual Studio 2012 installed.</span></span>
    
## <a name="hello-world-in-visual-studio-tools-for-applications"></a><span data-ttu-id="a3e54-112">Visual Studio Tools for Applications の Hello World</span><span class="sxs-lookup"><span data-stu-id="a3e54-112">Hello World in Visual Studio Tools for Applications</span></span>

<span data-ttu-id="a3e54-113">以下のチュートリアルでは、Visual Studio 2012 開発環境で [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) クラスの [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) イベントのイベント ハンドラーを記述することによって、[ **ボタン**] コントロールに関連付けられた単純な警告ダイアログ ボックスを表示する方法を学びます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-113">In the following walkthrough, you will learn how to write code in the Visual Studio 2012 development environment to display a simple alert dialog box by writing an event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of the [ButtonEvent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.aspx) class, which is associated with the **Button** control.</span></span> 
  
### <a name="create-a-new-project-and-specify-the-programming-language"></a><span data-ttu-id="a3e54-114">新しいプロジェクトを作成してプログラミング言語を指定する</span><span class="sxs-lookup"><span data-stu-id="a3e54-114">Create a new project and specify the programming language</span></span>

1. <span data-ttu-id="a3e54-115">InfoPath デザイン モードを起動して、[ **空白 (InfoPath エディター)**] フォーム テンプレートをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-115">Start the InfoPath designer, and then double-click the **Blank (InfoPath Editor)** form template.</span></span> 
    
2. <span data-ttu-id="a3e54-116">使用するプログラミング言語を指定するために、[ **ファイル**] タブをクリックし、[ **フォームのオプション**] をクリックして、[ **カテゴリ**] の一覧の [ **プログラミング**] をクリックします。次に、[ **フォーム テンプレートのコード言語**] ドロップダウン リストから [ **Visual Basic**] または [ **C#**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-116">To specify which programming language to use, click the **Office Button**, click **Form Options**, click **Programming** in the **Category** list, and then select either **Visual Basic** or **C#** from the **Form template code language** drop-down list.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="a3e54-p103">[!メモ] [ **フォーム テンプレートのコード言語**] ドロップダウン リスト内のその他のプログラミング言語オプションでは、以前のバージョンの InfoPath との互換性が提供されています。[ **C# (InfoPath 2007 互換)**] および [ **Visual Basic (InfoPath 2007 互換)**] オプションは、このトピック内の手順で機能します。[ **C# (InfoPath 2003 互換)**] および [ **Visual Basic (InfoPath 2003 互換)**] オプションを使用する場合は、「[[ウォークスルー] InfoPath 2003 オブジェクト モデルを使用して基本的なフォーム テンプレートを作成およびデバッグする方法](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3e54-p103">The other programming language options in the **Form template code language** drop-down list provide compatibility with previous versions of InfoPath. The **C# (InfoPath 2007 Compatible)** and **Visual Basic (InfoPath 2007 Compatible)** options will work with the procedures in this topic. However, to use the **C# (InfoPath 2003 Compatible)** and **Visual Basic (InfoPath 2003 Compatible)** options, see [Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md).</span></span> 
  
    <span data-ttu-id="a3e54-120">これで、[ **ボタン**] コントロールを追加して、イベント ハンドラーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-120">You are now ready to add a **Button** control and create its event handler.</span></span> 
    
### <a name="add-a-button-control-and-event-handler"></a><span data-ttu-id="a3e54-121">ボタン コントロールとイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="a3e54-121">Add a Button control and event handler</span></span>

1. <span data-ttu-id="a3e54-122">[ **コントロール**] グループの [ **ボタン**] コントロールをクリックして、ボタン コントロールをフォームに追加します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-122">In the **Controls** group, click the **Button** control to add it the form.</span></span> 
    
2. <span data-ttu-id="a3e54-p104">[ **ボタン**] コントロールをダブルクリックして、リボンの [ **プロパティ**] タブの [ **ラベル**] プロパティに「Hello」と入力し、[ **ユーザー設定コード**] をクリックします。入力を要求するメッセージが表示されたら、フォームに HelloWorld という名前を付けて保存します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-p104">Double-click the **Button** control, type Hello for the **Label** property on the **Properties** tab of the ribbon, and then click **Custom Code**. When prompted, save the form and name it HelloWorld.</span></span>
    
   <span data-ttu-id="a3e54-125">これにより、[ **ボタン**] コントロールの [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) イベントのイベント ハンドラーにカーソルが置かれた状態で [ **Visual Studio Tools for Applications**] 環境が開きます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-125">This will open the **Visual Studio Tools for Applications** environment with the cursor in the event handler for the [Clicked](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ButtonEvent.Clicked.aspx) event of **Button** control.</span></span> 
    
   <span data-ttu-id="a3e54-126">これでボタンのイベント ハンドラーにフォーム コードを追加する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="a3e54-126">You are now ready to add form code to the event handler for the button.</span></span> 
    
### <a name="add-hello-world-code-to-the-event-handler-and-preview-the-form"></a><span data-ttu-id="a3e54-127">イベント ハンドラーに "Hello World" コードを追加してフォームをプレビューする</span><span class="sxs-lookup"><span data-stu-id="a3e54-127">Add "Hello World" code to the event handler and preview the form</span></span>

1. <span data-ttu-id="a3e54-128">イベント ハンドラー スケルトンに次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-128">In the event handler skeleton, type:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="a3e54-129">フォーム テンプレートのコードは次のようになります。</span><span class="sxs-lookup"><span data-stu-id="a3e54-129">The code for your form template should look similar to the following:</span></span>
    
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

2. <span data-ttu-id="a3e54-130">InfoPath デザイン モード ウィンドウに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-130">Switch to the InfoPath designer window.</span></span>
    
3. <span data-ttu-id="a3e54-131">[ **ホーム**] タブの [ **プレビュー**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-131">Click the **Preview** button on the **Home** tab.</span></span> 
    
4. <span data-ttu-id="a3e54-132">フォーム上の [Hello] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-132">Click the Hello button on the form.</span></span> 
    
   <span data-ttu-id="a3e54-133">"Hello World!" という内容のメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-133">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="a3e54-134">次の手順は、フォーム コードにデバッグ用のブレークポイントを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a3e54-134">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="a3e54-135">フォーム コードをデバッグする</span><span class="sxs-lookup"><span data-stu-id="a3e54-135">Debug form code</span></span>

1. <span data-ttu-id="a3e54-136">Visual Studio 2012 ウィンドウに戻ります。</span><span class="sxs-lookup"><span data-stu-id="a3e54-136">Switch back to the Visual Studio 2012 window.</span></span>
    
2. <span data-ttu-id="a3e54-137">行の左にあるグレーのバーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-137">Click the grey bar to the left of the line:</span></span>
    
   ```cs
   MessageBox.Show("Hello World!");
   ```

   ```vb
   MessageBox.Show("Hello World!")
   ```

   <span data-ttu-id="a3e54-138">赤い円が表示され、コード行が強調表示されます。これは、ランタイムがフォーム コードのこのブレークポイントで一時停止することを表しています。</span><span class="sxs-lookup"><span data-stu-id="a3e54-138">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="a3e54-139">[ **デバッグ**] メニューの [ **デバッグ開始**] をクリックします (または F5 キーを押します)。</span><span class="sxs-lookup"><span data-stu-id="a3e54-139">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
4. <span data-ttu-id="a3e54-140">InfoPath の [ **プレビュー**] ウィンドウで、フォーム上の [Hello] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-140">In the InfoPath **Preview** window, click the Hello button on the form.</span></span> 
    
5. <span data-ttu-id="a3e54-141">Visual Studio 2012 コード エディターにフォーカスが移り、ブレークポイント行が強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-141">The Visual Studio 2012 code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
6. <span data-ttu-id="a3e54-142">[ **デバッグ**] メニューで [ **ステップ オーバー**] をクリックするか、または Shift キーを押しながら F8 キーを押して、コード内を順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-142">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
7. <span data-ttu-id="a3e54-p105">イベント ハンドラー コードが実行され、"Hello World!" メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-p105">The event handler code is executed, and the "Hello World!" message is displayed.</span></span> 
    
8. <span data-ttu-id="a3e54-145">[ **OK**] をクリックして Visual Studio 2012 コード エディターに戻り、[ **デバッグ**] メニューの [ **デバッグの停止**] をクリックするか、または Ctrl キーと Alt キーを押しながら Break キーを押します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-145">Click **OK** to return to the Visual Studio 2012 code editor, and then click **Stop Debugging** on the **Debug** menu (or press Ctrl+Alt+Break).</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="a3e54-146">現在のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-146">Getting the current user's name</span></span>

<span data-ttu-id="a3e54-147">次の例では、[User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) クラスの [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) プロパティを使用して現在のユーザーの名前を取得し、 **Loading** イベントのイベント ハンドラーを使用して、[ [テキスト ボックス](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx)] コントロールの値を挿入する方法を学びます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-147">In the following example, you will learn how to use the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to retrieve the name of the current user and populate the value of a **Text Box** control by using an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event.</span></span> 
  
<span data-ttu-id="a3e54-148">[ **テキスト ボックス**] コントロールへの値の設定は、[XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) クラスのインスタンスを使用して、そのコントロールのバインド先である XML ノードに現在のユーザーの名前を書き込んで行います。</span><span class="sxs-lookup"><span data-stu-id="a3e54-148">Populating the **Text Box** control is accomplished by using an instance of the [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) class to write the current user's name to the XML node that the control is bound to.</span></span> 
  
<span data-ttu-id="a3e54-p106">まず、[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) クラスの [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) プロパティを呼び出して、フォームの基盤となる XML ドキュメントを表す [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) クラスのインスタンスを取得します。次に、 [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) オブジェクトが [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) メソッドを呼び出して、このメソッドが **XPathNavigator** オブジェクトを作成し、そのオブジェクトをフォームのメイン データ ソースのルート ノードに置きます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-p106">First, the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class is called to retrieve an instance of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class that represents the underlying XML document of the form. The [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) object then calls the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method, which creates the **XPathNavigator** object and positions it at the root node of the form's main data source.</span></span> 
  
<span data-ttu-id="a3e54-p107">[XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) クラスの **SelectSingleNode** メソッドが呼び出され、フォームのデータ ソースの employee フィールドを選択します。最後に、 [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) メソッドが呼び出され、 [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) プロパティを使用してそのフィールドの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-p107">The [SelectSingleNode](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.selectsinglenode%28v=vs.100%29.aspx) method of the **XPathNavigator** class is called to select the employee field in the form's data source. Finally, the [SetValue](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator.setvalue%28v=vs.100%29.aspx) method is called to set the value of the field with the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property.</span></span> 
  
<span data-ttu-id="a3e54-153">マネージ コード フォーム テンプレートでの**System.Xml**の操作方法の詳細については、 [XPathNavigator と XPathNodeIterator クラスでの作業](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3e54-153">For more information on working with **System.Xml** in managed code form templates, see [Work with the XPathNavigator and XPathNodeIterator Classes](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).</span></span>
  
### <a name="add-a-loading-event-handler"></a><span data-ttu-id="a3e54-154">Loading イベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="a3e54-154">Add a Loading event handler</span></span>

1. <span data-ttu-id="a3e54-155">前の手順で作成した HelloWorld フォーム テンプレートを InfoPath デザイン モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-155">Open the HelloWorld form template that you created in the previous walkthrough in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="a3e54-156">[ **表示**] タブの [ **フィールドの表示**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-156">On the **View** tab, select **Show Fields**.</span></span>
    
3. <span data-ttu-id="a3e54-157">[ **マイフィールド**] フォルダーを右クリックして [ **追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-157">Right click the **myFields** folder, and then click **Add**.</span></span>
    
4. <span data-ttu-id="a3e54-158">[ **名前**] に「employee」と入力して、[ **OK**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-158">In **Name**, type employee, and then click **OK**.</span></span>
    
5. <span data-ttu-id="a3e54-159">employee フィールドをビューにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-159">Drag the employee field onto the view.</span></span> 
    
6. <span data-ttu-id="a3e54-160">[ **開発**] タブの [ **Loading イベント**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-160">On the **Developer** tab, click **Loading Event**.</span></span>
    
   <span data-ttu-id="a3e54-161">これにより [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) イベントのイベント ハンドラーが作成され、コード エディターのフォーカスがそのイベント ハンドラーに移動します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-161">This will create an event handler for the [Loading](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Loading.aspx) event, and move the focus to that event handler in the code editor.</span></span> 
    
7. <span data-ttu-id="a3e54-162">コード エディターで、以下のように入力します。</span><span class="sxs-lookup"><span data-stu-id="a3e54-162">In the code editor, type the following:</span></span>
    
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

8. <span data-ttu-id="a3e54-163">InfoPath フォーム デザイン ウィンドウに切り替え、[ **ホーム**] タブの [ **プレビュー**] ボタンをクリックしてフォームをプレビューします。</span><span class="sxs-lookup"><span data-stu-id="a3e54-163">Switch to the InfoPath form design window, and then click the **Preview** button on the **Home** tab to preview the form.</span></span> 
    
   <span data-ttu-id="a3e54-164">employee フィールドに現在のユーザー名が自動的に入力されます。</span><span class="sxs-lookup"><span data-stu-id="a3e54-164">The employee field should automatically fill in with your user name.</span></span> 
    
## <a name="next-steps"></a><span data-ttu-id="a3e54-165">次の手順</span><span class="sxs-lookup"><span data-stu-id="a3e54-165">Next steps</span></span>

- <span data-ttu-id="a3e54-166">その他のコントロールとイベントのイベント ハンドラーの操作方法の詳細については、[イベント ハンドラーの追加](how-to-add-an-event-handler.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3e54-166">For information about working with event handlers for other controls and events, see [Add an Event Handler](how-to-add-an-event-handler.md).</span></span>
    
- <span data-ttu-id="a3e54-167">プレビューして、フォーム テンプレート内のコードをデバッグする方法の詳細については、[プレビューとコードを含む InfoPath フォーム テンプレートのデバッグ](how-to-preview-and-debug-infopath-form-templates-with-code.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3e54-167">For more information about previewing and debugging code in form templates, see [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="a3e54-168">マネージ コード フォーム テンプレートを展開する方法の詳細については、[コードを含む InfoPath フォーム テンプレートの展開](how-to-deploy-infopath-form-templates-with-code.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3e54-168">For information about how to deploy a managed-code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span>
    
- <span data-ttu-id="a3e54-169">マネージ コード フォーム テンプレートの InfoPath オブジェクト モデルと一般的なプログラミング タスクについては、「[InfoPath オブジェクト モデルと一般的な開発タスクについて](understanding-the-infopath-object-model-and-common-developer-tasks.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a3e54-169">For information about the InfoPath object model and common programming tasks in managed-code form templates, see [Understanding the InfoPath Object Model and Common Developer Tasks](understanding-the-infopath-object-model-and-common-developer-tasks.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a3e54-170">関連項目</span><span class="sxs-lookup"><span data-stu-id="a3e54-170">See also</span></span>

- [<span data-ttu-id="a3e54-171">XmlForm</span><span class="sxs-lookup"><span data-stu-id="a3e54-171">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)

