---
title: メッセージ ストア プロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b3c907b0a53a41a52516b23ffb1cf7400d887d89
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801637"
---
# <a name="message-store-provider-sample"></a>メッセージ ストア プロバイダーのサンプル

  
  
**適用されます**: Outlook 
  
サンプル ラップ PST ストア プロバイダーは、データを格納するためのバックエンドとして、個人用フォルダー ファイル (PST) プロバイダーを使用します。 レプリケーション API とは、ラップされた PST ストア プロバイダーを使用してください。 
  
レプリケーション API を使用すると、バックエンド ・ データ ・ リポジトリからアイテムを Microsoft Outlook の PST ストアにレプリケートできます。 レプリケーション API を使用するには専用の PST ストアにデータをレプリケートし同期の状態の追跡します。 詳細については、 [「レプリケーション API 詳細](about-the-replication-api.md)を参照してください。
  
サンプル ラップ PST ストア プロバイダーの機能のほとんどでは、基になる PST プロバイダーに直接、引数を渡します。 特定の機能は特別な実装を必要としては、次のトピックで説明します。
  
|||
|:-----|:-----|
|実行可能ファイル:  <br/> |WrpPST32.dll  <br/> |
|ソース コードのディレクトリ:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|言語:  <br/> |C++  <br/> |
|プラットフォーム:  <br/> |Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 のプログラムをコンパイルするのには、Microsoft Visual Studio 2008  <br/> |
   
## <a name="supported-features"></a>サポートされている機能

このサンプルでは、Microsoft Outlook 2010 の 64年ビットをサポートし、Outlook 2013 が改訂されたようになりました。 詳細については、次のトピックを参照してください。
  
- [レプリケーション API について](about-the-replication-api.md)
    
- [ラップされた PST ストア プロバイダーを初期化しています。](initializing-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストア プロバイダーを使用します。](using-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストア プロバイダーをシャット ダウン](shutting-down-a-wrapped-pst-store-provider.md)
    
 **サンプル ラップ PST ストア プロバイダーをインストールするのには**
  
1. サンプル ラップ PST プロバイダーをダウンロードするには、 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)を参照してください。
    
2. Outlook MAPI サンプルを保存したフォルダーを見つけます。 右クリックし、 **OutlookMAPISamples ・\<バージョン番号\>** フォルダーを zip し、[**すべて展開**] をクリックします。
    
3. **参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。
    
4. Microsoft Visual Studio 2008 を実行します。
    
5. Microsoft Visual Studio 2008 では、[**ファイル**] をクリックして、[**開いている**、および**プロジェクト/ソリューション**] をクリックし。
    
6. サンプルを保存する場所を参照する**WrapPST.vcproj**をクリックし、[**開く**] をクリックします。
    
7. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
8. **ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。
    
9. サンプルを保存したフォルダーに**install.bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。
    
10. **ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。
    

