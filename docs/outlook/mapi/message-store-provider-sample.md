---
title: メッセージ ストア プロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: c9cd4c62dfff127763494c2edab0a3ec47ee9413
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571417"
---
# <a name="message-store-provider-sample"></a>メッセージ ストア プロバイダーのサンプル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
サンプル ラップされた PST ストア プロバイダーは、データを格納するためのバック エンドとして個人用フォルダー ファイル (PST) プロバイダーを使用します。 ラップされた PST ストア プロバイダーは、レプリケーション API と共に使用する必要があります。 
  
レプリケーション API を使用すると、アイテムをバック エンド データ リポジトリから Microsoft の PST ストアOutlookできます。 レプリケーション API を使用して、専用の PST ストアにデータをレプリケートし、同期状態を追跡します。 詳細については、「レプリケーション [API について」を参照してください](about-the-replication-api.md)。
  
サンプル ラップされた PST ストア プロバイダーのほとんどの関数は、基になる PST プロバイダーに直接引数を渡します。 一部の関数では、特別な実装が必要であり、次のトピックで説明します。
  
|||
|:-----|:-----|
|実行可能ファイル:  <br/> |WrpPST32.dll  <br/> |
|ソース コード ディレクトリ:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|言語:  <br/> |C++  <br/> |
|プラットフォーム:  <br/> |Microsoft Visual Studio Vista、Windows Windows Server 2008、Windows XP SP2、Windows Server 2003 SP1 用にコンパイルする 2008  <br/> |
   
## <a name="supported-features"></a>サポートされている機能

このサンプルでは 64 ビットMicrosoft Outlook 2010サポートされ、2013 年に向Outlookされました。 詳細については、次のトピックを参照してください。
  
- [レプリケーション API について](about-the-replication-api.md)
    
- [ラップされた PST ストア プロバイダーの初期化](initializing-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストア プロバイダーへのログオン](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストア プロバイダーの使用](using-a-wrapped-pst-store-provider.md)
    
- [ラップされた PST ストア プロバイダーのシャットダウン](shutting-down-a-wrapped-pst-store-provider.md)
    
 **ラップされた PST ストア プロバイダーのサンプルをインストールするには**
  
1. サンプル ラップされた PST プロバイダーをダウンロードするには、「MAPI サンプル[のダウンロードOutlookを参照してください](downloading-the-outlook-mapi-samples.md)。
    
2. MAPI サンプルに保存したフォルダー Outlook探します。 **OutlookMAPISamples- zip フォルダー \<version number\> を右クリック** し、[すべて抽出]**をクリックします**。
    
3. [ **参照]** をクリックし、サンプルを保存する場所を選択し、[抽出] を **クリックします**。
    
4. 2008 Microsoft Visual Studioを実行します。
    
5. [Microsoft Visual Studio 2008] で、[ファイル] をクリックし、[開く]**を選択し****、[Project/ソリューション] をクリックします**。
    
6. サンプルを保存した場所を参照し **、[WrapPST.vcproj]** をクリックし、[開く] を **クリックします**。
    
7. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
8. [ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。
    
9. サンプルを保存したフォルダーで、ファイルを右クリックし、[管理者としてinstall.bat]**をクリックします**。
    
10. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    

