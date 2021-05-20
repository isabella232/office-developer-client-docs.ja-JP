---
title: 完全に信頼できるフォームを理解する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 64d62990-6275-edef-c639-b6ba8d10c38c
description: InfoPath には、完全に信頼できるフォーム (セキュリティのより高いアクセス許可があり、ユーザーのコンピューターのシステム リソースおよびその他のコンポーネントにアクセスできるフォーム) を作成する機能があります。この記事では、完全に信頼できるフォームとは何か、このフォームを使用する理由、および標準のフォームを手動で変換および登録するか、または標準のフォームにデジタル署名して、完全に信頼できるフォームを作成する方法について説明します。
ms.openlocfilehash: 04560e0c844d6a6ff681fd366ca7da2e4db36ba1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430393"
---
# <a name="understanding-fully-trusted-forms"></a><span data-ttu-id="a868d-104">完全に信頼できるフォームを理解する</span><span class="sxs-lookup"><span data-stu-id="a868d-104">Understanding Fully Trusted Forms</span></span>

<span data-ttu-id="a868d-p102">InfoPath には、完全に信頼できるフォーム (セキュリティのより高いアクセス許可があり、ユーザーのコンピューターのシステム リソースおよびその他のコンポーネントにアクセスできるフォーム) を作成する機能があります。この記事では、完全に信頼できるフォームとは何か、このフォームを使用する理由、および標準のフォームを手動で変換および登録するか、または標準のフォームにデジタル署名して、完全に信頼できるフォームを作成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a868d-p102">InfoPath provides the ability to create fully trusted forms, which are forms that have greater security permissions and can access system resources and other components on a user's computer. This article describes what a fully trusted form is, and why it is used, and create a fully trusted form by manually converting and registering a standard form, or by digitally signing a standard form.</span></span>

<span data-ttu-id="a868d-p103">InfoPath フォーム テンプレートは、さまざまなレベルのセキュリティと共に展開できます。使用するレベルは、フォームで外部リソースにアクセスするために必要なレベルによって決まります。既定では、InfoPath フォーム テンプレートはシステム リソースへのアクセスを制限され、スクリプトを実行しても安全であるとマークされていないソフトウェア コンポーネントの使用は許可されません。ただし、この動作を無効にし、システム リソースや、スクリプトを実行しても安全であるとマークされていないソフトウェア コンポーネントを含むその他の外部リソースに、フォームがアクセスすることを許可できます。</span><span class="sxs-lookup"><span data-stu-id="a868d-p103">InfoPath form templates can be deployed with varying levels of security. The level you use is dictated by the level of access to external resources that you want a form to have. By default, InfoPath form templates are restricted from accessing system resources and are not allowed to use any software components that are not marked as safe for scripting. However, this behavior can be overridden so that a form can access system resources and other external resources, including software components that are not marked as safe for scripting.</span></span>
  
<span data-ttu-id="a868d-111">フォームが使用されるためには、InfoPath がそのフォームのベースとなったフォーム テンプレートにアクセスできなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a868d-111">For a form to be used, InfoPath must be able to access the form template that the form is based on.</span></span> <span data-ttu-id="a868d-112">InfoPath でフォーム テンプレートを作成すると、フォーム テンプレートの場所の URL を含むエントリが、フォーム定義ファイル (.xsf) に作成されます。</span><span class="sxs-lookup"><span data-stu-id="a868d-112">When you create a form template, InfoPath creates an entry in the form definition (.xsf) file that contains the URL of the location of the form template.</span></span> <span data-ttu-id="a868d-113">URL ベースのフォームは、*サンドボックス* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="a868d-113">A URL-based form is said to be *sandboxed*.</span></span> <span data-ttu-id="a868d-114">ユーザーがフォームに入力すると、フォームはローカル キャッシュに追加され、フォームからシステム リソースへのアクセスは拒否されます。</span><span class="sxs-lookup"><span data-stu-id="a868d-114">When a user fills it out, the form is added in a local cache and denied access to system resources.</span></span> <span data-ttu-id="a868d-115">この種類のフォームは、フォームが開かれたドメインからアクセス許可を継承します。</span><span class="sxs-lookup"><span data-stu-id="a868d-115">This kind of form inherits its permissions from the domain in which it is opened.</span></span> 
  
