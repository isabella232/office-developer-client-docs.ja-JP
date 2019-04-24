---
title: メッセージストアプロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356939"
---
# <a name="message-store-provider-sample"></a>メッセージストアプロバイダーのサンプル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サンプルのラップされた PST ストアプロバイダーは、データを保存するためのバックエンドとして個人用フォルダーファイル (pst) プロバイダを使用します。 ラップされた PST ストアプロバイダーは、レプリケーション API と一緒に使用する必要があります。 
  
レプリケーション API を使用すると、バックエンドデータリポジトリから Microsoft Outlook PST ストアにアイテムをレプリケートすることができます。 レプリケーション API を使用して、データを専用の PST ストアにレプリケートし、同期状態を追跡します。 詳細については、「[レプリケーション API につい](about-the-replication-api.md)て」を参照してください。
  
サンプルのラップされた pst ストアプロバイダーの多くの関数は、引数を基になる pst プロバイダーに直接渡します。 特定の機能には特別な実装が必要であり、以下のトピックで説明されています。
  
|||
|:-----|:-----|
|実行可能  <br/> |WrpPST32  <br/> |
|ソースコードディレクトリ:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|言語  <br/> |+  <br/> |
|対象  <br/> |windows Vista、windows server 2008、windows XP SP2、および windows server 2003 SP1 用にコンパイルする Microsoft Visual Studio 2008  <br/> |
   
## <a name="supported-features"></a>サポートされる機能

このサンプルは、Microsoft outlook 2010 64 ビット版をサポートしており、outlook 2013 用に改訂されました。 追加情報については、以下のトピックを参照してください。
  
- [レプリケーション API について](about-the-replication-api.md)
    
- [ラップされた PST ストアプロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストアプロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストアプロバイダーの使用](using-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストアプロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)
    
 **サンプルのラップされた PST ストアプロバイダーをインストールするには**
  
1. サンプルのラップされた PST プロバイダーをダウンロードするには、「 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)」を参照してください。
    
2. Outlook MAPI サンプルを保存したフォルダーを見つけます。 **OutlookMAPISamples-\<version\>番号**の zip フォルダーを右クリックし、[**すべて展開**] をクリックします。
    
3. [**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。
    
4. Microsoft Visual Studio 2008 を実行します。
    
5. Microsoft Visual Studio 2008 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。
    
6. サンプルを保存した場所を参照し、[ **WrapPST**] をクリックして、[**開く**] をクリックします。
    
7. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
8. [名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。
    
9. サンプルを保存したフォルダーで、**インストールする .bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。
    
10. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    

