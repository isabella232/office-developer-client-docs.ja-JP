---
title: サンプルのオフライン状態アドインのインストール
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: '最終更新日: 2012 年7月6日'
ms.openlocfilehash: b7b9ce539537e0759020ef7e3b4f6541a940d6fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317214"
---
# <a name="installing-the-sample-offline-state-add-in"></a>サンプルのオフライン状態アドインのインストール

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このトピックでは、サンプルのオフライン状態アドインをダウンロードしてインストールする手順について説明します。 サンプルのオフライン状態アドインは、オフライン状態のメニューを Outlook に追加し**** 、オフライン状態 API を利用する COM アドインです。 オフライン状態メニューを使用すると、状態監視を有効または無効にしたり、現在の状態を確認したり、現在の状態を変更したりすることができます。 オフライン状態アドインの実装方法の詳細については、「[オフライン状態アドインの設定](setting-up-an-offline-state-add-in.md)」を参照してください。
  
## <a name="install-the-sample-offline-state-add-in"></a>サンプルのオフライン状態アドインをインストールする

1. サンプルのオフライン状態アドインをここでダウンロードします。 [Outlook 2007 の補助リファレンスコードサンプルと再頒布可能なインストーラー](https://www.microsoft.com/en-us/download/details.aspx?id=24102)。
    
2. 管理者として Visual Studio 2005 を実行します。
    
    > [!NOTE]
    > Windows XP を実行しているコンピューターでは、管理者としてログインする必要があります。 Windows Vista を実行しているコンピューターでは、管理者としてログインする必要があります。 [Visual Studio 2005] アイコンを右クリックし、[**管理者として実行**] をクリックします。 
  
3. Visual Studio 2005 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。
    
4. サンプルを保存した場所を参照し、[ **connectionstateaddin**] をクリックして、[**開く**] をクリックします。
    
5. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
6. [名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。
    
7. [**スタート**] メニューの [**すべてのプログラム**]、[**アクセサリ**] の順にクリックし、[**コマンドプロンプト**] を右クリックし、[**管理者として実行**] をクリックします。
    
    > [!NOTE]
    > Windows XP を実行している場合は、管理者としてログインする必要があります。 
  
8. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    
9. **コマンドプロンプト**ウィンドウで、サンプルを保存した Debug フォルダーにディレクトリを変更します。 たとえば、サンプルを C:\ に保存した場合は、ドライブの場合は、「 **cd "C:\ConnectionStateAddin\Debug"」** と入力し、 **enter**キーを押します。 
    
10. 「 **regsvr32 offlinestateaddin** 」と入力し、 **enter**キーを押します。 
    
    > [!NOTE]
    > サンプルのオフライン状態アドインをアンインストールするには、「 **regsvr32-u offlinestateaddin** 」と入力します。
  
11. [ **RegSrv32** ] ダイアログボックスで、[ **OK**] をクリックします。
    
12. Outlook を再起動して、**オフライン状態**メニューを表示します。 
    
## <a name="see-also"></a>関連項目



[オフライン状態 API について](about-the-offline-state-api.md)
  
[サンプルのオフライン状態アドインのインストール](installing-the-sample-offline-state-add-in.md)
  
[サンプルのオフライン状態アドインについて](about-the-sample-offline-state-add-in.md)
  
[オフライン状態アドインのセットアップ](setting-up-an-offline-state-add-in.md)
  
[オフライン状態アドインを使用した接続状態変更の監視](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[オフライン状態アドインの切断](disconnecting-an-offline-state-add-in.md)

