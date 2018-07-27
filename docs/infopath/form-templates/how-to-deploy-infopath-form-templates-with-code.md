---
title: コードを含む InfoPath フォーム テンプレートを展開する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- deploying form templates [infopath 2007],InfoPath 2007, deploying form templates,form templates [InfoPath 2007], deploying,.NET Framework security settings [InfoPath 2007],deployment [InfoPath 2007], form templates
localization_priority: Normal
ms.assetid: ab66e26d-74ee-4211-b387-1385183a6803
description: InfoPath のマネージ コード フォーム テンプレートのフォーム コードは、共通言語ランタイム (CLR) の下で実行されるアセンブリとしてコンパイルされます。これは、フォーム コードを変更するときには、常に、Visual Studio 2012 でプロジェクトを開き、コード エディターで編集し、フォーム テンプレートを再コンパイルして、フォーム テンプレートを再展開する必要があることを意味します。さらに、マネージ コード フォーム テンプレートのプライベート アセンブリは、ホストされる CLR アプリケーション ドメインで実行されるので、完全な信頼を必要とするフォームのセキュリティ設定は、完全な信頼を必要としないフォーム テンプレートとは若干異なります。
ms.openlocfilehash: 56af865a80df75c7e1d973767066a03310cdde1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799112"
---
# <a name="deploy-infopath-form-templates-with-code"></a><span data-ttu-id="f690a-106">コードを含む InfoPath フォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="f690a-106">Deploy InfoPath Form Templates with Code?</span></span>

<span data-ttu-id="f690a-p102">InfoPath のマネージ コード フォーム テンプレートのフォーム コードは、共通言語ランタイム (CLR) の下で実行されるアセンブリとしてコンパイルされます。これは、フォーム コードを変更するときには、常に、Visual Studio 2012 でプロジェクトを開き、コード エディターで編集し、フォーム テンプレートを再コンパイルして、フォーム テンプレートを再展開する必要があることを意味します。さらに、マネージ コード フォーム テンプレートのプライベート アセンブリは、ホストされる CLR アプリケーション ドメインで実行されるので、完全な信頼を必要とするフォームのセキュリティ設定は、完全な信頼を必要としないフォーム テンプレートとは若干異なります。</span><span class="sxs-lookup"><span data-stu-id="f690a-p102">The form code for an InfoPath managed code form template is compiled as an assembly that runs under the common language runtime (CLR). This means that whenever you need to make changes to the form code, you must open its project in Visual Studio 2012, make changes in the code editor, recompile your form template, and then re-deploy the form template. Additionally, because the private assembly for a managed code form template is running under a hosted CLR application domain, the security settings for forms that require full trust differ somewhat from form templates that do not require full trust.</span></span>
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a><span data-ttu-id="f690a-110">完全な信頼を必要としないフォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="f690a-110">Deploying Form Templates That Do Not Require Full Trust</span></span>

<span data-ttu-id="f690a-p103">フォーム テンプレートのフォーム コードで完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーを使用しておらず、フォーム テンプレートで完全な信頼を必要とする機能を使用していない場合は、次の手順に従って InfoPath から直接フォーム テンプレートを発行することができます。InfoPath のセキュリティ モデルの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f690a-p103">If the form code for your form template does not use InfoPath object model members that require full trust, and the form template does not use features that require full trust, you can publish your form template directly from InfoPath using the following procedure. For information about the InfoPath security model, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md).</span></span>
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a><span data-ttu-id="f690a-113">完全な信頼を必要としないフォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="f690a-113">Deploy a form template that does not require full trust</span></span>

