---
title: コードを含むフォームを発行する
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: サイト コレクション管理者はだれでも、InfoPath Designer の発行ウィザードから直接、SharePoint 上のフォーム ライブラリに、コードを含むフォームを発行できます。コードはセキュリティ保護されたサンドボックス環境の中で実行されるので、悪意のあるコードがサーバーに害を与えることはありません。このことを、サンドボックス ソリューションの発行、またはSharePoint サンドボックス インフラストラクチャへの発行と呼びます。
ms.openlocfilehash: f8f8a48ea6810b5331198f6ddc112b3bd38ab886
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428327"
---
# <a name="publishing-forms-with-code"></a><span data-ttu-id="b38b1-105">コードを含むフォームを発行する</span><span class="sxs-lookup"><span data-stu-id="b38b1-105">Publishing Forms with Code</span></span>

<span data-ttu-id="b38b1-p102">サイト コレクション管理者はだれでも、InfoPath Designer の発行ウィザードから直接、SharePoint 上のフォーム ライブラリに、コードを含むフォームを発行できます。コードはセキュリティ保護された "サンドボックス" 環境の中で実行されるので、悪意のあるコードがサーバーに害を与えることはありません。このことを、"サンドボックス ソリューションの発行"、または "SharePoint サンドボックス インフラストラクチャへの発行" と呼びます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-p102">Any site collection administrator can publish forms with code directly from the InfoPath Designer publishing wizard to a form library on SharePoint. The code is executed in a sandboxed environment so that malicious code cannot harm the server. This is referred to as publishing a sandboxed solution or publishing to the SharePoint sandbox infrastructure.</span></span>
  
<span data-ttu-id="b38b1-p103">InfoPath 2010 および SharePoint Server 2010 では管理者展開用のソリューションもサポートされています。フォーム設計者がローカル ストアにコードを含むフォームを発行し、後で SharePoint ファーム管理者がそれらのフォームを確認しアップロードします。コードには完全信頼が付与されます。また、昇格された特権を必要とするファイル IO などの機能をコードに組み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-p103">InfoPath 2010 and SharePoint Server 2010 also support administrator-deployed solutions. A form designer publishes forms with code to a local store which are later reviewed and uploaded by a SharePoint farm administrator. The code is given full trust, and can incorporate functionality requiring elevated privileges such as file IO.</span></span>
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a><span data-ttu-id="b38b1-112">サンドボックス ソリューションと管理者が承認したソリューションの比較</span><span class="sxs-lookup"><span data-stu-id="b38b1-112">Comparing Sandboxed and Administrator-approved Solutions</span></span>

<span data-ttu-id="b38b1-113">次の表は、サンドボックス ソリューションと管理者が承認したソリューションの違いをまとめたものです。</span><span class="sxs-lookup"><span data-stu-id="b38b1-113">The following table summarizes the differences between publishing sandboxed and administrator-approved solutions.</span></span> 
  
||<span data-ttu-id="b38b1-114">**サンドボックス ソリューション**</span><span class="sxs-lookup"><span data-stu-id="b38b1-114">**Sandboxed Solutions**</span></span>|<span data-ttu-id="b38b1-115">**管理者が承認したソリューション**</span><span class="sxs-lookup"><span data-stu-id="b38b1-115">**Administrator-approved Solutions**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b38b1-116">**必要な権限**</span><span class="sxs-lookup"><span data-stu-id="b38b1-116">**Permissions Required**</span></span> <br/> |<span data-ttu-id="b38b1-117">サイト コレクション管理者ならだれでも発行できます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-117">Can be published by any site collection administrator.</span></span>  <br/> |<span data-ttu-id="b38b1-118">ファーム管理者が展開できます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-118">Can be deployed by a farm administrator.</span></span>  <br/> |
|<span data-ttu-id="b38b1-119">**Publishing**</span><span class="sxs-lookup"><span data-stu-id="b38b1-119">**Publishing**</span></span> <br/> |<span data-ttu-id="b38b1-120">InfoPath から直接発行できます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-120">Can be published directly from InfoPath.</span></span>  <br/> |<span data-ttu-id="b38b1-121">サーバーの全体管理または stsadm コマンドライン ツールを使用して展開できます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-121">Can be deployed using Central Administration or the stsadm command-line tool.</span></span>  <br/> |
|<span data-ttu-id="b38b1-122">**保護**</span><span class="sxs-lookup"><span data-stu-id="b38b1-122">**Protection**</span></span> <br/> |<span data-ttu-id="b38b1-p104">コードはサンドボックス環境の中で実行されます。そのため、サーバーを悪意のあるコードから守るのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-p104">Code is run in a sandboxed environment. This helps protect the server from malicious code.</span></span>  <br/> |<span data-ttu-id="b38b1-125">コードを完全信頼で実行でき、コードからサーバー上の任意のリソースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-125">Code can run with full trust and access any resource on the server.</span></span>  <br/> |
|<span data-ttu-id="b38b1-126">**推奨される用途**</span><span class="sxs-lookup"><span data-stu-id="b38b1-126">**Recommended Use**</span></span> <br/> |<span data-ttu-id="b38b1-127">少数のコードしか必要としないフォーム。</span><span class="sxs-lookup"><span data-stu-id="b38b1-127">Forms that only require a small amount of code.</span></span>  <br/> |<span data-ttu-id="b38b1-128">多数のコード行が含まれているフォーム。</span><span class="sxs-lookup"><span data-stu-id="b38b1-128">Forms that contain many lines of code.</span></span>  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a><span data-ttu-id="b38b1-129">サンドボックス ソリューションとしてフォーム テンプレートを発行する</span><span class="sxs-lookup"><span data-stu-id="b38b1-129">Publishing Form Templates as Sandboxed Solutions</span></span>

