---
title: 'チュートリアル: InfoPath オブジェクト モデルを使用して基本的なフォーム テンプレートを作成およびデバッグする'
manager: soliver
ms.date: 01/13/2015
ms.audience: Developer
keywords:
- フォーム テンプレート [infopath 2007]、ウォークスルー、フォーム テンプレート [InfoPath 2007]、InfoPath 2003 互換、InfoPath 2003 互換フォーム テンプレートの作成、チュートリアル
localization_priority: Normal
ms.assetid: 7658705f-c062-49a1-bea6-837737df2425
description: このトピックでは、Microsoft が提供する InfoPath 2003 互換オブジェクト モデルで動作する基本的な InfoPath マネージ コード フォーム テンプレートを作成する方法について説明します。Office.Interop.InfoPath.SemiTrust 名前空間。
ms.openlocfilehash: c559aedad5c62134c796196c63c1a84f70c4dc3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414341"
---
# <a name="walkthrough-create-and-debug-a-basic-form-template-using-the-infopath-object-model"></a><span data-ttu-id="dd583-104">チュートリアル: InfoPath オブジェクト モデルを使用して基本的なフォーム テンプレートを作成およびデバッグする</span><span class="sxs-lookup"><span data-stu-id="dd583-104">Walkthrough: Create and debug a basic form template using the InfoPath object model</span></span>

<span data-ttu-id="dd583-105">このトピックでは[、Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx)名前空間によって提供される InfoPath 2003 互換オブジェクト モデルで動作する基本的な InfoPath マネージ コード フォーム テンプレートを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd583-105">This topic provides a walkthrough of creating a basic InfoPath managed code form template that works with the InfoPath 2003-compatible object model provided by the [Microsoft.Office.Interop.InfoPath.SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) namespace.</span></span> 
  
## <a name="hello-world"></a><span data-ttu-id="dd583-106">Hello World</span><span class="sxs-lookup"><span data-stu-id="dd583-106">Hello World</span></span>

<span data-ttu-id="dd583-107">次の例では、InfoPath 2003 互換オブジェクト モデルの [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) メソッドを使用して、簡単なアラート ダイアログ ボックスを表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="dd583-107">In the following example, you will learn how to display a simple alert dialog box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the InfoPath 2003-compatible object model.</span></span> 
  
### <a name="create-a-new-infopath-form-template-that-works-with-the-infopath-2003-compatible-object-model"></a><span data-ttu-id="dd583-108">InfoPath 2003 互換オブジェクト モデルを使用する新しい InfoPath フォーム テンプレートを作成する</span><span class="sxs-lookup"><span data-stu-id="dd583-108">Create a new InfoPath form template that works with the InfoPath 2003-compatible object model</span></span>