1. <span data-ttu-id="f690a-114">Visual Studio 2012 でフォーム テンプレートを作成してデバッグします。</span><span class="sxs-lookup"><span data-stu-id="f690a-114">Create and debug your form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="f690a-115">Visual Studio 2012 コード エディターで作業している場合は、InfoPath に切り替えて、[ **ファイル**] タブをクリックし、[ **発行**] タブ上の目的の発行場所のボタンをクリックします (フォーム テンプレートを以前に既に発行済みの場合は、[ **ファイル**] タブをクリックし、[ **クイック発行**] をクリックして、フォーム テンプレートを同じ場所に再発行できます)。</span><span class="sxs-lookup"><span data-stu-id="f690a-115">If you are working in the Visual Studio 2012 code editor, switch to InfoPath, click the **File** tab, and then click the button for the desired publishing location on the **Publish** tab. (If you have published the form template previously, you can click the **File** tab, and then click **Quick Publish** to republish the form template to the same location.)</span></span> 
    
    <span data-ttu-id="f690a-p104">フォーム テンプレートがコンパイルされ、 **発行ウィザード**が開始されます。 **発行ウィザード**の手順に従って、選択した場所にフォームを展開します。 **発行ウィザード**の使用方法の詳細については、InfoPath のヘルプで「フォーム テンプレートを発行する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f690a-p104">The form template is compiled and the **Publishing Wizard** is launched. Follow the steps in the **Publishing Wizard** to deploy your form to the location of your choice. For more information about using the **Publishing Wizard**, search InfoPath Help for "Publish a form template".</span></span>
    
## <a name="deploying-form-templates-that-require-full-trust"></a><span data-ttu-id="f690a-119">完全な信頼を必要とするフォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="f690a-119">Deploying Form Templates That Require Full Trust</span></span>

<span data-ttu-id="f690a-p105">フォーム テンプレートのフォーム コードで完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーを使用している場合、またはフォーム テンプレートで完全な信頼を必要とする機能を使用している場合は、信頼できる発行元から発行されたコード署名用の証明書を使用して、フォーム テンプレート (.xsn) ファイルにデジタル署名する必要があります。ユーザーがフォームを開いたときに、この発行元を信頼するように求めるメッセージが表示されます。フォーム テンプレート ファイルにデジタル署名すると、フォームも完全に信頼され、フォーム コードに対して FullTrust アクセス許可が付与されます。</span><span class="sxs-lookup"><span data-stu-id="f690a-p105">If the form code for your form template does use InfoPath object model members that require full trust, or the form template uses features that require full trust, you must digitally sign your form template (.xsn) file with a code signing certificate from a trusted publisher, which your users will be prompted to trust when they open the form. This will also make your form fully-trusted, and in turn grant the FullTrust permission set to your form code.</span></span>
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a><span data-ttu-id="f690a-122">フォーム テンプレートをコンパイル、発行、およびデジタル署名する</span><span class="sxs-lookup"><span data-stu-id="f690a-122">Compile, publish, and digitally sign a form template</span></span>

