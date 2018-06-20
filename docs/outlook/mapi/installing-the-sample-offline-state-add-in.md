---
title: サンプル オフライン状態のアドインをインストールします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: e1b6ae6c-dcf2-a07f-c417-3a1049b758ad
description: '最終更新日: 2012 年 7 月 6 日'
ms.openlocfilehash: 00232f290c367c4bab1854bfe3909abc7b03cef8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801092"
---
# <a name="installing-the-sample-offline-state-add-in"></a>サンプル オフライン状態のアドインをインストールします。

  
  
**適用されます**: Outlook 
  
このトピックでは、ダウンロードしてオフライン状態のサンプル アドインをインストールする手順について説明します。 オフライン状態のサンプル アドインは、COM アドインを Outlook に、**オフライン状態**のメニューを追加し、オフライン状態 API を利用してします。 [オフラインの状態] メニューを有効にするまたは状態の監視を無効にする現在の状態を確認して現在の状態を変更します。 オフライン状態のアドインを実装する方法の詳細については、[アドインの設定をオフラインの状態](setting-up-an-offline-state-add-in.md)を参照してください。
  
## <a name="install-the-sample-offline-state-add-in"></a>サンプル オフライン状態アドインのインストールします。

1. オフライン状態のサンプル アドインは、ここをダウンロード: [Outlook 2007 補助リファレンス コード サンプルおよび再頒布可能なインストーラー](http://www.microsoft.com/en-us/download/details.aspx?id=24102)です。
    
2. 管理者として Visual Studio 2005 を実行します。
    
    > [!NOTE]
    > 場合は、コンピューターが Windows XP を実行して、必要がありますログインするは、管理者として。 場合は、コンピューターが Windows Vista を実行して、必要がありますログインするは、管理者として。 Visual Studio 2005] アイコンを右クリックし、**管理者として実行**] をクリックします。 
  
3. Visual Studio 2005 では、[**ファイル**] をクリックを選択し、**開く**] を選択し、[**プロジェクト/ソリューション**] をクリックします。
    
4. サンプルを保存する場所を参照する**ConnectionStateAddin**をクリックし、[**開く**] をクリックします。
    
5. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
6. **ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。
    
7. **[スタート**] メニューをクリックして**すべてのプログラム**、[**アクセサリ**] をクリックして、**コマンド プロンプト**を右クリックし、**管理者として実行**] をクリックします。
    
    > [!NOTE]
    > Windows XP を実行している場合必要がありますログインするは、管理者として。 
  
8. **ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。
    
9. **コマンド プロンプト**] ウィンドウでは、サンプルを保存するデバッグ フォルダーにディレクトリを変更します。 たとえば、C:\ ドライブのサンプルを保存する場合は、 **cd"C:\ConnectionStateAddin\Debug"** を入力し、し、 **ENTER**キーを押します。 
    
10. **Regsvr32 OfflineStateAddin.dll**を入力し、 **ENTER**キーを押します。 
    
    > [!NOTE]
    > オフライン状態のサンプル アドインをアンインストールするに **-u regsvr32 OfflineStateAddin.dll**と入力します
  
11. **RegSrv32** ] ダイアログ ボックスで [ **OK**を] をクリックします。
    
12. Outlook を再起動して、[**オフライン状態**] メニューを参照してください。 
    
## <a name="see-also"></a>関連項目



[オフラインの状態の API について](about-the-offline-state-api.md)
  
[サンプル オフライン状態のアドインをインストールします。](installing-the-sample-offline-state-add-in.md)
  
[アドインの状態をオフラインのサンプルについて](about-the-sample-offline-state-add-in.md)
  
[オフライン状態のアドインを設定します。](setting-up-an-offline-state-add-in.md)
  
[接続状態の監視は、アドインを使用して、オフライン状態を変更します。](monitoring-connection-state-changes-using-an-offline-state-add-in.md)
  
[オフライン状態の追加の接続を切断します。](disconnecting-an-offline-state-add-in.md)

