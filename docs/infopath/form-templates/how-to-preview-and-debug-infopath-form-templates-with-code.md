---
title: コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- previewing form templates [infopath 2007],debugging form templates [InfoPath 2007],form templates [InfoPath 2007], previewing,debugging [InfoPath 2007], managed-code form templates,form templates [InfoPath 2007], debugging,InfoPath 2007, debugging form templates,InfoPath 2007, previewing form templates
localization_priority: Normal
ms.assetid: c8387f1c-b34c-490e-8bf9-d824bf98d826
description: Microsoft InfoPath (Visual Studio 2012 インストール済み) では、フォーム コードをプレビュー モードで実行してデバッグすることができます。フォーム コードのデバッグを開始すると、プロジェクトがコンパイルされて、InfoPath の [プレビュー] ウィンドウにフォームが表示されます。ブレークポイントが設定されたコード行が見つかるとコード エディターにフォーカスが移動し、ブレークポイントを過ぎると [プレビュー] ウィンドウにフォーカスが戻ります。[プレビュー] ウィンドウを閉じるとデバッグが停止します。
ms.openlocfilehash: 8f9ff97fdd5b4b016d96129304fa6f994d7b4561
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405241"
---
# <a name="preview-and-debug-infopath-form-templates-with-code"></a><span data-ttu-id="df8c2-108">コードを含む InfoPath フォーム テンプレートをプレビューおよびデバッグする</span><span class="sxs-lookup"><span data-stu-id="df8c2-108">Preview and Debug InfoPath Form Templates with Code</span></span>

<span data-ttu-id="df8c2-p102">Microsoft InfoPath (Visual Studio 2012 インストール済み) では、フォーム コードをプレビュー モードで実行してデバッグすることができます。フォーム コードのデバッグを開始すると、プロジェクトがコンパイルされて、InfoPath の [プレビュー] ウィンドウにフォームが表示されます。ブレークポイントが設定されたコード行が見つかるとコード エディターにフォーカスが移動し、ブレークポイントを過ぎると [プレビュー] ウィンドウにフォーカスが戻ります。[プレビュー] ウィンドウを閉じるとデバッグが停止します。</span><span class="sxs-lookup"><span data-stu-id="df8c2-p102">Microsoft InfoPath with Visual Studio 2012 enables debugging by running form code in preview mode. When you start debugging form code, your project is compiled and InfoPath displays your form in the InfoPath preview window. When a line of code that has a breakpoint set for it is encountered, the focus moves to the code editor. When you continue past a breakpoint, the focus moves back to the preview window. Debugging stops when you close the preview window.</span></span>
  
<span data-ttu-id="df8c2-114">フォーム テンプレートのフォーム オプションを変更して、プレビューやデバッグの際に特定のユーザー ロールやサンプル データ ファイルを使用したり、フォームの発行先となるドメインを指定したりすることもできます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-114">You can also modify the form options of the form template to preview and debug using a specific user role, a sample data file, or by specifying the domain to which the form will be published.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="df8c2-115">フォーム テンプレートを展開後、Visual Studio 2012 での実行時にデバッグすることはできません。</span><span class="sxs-lookup"><span data-stu-id="df8c2-115">It is not possible to debug form templates after they are deployed at run time from Visual Studio 2012.</span></span> <span data-ttu-id="df8c2-116">これは、InfoPath のみと互換性があるフォーム テンプレートについても、InfoPath および InfoPath Forms Services を使用する Web ブラウザーと互換性があるフォーム テンプレートについても同様です。</span><span class="sxs-lookup"><span data-stu-id="df8c2-116">This includes form templates that are compatible only with InfoPath, as well as those that are compatible with InfoPath and the Web browser using InfoPath Forms Services.</span></span> <span data-ttu-id="df8c2-117">ただし、実行時に、コードからフィールドに値のログを記録すると、フォーム テンプレートのビジネス ロジックのデバッグに有効です。</span><span class="sxs-lookup"><span data-stu-id="df8c2-117">However, it is possible to log values to a field from code at run time to help with debugging a form template's business logic.</span></span> <span data-ttu-id="df8c2-118">この方法については、「[デバッグのために値のログをフィールドに記録する方法](how-to-log-values-to-a-field-for-debugging.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df8c2-118">For information about how to do that, see [Log Values to a Field for Debugging](how-to-log-values-to-a-field-for-debugging.md).</span></span> 
  
## <a name="debugging-in-preview-mode"></a><span data-ttu-id="df8c2-119">プレビュー モードでデバッグする</span><span class="sxs-lookup"><span data-stu-id="df8c2-119">Debugging in Preview Mode</span></span>

### <a name="to-debug-an-infopath-project-in-preview-mode"></a><span data-ttu-id="df8c2-120">InfoPath プロジェクトをプレビュー モードでデバッグするには</span><span class="sxs-lookup"><span data-stu-id="df8c2-120">To debug an InfoPath project in Preview Mode</span></span>

