---
title: このセクションで使用されるサンプルをインストールします。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397059"
---
# <a name="install-the-samples-used-in-this-section"></a>このセクションで使用されるサンプルをインストールします。

**適用対象**: Outlook 2013 | Outlook 2016 
  
MFCMAPI アプリケーションと CreateOutlookItemsAddin のプロジェクトを表示しを[MAPI を使用して Outlook アイテムを作成する](creating-outlook-items-by-using-mapi.md)セクションのトピックによって参照されているサンプル コードを実行するをインストールするには、以下の手順を実行します。 

ダウンロードして、「を使用する Outlook アイテムを作成するための MAPI」で使用されている例をインストールするセクション次手順に従います。

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>ダウンロードと MFCMAPI アプリケーションをインストールし、CreateOutlookItemsAddin プロジェクトを開く

1. [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154)実行可能ファイルの現在のバージョンをシステム上のフォルダーにダウンロードします。 
    
2. MFCMapi.exe で MFCMapi.exe ファイルを抽出します。 ハード ドライブに空のフォルダーに .zip を_バージョン_です。
    
3. [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828)プロジェクトの現在のバージョンをダウンロードします。 
    
4. MFCMapi.exe ファイルを手順 2 で展開したフォルダーに CreateOutlookItemsAddin.zip ファイル内のすべてのファイルを抽出します。
    
5. MFCMapi.exe を CreateOutlookItemsAddin プロジェクト (\CreateOutlookItemsAddin\Debug) のビルド ディレクトリを手順 2 で使用するフォルダーからコピーします。
    
6. CreateOutlookItemsAddin プロジェクト (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) は、Visual Studio のソース コードを調べることで開きます。 のどのソース ・ ファイルを開くには、 [MAPI を使用して Outlook アイテムを作成する](creating-outlook-items-by-using-mapi.md)セクションのトピックを参照してください。 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>MFCMAPI と CreateOutlookItemsAddin プロジェクトを実行します。

次の手順は、ダウンロードしている MFCMAPI の実行可能ファイルと上記の手順で説明したように、CreateOutlookItemsAddin プロジェクトの現在のバージョンがインストールされていると仮定します。 次の手順では、MFCMAPI アプリケーションと CreateOutlookItemsAddin のプロジェクトを使用して Outlook アイテムを作成することを可能にする**アドイン**のメニュー項目に説明します。 
  
> [!NOTE]
> 手順 8 と手順 9 で選択したコマンドを選択したフォルダーは、 [MAPI を使用して Outlook アイテムを作成する](creating-outlook-items-by-using-mapi.md)」セクションからトピックの 1 つで説明されている項目の種類によって異なります。 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>MFCMAPI アプリケーションとアドインのメニュー コマンドを実行するには

1. インストール手順を実行するときに作成される CreateOutlookItemsAddin\Debug フォルダーには、Mfcmapi.exe を起動します。
    
2. MFCMAPI のスプラッシュ スクリーンを閉じます **[ok]** をクリックします。 
    
3. [**セッション**] メニューで、**ログオンとストアのテーブルを表示**] をクリックします。
    
4. **プロファイルの選択**] ダイアログ ボックスで正しいプロファイルを選択し、し、[ **OK**] をクリックします。 
    
5. ストアのテーブルのリスト ビューで、 **[メールボックス]- _[ユーザー名]_** をダブルクリックします。 
    
6. フォルダー ツリー ビューでは、ルート ノードを展開します。 ルート ノードの表示名は、選択したプロファイルの種類によって異なります。 通常このノードは、**メールボックスのルート**として表示されます。
    
7. フォルダー ツリー ビューでは、インフォメーション ストアを含むノードを展開します。 このノードに対して表示される名前は、選択したプロファイルの種類によって異なります。 通常このノードは、 **IPM_SUBTREE**または**インフォメーション ストアの最上位**として表示されます。
    
8. 作成する項目の種類のフォルダーをダブルクリックします。 などの予定を作成するには、**予定**のフォルダーをクリックします。 
    
9. [**アドイン**] メニュー項目を作成するための適切なコマンドをクリックします。 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>MFCMAPI アプリケーションからコードをダウンロードして

いくつかのトピックは、MFCMAPI アプリケーション自体から、ソース コードを参照します。 MFCMAPI ソース コードをダウンロードし、Visual Studio で表示する方法を次に説明します。 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>MFCMAPI アプリケーションのソース コードをダウンロードして

1. [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154)アプリケーション、システム上のフォルダーの現在のバージョンのソース コードをダウンロードします。 
    
2. MFCMAPI の_変更セット_.zip を空のフォルダーのハード ドライブのファイルを抽出します。
    
3. MFCMapi プロジェクトを開きます (\_フォルダー名_\ MFCMapi.vcproj) では、Visual Studio のソース コードをチェックします。
    
## <a name="see-also"></a>関連項目

- [単純なメール アイテムを作成する](how-to-create-a-simple-mail-item.md)
- [単純な定期実行タスク アイテムを作成する](how-to-create-a-simple-recurrent-task-item.md)
- [複雑な定期実行予定アイテムを作成する](how-to-create-a-complex-recurrent-appointment-item.md)
- [定期実行パターンを読んで解析する](how-to-read-and-parse-a-recurrence-pattern.md)

