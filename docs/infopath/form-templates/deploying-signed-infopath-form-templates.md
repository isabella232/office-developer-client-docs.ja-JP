---
title: 署名済み InfoPath フォーム テンプレートを展開する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: このトピックを読む前に、「InfoPath フォームの追加のセキュリティ概念」の「署名済みフォーム テンプレート」セクションを読んで、署名済みフォーム テンプレートのセキュリティについて理解しておく必要があります。「セキュリティ レベル、電子メール配信、リモート フォーム テンプレート」の説明も関連性があります。
ms.openlocfilehash: 76cc6dfdbd2c01827182c348281a98ad7cd17b69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303718"
---
# <a name="deploying-signed-infopath-form-templates"></a><span data-ttu-id="474a6-104">署名済み InfoPath フォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="474a6-104">Deploying Signed InfoPath Form Templates</span></span>

<span data-ttu-id="474a6-p102">このトピックを読む前に、「[InfoPath フォームの追加のセキュリティ概念](additional-infopath-form-security-concepts.md)」の「署名済みフォーム テンプレート」セクションを読んで、署名済みフォーム テンプレートのセキュリティについて理解しておく必要があります。「[セキュリティ レベル、電子メール配信、リモート フォーム テンプレート](security-levels-email-deployment-and-remote-form-templates.md)」の説明も関連性があります。</span><span class="sxs-lookup"><span data-stu-id="474a6-p102">Before reading this topic, see the "Signed Form Templates" section in [Additional InfoPath Form Security Concepts](additional-infopath-form-security-concepts.md) for an understanding of signed form template security. Information and discussions in the [Security Levels, E-Mail Deployment, and Remote Form Templates](security-levels-email-deployment-and-remote-form-templates.md) topic are also relevant.</span></span> 
  
## <a name="digitally-signing-a-form-template"></a><span data-ttu-id="474a6-107">フォーム テンプレートにデジタル署名する</span><span class="sxs-lookup"><span data-stu-id="474a6-107">Digitally Signing a Form Template</span></span>

<span data-ttu-id="474a6-108">フォーム テンプレートにデジタル署名する場合、そのフォーム テンプレートのセキュリティ レベルを [完全信頼] に設定できます。完全信頼のセキュリティ レベルとは、フォームから、ユーザーのコンピューター上や別のドメインにあるファイルと設定にアクセスできることを意味します。</span><span class="sxs-lookup"><span data-stu-id="474a6-108">If you digitally sign a form template, you can set the security level for the form template to Full Trust, which means the form can access files and settings on the user's computer or on a different domain.</span></span> <span data-ttu-id="474a6-109">(フォーム テンプレートにデジタル署名すると、他のセキュリティ レベルを使用できなくなるというわけではありません。</span><span class="sxs-lookup"><span data-stu-id="474a6-109">(Also, digitally signing a form template does not prevent you from using other security levels, if you prefer.</span></span> <span data-ttu-id="474a6-110">必要に応じて、署名付きフォーム テンプレートのセキュリティ レベルを [ドメイン] や [制限付き] に設定することもできます)。さらに、電子メール プログラムを使用しているユーザー対して署名付きフォーム テンプレートを展開した上で、そのユーザーへの電子メール メッセージの添付ファイルとしてフォーム テンプレートの更新バージョンを送信することで、署名付きフォーム テンプレートを自動的に更新することもできます。それには、以下の手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="474a6-110">You set the security level of a signed form template to the Domain or Restricted security level.) In addition, you can deploy the signed form template to users who are using an email program and then later automatically update the signed form template by sending the updated version to the users as an attachment to an email message, follow these steps:</span></span>
  
### <a name="to-digitally-sign-a-form-template"></a><span data-ttu-id="474a6-111">フォーム テンプレートにデジタル署名するには</span><span class="sxs-lookup"><span data-stu-id="474a6-111">To digitally sign a form template</span></span>

1. <span data-ttu-id="474a6-112">InfoPath デザイナーで、[ **ファイル**] タブをクリックし、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474a6-112">In the InfoPath designer, click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
2. <span data-ttu-id="474a6-113">[ **フォームのオプション**] ダイアログ ボックスの [ **セキュリティと信頼**] カテゴリをクリックします。</span><span class="sxs-lookup"><span data-stu-id="474a6-113">In the **Form Options** dialog box, click the **Security and Trust** category.</span></span> 
    
3. <span data-ttu-id="474a6-114">[ **フォーム テンプレートの署名**] の [ **このフォーム テンプレートに署名する**] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="474a6-114">Under **Form Template Signature**, select the **Sign this form template** check box.</span></span> 
    