<span data-ttu-id="a868d-p105">ただし、フォームを変更し、システム リソースへのアクセスが許可される URN (Uniform Resource Name) ベースのフォームにすることができます。この種類のフォームを *完全に信頼できる* と呼びます。</span><span class="sxs-lookup"><span data-stu-id="a868d-p105">However, you can modify a form so that it is based on a Uniform Resource Name (URN) instead, which allows access to system resources. Forms of this kind are said to be *fully trusted*.</span></span> 
  
## <a name="why-use-a-fully-trusted-form"></a><span data-ttu-id="a868d-118">完全に信頼できるフォームを使用する理由</span><span class="sxs-lookup"><span data-stu-id="a868d-118">Why Use a Fully Trusted Form?</span></span>

<span data-ttu-id="a868d-p106">完全に信頼できるフォームには、セキュリティで保護されたフォームよりも高いアクセス許可のセットが与えられます。たとえば、システム リソースにアクセスするために外部オブジェクトを使用するプログラミング コードを含むこと、スクリプトを実行しても安全であるとマークされていないソフトウェア コンポーネントまたは Microsoft ActiveX コントロールを使用すること、および .NET アセンブリで提供されるカスタム ビジネス ロジックを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="a868d-p106">Fully trusted forms have a better set of permissions than sandboxed forms. For example, they can contain programming code that uses external objects for accessing system resources, they can use software components or Microsoft ActiveX controls that are not marked as safe for scripting, and they can use custom business logic provided by .NET assemblies.</span></span>
  
