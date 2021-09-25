---
title: アドレス帳プロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 66477d096dae5c9243a251d4c592856297d4456d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580294"
---
# <a name="address-book-provider-sample"></a>アドレス帳プロバイダーのサンプル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このサンプルでは、フラット バイナリ ファイルから読み取る表示名と電子メール アドレスの読み取り専用コンテナーが 1 つサポートされています。 このサンプルでは、プロファイル ウィザード以外の 1 回きりテンプレートとすべての構成オプションがサポートされています。
  
このサンプルは、メッセージング[API (MAPI) Outlookサンプルからダウンロードできます](https://go.microsoft.com/fwlink/?LinkId=129740
)。
  
|||
|:-----|:-----|
|実行可能ファイル:  <br/> |SABP32.dll  <br/> |
| ソース コード ディレクトリ:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|言語:  <br/> |C++  <br/> |
|プラットフォーム:  <br/> |Microsoft Visual Studio Vista、Windows Windows Server 2008、Windows XP SP2、Windows Server 2003 SP1 用にコンパイルする 2008  <br/> |
   
## <a name="supported-features"></a>サポートされている機能

このサンプルでは、次の機能がサポートされています。
  
- テーブルの制限。 このサンプルでは、プレフィックス一致とあいまいな名前解決を実装します。 MAPI の完全な制限言語は実装されません。制限は表示名でのみサポートされます。
    
- メッセージング ユーザーの詳細表示テーブル。 
    
- 1 回のアドレス。
    
- 高度な検索ダイアログ ボックス。
    
- [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)インターフェイス。 このインターフェイスは部分的にサポートされています。 **IMAPIProp** メソッドは **IPropData インターフェイスに委任** されます。 詳細については [、「IPropData : IMAPIProp インターフェイス」を参照](ipropdataimapiprop.md) してください。 
    
- 対話型およびプログラムによる構成。
    
## <a name="unsupported-features"></a>サポートされていない機能

このサンプルでは、次の機能はサポートされていません。
  
- 並べ替え。
    
- 配布リスト。
    
- エントリの作成、削除、および変更。
    
- 複数の値を持つプロパティ。
    
- 名前付きプロパティ。
    
- 表示名の名と名を区別します。
    
 **サンプル アドレス帳プロバイダーをインストールするには**
  
1. サンプル アドレス帳プロバイダーをダウンロードするには、「MAPI サンプルのダウンロード[Outlookを参照してください](downloading-the-outlook-mapi-samples.md)。
    
2. MAPI サンプルに保存したフォルダー Outlook探します。 **OutlookMAPISamples- zip フォルダー \<version number\> を右クリック** し、[すべて抽出]**をクリックします**。
    
3. [ **参照] を** クリックし、サンプルを保存する場所を選択し、[抽出] を **クリックします**。
    
4. 2008 Visual Studioを実行します。
    
5. [Visual Studio 2008 で、[ファイル] を **クリック** し、[開く]**を選択し**、[Project/**ソリューション] をクリックします**。
    
6. サンプルを保存した場所を参照し **、[SABP.vcproj]** をクリックし、[開く] を **クリックします**。
    
7. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
8. [ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。
    
9. サンプルを保存したフォルダーで、ファイルを右クリックし、[管理者として **install.batを****クリックします**。
    
10. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    
    > [!NOTE]
    > **Install.bat** を既定.dll Microsoft Officeインストール フォルダー C:\Program Files\Microsoft Office\Office12 にコピーします。\. 別の場所にOffice製品をインストールしている場合は、[編集] をInstall.bat **クリック****します**。 ファイルが [ファイル] ウィンドウメモ帳。 既定のインストール パスを、コンピューターで使用されるインストール パスに置き換える。 
  

