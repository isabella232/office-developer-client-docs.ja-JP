---
title: このセクションで使用されるサンプルをインストールする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a0ef67ce46c2751f9c38cb6091f8eb1b21108a3e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564310"
---
# <a name="install-the-samples-used-in-this-section"></a>このセクションで使用されるサンプルをインストールする

**適用対象**: Outlook 2013 | Outlook 2016 
  
MFCMAPI アプリケーションと CreateOutlookItemsAddin プロジェクトをインストールして[、「MAPI](creating-outlook-items-by-using-mapi.md)を使用して Outlook アイテムを作成する」セクションのトピックで参照されているサンプル コードを表示および実行するには、次の手順を実行します。 

「MAPI を使用してアイテムを作成する」セクションで使用する例をダウンロードOutlook手順に従います。

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>MFCMAPI アプリケーションをダウンロードしてインストールし、CreateOutlookItemsAddin プロジェクトを開く方法

1. MFCMAPI 実行可能ファイルの現在 [のバージョンを](https://go.microsoft.com/fwlink/?LinkID=124154) システム上のフォルダーにダウンロードします。 
    
2. ファイル内のMFCMapi.exeファイルをMFCMapi.exe。 _バージョン_.zip、ハード ドライブ上の空のフォルダーに移動します。
    
3. [CreateOutlookItemsAddin プロジェクトの現在のバージョンをダウンロード](https://go.microsoft.com/fwlink/?LinkID=127828)します。 
    
4. 手順 2 で CreateOutlookItemsAddin.zip MFCMapi.exeファイルを抽出したフォルダーに、CreateOutlookItemsAddin.zipファイル内のすべてのファイルを抽出します。
    
5. 手順 2 でMFCMapi.exeフォルダーから CreateOutlookItemsAddin プロジェクトのビルド ディレクトリにコピーします (\CreateOutlookItemsAddin\Debug)。
    
6. Visual Studio で CreateOutlookItemsAddin プロジェクト (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) を開き、ソース コードを確認します。 開くソース ファイルを決定するにはOutlook [MAPI](creating-outlook-items-by-using-mapi.md)を使用してアイテムを作成するセクションのトピックを参照してください。 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>MFCMAPI と CreateOutlookItemsAddin プロジェクトを実行する

次の手順では、前の手順で説明したように、MFCMAPI 実行可能ファイルと CreateOutlookItemsAddin プロジェクトの現在のバージョンをダウンロードしてインストールしたと仮定します。 次の手順では、MFCMAPI アプリケーションと CreateOutlookItemsAddin プロジェクトを使用して Outlook アイテムを作成できるアドイン メニュー項目について説明します。  
  
> [!NOTE]
> 手順 8 で選択したフォルダーと、手順 9 で選択するコマンドは[、[MAPI](creating-outlook-items-by-using-mapi.md)を使用して Outlook アイテムを作成する] セクションのいずれかのトピックで説明されている項目の種類によって異なります。 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>MFCMAPI アプリケーションと Addins メニュー コマンドを実行するには

1. インストールMfcmapi.exeに従って作成される CreateOutlookItemsAddin\Debug フォルダーから開始します。
    
2. **[OK] を** クリックして、MFCMAPI スプラッシュ画面を閉じします。 
    
3. [セッション] **メニューの** [ログオンと **ストアテーブルの表示] をクリックします**。
    
4. [プロファイルの **選択] ダイアログ** ボックスで、正しいプロファイルを選択し **、[OK] をクリックします**。 
    
5. [メールボックス] **-  _[ユーザー名] を_** ストア テーブルの一覧ビューでダブルクリックします。 
    
6. フォルダー ツリー ビューで、ルート ノードを展開します。 ルート ノードに表示される名前は、選択したプロファイルの種類によって異なります。 通常、このノードはルート **- メールボックスとして表示されます**。
    
7. フォルダー ツリー ビューで、情報ストアを含むノードを展開します。 このノードに表示される名前は、選択したプロファイルの種類によって異なります。 通常、このノードは **、IPM_SUBTREEまたは** Top of Information **Store として表示されます**。
    
8. 作成するアイテムの種類のフォルダーをダブルクリックします。 たとえば、予定を作成するには、[予定] **フォルダーをクリック** します。 
    
9. [アドイン **] メニューで** 、作成するアイテムの適切なコマンドをクリックします。 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>MFCMAPI アプリケーションからコードをダウンロードして表示する

一部のトピックでは、MFCMAPI アプリケーション自体のソース コードを参照します。 次の手順では、MFCMAPI ソース コードをダウンロードし、そのソース コードを表示する方法Visual Studio。 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>MFCMAPI アプリケーションのソース コードをダウンロードして表示するには

1. [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154)アプリケーションの現在のバージョンのソース コードをシステム上のフォルダーにダウンロードします。 
    
2. MFCMAPI- 変更セット内の.zip、ハード ドライブ上の空のフォルダーに展開します。
    
3. ソース コードを調べるには、MFCMapi プロジェクト (\ _foldername_\ MFCMapi.vcproj) をVisual Studioで開きます。
    
## <a name="see-also"></a>関連項目

- [簡易メール アイテムの作成](how-to-create-a-simple-mail-item.md)
- [単純な繰り返しタスク アイテムの作成](how-to-create-a-simple-recurrent-task-item.md)
- [複雑な繰り返し予定アイテムの作成](how-to-create-a-complex-recurrent-appointment-item.md)
- [定期的なパターンの読み取りと解析](how-to-read-and-parse-a-recurrence-pattern.md)

