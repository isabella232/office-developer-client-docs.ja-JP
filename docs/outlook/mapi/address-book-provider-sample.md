---
title: アドレス帳プロバイダー サンプル
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2ccf1643-5604-4fee-92cc-3d6af00e7f98
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: c32017598407760d5dbbb01ee6c28267bbffd152
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799639"
---
# <a name="address-book-provider-sample"></a>アドレス帳プロバイダー サンプル

  
  
**適用対象**: Outlook 
  
このサンプルには、表示名と電子メール アドレスは、バイナリのフラット ファイルからの読み取りは、1 つの読み取り専用コンテナーがサポートしています。 サンプルには、1 回限りのテンプレートおよびプロファイル ウィザードを除くすべての構成オプションがサポートされています。
  
[Outlook メッセージング API (MAPI) のサンプル コード](http://go.microsoft.com/fwlink/?LinkId=129740
)からは、このサンプルをダウンロードできます。
  
|||
|:-----|:-----|
|実行可能ファイル:  <br/> |SABP32.dll  <br/> |
| ソース コードのディレクトリ:  <br/> |SampleAddressBookProvider\SABP  <br/> |
|言語:  <br/> |C++  <br/> |
|プラットフォーム:  <br/> |Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 のプログラムをコンパイルするのには、Microsoft Visual Studio 2008  <br/> |
   
## <a name="supported-features"></a>サポートされている機能

このサンプルには、次の機能がサポートされています。
  
- テーブルの制限です。 サンプルでは、プレフィックスに一致およびあいまいな名前解決を実装します。 完全な MAPI 制限言語を実装していないと表示名にのみ制限をサポートします。
    
- メッセージング ユーザーの詳細表示のテーブル。 
    
- 1 回限りのアドレスです。
    
- 高度な検索] ダイアログ ボックスの場合。
    
- [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md)インタ フェースです。 このインターフェイスは部分的にサポートされています。**IMAPIProp**メソッドは、 **IPropData**インターフェイスに委任されます。 詳細についてを参照してください、 [IPropData: IMAPIProp](ipropdataimapiprop.md)インタ フェースです。 
    
- インタラクティブおよびプログラマティックな構成です。
    
## <a name="unsupported-features"></a>サポートされていない機能

このサンプルでは、次の機能はサポートされていません。
  
- 並べ替えします。
    
- 配布リストです。
    
- 作成、削除、およびエントリを変更します。
    
- 複数値を持つプロパティです。
    
- 名前付きプロパティ。
    
- 表示名の最初と最後の名前を区別します。
    
 **サンプルのアドレス帳プロバイダーをインストールするのには**
  
1. サンプルのアドレス帳プロバイダーをダウンロードするには、 [Outlook MAPI サンプルのダウンロード](downloading-the-outlook-mapi-samples.md)を参照してください。
    
2. Outlook MAPI サンプルを保存したフォルダーを見つけます。 右クリックし、 **OutlookMAPISamples ・\<バージョン番号\>** フォルダーを zip し、[**すべて展開**] をクリックします。
    
3. **参照**] をクリックして、サンプルを保存する場所を選択し、[**抽出**] をクリックします。
    
4. Visual Studio 2008年を実行します。
    
5. Visual Studio 2008 では、[**ファイル**] をクリックして、[**開いている**、および**プロジェクト/ソリューション**] をクリックし。
    
6. サンプルを保存する場所を参照する**SABP.vcproj**をクリックし、[**開く**] をクリックします。
    
7. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
8. **ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。
    
9. サンプルを保存したフォルダーに**install.bat**ファイルを右クリックし、**管理者として実行**] をクリックします。
    
10. **ユーザー アカウント制御**] ダイアログ ボックスで [**続行**] をクリックします。
    
    > [!NOTE]
    > **Install.bat**コピー .dll ファイルを既定の Microsoft Office のインストール フォルダー、C:\Program ファイル Office\Office12\. 別の場所に Office 製品をインストールした場合は、 **Install.bat**を右クリックし、[**編集**] をクリックします。 ファイルがメモ帳で開きます。 既定のインストール パスをお使いのコンピューターで使用されているインストール パスに置き換えます。 
  

