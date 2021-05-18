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
ms.openlocfilehash: ba3629e786a224ea950e78bbec9a9fe94d4499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406900"
---
# <a name="deploy-infopath-form-templates-with-code"></a>コードを含む InfoPath フォーム テンプレートを展開する

InfoPath のマネージ コード フォーム テンプレートのフォーム コードは、共通言語ランタイム (CLR) の下で実行されるアセンブリとしてコンパイルされます。これは、フォーム コードを変更するときには、常に、Visual Studio 2012 でプロジェクトを開き、コード エディターで編集し、フォーム テンプレートを再コンパイルして、フォーム テンプレートを再展開する必要があることを意味します。さらに、マネージ コード フォーム テンプレートのプライベート アセンブリは、ホストされる CLR アプリケーション ドメインで実行されるので、完全な信頼を必要とするフォームのセキュリティ設定は、完全な信頼を必要としないフォーム テンプレートとは若干異なります。
  
## <a name="deploying-form-templates-that-do-not-require-full-trust"></a>完全な信頼を必要としないフォーム テンプレートを展開する

フォーム テンプレートのフォーム コードで完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーを使用しておらず、フォーム テンプレートで完全な信頼を必要とする機能を使用していない場合は、次の手順に従って InfoPath から直接フォーム テンプレートを発行することができます。InfoPath のセキュリティ モデルの詳細については、「[コードを含むフォーム テンプレートのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)」を参照してください。
  
### <a name="deploy-a-form-template-that-does-not-require-full-trust"></a>完全な信頼を必要としないフォーム テンプレートを展開する

1. Visual Studio 2012 でフォーム テンプレートを作成してデバッグします。
    
2. Visual Studio 2012 コード エディターで作業している場合は、InfoPath に切り替えて、[ **ファイル**] タブをクリックし、[ **発行**] タブ上の目的の発行場所のボタンをクリックします (フォーム テンプレートを以前に既に発行済みの場合は、[ **ファイル**] タブをクリックし、[ **クイック発行**] をクリックして、フォーム テンプレートを同じ場所に再発行できます)。 
    
    フォーム テンプレートがコンパイルされ、 **発行ウィザード** が開始されます。 **発行ウィザード** の手順に従って、選択した場所にフォームを展開します。 **発行ウィザード** の使用方法の詳細については、InfoPath のヘルプで「フォーム テンプレートを発行する」を参照してください。
    
## <a name="deploying-form-templates-that-require-full-trust"></a>完全な信頼を必要とするフォーム テンプレートを展開する

フォーム テンプレートのフォーム コードで完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーを使用している場合、またはフォーム テンプレートで完全な信頼を必要とする機能を使用している場合は、信頼できる発行元から発行されたコード署名用の証明書を使用して、フォーム テンプレート (.xsn) ファイルにデジタル署名する必要があります。ユーザーがフォームを開いたときに、この発行元を信頼するように求めるメッセージが表示されます。フォーム テンプレート ファイルにデジタル署名すると、フォームも完全に信頼され、フォーム コードに対して FullTrust アクセス許可が付与されます。
  
### <a name="compile-publish-and-digitally-sign-a-form-template"></a>フォーム テンプレートをコンパイル、発行、およびデジタル署名する

1. Visual Studio 2012 でフォーム テンプレートを作成してデバッグします。
    
2. Visual Studio 2012 コード エディターで作業している場合は、InfoPath に切り替えて、[ **ファイル**] タブの [ **フォームのオプション**] をクリックします。
    
3. [ **セキュリティと信頼**] カテゴリをクリックします。 
    
4. [ **セキュリティ レベル**] で、[ **自動的にセキュリティ レベルを設定する**] チェック ボックスをオフにして、[ **完全信頼**] をオンにします。
    
5. [ **フォーム テンプレートの署名**] で、[ **このフォーム テンプレートに署名する**] チェック ボックスをオンにして、[ **証明書の選択**] をクリックし、フォーム テンプレートへの署名に使用するコード署名用の証明書を指定します。
    
6. [ **OK**] を 2 回クリックして [ **フォームのオプション**] ダイアログ ボックスを閉じ、変更内容を保存します。 
    
7. [ **発行**] タブをクリックし、目的の発行場所のボタンをクリックします。 
    
8. The form template is compiled and the **Publishing Wizard** is launched. Follow the steps in the **Publishing Wizard** to deploy your form template. For more information about using the **Publishing Wizard** to deploy a form template that requires full trust, search InfoPath Help for "Publish a form template with full trust". 
    
 **メモ**
- フォームにデジタル署名するには、認証されたコード署名用の証明書がコンピューターにインストールされている必要があります。この証明書を取得するには、認証機関またはネットワーク管理者に問い合わせてください。
    
- 発行後にフォームを変更する必要がある場合は、この手順を繰り返して、フォーム テンプレートをもう一度署名する必要があります。 これは、フォームを変更するとデジタル署名が無効になるためです。 完全信頼のアクセス許可を必要とするフォームを開発するときには、「[完全信頼が必要なフォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-form-templates-that-require-full-trust.md)」で説明している手順に従って、ローカル コンピューター上のフォーム テンプレートを登録できます。 
    
## <a name="configuring-net-framework-security-settings"></a>.NET Framework のセキュリティ設定を構成する

InfoPath マネージ コード フォーム テンプレートで実行されるマネージ コードに付与するアクセス許可をさらに細かく制御するには, .NET Framework 2.0 Configuration ユーティリティを使用して、フォーム コードに特定のアクセス許可を付与します。
  
> [!IMPORTANT]
> InfoPath マネージ コード フォーム テンプレートについて .NET Framework セキュリティ設定を構成しても、完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーが実行を許可されるかどうかには影響しません。完全な信頼を必要とする InfoPath オブジェクト モデルのメンバーに対する呼び出しを有効にするには、このトピックで既に説明したように、フォーム テンプレートにデジタル署名するか、フォーム テンプレートを登録する必要があります。.NET Framework セキュリティ設定の構成は、InfoPath オブジェクト モデル以外の, .NET Framework クラスおよびマネージ コンポーネントのメンバーにのみ適用されます。 
  
### <a name="compile-publish-and-configure-net-security-settings-for-a-form-template"></a>フォーム テンプレートをコンパイル、発行、およびフォーム テンプレートの .NET セキュリティ設定を構成する

1. Visual Studio 2012 でフォーム テンプレートを作成してデバッグします。
    
2. Visual Studio 2012 コード エディターで作業している場合は、InfoPath に切り替えて、[ **ファイル**] タブをクリックし、[ **発行**] をクリックして、目的の発行場所のボタンをクリックします。
    
    The form template is compiled and the **Publishing Wizard** is launched. Follow the steps in the **Publishing Wizard** to deploy your form template. For more information about using the **Publishing Wizard**, search InfoPath Help for "Publish a form template".
    
3. 「[コードを含むフォーム テンプレートのセキュリティ設定を構成する](how-to-configure-security-settings-for-form-templates-with-code.md)」の「特定の URL または UNC にあるフォームに FullTrust を割り当てる」で説明している手順を実行します。
    
## <a name="see-also"></a>関連項目

#### <a name="tasks"></a>タスク

[コードを含むフォーム テンプレートのセキュリティ設定を構成する](how-to-configure-security-settings-for-form-templates-with-code.md)


[コードを含むフォーム テンプレートのためのセキュリティ モデルについて](about-the-security-model-for-form-templates-with-code.md)
  
[完全信頼が必要なフォーム テンプレートをプレビューおよびデバッグする](how-to-preview-and-debug-form-templates-that-require-full-trust.md)

