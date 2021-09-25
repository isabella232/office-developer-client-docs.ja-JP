---
title: サンプル オフライン状態アドインのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: f57055c0c9b5651023f110e9540a49382f275696
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59630439"
---
# <a name="installing-the-sample-offline-state-add-in"></a>サンプル オフライン状態アドインのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、サンプル オフライン状態アドインをダウンロードしてインストールする手順について説明します。 サンプル オフライン状態アドインは、オフライン状態メニューを追加し、オフライン状態API を使用Outlook COM アドインです。 [オフライン状態] メニューを使用すると、状態の監視を有効または無効にしたり、現在の状態を確認したり、現在の状態を変更することができます。 オフライン状態アドインの実装方法の詳細については、「オフライン状態アドインのセットアップ」 [を参照してください](setting-up-an-offline-state-add-in.md)。
  
## <a name="install-the-sample-offline-state-add-in"></a>サンプル オフライン状態アドインのインストール

1. サンプル オフライン状態アドインは[、2007](https://www.microsoft.com/en-us/download/details.aspx?id=24102)Outlookリファレンス コード サンプルと再頒布可能インストーラーからダウンロードします。
    
2. 管理者Visual Studio 2005 を実行します。
    
    > [!NOTE]
    > XP でコンピューターがWindowsしている場合は、管理者としてログインする必要があります。 Vista でコンピューターがWindowsしている場合は、管理者としてログインする必要があります。 [2005 年 2005 年Visual Studio右クリックし、[管理者として **実行] をクリックします**。 
  
3. [Visual Studio 2005 で、[ファイル] をクリックし、[開く]**を選択して****、[Project/ソリューション] をクリックします**。
    
4. サンプルを保存した場所を参照し **、[ConnectionStateAddin]** をクリックし、[開く] を **クリックします**。
    
5. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
6. [ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。
    
7. [スタート]**メニューをクリック** し、[**すべての** プログラム] をクリックし、[アクセサリ] をクリックし、[コマンド プロンプト] を右クリックして、[管理者として実行]**をクリックします**。
    
    > [!NOTE]
    > XP を実行しているWindows管理者としてログインする必要があります。 
  
8. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    
9. [コマンド **プロンプト] ウィンドウ** で、ディレクトリをサンプルを保存した Debug フォルダーに変更します。 たとえば、サンプルを C:\ に保存した場合ドライブでは **、cd "C:\ConnectionStateAddin\Debug"** と入力し **、Enter** キーを押します。 
    
10. **regsvr32 と入力OfflineStateAddin.dll** Enter キーを **押します**。 
    
    > [!NOTE]
    > サンプル オフライン状態アドインをアンインストールするには **、「regsvr32 -u」と入力OfflineStateAddin.dll**
  
11. **[RegSrv32] ダイアログ** ボックスで **、[OK] をクリックします**。
    
12. [オフラインOutlookを再起動して、[**オフライン状態] メニューを表示** します。 
    
## <a name="see-also"></a>関連項目



[オフライン状態 API について](about-the-offline-state-api.md)
  
[サンプルのオフライン状態アドインのインストール](installing-the-sample-offline-state-add-in.md)
  
[サンプルのオフライン状態アドインについて](about-the-sample-offline-state-add-in.md)
  
[オフライン状態アドインのセットアップ](setting-up-an-offline-state-add-in.md)
  
[オフライン状態アドインを使用した接続状態変更の監視](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[オフライン状態アドインの切断](disconnecting-an-offline-state-add-in.md)

