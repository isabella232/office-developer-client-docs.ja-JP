---
title: ラップされた PST ストア プロバイダーのサンプルのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: a1574de555eb74d06c4dbe721e7e013ac59d3071
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397766"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーのサンプルのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、ダウンロードしてサンプル ラップ PST ストア プロバイダーをインストールする手順について説明します。 サンプル ラップ PST ストア プロバイダー、WrapPST は、レプリケーション API と連携して使用するものでは、ラップされた PST ストア プロバイダーを実装します。 レプリケーション API の詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>サンプルのラップされた PST ストア プロバイダーをインストールします。

1. サンプル ラップ PST ストア プロバイダーをダウンロードするには、 [Outlook 2007 の補助リファレンス コード サンプルおよび再頒布可能なインストーラー](https://www.microsoft.com/en-us/download/details.aspx?id=24102)を参照してください。
    
2. **SampleWrappedPSTStoreProvider**フォルダーを開き、[**すべてのファイルの抽出**] をクリックします。
    
3. [**参照**] をクリックして、サンプルを保存する場所を選択し、[ **OK**] をクリックします。
    
4. [**展開**] をクリックします。 選択したフォルダーが表示され、展開されたファイルが含まれています。
    
5. 管理者として Visual Studio 2005 を開きます。
    
    > [!NOTE]
    > 場合は、コンピューターが Windows XP を実行して、必要がありますログインするは、管理者として。 場合は、コンピューターが Windows Vista を実行して、する必要がありますに記録される管理者とする必要があります、Visual Studio 2005] アイコンを右クリックし、**管理者として実行**] をクリックします。 
  
6. Visual Studio 2005 では、[**ファイル**] をクリックを選択し、**開く**] を選択し、[**プロジェクト/ソリューション**] をクリックします。
    
7. サンプルを保存する場所を参照する**WrapPST**をクリックし、[**開く**] をクリックします。
    
8. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
9. **ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。
    
10. サンプルを保存したフォルダーに**Install.bat**ファイルを右クリックし、**管理者として実行**] をクリックします。
    
11. **ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。
    
## <a name="see-also"></a>関連項目



[ラップされた PST ストア プロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーの使用](using-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