<span data-ttu-id="b38b1-p105">コードを含むフォームをセキュリティで保護されたソリューションとして発行する場合も、他の任意のフォームをドキュメント ライブラリに発行する場合と違いはありません。通常どおり発行ウィザードを使用すれば、フォームがサーバーにアップロードされ、サンドボックス内で動作します。</span><span class="sxs-lookup"><span data-stu-id="b38b1-p105">Publishing a form with code as a sandboxed solution is no different from publishing any other form to a document library. Just use the publishing wizard as usual and your form will be uploaded to the server and will operate in the sandbox.</span></span>
  
<span data-ttu-id="b38b1-132">フォームをセキュリティで保護されたソリューションとして展開する場合、特定の制限事項があります。</span><span class="sxs-lookup"><span data-stu-id="b38b1-132">Note that there are certain restrictions to deploying your form as a sandboxed solution:</span></span>
  
- <span data-ttu-id="b38b1-133">InfoPath のフォームであることが必要です。</span><span class="sxs-lookup"><span data-stu-id="b38b1-133">Must be an InfoPath form.</span></span>
    
- <span data-ttu-id="b38b1-134">プログラム言語として C# または Visual Basic を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b38b1-134">Must use C# or Visual Basic as the programming language.</span></span>
    
- <span data-ttu-id="b38b1-135">電子メール データ接続への送信はできません。</span><span class="sxs-lookup"><span data-stu-id="b38b1-135">Cannot submit to email data connections.</span></span>
    
- <span data-ttu-id="b38b1-136">パーツ間の接続用にプロパティを昇格させることはできません。</span><span class="sxs-lookup"><span data-stu-id="b38b1-136">Cannot have properties promoted for part-to-part connections.</span></span>
    
- <span data-ttu-id="b38b1-137">マネージ メタデータ コントロールまたはデータ接続を持たせることはできません。</span><span class="sxs-lookup"><span data-stu-id="b38b1-137">Must not have any managed meta-data controls or data connections.</span></span>
    
<span data-ttu-id="b38b1-138">Microsoft SharePoint Server 2010 上、または Microsoft SharePoint Foundation 2010 を実行しているサーバー上で、サイト コレクション管理者がセキュリティで保護されたソリューションを使用できるようにするには、ファーム管理者が Windows SharePoint User Code サービスを開始する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b38b1-138">To enable site collection administrators to use sandboxed solutions on Microsoft SharePoint Server 2010 or a server that runs Microsoft SharePoint Foundation 2010, the farm administrator must start the Windows SharePoint User Code service.</span></span>
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a><span data-ttu-id="b38b1-139">Windows SharePoint User Code サービスを開始するには</span><span class="sxs-lookup"><span data-stu-id="b38b1-139">To start the Windows SharePoint User Code service</span></span>

1. <span data-ttu-id="b38b1-140">サーバーの全体管理 を開きます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-140">Open Central Administration.</span></span>
    