<span data-ttu-id="a868d-p107">さらに、InfoPath オブジェクト モデルの一部のメンバーはセキュリティ レベル 3 に設定されます。これは、それらのメンバーが完全に信頼できるフォームのみで使用できることを意味します。たとえば、Microsoft Office **CommandBars** オブジェクトにアクセスするには、InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) クラスの [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) プロパティを使用して、メンバーへの参照を設定します。このプロパティはセキュリティ レベル 3 に設定されるので、完全に信頼されていないフォームでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="a868d-p107">In addition, some members of the InfoPath object model are set to security level 3, which means that they can only be used in a fully trusted form. For example, to access the Microsoft Office **CommandBars** object, you use the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the InfoPath [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class to set a reference to it. Because this property is set to security level 3, it cannot be used in a form that is not fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a868d-124">完全に信頼されていないフォームで、[Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) クラスの [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) プロパティ、またはセキュリティ レベルが 3 のその他のオブジェクト モデル メンバーを使用すると、"アクセスは拒否されました" というエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="a868d-124">Using the [CommandBars](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.CommandBars.aspx) property of the [Window](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Window.aspx) class, or any other object model member that has a security level of 3, in a form that is not fully trusted will result in a "permission denied" error.</span></span> 
  
## <a name="what-makes-a-form-fully-trusted"></a><span data-ttu-id="a868d-125">フォームを完全に信頼する方法</span><span class="sxs-lookup"><span data-stu-id="a868d-125">What Makes a Form Fully Trusted?</span></span>

<span data-ttu-id="a868d-126">完全に信頼できるフォームの作成と使用には、InfoPath ユーザー インターフェイスとフォーム ファイルの両方が関連する、次の操作が必要です。</span><span class="sxs-lookup"><span data-stu-id="a868d-126">The following actions, involving both the InfoPath user interface and the form files, are required to create and use a fully trusted form:</span></span>
  
- <span data-ttu-id="a868d-p108">[ **セキュリティ センター**] ダイアログ ボックスの [ **信頼できる発行元**] カテゴリで、InfoPath が完全に信頼できるフォームの使用を許可するようにする。このオプションは、完全に信頼できるフォームをユーザーが開けるようにするために有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a868d-p108">Enabling InfoPath to allow for the use of fully trusted forms on the **Trusted Publishers** category of the **Trust Center** dialog box. This option must be enabled for users to open fully trusted forms.</span></span> 
    
- <span data-ttu-id="a868d-129">InfoPath **Application** オブジェクトの **RegisterSolution** メソッドを使用して、完全に信頼できるフォームをターゲット コンピューターに登録する。</span><span class="sxs-lookup"><span data-stu-id="a868d-129">Registering the fully trusted form on the target computer by using the **RegisterSolution** method of the InfoPath **Application** object.</span></span> 
    
## <a name="creating-a-fully-trusted-form"></a><span data-ttu-id="a868d-130">完全に信頼できるフォームを作成する</span><span class="sxs-lookup"><span data-stu-id="a868d-130">Creating a Fully Trusted Form</span></span>

- <span data-ttu-id="a868d-131">フォームを手動で作成することができます。これには、フォーム ファイルの一部を直接変更する操作が必要になります。</span><span class="sxs-lookup"><span data-stu-id="a868d-131">You can create the form manually, which involves modifying some of the form files directly.</span></span>
    
- <span data-ttu-id="a868d-132">フォーム テンプレートにデジタル署名することができます。</span><span class="sxs-lookup"><span data-stu-id="a868d-132">You can digitally sign the form template.</span></span>
    
### <a name="manually-creating-a-fully-trusted-form"></a><span data-ttu-id="a868d-133">完全に信頼できるフォームを手動で作成する</span><span class="sxs-lookup"><span data-stu-id="a868d-133">Manually Creating a Fully Trusted Form</span></span>

#### <a name="to-manually-create-a-fully-trusted-form"></a><span data-ttu-id="a868d-134">完全に信頼できるフォームを手動で作成するには</span><span class="sxs-lookup"><span data-stu-id="a868d-134">To manually create a fully trusted form</span></span>

1. <span data-ttu-id="a868d-135">完全に信頼できるようにするフォーム テンプレートのバックアップ コピーを作成します。</span><span class="sxs-lookup"><span data-stu-id="a868d-135">Make a backup copy of the form template that you want to make fully trusted.</span></span>
    
2. <span data-ttu-id="a868d-136">InfoPath でフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="a868d-136">Open the form template in InfoPath.</span></span>
    
3. <span data-ttu-id="a868d-137">フォームのソース ファイルをハード ディスク上のフォルダーに保存します。そのためには、[ **ファイル**] タブ、[ **発行**]、[ **ソース ファイルのエクスポート**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-137">Save the form source files to a folder on your hard disk by clicking the **File** tab, clicking **Publish**, and then clicking **Export Source Files**.</span></span>
    
4. <span data-ttu-id="a868d-138">フォームのソース ファイルを保存するフォルダーを指定し、[ **OK**] をクリックします。次に、InfoPath デザイナーを終了します。</span><span class="sxs-lookup"><span data-stu-id="a868d-138">Specify the folder in which to save the form source files, click **OK**, and then exit the InfoPath designer.</span></span>
    
5. <span data-ttu-id="a868d-139">フォーム ファイルを抽出したフォルダーで、既定では  `manifest.xsf` という名前のフォーム定義ファイル (.xsf) を、Microsoft メモ帳などのテキスト エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="a868d-139">In the folder in which you extracted the form files, open the form definition (.xsf) file, named  `manifest.xsf` by default, in a text editor such as Microsoft Notepad.</span></span> 
    
6. <span data-ttu-id="a868d-140">.xsf ファイルの **xDocumentClass** 要素に、次の属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="a868d-140">Add the following attributes to the **xDocumentClass** element in the .xsf file:</span></span> 
   
   `requireFullTrust="yes"`<br/>
   `name="urn:MyForm:MyCompany`

   > [!NOTE]
   > URN として使用する値は、その値が一意である限り、任意の文字列値にすることができます。 `urn:` プレフィックスの後には少なくとも 2 つの値が必要であり、これらの値はコロンで区切る必要があります。 <span data-ttu-id="a868d-143">さらに、URN は 255 文字以下でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="a868d-143">In addition, the URN should not exceed 255 characters.</span></span> 
  
7. <span data-ttu-id="a868d-144">.xsf ファイルを保存して閉じ、既定では  `Template.xml` という名前の XML テンプレート ファイル (.xml) を、メモ帳などのテキスト エディターで開きます。</span><span class="sxs-lookup"><span data-stu-id="a868d-144">Save and close the .xsf file, and then open the XML template (.xml) file that is named  `Template.xml` by default, in a text editor such as Notepad.</span></span> 
    
8. <span data-ttu-id="a868d-145">**href** 属性を  `mso-infoPathSolution` 処理命令から削除し, .xsf ファイルの手順 6. で使用したのと同じ **name** 属性に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="a868d-145">Remove the **href** attribute from the  `mso-infoPathSolution` processing instruction and replace it with the same **name** attribute that you used in step 6 for the .xsf file.</span></span> 
    
   > [!NOTE]
   > <span data-ttu-id="a868d-146">**name** 属性に使用される URN 値は, .xsf ファイルと XML テンプレート ファイルの両方で同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="a868d-146">The URN values that are used for the **name** attribute must be the same in both the .xsf file and XML template file.</span></span> 
  
9. <span data-ttu-id="a868d-147">XML テンプレート ファイルを保存して閉じます。</span><span class="sxs-lookup"><span data-stu-id="a868d-147">Save and close the XML template file.</span></span>
    
10. <span data-ttu-id="a868d-148">makecab.exe などのツールを使用して、ファイルを .xsn CAB 形式に再パッケージ化します。</span><span class="sxs-lookup"><span data-stu-id="a868d-148">Repackage the files into the .xsn CAB format with a tool such as makecab.exe.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a868d-p110">InfoPath フォーム デザイナーはフォーム ファイルの .xsn ファイルへの再パッケージ化をサポートしていますが、この処理を実行すると、フォームが URL ベースのフォームに戻ります。このため、変更がフォーム ファイルに上書きされないようにするには、ファイルを手動で再パッケージ化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a868d-p110">Although InfoPath form designer supports repackaging the form files into an .xsn file, doing this will revert the form to a URL-based form. For this reason, you must repackage the files manually to avoid overwriting your changes to the form files.</span></span> 
  
11. <span data-ttu-id="a868d-p111">InfoPath **Application** オブジェクトの **RegisterSolution** メソッドを使用してカスタム インストール プログラムを作成して、完全に信頼できるフォームをインストールします。このための簡単な方法は、次のコード行を使用するスクリプト ファイルを、Microsoft JScript または VBScript 構文のどちらかで作成することです。</span><span class="sxs-lookup"><span data-stu-id="a868d-p111">Create a custom installation program by using the **RegisterSolution** method of the InfoPath **Application** object to install the fully trusted form. A simple way to do this is to create a script file that uses the following lines of code (in either Microsoft JScript or VBScript syntax):</span></span> 
    
    ```js
        objIPApp = new ActiveXObject("InfoPath.Application"); 
        objIPApp.RegisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
        objIPApp.Quit(); 
        objIPApp = null;
    ```
   
    ```vb
        Public Sub InstallForm()
            Dim objIPApp As Object
            ' Create a reference to the Application object.
            Set objIPApp = CreateObject("InfoPath.Application")
            ' Register the InfoPath form template.
            objIPApp.RegisterSolution ("C:\\My Forms\\MyFormTemplate.xsn")
            MsgBox "The InfoPath form template has been registered."
            Set objIPApp = Nothing
        End Sub
        
    ```

> [!NOTE] 
> <span data-ttu-id="a868d-p112">この例では簡単なスクリプト ファイルを使用していますが、Microsoft Windows インストーラー (.msi) ファイルなどの、より堅牢なインストール メカニズムを使用することもできます。ただし、 **RegisterSolution** メソッドを使用して、完全に信頼できるフォームをターゲット コンピューターに正しくインストールしてください。Visual Basic または Visual Studio から、InfoPath **Application** オブジェクトの **RegisterSolution** メソッドにアクセスするには、Microsoft InfoPath 3.0 タイプ ライブラリへの参照を設定します。これは、C:\Program Files\Microsoft Office\Office14 フォルダーにインストールされる IPEDITOR.dll によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="a868d-p112">Although this example uses a simple script file, you can also use a more robust installation mechanism such as Microsoft Windows Installer (.msi) files. Be sure, however, to use the **RegisterSolution** method to correctly install the fully trusted form on the target computer. To access the **RegisterSolution** method of the InfoPath the **Application** object from Visual Basic or Visual Studio, set a reference to the Microsoft InfoPath 3.0 Type Library, which is provided by IPEDITOR.dll that is installed in the C:\Program Files\Microsoft Office\Office14 folder.</span></span> 
  
<span data-ttu-id="a868d-156">完全に信頼できるフォームを削除する必要がある場合は、次の JScript および VBScript の例に示すように、 **Application** オブジェクトの **UnregisterSolution** メソッドを使用できます。</span><span class="sxs-lookup"><span data-stu-id="a868d-156">If you have to remove a fully trusted form, you can use the **UnregisterSolution** method of the **Application** object as shown in the following JScript and VBScript examples.</span></span> 
    
```js
    objIPApp = new ActiveXObject("InfoPath.Application"); 
    objIPApp.UnregisterSolution("C:\\MyForms\\MyTrustedForm.xsn"); 
    objIPApp.Quit(); 
    objIPApp = null;
```

```vb
    Public Sub UninstallForm()
        Dim objIPApp As Object
        ' Create a reference to the Application object.
        Set objIPApp = CreateObject("InfoPath.Application")
        ' Unregister the InfoPath form template.
        objIPApp.UnregisterSolution ("C:\My Forms\MyFormTemplate.xsn")
        MsgBox ("The InfoPath form template has been unregistered.")
        Set objIPApp = Nothing
    End Sub
    
```

### <a name="digitally-signing-a-form-template-to-create-a-fully-trusted-form"></a><span data-ttu-id="a868d-157">フォーム テンプレートにデジタル署名して、完全に信頼できるフォームを作成する</span><span class="sxs-lookup"><span data-stu-id="a868d-157">Digitally Signing a Form Template to Create a Fully Trusted Form</span></span>

<span data-ttu-id="a868d-158">フォーム テンプレートにデジタル署名すると、電子メール、または Microsoft SharePoint Foundation を実行しているサーバーなどの Web サーバーを使用して、完全に信頼できるフォーム テンプレートを展開することができます。</span><span class="sxs-lookup"><span data-stu-id="a868d-158">Digitally signing a form template enables you to deploy a fully trusted form template by email or on a Web server, such as a server that is running Microsoft SharePoint Foundation.</span></span> <span data-ttu-id="a868d-159">フォームの完全な信頼を指定し、デジタル署名して発行することによりフォームを完全に信頼するには、次の 3 つの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="a868d-159">Use the steps in the following three procedures to make a form fully trusted by specifying full trust for the form, signing it digitally, and then publishing it.</span></span>
  
#### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="a868d-160">フォーム テンプレートにデジタル署名するには</span><span class="sxs-lookup"><span data-stu-id="a868d-160">To digitally sign a form template</span></span>

1. <span data-ttu-id="a868d-161">フォームを InfoPath デザイナーで開き、[ **ファイル**] タブをクリックし、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-161">Open the form in the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="a868d-162">[ **フォームのオプション**] ダイアログ ボックスの [ **セキュリティと信頼**] カテゴリをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-162">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="a868d-163">[ **自動的にセキュリティ レベルを設定する (推奨)**] チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="a868d-163">Clear the selection for **Automatically determine security level (recommended)**.</span></span>
    
4. <span data-ttu-id="a868d-164">[ **完全信頼 (コンピューターにあるファイルおよび設定にアクセスできる)**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-164">Select **Full Trust (the form has access to files and settings on the user's computer)**.</span></span>
    
5. <span data-ttu-id="a868d-165">[ **フォーム テンプレートの署名**] の [ **このフォーム テンプレートに署名する**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="a868d-165">Under **Form Template Signature**, select **Sign this form template**.</span></span>
    
6. <span data-ttu-id="a868d-166">[ **証明書の選択**] をクリックして、信頼されている証明書プロバイダーから以前にダウンロードおよびインストールされている証明書を選択します。</span><span class="sxs-lookup"><span data-stu-id="a868d-166">Click **Select Certificate** to select a certificate that was previously downloaded and installed from a trusted certificate provider.</span></span> 
    
7. <span data-ttu-id="a868d-167">[OK] を 2 回クリックして完全に終了します。</span><span class="sxs-lookup"><span data-stu-id="a868d-167">Click OK two times to exit completely.</span></span>
    
#### <a name="to-publish-the-form-template-to-a-sharepoint-document-library"></a><span data-ttu-id="a868d-168">フォーム テンプレートを SharePoint ドキュメント ライブラリに発行するには</span><span class="sxs-lookup"><span data-stu-id="a868d-168">To publish the form template to a SharePoint Document Library</span></span>

1. <span data-ttu-id="a868d-169">[ **ファイル**] タブの [ **発行**] をクリックし、[ **SharePoint Server**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-169">Click the **File** tab, click **Publish**, and then click **SharePoint Server**.</span></span>
    
2. <span data-ttu-id="a868d-170">[ **発行ウィザード**] の指示に従って、フォーム テンプレートを新しい SharePoint ドキュメント ライブラリまたは既存の SharePoint ドキュメント ライブラリに発行します。</span><span class="sxs-lookup"><span data-stu-id="a868d-170">Follow the instructions in the **Publishing Wizard** to publish the form template to a new or existing SharePoint document library.</span></span> 
    
#### <a name="to-a-create-a-form-that-is-based-on-your-fully-trusted-digitally-signed-form-template"></a><span data-ttu-id="a868d-171">完全に信頼できるデジタル署名されたフォーム テンプレートに基づいてフォームを作成するには</span><span class="sxs-lookup"><span data-stu-id="a868d-171">To a create a form that is based on your fully trusted, digitally signed form template</span></span>

1. <span data-ttu-id="a868d-172">SharePoint ドキュメント ライブラリで、[ **フォームの入力**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-172">In the SharePoint document library, click **Fill Out the Form**.</span></span>
    
   > [!NOTE]
   > <span data-ttu-id="a868d-p114">[ **発行ウィザード**] を使用して SharePoint ドキュメント ライブラリにフォーム テンプレートを発行しても、テンプレートはフォーム ライブラリの項目として表示されません。このドキュメント ライブラリでフォームを作成すると、テンプレートは、新しいフォームのテンプレートとして既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="a868d-p114">After publishing the form template to a SharePoint document library using the **Publishing Wizard**, the template is not displayed as an item in the form library. When you create a form in that document library, the template will be used by default as the template for the new form.</span></span> 
  
2. <span data-ttu-id="a868d-p115">InfoPath では、既定のフォーム テンプレートがデジタル署名されている場合、デジタル署名されたフォーム テンプレートに関するセキュリティ警告が表示されます。[ **この発行元のファイルを常に信頼し、自動的にファイルを開く**] をクリックし、[ **開く**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-p115">If the default form template was digitally signed, InfoPath displays a security warning about the digitally signed form template. Select **Always trust files from this publisher and open them automatically**, and then click **Open**.</span></span>
    
## <a name="using-a-fully-trusted-form"></a><span data-ttu-id="a868d-177">完全に信頼できるフォームを使用する</span><span class="sxs-lookup"><span data-stu-id="a868d-177">Using a Fully Trusted Form</span></span>

<span data-ttu-id="a868d-p116">完全に信頼できるフォームの使用は、標準のフォームの使用に非常に似ています。唯一の重要な違いは、制限されたリソースにフォームがアクセスすることができ、警告は表示されないことです。</span><span class="sxs-lookup"><span data-stu-id="a868d-p116">Using a fully trusted form is very similar to using a standard form. The only significant differences are that the form can access restricted resources and warnings will no longer be displayed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a868d-p117">InfoPath で完全に信頼できるフォームを有効にするには、ユーザーは [ **セキュリティ センター**] ダイアログ ボックスの [ **信頼できる発行元**] カテゴリで [ **完全に信頼できるフォームをこのコンピューターで実行できるようにする**] チェック ボックスがオンになっていることを確認する必要があります。[ **セキュリティ センター**] ダイアログ ボックスを開くには、[ **ファイル**] タブ、([ **InfoPath**] タブの下にある) [ **オプション**]、[ **セキュリティ センター**]、[ **セキュリティ センターの設定**] の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-p117">To enable InfoPath to use a fully trusted form, users must ensure that the **Allow fully trusted forms to run on my computer** check box is selected on the **Trusted Publishers** category of the **Trust Center** dialog box. To open the **Trust Center** dialog box, click the **File** tab, click **Options** (below the **InfoPath** tab), click **Trust Center**, and then click **Trust Center Settings**.</span></span> 
  
<span data-ttu-id="a868d-182">完全に信頼できるフォームは InfoPath の [ **フォームの入力**] ダイアログ ボックスから開くことができます。</span><span class="sxs-lookup"><span data-stu-id="a868d-182">A fully trusted form can be opened in InfoPath from the **Fill Out a Form** dialog box.</span></span> 
  
<span data-ttu-id="a868d-183">[ **フォームの入力**] ダイアログ ボックスを開くには、[ **フォームの入力**] 作業ウィンドウの [ **その他のフォーム**] をクリックするか、または [ **ファイル**] メニューの [ **フォームの入力**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a868d-183">The **Fill Out a Form** dialog box opens when you click **More Forms** in the **Fill Out a Form** task pane, or you click **Fill Out a Form** on the **File** menu.</span></span> 
  
### <a name="making-changes-to-a-fully-trusted-form"></a><span data-ttu-id="a868d-184">完全に信頼できるフォームに変更を加える</span><span class="sxs-lookup"><span data-stu-id="a868d-184">Making Changes to a Fully Trusted Form</span></span>

<span data-ttu-id="a868d-p118">.xsn ファイルに変更を加えるだけの場合は、変更後に、ユーザーが既存の .xsn ファイルを新しいファイルに置き換えるようにします。ユーザーがカスタム インストール プログラムを使用してファイルを再インストールする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="a868d-p118">If you only have to make changes to the .xsn file, you can have users replace their existing .xsn file with the new one after the changes are made. They will not have to reinstall it by using a custom installation program.</span></span>
  
<span data-ttu-id="a868d-187">ただし, .xsn ファイルに含まれているフォーム ファイルに変更を加える場合は、前に説明したように、ファイルを再パッケージ化し、完全に信頼できるフォームをユーザーが再インストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a868d-187">However, if you are making changes to the form files that the .xsn file contains, you must repackage the files, as explained earlier, and then have users reinstall the fully trusted form.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a868d-188">最善の方法は、InfoPath デザイナーからフォーム テンプレートを .xsn 形式に戻して保存し、この記事の手順に従って、完全に信頼できるフォームを作成することです。</span><span class="sxs-lookup"><span data-stu-id="a868d-188">The best approach is to save the form template back to the .xsn format from the InfoPath designer, and then follow the steps in this article to create a fully trusted form.</span></span> 
  
## <a name="conclusion"></a><span data-ttu-id="a868d-189">終わりに</span><span class="sxs-lookup"><span data-stu-id="a868d-189">Conclusion</span></span>

<span data-ttu-id="a868d-p119">ビジネスの要件やユーザーのニーズによっては、標準の InfoPath フォームよりも高いアクセス許可のセットが与えられたフォームの作成が必要になることもあります。InfoPath には、フォームを変更することで、システム リソース、およびスクリプトを実行しても安全であるとマークされていないその他の外部リソースにアクセスできるようにする機能があります。この操作は、フォーム テンプレートに含まれるフォーム ファイルを変更し、インストール スクリプトを実行するか、またはフォーム テンプレートにデジタル署名することにより、手動で行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a868d-p119">Depending on your business requirements and the needs of your users, you may have to create a form that has a higher set of permissions than the standard InfoPath form. InfoPath provides the ability to modify a form so that it can access system resources and other external resources that are not marked as safe for scripting. This can be done manually by making modifications to the form files that a form template contains and running an installation script, or by digitally signing the form template.</span></span>
  

