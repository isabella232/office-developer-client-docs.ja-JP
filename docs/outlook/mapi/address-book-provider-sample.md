---
title: アドレス帳プロバイダーのサンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fa2a447d0757e75c95d7dc3d9b1dd16b8c7a8084
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331109"
---
# <a name="address-book-provider-sample"></a>アドレス帳プロバイダーのサンプル

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
このサンプルでは、表示名と電子メールアドレス用の単一の読み取り専用コンテナーをサポートしています。これは、フラットなバイナリファイルから読み取られます。 サンプルでは、プロファイルウィザードを除く、1回限りのテンプレートとすべての構成オプションをサポートしています。
  
このサンプルは、 [Outlook Messaging API (MAPI) コードサンプル](https://go.microsoft.com/fwlink/?LinkId=129740
)からダウンロードできます。
  
|||
|:-----|:-----|
|実行可能  <br/> |SABP32  <br/> |
| ソースコードディレクトリ:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|言語  <br/> |+  <br/> |
|対象  <br/> |windows Vista、windows server 2008、windows XP SP2、および windows server 2003 SP1 用にコンパイルする Microsoft Visual Studio 2008  <br/> |
   
## <a name="supported-features"></a>サポートされる機能

この例では、次の機能をサポートしています。
  
- 表の制限 この例では、プレフィックスとあいまいな名前の解決を実装しています。 完全な MAPI 制限言語を実装するわけではなく、表示名でのみ制限がサポートされています。
    
- メッセージングユーザーの詳細表示テーブル。 
    
- 1回限りの住所。
    
- [高度な検索] ダイアログボックス
    
- [imapistatus: imapistatus](imapistatusimapiprop.md)インターフェイス。 このインターフェイスは部分的にサポートされています。**imapiprop**メソッドは、 **ipropdata**インターフェイスに委任されます。 詳細については、 [ipropdata: imapiprop](ipropdataimapiprop.md)インターフェイスを参照してください。 
    
- 対話型およびプログラムによる構成。
    
## <a name="unsupported-features"></a>サポートされない機能

このサンプルでは、次の機能はサポートされていません。
  
- 替え.
    
- 配布リスト。
    
- エントリの作成、削除、変更。
    
- 複数の値を持つプロパティ。
    
- 名前付きプロパティ。
    
- 表示名の最初と最後の名前を区別します。
    
 **サンプルアドレス帳プロバイダーをインストールするには**
  
1. サンプルのアドレス帳プロバイダーをダウンロードするには、「 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)」を参照してください。
    
2. Outlook MAPI サンプルを保存したフォルダーを見つけます。 **OutlookMAPISamples-\<version\>番号**の zip フォルダーを右クリックし、[**すべて抽出**] をクリックします。
    
3. [**参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。
    
4. Visual Studio 2008 を実行します。
    
5. Visual Studio 2008 で、[**ファイル**] をクリックし、[**開く**] を選択して、[**プロジェクト/ソリューション**] をクリックします。
    
6. サンプルを保存した場所を参照し、[ **SABP**] をクリックして、[**開く**] をクリックします。
    
7. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
8. [名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。
    
9. サンプルを保存したフォルダーで、**インストールする .bat**ファイルを右クリックし、[**管理者として実行**] をクリックします。
    
10. [**ユーザー アカウント制御**] ダイアログ ボックスで、[**続行**] をクリックします。
    
    > [!NOTE]
    > **.bat をインストール**すると、.dll は既定の Microsoft Office インストールフォルダーである C:\Program C:\Program Office\Office12 にコピーされます。\. 別の場所に Office 製品をインストールした場合は、[**インストール**] を右クリックし、[**編集**] をクリックします。 ファイルがメモ帳で開きます。 既定のインストールパスを、コンピューターで使用されているインストールパスに置き換えます。 
  

