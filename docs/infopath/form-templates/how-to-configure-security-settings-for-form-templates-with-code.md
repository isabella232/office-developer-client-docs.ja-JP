---
title: コードを含むフォーム テンプレートのセキュリティ設定を構成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- security policy deployment package [infopath 2007],URLs [InfoPath 2007], assigning FullTrust,code access security [InfoPath 2007],UNCs [InfoPath 2007], assigning FullTrust,CAS [InfoPath 2007],security [InfoPath 2007], configuring,code groups [InfoPath 2007],FullTrust [InfoPath 2007], assigning to UNCs,FullTrust [InfoPath 2007], assigning to URLs
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: .NET 構成スナップインを使用して、InfoPath マネージ コード フォーム テンプレートに適用されるアクセス許可セットをカスタマイズできます。
ms.openlocfilehash: f04ce71875eac7695d2900131ca7c9cd333fa90f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799128"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="3d554-104">コードを含むフォーム テンプレートのセキュリティ設定を構成する</span><span class="sxs-lookup"><span data-stu-id="3d554-104">How to: Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="3d554-105">.NET 構成スナップインを使用して、InfoPath マネージ コード フォーム テンプレートに適用されるアクセス許可セットをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="3d554-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="3d554-106">InfoPath でホストされている共通言語ランタイム (CLR) は、All_Code グループ内の *InfoPath フォーム テンプレート*という名前の事前定義コード グループを検索します。</span><span class="sxs-lookup"><span data-stu-id="3d554-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="3d554-107">CLR は、そのグループで定義されているアクセス許可セットを、フォーム コードが実行されるアプリケーション ドメイン (AppDomain) に適用します。</span><span class="sxs-lookup"><span data-stu-id="3d554-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="3d554-108">これにより、InfoPath マネージ コード フォーム テンプレートに付与されるアクセス許可セットをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="3d554-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="3d554-109">たとえば、http://MySite からダウンロードしたフォーム テンプレートに、Active Directory へのアクセス許可を付与できます。</span><span class="sxs-lookup"><span data-stu-id="3d554-109">For example, you can grant a form template downloaded from http://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="3d554-110">.NET 構成スナップインで定義したカスタム セキュリティ ポリシーを適用するには、フォーム テンプレートが実行されるすべてのクライアント コンピューター上にポリシーを配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d554-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="3d554-111">InfoPath マネージ コード フォーム テンプレートのセキュリティ モデルの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d554-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="3d554-112">InfoPath フォーム テンプレートのコード グループを作成する</span><span class="sxs-lookup"><span data-stu-id="3d554-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="3d554-p102">次の手順では、InfoPath マネージ コード フォーム テンプレートにアクセス許可を付与しないコード グループを作成します (ローカル コンピューターにインストールまたは登録されているフォーム テンプレートを除く)。このコード グループの下で、特定の URL または UNC にある InfoPath フォーム テンプレートにアクセス許可セットを割り当てることができます。 `InfoPath Form Templates` コード グループ内にコード グループを作成し、アクセス許可セットを割り当てる方法については、次の手順を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d554-p102">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs. For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3d554-115">Microsoft .NET Framework 1.1 再頒布可能パッケージと共にインストールされる **Microsoft .NET Framework 1.1 構成** ツールと異なり、 **Microsoft .NET Framework 2.0 Configuration** は Microsoft .NET Framework 2.0 Software Development Kit (SDK) をインストールしなければインストールされません。</span><span class="sxs-lookup"><span data-stu-id="3d554-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="3d554-116">InfoPath マネージ コード フォームのカスタム セキュリティ コード グループを作成するには</span><span class="sxs-lookup"><span data-stu-id="3d554-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="3d554-117">[ **スタート**] メニューの [ **管理ツール**] をポイントし、[ **Microsoft .NET Framework 2.0 Configuration**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="3d554-118">[ **スタート**] メニューに [ **管理ツール**] が表示されない場合は、[ **コントロール パネル**] から [ **管理ツール**] を開き、[ **Microsoft .NET Framework 2.0 Configuration**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="3d554-119">[ **マイ コンピューター**] の下の [ **ランタイム セキュリティ ポリシー**] ノードを展開し、[ **コンピューター (Machine)**] ノードを展開します。次に、[ **コード グループ**] ノードを展開し、[ **All_Code**] ノードを展開します。[ **All_Code**] ノードを右クリックし、[ **新規作成**] をクリックして [ **コード グループの作成**] ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="3d554-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="3d554-120">新しいコード グループに  `InfoPath Form Templates` という名前を付けて (このとおりの名前を正確に入力する必要があります)、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="3d554-121">コード グループの条件の種類を [ **すべてのコード**] に設定し、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="3d554-122">[ **既存のアクセス許可セットを使用**] をクリックし、コード グループに [ **Nothing**] アクセス許可セットを割り当てます。[ **次へ**] をクリックし、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="3d554-123">新しい設定を適用するには、InfoPath を閉じて再起動します。</span><span class="sxs-lookup"><span data-stu-id="3d554-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="3d554-124">必要に応じて、 **InfoPath Form Templates** コード グループに [ **Nothing**] 以外のアクセス許可セットを割り当て、すべての InfoPath マネージ コード フォーム テンプレートのアクセス許可セットを管理することができます。</span><span class="sxs-lookup"><span data-stu-id="3d554-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="3d554-p103">[ **.NET Configuration 2.0**] スナップインで、グループを右クリックして [ **プロパティ**] をクリックし、[ **アクセス許可セット**] タブをクリックすることにより、セキュリティ コード グループのアクセス許可セットをいつでも変更できます。</span><span class="sxs-lookup"><span data-stu-id="3d554-p103">You can change the permission set for a security code group at any time by right-clicking the group in the . **NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="3d554-127">特定の URL または UNC にあるフォームに FullTrust を割り当てる</span><span class="sxs-lookup"><span data-stu-id="3d554-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="3d554-p104">**InfoPath Form Templates** グループの下にコード グループを作成し、特定の URL または UNC の場所からのフォーム テンプレートに完全信頼のアクセス許可セットを付与することができます。その後は、指定した場所に発行されるすべてのフォーム テンプレートが完全に信頼されて実行されます。</span><span class="sxs-lookup"><span data-stu-id="3d554-p104">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location. After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3d554-130">ローカル コンピューターから読み込んだフォーム テンプレート (My Computer Zone コード グループ) が、InfoPath によりランダムな URL を使用して読み込まれます。</span><span class="sxs-lookup"><span data-stu-id="3d554-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="3d554-131">このため、次の手順を使用してこのようなフォーム テンプレートに FullTrust アクセス許可を付与することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d554-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="3d554-132">ローカルにインストールされたフォーム テンプレートに FullTrust アクセス許可セットを付与するには、「[コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)」の「完全な信頼を必要とするフォーム テンプレートを展開する」に記載されているいずれかの手順を使用します。</span><span class="sxs-lookup"><span data-stu-id="3d554-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [How to: Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="3d554-133">特定の URL または UNC の場所にある InfoPath フォームに FullTrust を割り当てるには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="3d554-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="3d554-134">[ **スタート**] メニューの [ **管理ツール**] をポイントし、[ **Microsoft .NET Framework 2.0 Configuration**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="3d554-135">[ **スタート**] メニューに [ **管理ツール**] が表示されない場合は、[ **コントロール パネル**] から [ **管理ツール**] を開き、[ **Microsoft .NET Framework 2.0 Configuration**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="3d554-136">[ **マイ コンピューター**] の下の [ **ランタイム セキュリティ ポリシー**] ノードを展開し、[ **コンピューター (Machine)**] ノードを展開します。次に、[ **コード グループ**] ノードを展開し、[ **All_Code**] ノードを展開します。次に、[ **InfoPath Form Templates**] ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="3d554-137">右側のペインの [ **タスク**] ボックスの一覧で、[ **子コード グループを追加**] をクリックし、コード グループに名前を付けて、[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="3d554-138">[ **このコード グループの条件の種類を選択します**] ボックスの一覧で [ **URL**] を選択し、[ **FullTrust**] アクセス許可セットを付与する InfoPath マネージ コード フォーム テンプレートの場所の URL または UNC を入力します。</span><span class="sxs-lookup"><span data-stu-id="3d554-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="3d554-p106">アクセス許可セットを 1 つのフォーム テンプレートに制限する場合は、その特定のフォーム テンプレートの完全パスを指定します。たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3d554-p106">To restrict the permission set to a single form template, specify the full path of that particular form template. For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `http://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="3d554-p107">単一の URL または UNC を使用してすべてのフォーム テンプレートにアクセス許可セットを付与するには、テンプレート名を省略し、URL または UNC の末尾にアスタリスク (\*) を追加します。たとえば、次のように入力します。</span><span class="sxs-lookup"><span data-stu-id="3d554-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `http://MySite/MySubsite/*`
    
5. <span data-ttu-id="3d554-143">[ **次へ**] をクリックします。次に、[ **既存のアクセス許可セットを使用**] をクリックし、コード グループに [ **FullTrust**] アクセス許可セットを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="3d554-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="3d554-144">[ **次へ**] をクリックし、[ **完了**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="3d554-145">新しい設定を適用するには、InfoPath を閉じて再起動します。</span><span class="sxs-lookup"><span data-stu-id="3d554-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="3d554-146">より制限の厳しいアクセス許可セットや、独自のアクセス許可セットを適用するには、手順 4. で [ **FullTrust**] の代わりに適切なオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d554-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="3d554-147">InfoPath セキュリティ ポリシーの配置パッケージを作成する</span><span class="sxs-lookup"><span data-stu-id="3d554-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="3d554-148">InfoPathマネージ フォーム テンプレートのカスタム セキュリティ ポリシーを定義した後で、Windows インストーラー パッケージ (.msi) を作成し、グループ ポリシーまたは Microsoft Systems Management Server を使用して、このセキュリティ ポリシーをユーザーのコンピューターに展開できます。</span><span class="sxs-lookup"><span data-stu-id="3d554-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="3d554-149">InfoPath のカスタム セキュリティ ポリシーの配置パッケージを作成するには</span><span class="sxs-lookup"><span data-stu-id="3d554-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="3d554-150">[ **スタート**] メニューの [ **管理ツール**] をポイントし、[ **Microsoft .NET Framework 2.0 Configuration**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="3d554-151">[ **スタート**] メニューに [ **管理ツール**] が表示されない場合は、[ **コントロール パネル**] から [ **管理ツール**] を開き、[ **Microsoft .NET Framework 2.0 Configuration**] をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="3d554-152">[ **ランタイム セキュリティ ポリシー**] を右クリックし、[ **配置パッケージの作成**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="3d554-153">[ **配置するセキュリティ ポリシー レベルを選択する**] で [ **コンピューター - "Machine"**] をクリックし、Windows インストーラー パッケージのフォルダーおよびファイル名を指定します。[ **次へ**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d554-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="3d554-154">[ **完了**] をクリックし、配置パッケージを作成します。</span><span class="sxs-lookup"><span data-stu-id="3d554-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="3d554-155">.NET Framework 構成ツールの使用方法については、Visual Studio ヘルプまたは MSDN Web サイトで ".NET Framework 構成ツール (Mscorcfg.msc)" を検索してください。</span><span class="sxs-lookup"><span data-stu-id="3d554-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN Web site for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d554-156">関連項目</span><span class="sxs-lookup"><span data-stu-id="3d554-156">See also</span></span>



[<span data-ttu-id="3d554-157">コードを含むフォーム テンプレートのためのセキュリティ モデルについて</span><span class="sxs-lookup"><span data-stu-id="3d554-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

