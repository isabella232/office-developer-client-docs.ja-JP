---
title: コードを含むフォーム テンプレートのセキュリティ設定を構成する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- security policy deployment package [infopath 2007],URLs [InfoPath 2007], assigning FullTrust,code access security [InfoPath 2007],UNCs [InfoPath 2007], assigning FullTrust,CAS [InfoPath 2007],security [InfoPath 2007], configuring,code groups [InfoPath 2007],FullTrust [InfoPath 2007], assigning to UNCs,FullTrust [InfoPath 2007], assigning to URLs
ms.localizationpriority: medium
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: .NET 構成スナップインを使用して、InfoPath マネージ コード フォーム テンプレートに適用されるアクセス許可セットをカスタマイズできます。
ms.openlocfilehash: c420a88f6c6c1d4e1821efe310722d0f4f6845db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621235"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a>コードを含むフォーム テンプレートのセキュリティ設定を構成する

.NET 構成スナップインを使用して、InfoPath マネージ コード フォーム テンプレートに適用されるアクセス許可セットをカスタマイズできます。
  
The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group. The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs. This enables you to customize the permission sets that are granted to InfoPath managed code form templates. For example, you can grant a form template downloaded from https://MySite permission to access the Active Directory. 
  
.NET 構成スナップインで定義したカスタム セキュリティ ポリシーを適用するには、フォーム テンプレートが実行されるすべてのクライアント コンピューター上にポリシーを配置する必要があります。
  
InfoPath マネージ コード フォーム テンプレートのセキュリティ モデルの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a>InfoPath フォーム テンプレートのコード グループを作成する

次の手順では、InfoPath マネージ コード フォーム テンプレートにアクセス許可を付与しないコード グループを作成します (ローカル コンピューターにインストールまたは登録されているフォーム テンプレートを除く)。このコード グループの下で、特定の URL または UNC にある InfoPath フォーム テンプレートにアクセス許可セットを割り当てることができます。 `InfoPath Form Templates` コード グループ内にコード グループを作成し、アクセス許可セットを割り当てる方法については、次の手順を参照してください。 
  
> [!NOTE]
> Microsoft .NET Framework 1.1 再頒布可能パッケージと共にインストールされる **Microsoft .NET Framework 1.1 構成** ツールと異なり、 **Microsoft .NET Framework 2.0 Configuration** は Microsoft .NET Framework 2.0 Software Development Kit (SDK) をインストールしなければインストールされません。 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a>InfoPath マネージ コード フォームのカスタム セキュリティ コード グループを作成するには

1. [ **スタート**] メニューの [ **管理ツール**] をポイントし、[ **Microsoft .NET Framework 2.0 Configuration**] をクリックします。
    
    [ **スタート**] メニューに [ **管理ツール**] が表示されない場合は、[ **コントロール パネル**] から [ **管理ツール**] を開き、[ **Microsoft .NET Framework 2.0 Configuration**] をダブルクリックします。
    
2. [ **マイ コンピューター**] の下の [ **ランタイム セキュリティ ポリシー**] ノードを展開し、[ **コンピューター (Machine)**] ノードを展開します。次に、[ **コード グループ**] ノードを展開し、[ **All_Code**] ノードを展開します。[ **All_Code**] ノードを右クリックし、[ **新規作成**] をクリックして [ **コード グループの作成**] ダイアログ ボックスを開きます。 
    
3. 新しいコード グループに  `InfoPath Form Templates` という名前を付けて (このとおりの名前を正確に入力する必要があります)、[ **次へ**] をクリックします。
    
4. コード グループの条件の種類を [ **すべてのコード**] に設定し、[ **次へ**] をクリックします。
    
5. [ **既存のアクセス許可セットを使用**] をクリックし、コード グループに [ **Nothing**] アクセス許可セットを割り当てます。[ **次へ**] をクリックし、[ **完了**] をクリックします。
    
6. 新しい設定を適用するには、InfoPath を閉じて再起動します。
    
必要に応じて、 **InfoPath Form Templates** コード グループに [ **Nothing**] 以外のアクセス許可セットを割り当て、すべての InfoPath マネージ コード フォーム テンプレートのアクセス許可セットを管理することができます。 
> [!NOTE]
> [ **.NET Configuration 2.0**] スナップインで、グループを右クリックして [ **プロパティ**] をクリックし、[ **アクセス許可セット**] タブをクリックすることにより、セキュリティ コード グループのアクセス許可セットをいつでも変更できます。 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a>特定の URL または UNC にあるフォームに FullTrust を割り当てる

**InfoPath Form Templates** グループの下にコード グループを作成し、特定の URL または UNC の場所からのフォーム テンプレートに完全信頼のアクセス許可セットを付与することができます。その後は、指定した場所に発行されるすべてのフォーム テンプレートが完全に信頼されて実行されます。 
  