1. <span data-ttu-id="dd583-109">[「InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用してフォーム テンプレートを作成する」の説明に従って、InfoPath 2003 互換オブジェクト モデルで動作する新しいフォーム テンプレートを作成します。</span><span class="sxs-lookup"><span data-stu-id="dd583-109">Create a new form template that works with the InfoPath 2003-compatible object model, as described in [Create a Form Template Using the InfoPath 2003 Object Model](how-to-create-a-form-template-using-the-infopath-2003-object-model.md).</span></span>
    
2. <span data-ttu-id="dd583-110">フォーム テンプレート プロジェクトを HelloWorld という名前で保存します。</span><span class="sxs-lookup"><span data-stu-id="dd583-110">Name the form template project HelloWorld and save it.</span></span> 
    
   <span data-ttu-id="dd583-p101">プロジェクト システムがコード ファイルとプロジェクト ファイルを作成し、InfoPath のデザイン モードで空白のフォーム テンプレートを開きます。これでイベント ハンドラーを追加する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="dd583-p101">The project system creates code and project files, and then opens a blank form template in InfoPath design mode. You are now ready to add event handlers.</span></span>
    
### <a name="add-a-button-with-an-onclick-event-handler"></a><span data-ttu-id="dd583-113">OnClick イベント ハンドラーを設定したボタンを追加する</span><span class="sxs-lookup"><span data-stu-id="dd583-113">Add a button with an OnClick event handler</span></span>

1. <span data-ttu-id="dd583-114">[**ホーム**] タブの [**コントロール**] セクションで、[**ボタン**] コントロールをクリックして、ビューに挿入します。</span><span class="sxs-lookup"><span data-stu-id="dd583-114">In the **Controls** section on the **Home** tab, click the **Button** control to insert it into the view.</span></span> 
    
2. <span data-ttu-id="dd583-115">挿入したコントロールを右クリックして、[**ボタンのプロパティ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-115">Right-click the control, and then click **Button Properties**.</span></span>
    
3. <span data-ttu-id="dd583-116">[ラベル] **を [アラート** ] に変更します。</span><span class="sxs-lookup"><span data-stu-id="dd583-116">Change the **Label** to Alert.</span></span>
    
4. <span data-ttu-id="dd583-117">ID を **AlertID** に変更します。</span><span class="sxs-lookup"><span data-stu-id="dd583-117">Change the **ID** to AlertID.</span></span>
    
5. <span data-ttu-id="dd583-118">[**フォームのコードを編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-118">Click **Edit Form Code**.</span></span>
    
   <span data-ttu-id="dd583-119">[OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx)イベントのイベント ハンドラー スケルトンが作成され、フォーカスは 2012 年にコード エディター Visual Studioされます。</span><span class="sxs-lookup"><span data-stu-id="dd583-119">An event handler skeleton for the [OnClick](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._ButtonEventSink_Event.OnClick.aspx) event is created and the focus moves to the code editor in Visual Studio 2012.</span></span> <span data-ttu-id="dd583-120">イベント ハンドラーの操作の詳細については [、「InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)オブジェクト モデルを使用してイベント ハンドラーを追加する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd583-120">For more information on working with event handlers, see [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span> 
    
   <span data-ttu-id="dd583-121">これでボタンのイベント ハンドラーにフォーム コードを追加する準備ができました。</span><span class="sxs-lookup"><span data-stu-id="dd583-121">You are now ready to add form code to the event handler for the button.</span></span>
    
### <a name="add-form-code-to-the-event-handler"></a><span data-ttu-id="dd583-122">イベント ハンドラーにフォーム コードを追加する</span><span class="sxs-lookup"><span data-stu-id="dd583-122">Add form code to the event handler</span></span>

1. <span data-ttu-id="dd583-123">**OnClick** イベント ハンドラーに次のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="dd583-123">In the **OnClick** event handler, type the following code:</span></span> 
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="dd583-p103">コード行に含まれるピリオドを入力するたびに Microsoft IntelliSense のボックスが表示されます。イベント ハンドラー全体は次のようになります。</span><span class="sxs-lookup"><span data-stu-id="dd583-p103">Note that a Microsoft IntelliSense drop-down list is displayed after you type each period in the line of code. The entire event handler should look like the following:</span></span>
    
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
   > <span data-ttu-id="dd583-126">**Alert** メソッドを使用する代わりに、**System.Windows.Forms** 名前空間の **MessageBox.Show** メソッドを使用してメッセージ ボックスを表示することもできます。</span><span class="sxs-lookup"><span data-stu-id="dd583-126">As an alternative to using the **Alert** method, you can use the **MessageBox.Show** method of the **System.Windows.Forms** namespace to display a message box.</span></span> <span data-ttu-id="dd583-127">これを行うには、システムへの参照を追加する必要があります。Windows。フォーム アセンブリを作成し、コード ファイルの先頭にあるディレクティブを追加または追加し、次のようなコード行 `using System.Windows.Forms;` `Imports System.Windows.Forms` を入力します。`MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span><span class="sxs-lookup"><span data-stu-id="dd583-127">To do so, you must add a reference to the System.Windows.Forms assembly, add  `using System.Windows.Forms;` or  `Imports System.Windows.Forms` to the directives at the beginning of your code file, and then type a line of code such as the following:  `MessageBox.Show("Hello World!); or MessageBox.Show("Hello World!)`</span></span>
  
2. <span data-ttu-id="dd583-128">InfoPath のデザイン モード ウィンドウに切り替え、[**ホーム**] タブの [**プレビュー**] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-128">Switch to the InfoPath design mode window, and then click the **Preview** button on the **Home** tab.</span></span> 
    
3. <span data-ttu-id="dd583-129">[**プレビュー**] ウィンドウで [**Alert**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-129">In the **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="dd583-130">"Hello World!" という内容のメッセージ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd583-130">A message box will be displayed with the text "Hello World!"</span></span>
    
   <span data-ttu-id="dd583-131">次の手順は、フォーム コードにデバッグ用のブレークポイントを追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="dd583-131">The next procedure shows how to add debugging breakpoints to your form code.</span></span>
    
### <a name="debug-form-code"></a><span data-ttu-id="dd583-132">フォーム コードをデバッグする</span><span class="sxs-lookup"><span data-stu-id="dd583-132">Debug form code</span></span>

1. <span data-ttu-id="dd583-133">コード エディターで次の行の左にあるグレーのバーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-133">In the code editor, click the grey bar to the left of the line:</span></span>
    
   ```cs
    thisXDocument.UI.Alert("Hello World!");
   ```

   ```vb
    thisXDocument.UI.Alert("Hello World!")
   ```

   <span data-ttu-id="dd583-134">赤い円が表示され、コード行が強調表示されます。これは、ランタイムがフォーム コードのこのブレークポイントで一時停止することを表しています。</span><span class="sxs-lookup"><span data-stu-id="dd583-134">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
2. <span data-ttu-id="dd583-135">[**デバッグ**] メニューの [**デバッグ開始**] をクリックします (または F5 キーを押します)。</span><span class="sxs-lookup"><span data-stu-id="dd583-135">On the **Debug** menu, click **Start Debugging** (or press F5).</span></span> 
    
3. <span data-ttu-id="dd583-136">InfoPath の [**プレビュー**] ウィンドウで [**Alert**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-136">In the InfoPath **Preview** window, click the **Alert** button.</span></span> 
    
   <span data-ttu-id="dd583-137">コード エディターにフォーカスが移動し、ブレークポイント行が強調表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd583-137">The code editor is given focus, and the breakpoint line is highlighted.</span></span>
    
4. <span data-ttu-id="dd583-138">[**デバッグ**] メニューで [**ステップ オーバー**] をクリックするか、または Shift キーを押しながら F8 キーを押して、コード内を順に移動します。</span><span class="sxs-lookup"><span data-stu-id="dd583-138">On the **Debug** menu, click **Step Over** (or press Shift+F8) to continue stepping through the code.</span></span> 
    
   <span data-ttu-id="dd583-p105">**Alert** メソッドのコードが実行され、InfoPath の [**プレビュー**] ウィンドウに "Hello World!" という通知が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd583-p105">The **Alert** method code is executed, and the "Hello World!" alert is displayed in the InfoPath **Preview** window.</span></span> 
    
## <a name="getting-the-current-users-name"></a><span data-ttu-id="dd583-141">現在のユーザーの名前を取得する</span><span class="sxs-lookup"><span data-stu-id="dd583-141">Getting the Current User's Name</span></span>

<span data-ttu-id="dd583-p106">.NET Framework のクラスを使用すると、スクリプトでは簡単に利用できなかった機能を利用できます。この例では、.NET Framework のクラスを使用して現在のユーザーの名前を取得する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="dd583-p106">By using the .NET Framework classes, you can get access to functionality that was not easily available in script. In this example, you will learn how use the .NET Framework classes to retrieve the name of the current user.</span></span>
  
### <a name="add-an-onload-event-handler"></a><span data-ttu-id="dd583-144">OnLoad イベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="dd583-144">Add an OnLoad event handler</span></span>

1. <span data-ttu-id="dd583-145">前の例で作成した InfoPath HelloWorld プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="dd583-145">Open the InfoPath HelloWorld project that you created earlier.</span></span>
    
2. <span data-ttu-id="dd583-146">[**表示**] タブの [**フィールドの表示**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-146">On the **View** tab, click **Show Fields**.</span></span>
    
3. <span data-ttu-id="dd583-147">[**マイフィールド**] ノードを右クリックし、[**追加**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-147">Right-click the **myFields** node, and then click **Add**.</span></span>
    
4. <span data-ttu-id="dd583-148">[**名前] に\*\*\*\*「employee」と入力** し **、[OK] をクリックします**。</span><span class="sxs-lookup"><span data-stu-id="dd583-148">In **Name**, type **employee**, then click **OK**.</span></span>
    
5. <span data-ttu-id="dd583-149">[**employee**] ノードをビューにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="dd583-149">Drag the **employee** node into the view.</span></span> 
    
6. <span data-ttu-id="dd583-150">[**開発**] タブの [**OnLoad イベント**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="dd583-150">On the **Developer** tab, click **On Load Event**.</span></span>
    
   <span data-ttu-id="dd583-151">これにより [、OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) イベントのイベント ハンドラーが作成され、コード エディターにフォーカスが移動します。</span><span class="sxs-lookup"><span data-stu-id="dd583-151">This will create an event handler for the [OnLoad](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocumentEventSink2_Event.OnLoad.aspx) event, and focus moves to the code editor.</span></span> <span data-ttu-id="dd583-152">フォームを読み込むたびに、このイベント ハンドラーのコードが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="dd583-152">The code in this event handler will be called each time the form is loaded.</span></span> <span data-ttu-id="dd583-153">次の手順は、ユーザーの名前を取得するフォーム コードをイベント ハンドラーに追加する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="dd583-153">The next procedure shows how to add form code that retrieves the user's name to the event handler.</span></span> 
    
### <a name="add-form-code"></a><span data-ttu-id="dd583-154">フォーム コードを追加する</span><span class="sxs-lookup"><span data-stu-id="dd583-154">Add form code</span></span>

1. <span data-ttu-id="dd583-155">**OnLoad** イベント ハンドラーに次のコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="dd583-155">In the **OnLoad** event handler, type the following code:</span></span> 
    
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

2. <span data-ttu-id="dd583-156">フォームをコンパイルおよびプレビューします。</span><span class="sxs-lookup"><span data-stu-id="dd583-156">Compile and preview the form.</span></span>
    
   <span data-ttu-id="dd583-157">[employee] ボックスに自分のユーザー名が表示されます。</span><span class="sxs-lookup"><span data-stu-id="dd583-157">The employee text box should now be populated with your username.</span></span> 
    
<span data-ttu-id="dd583-158">マネージ コード フォーム テンプレートを展開する方法については、「コードを使用して InfoPath フォーム テンプレートを展開 [する」を参照してください](how-to-deploy-infopath-form-templates-with-code.md)。</span><span class="sxs-lookup"><span data-stu-id="dd583-158">For information about how to deploy a managed code form template, see [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> <span data-ttu-id="dd583-159">InfoPath 2003 互換オブジェクト モデルで動作するマネージ コード フォーム テンプレートの InfoPath オブジェクト モデルと一般的なプログラミング タスクの詳細については [、「InfoPath 2003](understanding-the-infopath-2003-object-model.md)オブジェクト モデルについて」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dd583-159">For information on the InfoPath object model and common programming tasks in managed code form templates that work with the InfoPath 2003-compatible object model, see [Understanding the InfoPath 2003 Object Model](understanding-the-infopath-2003-object-model.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dd583-160">関連項目</span><span class="sxs-lookup"><span data-stu-id="dd583-160">See also</span></span>

- [<span data-ttu-id="dd583-161">InfoPath 2003 オブジェクト モデルを使用する初期化コードと後処理コード</span><span class="sxs-lookup"><span data-stu-id="dd583-161">Initialization and Clean-up Code Using InfoPath 2003 Object Model</span></span>](initialization-and-clean-up-code-using-infopath-2003-object-model.md)
- [<span data-ttu-id="dd583-162">InfoPath 2003 互換オブジェクト モデル</span><span class="sxs-lookup"><span data-stu-id="dd583-162">InfoPath 2003 Compatible Object Models</span></span>](infopath-2003-compatible-object-models.md)
- [<span data-ttu-id="dd583-163">InfoPath 2003 オブジェクト モデルを使用してイベント ハンドラーを追加する</span><span class="sxs-lookup"><span data-stu-id="dd583-163">Add an Event Handler Using the InfoPath 2003 Object Model</span></span>](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md)