4. <span data-ttu-id="474a6-115">[ **証明書の選択**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474a6-115">Click **Select Certificate**.</span></span>
    
5. <span data-ttu-id="474a6-116">[ **証明書の選択**] ダイアログ ボックスで、フォームのデジタル署名に使用する証明書をクリックします。</span><span class="sxs-lookup"><span data-stu-id="474a6-116">In the **Select Certificate** dialog box, click the certificate that you want to use to digitally sign the form.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="474a6-p104">[ **フォームのオプション**] ダイアログ ボックスの [ **証明書の作成**] ボタンを使用すると、フォーム テンプレートに署名するテスト証明書を生成できます。テスト証明書は、テスト目的に限りフォーム テンプレートの署名に使用できます。テスト証明書は公式に配布するフォーム テンプレートの署名には使用しないでください。この証明書は、ルート証明書が既にユーザーのコンピューターで信頼されている証明機関が発行した証明書ではないので、テスト証明書はユーザーのコンピューターで正しく検証されません。テスト証明書を使用して署名済みフォーム テンプレートを展開すると、そのフォーム テンプレートのユーザーは、テンプレートを開くことができません。</span><span class="sxs-lookup"><span data-stu-id="474a6-p104">The **Create Certificate** button in the **Form Options** dialog box can be used to generate a test certificate to sign a form template. The test certificate should be used to sign form templates for testing only. Test certificates should not be used to sign form templates that will be distributed publicly. Because the certificates are not issued by a Certificate Authority whose root certificate is already trusted on a user's computer, the test certificate will not validate correctly on the user's computer. If you deploy a form template signed with a test certificate, users of your form template will most likely be unable to open it.</span></span> 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a><span data-ttu-id="474a6-122">信頼されたルート証明書と発行元を確立する</span><span class="sxs-lookup"><span data-stu-id="474a6-122">Establishing a Trusted Root Certificate and Publisher</span></span>

 <span data-ttu-id="474a6-p105">フォーム テンプレートの署名に使用される証明書の信頼されたルート証明書は、クライアント コンピューターの信頼されたルート証明書ストアにある必要があります。そうでない場合、フォーム テンプレートの発行元を検証できず、フォーム テンプレートのユーザーには発行元を信頼するオプションが与えられません。信頼されたルート証明書が信頼されたルート証明書ストアにあるが、発行元が信頼された発行元リストにない場合、ユーザーにはプロンプトが表示され、フォーム テンプレートの発行元を信頼するオプションが与えられます。</span><span class="sxs-lookup"><span data-stu-id="474a6-p105">The trusted root certificate of the certificate that is used to sign the form template must be in the trusted root certificate store on the client computer. If not, the publisher of the form template cannot be verified, and users of your form template will not be given the option to trust the publisher. If the trusted root certificate is in the trusted root certificate store, but the publisher is not in the trusted publisher list, users are prompted and given the option to trust the publisher of the form template.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="474a6-p106">署名済みフォーム テンプレートがドメイン アクセスまたは制限付きアクセスを要求する場合、InfoPath は署名を使用して、フォーム テンプレートが署名後に改ざんされていないこと、およびフォーム テンプレートを自動的に更新できることを確認します。</span><span class="sxs-lookup"><span data-stu-id="474a6-p106">If a signed form template requests Domain or Restricted access, InfoPath will use the signature to verify that the form template was not tampered with after it was signed. InfoPath also uses the signature to determine whether the form template can be updated automatically.</span></span> 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a><span data-ttu-id="474a6-128">完全信頼アクセスを使用して署名済みフォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="474a6-128">Deploying Signed Form Templates with Full Trust Access</span></span>

<span data-ttu-id="474a6-p107">署名済みフォーム テンプレートを展開する主なシナリオは、自動更新など、ドメインのような機能を完全信頼フォームに展開することです。完全信頼を要求する署名済みフォーム テンプレートには、 *完全に信頼できるフォーム*  と同じ、システム リソースへのアクセス権があります。完全に信頼できるフォームの動作と、それらの作成および展開方法の詳細については、「 [完全に信頼できるフォームを理解する](understanding-fully-trusted-forms.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="474a6-p107">The primary scenario for deploying signed form templates is to enable domain-like functionality, such as automatic update, in full-trust forms. A signed form template requesting full-trust access has the same access to system resources as a  *fully trusted form*  . For a detailed discussion of how fully trusted forms work and how to create and deploy them, see [Understanding Fully Trusted Forms](understanding-fully-trusted-forms.md).</span></span>
  
<span data-ttu-id="474a6-p108">ただし、組織のコンピューター環境によっては、署名済みフォーム テンプレートまたは完全に信頼できるフォームのどちらか一方の使用が必要になることもあります。たとえば、登録済みの完全に信頼できるフォームではなく、完全信頼アクセスを要求する署名済みフォーム テンプレートを使用することには利点があります。完全信頼アクセスを要求する署名済みフォーム テンプレートには、次のような利点があります。</span><span class="sxs-lookup"><span data-stu-id="474a6-p108">However, depending on your organization's computing environment, you might prefer to use either signed form templates or fully trusted forms. For example, there are benefits to using a signed form template that requests full-trust access instead of a registered, fully trusted form. A signed form template requesting full-trust access has the following benefits:</span></span>
  
- <span data-ttu-id="474a6-135">署名されていない完全に信頼できるフォーム テンプレートとは異なり、登録されている必要はありません。</span><span class="sxs-lookup"><span data-stu-id="474a6-135">Does not have to be registered, unlike an unsigned, fully trusted form template.</span></span>
    
- <span data-ttu-id="474a6-136">フォーム テンプレートの自動サイレント更新が有効になります。</span><span class="sxs-lookup"><span data-stu-id="474a6-136">Enables silent automatic update of the form template.</span></span>
    
<span data-ttu-id="474a6-p109">完全信頼アクセスを要求する署名済みフォーム テンプレートを登録する必要はないので、インストーラー パッケージまたはスクリプト ファイルを使用して展開する必要はありません。この利点により、完全信頼フォーム テンプレートの展開が大幅に簡略化されます。</span><span class="sxs-lookup"><span data-stu-id="474a6-p109">Because you do not have to register a signed form template that requests full-trust access, you do not have to use an installer package or script file to deploy it. This benefit greatly simplifies the deployment of a full-trust form template.</span></span>
  
<span data-ttu-id="474a6-p110">完全信頼アクセスを要求する署名済みフォーム テンプレートを更新するときは、更新されたテンプレートをユーザーに送信するか、または共有された場所で更新するだけで済みます。更新されたテンプレートをユーザーが開くときにプロンプトは表示されず、ユーザーのコンピューター上で、更新されたバージョンが確認なしで古いコピーに上書きされます。共有された場所でテンプレートを更新した場合、ユーザーは、プロンプトが表示されることなく、更新されたコピーを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="474a6-p110">When you update your signed form template that requests full-trust access, you can just send the updated template to the user or update it in a shared location. When the user opens the updated template, the user will not be prompted, and the updated version will silently overwrite the older copy on the user's computer. If you updated the template in a shared location, the user will be able to use the updated copy without being prompted.</span></span>
  
<span data-ttu-id="474a6-p111">署名されていない完全に信頼できるフォームを更新する場合は、フォームを再パッケージ化して再登録する必要があります。さらに、インストールされている既存の完全に信頼できるフォーム テンプレートは、ローカル コンピューターのパスのみに対して動作し、ネットワーク パスに対しては動作しません。これは、登録プロセスが、ローカル コンピューター パスからネットワーク パスへの変更をサポートしていないためです。ただし、フォーム テンプレートの署名には証明書が必要なので、証明書を購入しない場合は、完全に信頼できる登録済みフォーム テンプレートを展開することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="474a6-p111">If you want to update an unsigned, fully trusted form, you must repackage your form and re-register it. Additionally, an existing, installed fully trusted form template works only for the path of the local computer but does not work for a network path, because the registration process does not support changing a local computer path to a network path. However, because a certificate is needed to sign a form template, you may prefer to deploy fully trusted, registered form templates, if you do not want to purchase a certificate.</span></span>
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a><span data-ttu-id="474a6-145">ドメインまたは制限付きアクセスを使用して署名済みフォーム テンプレートを展開する</span><span class="sxs-lookup"><span data-stu-id="474a6-145">Deploying Signed Form Templates with Domain or Restricted Access</span></span>

<span data-ttu-id="474a6-p112">[ドメイン] または [制限付き] セキュリティ レベルを使用する署名済みフォーム テンプレートには、自動更新機能という利点もあります。たとえば、署名済みフォーム テンプレートを、Microsoft SharePoint Foundation を実行しているサーバー、または [ドメイン] セキュリティ レベルを持つサーバーのドキュメント ライブラリに発行することができます。共有された場所でフォーム テンプレートを更新すると、ユーザーは更新されたコピーを自動的に取得します。</span><span class="sxs-lookup"><span data-stu-id="474a6-p112">A signed form template that has a Domain or Restricted security level also has the advantage of the automatic update functionality. For example, you could publish a signed form template to a document library on a server that is running Microsoft SharePoint Foundation or on a server that has a Domain security level. When you update your form template in the shared location, users will get the updated copy automatically.</span></span>
  