2. <span data-ttu-id="b38b1-141">[ **システム設定**] で、[ **サーバーのサービスの管理**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-141">Under **System Services**, click **Manage services on server**.</span></span>
    
3. <span data-ttu-id="b38b1-142">[ **Microsoft SharePoint Foundation User Code Service**] を開始します。</span><span class="sxs-lookup"><span data-stu-id="b38b1-142">Start the **Microsoft SharePoint Foundation User Code Service**.</span></span>
    
### <a name="to-publish-a-sandboxed-solution"></a><span data-ttu-id="b38b1-143">サンドボックス ソリューションを発行するには</span><span class="sxs-lookup"><span data-stu-id="b38b1-143">To publish a sandboxed solution</span></span>

1. <span data-ttu-id="b38b1-144">InfoPath デザイン モードでフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-144">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="b38b1-145">[ **ファイル**] タブをクリックし、Backstage の [ **発行**] タブで [ **SharePoint サーバー**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-145">Click the **File** tab, and then click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
    
3. <span data-ttu-id="b38b1-146">発行先の SharePoint サイトの URL を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-146">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="b38b1-147">このフォーム テンプレートをセキュリティで保護されたソリューションとして発行するためには、このサイトのサイト コレクション管理者である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b38b1-147">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
  
4. <span data-ttu-id="b38b1-148">[ **フォーム ライブラリ**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-148">Select **Form Library**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="b38b1-149">[ **新しいフォーム ライブラリを作成する**] をクリックし、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-149">Select **Create a new form library**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="b38b1-150">フォーム ライブラリの名前と説明を入力し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-150">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
    
7. <span data-ttu-id="b38b1-151">[ **発行**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-151">Click **Publish**.</span></span>
    
<span data-ttu-id="b38b1-152">セキュリティで保護されたソリューションとして発行するフォーム テンプレートに適したシナリオを紹介するソリューション例の詳細については、「[サンドボックス ソリューションのサンプル](sample-sandboxed-solutions.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b38b1-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a><span data-ttu-id="b38b1-153">管理者展開用のソリューションとしてフォーム テンプレートを発行する</span><span class="sxs-lookup"><span data-stu-id="b38b1-153">Publishing Form Templates as Administrator-Deployed Solutions</span></span>

<span data-ttu-id="b38b1-154">フォームにデータ接続が多数ある場合、完全信頼のセキュリティを必要とする場合、またはファーム規模のテンプレートを必要とする場合は、フォームを管理者が承認したテンプレートとして発行することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-154">Publishing your form as an administrator-approved template is recommended if your form has many data connections, if it requires full-trust security, or if you require a farm-wide template.</span></span>
  
<span data-ttu-id="b38b1-155">管理者展開用のソリューションを SharePoint 上で使用できるようにするには、あらかじめファーム管理者がいくつかの手順を実行しておく必要があり、管理者が利用する前に開発者がソリューションを準備しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="b38b1-155">There are several steps that a farm administrator must complete before an administrator-deployed solution is available on SharePoint, and you as the developer must prepare the solution before the administrator is engaged.</span></span>
  
<span data-ttu-id="b38b1-156">まず、フォームを完全信頼として展開する場合は、次の手順に従ってセキュリティ レベルを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b38b1-156">First, if your form is going to be deployed as full trust, you must set the security level as described in the following procedure.</span></span>
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a><span data-ttu-id="b38b1-157">フォーム テンプレートのセキュリティ レベルを完全信頼に設定するには</span><span class="sxs-lookup"><span data-stu-id="b38b1-157">To set the security level of a form template to full trust</span></span>

1. <span data-ttu-id="b38b1-158">InfoPath デザイン モードでフォーム テンプレートを開きます。</span><span class="sxs-lookup"><span data-stu-id="b38b1-158">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="b38b1-159">[ **ファイル**] タブをクリックし、[ **情報**] タブの [ **フォームのオプション**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-159">Click the **File** tab, on the **Info** tab click **Form Options**.</span></span>
    
3. <span data-ttu-id="b38b1-160">[ **セキュリティと信頼**] カテゴリをクリックし、[ **自動的にセキュリティ レベルを設定する**] チェック ボックスをオフにします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-160">Click the **Security and Trust** category, and then clear the **Automatically determine security level** check box.</span></span> 
    
4. <span data-ttu-id="b38b1-161">[ **完全信頼**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b38b1-161">Select **Full Trust**.</span></span>
    
<span data-ttu-id="b38b1-162">続いて、次の手順を実行してフォームを発行しますが、標準の発行手順とはいくつか異なる点があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b38b1-162">Then, publish the form by using the following procedure, but be aware that there are some differences from a standard publishing procedure.</span></span>
  
### <a name="to-publish-an-administrator-deployed-solution"></a><span data-ttu-id="b38b1-163">管理者展開用のソリューションを発行するには</span><span class="sxs-lookup"><span data-stu-id="b38b1-163">To publish an administrator-deployed solution</span></span>

1. <span data-ttu-id="b38b1-164">**発行ウィザード** の 1 ページ目で、SharePoint Server 2010 または SharePoint Foundation 2010 サイトの場所を指定し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-164">In the first page of the **Publishing Wizard**, specify the location of the SharePoint Server 2010 or SharePoint Foundation 2010 site, and then click **Next**.</span></span>
    
2. <span data-ttu-id="b38b1-p106">InfoPath によって、ウィザードの 2 ページ目の [ **管理者承認用フォーム テンプレート**] チェック ボックスが自動的にオンになります。[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b38b1-p106">InfoPath will automatically select the **Administrator-approved form template** check box on the second page of the wizard. Click **Next**.</span></span>
    
3. <span data-ttu-id="b38b1-p107">3 ページ目の内容は、管理者が展開するシナリオに固有のものになります。SharePoint Server を選択する代わりに、フォームをローカル ストアに発行します。SharePoint 管理者は、管理者の展開プロセス時にこの場所からファイルをアップロードすることになります。</span><span class="sxs-lookup"><span data-stu-id="b38b1-p107">The third page is unique to administrator-deployed scenarios. Instead of selecting a SharePoint Server, publish the form to a local store. The SharePoint administrator will upload the file from this location during the administrator deployment process.</span></span>
    
4. <span data-ttu-id="b38b1-170">**発行ウィザード** の残りのページを実行します。</span><span class="sxs-lookup"><span data-stu-id="b38b1-170">Complete the remaining pages of the **Publishing Wizard**.</span></span>
    