1. <span data-ttu-id="f690a-123">Visual Studio 2012 でフォーム テンプレートを作成してデバッグします。</span><span class="sxs-lookup"><span data-stu-id="f690a-123">Create and debug your form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="f690a-124">Visual Studio 2012 コード エディターで作業している場合は、InfoPath に切り替えて、[ **ファイル**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f690a-124">If you are working in the Visual Studio 2012 code editor, switch to InfoPath, click the **File** tab, and then click **Form Options**.</span></span>
    
3. <span data-ttu-id="f690a-125">[ **セキュリティと信頼**] カテゴリをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f690a-125">Click the **Security and Trust** category.</span></span> 
    
4. <span data-ttu-id="f690a-126">[ **セキュリティ レベル**] で、[ **自動的にセキュリティ レベルを設定する**] チェック ボックスをオフにして、[ **完全信頼**] をオンにします。</span><span class="sxs-lookup"><span data-stu-id="f690a-126">Under **Security Level**, clear the **Automatically determine security level** check box, and then select **Full Trust**.</span></span>
    
5. <span data-ttu-id="f690a-127">[ **フォーム テンプレートの署名**] で、[ **このフォーム テンプレートに署名する**] チェック ボックスをオンにして、[ **証明書の選択**] をクリックし、フォーム テンプレートへの署名に使用するコード署名用の証明書を指定します。</span><span class="sxs-lookup"><span data-stu-id="f690a-127">Under **Form Template Signature**, select **Sign this form template**, click **Select Certificate**, and then specify the code signing certificate with which to sign the form template.</span></span>
    
6. <span data-ttu-id="f690a-128">[ **OK**] を 2 回クリックして [ **フォームのオプション**] ダイアログ ボックスを閉じ、変更内容を保存します。</span><span class="sxs-lookup"><span data-stu-id="f690a-128">Click **OK** twice to close the **Form Options** dialog box, and then save your changes.</span></span> 
    
7. <span data-ttu-id="f690a-129">[ **発行**] タブをクリックし、目的の発行場所のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f690a-129">Click the **Publish** tab, and then click the button for the desired publishing location.</span></span> 
    
8. <span data-ttu-id="f690a-130">フォーム テンプレートがコンパイルされ、**発行ウィザード**が開始されます。</span><span class="sxs-lookup"><span data-stu-id="f690a-130">The form template is compiled and the **Publishing Wizard** is launched.</span></span> <span data-ttu-id="f690a-131">**発行ウィザード**の手順に従って、フォーム テンプレートを展開します。</span><span class="sxs-lookup"><span data-stu-id="f690a-131">Follow the steps in the **Publishing Wizard** to deploy your form to the location of your choice.</span></span> <span data-ttu-id="f690a-132">**発行ウィザード**を使用して、完全な信頼を必要とするフォーム テンプレートを展開する方法の詳細については、InfoPath のヘルプで「完全信頼のフォーム テンプレートを発行する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f690a-132">The form template is compiled and the **Publishing Wizard** is launched. Follow the steps in the Publishing Wizard to deploy your form template. For more information about using the Publishing Wizard to deploy a form template that requires full trust, search InfoPath Help for "Publish a form template with full trust".</span></span> 
    
 <span data-ttu-id="f690a-133">**メモ**</span><span class="sxs-lookup"><span data-stu-id="f690a-133">**Notes**</span></span>
- <span data-ttu-id="f690a-p107">フォームにデジタル署名するには、認証されたコード署名用の証明書がコンピューターにインストールされている必要があります。この証明書を取得するには、認証機関またはネットワーク管理者に問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="f690a-p107">To digitally sign a form, you must have an authenticated code signing certificate installed on your computer. To acquire such a certificate, you must contact a certification authority or your network administrator.</span></span>
    
- <span data-ttu-id="f690a-136">発行後にフォームを変更する必要がある場合は、この手順を繰り返して、フォーム テンプレートをもう一度署名する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f690a-136">If you need to make changes to the form after publishing, you must repeat the procedure and re-sign the form template.</span></span> <span data-ttu-id="f690a-137">これは、フォームを変更するとデジタル署名が無効になるためです。</span><span class="sxs-lookup"><span data-stu-id="f690a-137">This is because altering the form invalidates the digital signature.</span></span> <span data-ttu-id="f690a-138">完全信頼のアクセス許可を必要とするフォームを開発するときには、「[完全信頼が必要なフォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-form-templates-that-require-full-trust.md)」で説明している手順に従って、ローカル コンピューター上のフォーム テンプレートを登録できます。</span><span class="sxs-lookup"><span data-stu-id="f690a-138">During the development of a form that requires full trust permissions you can use the procedure described in [How to: Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md) to register the form template on your local computer.</span></span> 
    
## <a name="configuring-net-framework-security-settings"></a><span data-ttu-id="f690a-139">.NET Framework のセキュリティ設定を構成する</span><span class="sxs-lookup"><span data-stu-id="f690a-139">Configuring .NET Framework Security Settings</span></span>

<span data-ttu-id="f690a-140">InfoPath マネージ コード フォーム テンプレートで実行されるマネージ コードに付与するアクセス許可をさらに細かく制御するには, .NET Framework 2.0 Configuration ユーティリティを使用して、フォーム コードに特定のアクセス許可を付与します。</span><span class="sxs-lookup"><span data-stu-id="f690a-140">For additional control over the permissions granted to managed code running in an InfoPath managed code form template, you can use the .NET Framework 2.0 Configuration utility to grant a particular permission set to your form code.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f690a-p109">InfoPath マネージ コード フォーム テンプレートについて .NET Framework セキュリティ設定を構成しても、完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーが実行を許可されるかどうかには影響しません。完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーに対する呼び出しを有効にするには、このトピックで既に説明したように、フォーム テンプレートにデジタル署名するか、フォーム テンプレートを登録する必要があります。.NET Framework セキュリティ設定の構成は、InfoPath オブジェクト モデル以外の, .NET Framework クラスおよびマネージ コンポーネントのメンバーにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f690a-p109">Configuring .NET Framework security settings for an InfoPath managed code form template does not affect whether InfoPath object model members that require full trust are allowed to run. You must either digitally sign or register a form template as described earlier in this topic to enable calls to InfoPath object model members that require full trust. Configuring .NET Framework security settings apply only to calls to members of .NET Framework classes and managed components other than the InfoPath object model.</span></span> 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a><span data-ttu-id="f690a-144">フォーム テンプレートをコンパイル、発行、およびフォーム テンプレートの .NET セキュリティ設定を構成する</span><span class="sxs-lookup"><span data-stu-id="f690a-144">Compile, publish, and configure .NET security settings for a form template</span></span>

1. <span data-ttu-id="f690a-145">Visual Studio 2012 でフォーム テンプレートを作成してデバッグします。</span><span class="sxs-lookup"><span data-stu-id="f690a-145">Create and debug your form template in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="f690a-146">Visual Studio 2012 コード エディターで作業している場合は、InfoPath に切り替えて、[ **ファイル**] タブをクリックし、[ **発行**] をクリックして、目的の発行場所のボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="f690a-146">If you are working in the Visual Studio 2012 code editor, switch to InfoPath, click the **File** tab, click **Publish**, and then click the button for the desired publishing location.</span></span>
    
    <span data-ttu-id="f690a-147">フォーム テンプレートがコンパイルされ、**発行ウィザード**が開始されます。</span><span class="sxs-lookup"><span data-stu-id="f690a-147">The form template is compiled and the **Publishing Wizard** is launched.</span></span> <span data-ttu-id="f690a-148">**発行ウィザード**の手順に従って、フォーム テンプレートを展開します。</span><span class="sxs-lookup"><span data-stu-id="f690a-148">Follow the steps in the **Publishing Wizard** to deploy your form to the location of your choice.</span></span> <span data-ttu-id="f690a-149">**発行ウィザード**を使用する方法の詳細については、InfoPath のヘルプで「フォーム テンプレートを発行する」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f690a-149">For more information about using the **Publishing Wizard**, search InfoPath Help for "Publish a form template".</span></span>
    
3. <span data-ttu-id="f690a-150">「[コードを含むフォーム テンプレートのセキュリティ設定を構成する](how-to-configure-security-settings-for-form-templates-with-code.md)」の「特定の URL または UNC にあるフォームに FullTrust を割り当てる」で説明している手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="f690a-150">Perform the procedure described in the "Assigning FullTrust to Forms at a Specific URL or UNC" section of the [How to: Configure Security Settings for Form Templates with Code](how-to-configure-security-settings-for-form-templates-with-code.md)</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f690a-151">関連項目</span><span class="sxs-lookup"><span data-stu-id="f690a-151">See also</span></span>

#### <a name="tasks"></a><span data-ttu-id="f690a-152">タスク</span><span class="sxs-lookup"><span data-stu-id="f690a-152">Tasks</span></span>

[<span data-ttu-id="f690a-153">コードを含むフォーム テンプレートのセキュリティ設定を構成する</span><span class="sxs-lookup"><span data-stu-id="f690a-153">How to: Configure Security Settings for Form Templates with Code</span></span>](how-to-configure-security-settings-for-form-templates-with-code.md)


[<span data-ttu-id="f690a-154">コードを含むフォーム テンプレートのためのセキュリティ モデルについて</span><span class="sxs-lookup"><span data-stu-id="f690a-154">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)
  
[<span data-ttu-id="f690a-155">完全信頼が必要なフォーム テンプレートをプレビューおよびデバッグする</span><span class="sxs-lookup"><span data-stu-id="f690a-155">How to: Preview and Debug Form Templates that Require Full Trust</span></span>](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