1. <span data-ttu-id="df8c2-121">Visual Studio 2012 で、InfoPath マネージ コード フォーム テンプレートを作成するか開きます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-121">Create or open an InfoPath managed code form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="df8c2-122">コード エディターでフォーム コードにブレークポイントを 1 つ以上設定します。ブレークポイントを設定するには、ブレークポイントを挿入するコード行の左にあるグレーのバーをクリックします。</span><span class="sxs-lookup"><span data-stu-id="df8c2-122">Set one or more breakpoints in your form code in the code editor by clicking the grey bar to the left of the line of code where you want to insert a breakpoint.</span></span>
    
    <span data-ttu-id="df8c2-123">赤い円が表示され、コード行が強調表示されます。これは、ランタイムがフォーム コードのこのブレークポイントで一時停止することを表しています。</span><span class="sxs-lookup"><span data-stu-id="df8c2-123">A red circle is displayed and the line of code is highlighted to indicate that the runtime will pause at this breakpoint in your form code.</span></span>
    
3. <span data-ttu-id="df8c2-124">[ **デバッグ**] メニューの [ **デバッグ開始**] をクリックします (または F5 キーを押します)。</span><span class="sxs-lookup"><span data-stu-id="df8c2-124">On the **Debug** menu, click **Start Debugging**; or press F5.</span></span>
    
    <span data-ttu-id="df8c2-125">プロジェクトがコンパイルされて、フォームが [プレビュー] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-125">The project will be compiled and the form is displayed in the preview window.</span></span>
    
4. <span data-ttu-id="df8c2-126">ブレークポイントを含むコード行が見つかるまでフォームを操作します。</span><span class="sxs-lookup"><span data-stu-id="df8c2-126">Interact with the form until a line of code containing a breakpoint is encountered.</span></span>
    
    <span data-ttu-id="df8c2-127">コード エディターにフォーカスが戻ります。</span><span class="sxs-lookup"><span data-stu-id="df8c2-127">The focus returns to the code editor.</span></span>
    
5. <span data-ttu-id="df8c2-128">[ **デバッグ**] メニューの [ **続行**] をクリックします (または F5 キーを押します)。</span><span class="sxs-lookup"><span data-stu-id="df8c2-128">On the **Debug** menu, click **Continue**; or press F5.</span></span>
    
6. <span data-ttu-id="df8c2-129">デバッグが完了したら、プレビュー ウィンドウを閉じるか、**[デバッグ]** メニューで **[デバッグの停止]** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="df8c2-129">When you are finished debugging, close the preview window; or on the **Debug** menu, click **Stop Debugging**.</span></span>
    
