---
title: ラップされた PST ストア プロバイダーのサンプルのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 90ce0ea3-ba73-cb57-0fa9-8898bc4ac9de
description: '�ŏI�X�V��: 2012�N7��5��'
ms.openlocfilehash: 2b47d2bc38ae0d61bbfb2a4002734b00bbfcbece
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620647"
---
# <a name="installing-the-sample-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーのサンプルのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、サンプル ラップされた PST ストア プロバイダーをダウンロードしてインストールする手順について説明します。 サンプル ラップされた PST ストア プロバイダー WrapPST は、レプリケーション API と組み合わせて使用することを目的としたラップされた PST ストア プロバイダーを実装します。 レプリケーション API の詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。
  
## <a name="install-the-sample-wrapped-pst-store-provider"></a>ラップされた PST ストア プロバイダーのサンプルをインストールする

1. ラップされた PST ストア プロバイダーのサンプルをダウンロードするには[、「Outlook 2007](https://www.microsoft.com/en-us/download/details.aspx?id=24102)補助リファレンス コード サンプルと再頒布可能インストーラー」を参照してください。
    
2. **SampleWrappedPSTStoreProvider フォルダー** を開き、[すべてのファイルの抽出 **] をクリックします**。
    
3. [ **参照]** をクリックし、サンプルを保存する場所を選択し **、[OK] をクリックします**。
    
4. [**展開**] をクリックします。 選択したフォルダーが表示され、抽出されたファイルが格納されます。
    
5. 管理者Visual Studio 2005 を開きます。
    
    > [!NOTE]
    > XP でコンピューターがWindowsしている場合は、管理者としてログインする必要があります。 コンピューターが Windows Vista を実行している場合は、管理者としてログインし、Visual Studio 2005 アイコンを右クリックし、[管理者として実行] をクリックする必要 **があります**。 
  
6. [Visual Studio 2005 で、[ファイル] をクリックし、[開く]**を選択して****、[Project/ソリューション] をクリックします**。
    
7. サンプルを保存した場所を参照し **、[WrapPST]** をクリックし、[開く] を **クリックします**。
    
8. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
9. [ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。
    
10. サンプルを保存したフォルダーで、ファイルを右クリックし、[管理者として **Install.batを****クリックします**。
    
11. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    
## <a name="see-also"></a>関連項目



[ラップされた PST ストア プロバイダーのサンプルについて](about-the-sample-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーの使用](using-a-wrapped-pst-store-provider.md)
  
[ラップされた PST ストア プロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)

