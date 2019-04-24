---
title: ラップされた PST ストアプロバイダーのサンプルのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309633"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>ラップされた PST ストアプロバイダーのサンプルのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、サンプルのラップされた PST ストアプロバイダーをダウンロードしてインストールするための手順について説明します。 このサンプルのラップされた pst ストアプロバイダー WrapPST は、レプリケーション API と共に使用することを目的とした、ラップされた pst ストアプロバイダーを実装しています。 レプリケーション api の詳細については、「[レプリケーション api につい](about-the-replication-api.md)て」を参照してください。
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>サンプルのラップされた PST ストアプロバイダーをインストールする

1. サンプルのラップされた PST ストアプロバイダーをダウンロードするには、「 [Outlook 2007 の補助リファレンスコードサンプルと再配布可能なインストーラー](https://www.microsoft.com/en-us/download/details.aspx?id=24102)」を参照してください。
    
2. **SampleWrappedPSTStoreProvider**フォルダーを開き、[**すべてのファイルを抽出**] をクリックします。
    
3. [**参照**] をクリックして、サンプルを保存する場所を選択し、[ **OK]** をクリックします。
    
4. [**展開**] をクリックします。 選択したフォルダーが表示され、抽出したファイルが含まれます。
    
5. 管理者として Visual Studio 2005 を開きます。
    
    > [!NOTE]
    > Windows XP を実行しているコンピューターでは、管理者としてログインする必要があります。 Windows Vista を実行しているコンピューターでは、管理者としてログインしている必要があり、Visual Studio 2005 アイコンを右クリックして [**管理者として実行**] をクリックする必要があります。 
  
6. Visual Studio 2005 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。
    
7. サンプルを保存した場所を参照し、[ **WrapPST**] をクリックして、[**開く**] をクリックします。
    
8. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
9. [名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。
    
10. サンプルを保存したフォルダーで、**インストールする .bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。
    
11. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    
## <a name="see-also"></a>関連項目



[ラップされた PST ストアプロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストアプロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