> [!NOTE]
> <span data-ttu-id="df8c2-130">完全な信頼が必要なオブジェクト モデル メンバーを使用している場合に InfoPath マネージ コード フォーム テンプレートをデバッグするには、「[完全信頼が必要なフォーム テンプレートをプレビューおよびデバッグする方法](how-to-preview-and-debug-form-templates-that-require-full-trust.md)」の説明に従ってフォーム テンプレートを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="df8c2-130">To debug an InfoPath managed code form template when using an object model member that requires full trust, you must configure your form template as described in [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  
## <a name="using-a-sample-data-file"></a><span data-ttu-id="df8c2-131">サンプル データ ファイルを使用する</span><span class="sxs-lookup"><span data-stu-id="df8c2-131">Using a Sample Data File</span></span>

<span data-ttu-id="df8c2-p104">既定では、フォーム テンプレートの作成時に作成される template.xml ファイルがデバッグやプレビューの際に使用されますが、独自のデータ ファイルを作成して、そのファイルを使用するように指定することもできます。そのためには、次のいずれかの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="df8c2-p104">By default, debugging and previewing uses the template.xml file that is created when a form template is created. You can create your own data file and specify to use it when previewing or debugging by using one of the following procedures.</span></span> 
  
### <a name="to-specify-a-sample-data-file-to-use-while-debugging-or-previewing-in-visual-studio-tools-for-applications"></a><span data-ttu-id="df8c2-134">Visual Studio Tools for Applications でのデバッグやプレビューの際に使用するサンプル データ ファイルを指定するには</span><span class="sxs-lookup"><span data-stu-id="df8c2-134">To specify a sample data file to use while debugging or previewing in Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="df8c2-135">template.xml を表示するために、フォーム テンプレートを InfoPath のデザイン モードで開きます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-135">To view template.xml, open the form template in InfoPath design mode.</span></span>
    
2. <span data-ttu-id="df8c2-136">[ **ファイル**] タブをクリックし、[ **保存**]、[ **フォーム テンプレートに名前を付けて保存**]、[ **ソース ファイル**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="df8c2-136">Click the **File** tab, click **Saving**, click **Save Form Template As**, and the click **Source Files**.</span></span>
    
3. <span data-ttu-id="df8c2-137">フォーム テンプレート ファイルをフォルダーに保存してから、template.xml ファイルをテキスト エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-137">Save the form template files to a folder, and then open the template.xml file in a text editor.</span></span>
    
4. <span data-ttu-id="df8c2-138">使用するサンプル データを使って template.xml と同じ構造のファイルを作成し、そのファイルを保存します。</span><span class="sxs-lookup"><span data-stu-id="df8c2-138">Create and save a file with the same structure as template.xml with the sample data you want to use.</span></span>
    
5. <span data-ttu-id="df8c2-139">[ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="df8c2-139">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
6. <span data-ttu-id="df8c2-140">[ **フォームのオプション**] ダイアログ ボックスの [ **プレビュー**] カテゴリをクリックし、[ **サンプル データ**] の下の [ **ファイルの場所**] ボックスに作成したサンプル データ ファイルを指定します。</span><span class="sxs-lookup"><span data-stu-id="df8c2-140">Click the **Preview** category of the **Form Options** dialog box, and then under **Sample data** specify the sample data file you created in the **File location** box.</span></span> 
    
## <a name="specifying-a-user-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="df8c2-141">デバッグやプレビューの際に使用するユーザー ロールを指定する</span><span class="sxs-lookup"><span data-stu-id="df8c2-141">Specifying a User Role to Use While Debugging or Previewing</span></span>

<span data-ttu-id="df8c2-p105">使用しているフォームにユーザー ロールが定義されている場合は、フォームのデバッグやプレビューの際に使用するユーザー ロールを指定することができます。ユーザー ロールを定義する方法については、InfoPath ヘルプで "ユーザー ロール" を検索してください。</span><span class="sxs-lookup"><span data-stu-id="df8c2-p105">If the form you are working with has user roles defined for it, you can specify a user role to use while debugging or previewing your form. For information on how to define user roles, search InfoPath help for "user role".</span></span>
  
> [!NOTE]
> <span data-ttu-id="df8c2-p106">フォーム テンプレートの互換性設定が [ **Web ブラウザー フォーム**] に設定されている場合、ユーザー ロールを指定するオプションは使用できません。InfoPath Forms Services からブラウザーで開かれたフォーム テンプレートでは、ユーザー ロールはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="df8c2-p106">The option to specify a user role is not available if the compatibility setting for your form template is set to **Web Browser Form**. User roles are not supported in form templates opened in the browser from InfoPath Forms Services.</span></span> 
  
### <a name="to-specify-a-role-to-use-while-debugging-or-previewing"></a><span data-ttu-id="df8c2-146">デバッグやプレビューの際に使用するロールを指定するには</span><span class="sxs-lookup"><span data-stu-id="df8c2-146">To specify a role to use while debugging or previewing</span></span>

1. <span data-ttu-id="df8c2-147">Visual Studio 2012 で作業している場合は、InfoPath に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-147">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="df8c2-148">[ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="df8c2-148">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="df8c2-149">[ **フォームのオプション**] ダイアログ ボックスの [ **プレビュー**] カテゴリをクリックし、[ **プレビューのロール**] ボックスの一覧で、使用するユーザー ロールを指定します。</span><span class="sxs-lookup"><span data-stu-id="df8c2-149">Click the **Preview** category of the **Form Options** dialog box, and then specify the user role to use in the **Preview as** drop-down box.</span></span> 
    
## <a name="specifying-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="df8c2-150">デバッグやプレビューの際に使用するドメインを指定する</span><span class="sxs-lookup"><span data-stu-id="df8c2-150">Specifying a Domain to Use While Debugging or Previewing</span></span>

<span data-ttu-id="df8c2-p107">特定のドメインに発行された場合のフォームの表示状態を、発行前にプレビューすることができます。この設定は、フォームのセキュリティ レベルが [ **ドメイン**] に明示的に設定されている場合にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-p107">You can preview a form as if it was published to a specific domain. This setting will only apply if the security level of the form template is explicitly set to **Domain**.</span></span>
  
### <a name="to-specify-a-domain-to-use-while-debugging-or-previewing"></a><span data-ttu-id="df8c2-153">デバッグやプレビューの際に使用するドメインを指定するには</span><span class="sxs-lookup"><span data-stu-id="df8c2-153">To specify a domain to use while debugging or previewing</span></span>

1. <span data-ttu-id="df8c2-154">Visual Studio 2012 で作業している場合は、InfoPath に切り替えます。</span><span class="sxs-lookup"><span data-stu-id="df8c2-154">If you are working in Visual Studio 2012, switch to the InfoPath designer.</span></span>
    
2. <span data-ttu-id="df8c2-155">[ **ファイル**] タブをクリックして、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="df8c2-155">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="df8c2-156">[ **フォームのオプション**] ダイアログ ボックスの [ **プレビュー**] カテゴリをクリックし、プレビューやデバッグの際に使用するドメインを [ **ドメイン**] ボックスで指定します。</span><span class="sxs-lookup"><span data-stu-id="df8c2-156">Click the **Preview** category of the **Form Options** dialog box, and then specify the domain to use while previewing and debugging in the **Domain** box.</span></span> 
    
4. <span data-ttu-id="df8c2-157">[ **フォームのオプション**] ダイアログ ボックスの [ **セキュリティと信頼**] カテゴリをクリックし、[ **自動的にセキュリティ レベルを設定する**] チェック ボックスをオフにして、[ **ドメイン**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="df8c2-157">Click the **Security and Trust** category of the **Forms Options** dialog box, clear the **Automatically determine security level** check box, and then click **Domain**.</span></span>
    