> [!NOTE]
> ローカル コンピューターから読み込んだフォーム テンプレート (My Computer Zone コード グループ) が、InfoPath によりランダムな URL を使用して読み込まれます。 このため、次の手順を使用してこのようなフォーム テンプレートに FullTrust アクセス許可を付与することはできません。 ローカルにインストールされたフォーム テンプレートに FullTrust アクセス許可セットを付与するには、「[コードを含む InfoPath フォーム テンプレートを展開する](how-to-deploy-infopath-form-templates-with-code.md)」の「完全な信頼を必要とするフォーム テンプレートを展開する」に記載されているいずれかの手順を使用します。 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a>特定の URL または UNC の場所にある InfoPath フォームに FullTrust を割り当てるには、次の操作を行います。

1. [ **スタート**] メニューの [ **管理ツール**] をポイントし、[ **Microsoft .NET Framework 2.0 Configuration**] をクリックします。
    
    [ **スタート**] メニューに [ **管理ツール**] が表示されない場合は、[ **コントロール パネル**] から [ **管理ツール**] を開き、[ **Microsoft .NET Framework 2.0 Configuration**] をダブルクリックします。
    
2. [ **マイ コンピューター**] の下の [ **ランタイム セキュリティ ポリシー**] ノードを展開し、[ **コンピューター (Machine)**] ノードを展開します。次に、[ **コード グループ**] ノードを展開し、[ **All_Code**] ノードを展開します。次に、[ **InfoPath Form Templates**] ノードをクリックします。 
    
3. 右側のペインの [ **タスク**] ボックスの一覧で、[ **子コード グループを追加**] をクリックし、コード グループに名前を付けて、[ **次へ**] をクリックします。
    
4. [ **このコード グループの条件の種類を選択します**] ボックスの一覧で [ **URL**] を選択し、[ **FullTrust**] アクセス許可セットを付与する InfoPath マネージ コード フォーム テンプレートの場所の URL または UNC を入力します。 
    
    アクセス許可セットを 1 つのフォーム テンプレートに制限する場合は、その特定のフォーム テンプレートの完全パスを指定します。たとえば、次のように入力します。
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    単一の URL または UNC を使用してすべてのフォーム テンプレートにアクセス許可セットを付与するには、テンプレート名を省略し、URL または UNC の末尾にアスタリスク (*) を追加します。たとえば、次のように入力します。
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. [ **次へ**] をクリックします。次に、[ **既存のアクセス許可セットを使用**] をクリックし、コード グループに [ **FullTrust**] アクセス許可セットを割り当てます。 
    
6. [ **次へ**] をクリックし、[ **完了**] をクリックします。
    
7. 新しい設定を適用するには、InfoPath を閉じて再起動します。
    
> [!NOTE]
> より制限の厳しいアクセス許可セットや、独自のアクセス許可セットを適用するには、手順 4. で [ **FullTrust**] の代わりに適切なオプションを選択します。 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a>InfoPath セキュリティ ポリシーの配置パッケージを作成する

InfoPathマネージ フォーム テンプレートのカスタム セキュリティ ポリシーを定義した後で、Windows インストーラー パッケージ (.msi) を作成し、グループ ポリシーまたは Microsoft Systems Management Server を使用して、このセキュリティ ポリシーをユーザーのコンピューターに展開できます。
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a>InfoPath のカスタム セキュリティ ポリシーの配置パッケージを作成するには

1. [ **スタート**] メニューの [ **管理ツール**] をポイントし、[ **Microsoft .NET Framework 2.0 Configuration**] をクリックします。
    
    [ **スタート**] メニューに [ **管理ツール**] が表示されない場合は、[ **コントロール パネル**] から [ **管理ツール**] を開き、[ **Microsoft .NET Framework 2.0 Configuration**] をダブルクリックします。
    
2. [ **ランタイム セキュリティ ポリシー**] を右クリックし、[ **配置パッケージの作成**] をクリックします。
    
3. [ **配置するセキュリティ ポリシー レベルを選択する**] で [ **コンピューター - "Machine"**] をクリックし、Windows インストーラー パッケージのフォルダーおよびファイル名を指定します。[ **次へ**] をクリックします。
    
4. [ **完了**] をクリックし、配置パッケージを作成します。 
    
5. .NET Framework 構成ツールの使用方法については、Visual Studio ヘルプまたは MSDN Web サイトで ".NET Framework 構成ツール (Mscorcfg.msc)" を検索してください。
    
## <a name="see-also"></a>関連項目



[コードを含むフォーム テンプレートのためのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)

