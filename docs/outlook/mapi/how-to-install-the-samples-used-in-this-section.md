---
title: このセクションで使用されるサンプルをインストールする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345550"
---
# <a name="install-the-samples-used-in-this-section"></a>このセクションで使用されるサンプルをインストールする

**適用対象**: Outlook 2013 | Outlook 2016 
  
mfcmapi アプリケーションと createoutlookitemsaddin プロジェクトをインストールするには、「 [MAPI を使用した Outlook アイテムの作成](creating-outlook-items-by-using-mapi.md)」セクションのトピックで参照されているサンプルコードを表示して実行するには、次の手順を実行します。 

「MAPI を使用して Outlook アイテムを作成する」セクションで使用されている例をダウンロードしてインストールするには、次の手順を実行します。

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a>mfcmapi アプリケーションをダウンロードしてインストールし、createoutlookitemsaddin プロジェクトを開くには

1. 現在のバージョンの[mfcmapi](https://go.microsoft.com/fwlink/?LinkID=124154)実行可能ファイルを、システム上のフォルダーにダウンロードします。 
    
2. mfcmapi の mfcmapi .exe ファイルを抽出します。 __ ハードドライブの空のフォルダーに .zip を圧縮します。
    
3. [createoutlookitemsaddin](https://go.microsoft.com/fwlink/?LinkID=127828)プロジェクトの現在のバージョンをダウンロードします。 
    
4. 手順2で mfcmapi の .exe ファイルを抽出したフォルダーに、createoutlookitemsaddin .zip ファイル内のすべてのファイルを抽出します。
    
5. 手順2で使用したフォルダーから、createoutlookitemsaddin プロジェクト (\CreateOutlookItemsAddin\Debug) のビルドディレクトリに mfcmapi をコピーします。
    
6. Visual Studio で createoutlookitemsaddin プロジェクト (\ createoutlookitemsaddin¥ createoutlookitemsaddin¥ .vcproj) を開き、ソースコードを調べます。 開くソースファイルを確認するには、「 [MAPI を使用して Outlook アイテムを作成](creating-outlook-items-by-using-mapi.md)する」セクションのトピックを参照してください。 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a>mfcmapi および createoutlookitemsaddin プロジェクトを実行する

次の手順では、前の手順で説明したように、現在のバージョンの mfcmapi 実行可能ファイルおよび createoutlookitemsaddin プロジェクトをダウンロードしてインストールしていることを前提としています。 次の手順では、mfcmapi アプリケーションと createoutlookitemsaddin プロジェクトを使用して Outlook アイテムを作成できる**Addins**メニューの項目について説明します。 
  
> [!NOTE]
> 手順8で選択するフォルダーと手順9で選択するコマンドは、「 [MAPI を使用した Outlook アイテムの作成](creating-outlook-items-by-using-mapi.md)」セクションに記載されているアイテムの種類によって異なります。 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a>mfcmapi アプリケーションと Addins メニューコマンドを実行するには

1. インストール手順に従って作成された CreateOutlookItemsAddin\Debug フォルダーで、mfcmapi を起動します。
    
2. [ **OK]** をクリックして、mfcmapi のスプラッシュ画面を閉じます。 
    
3. [**セッション**] メニューの [**ログオンおよび表示ストアテーブル**] をクリックします。
    
4. [**プロファイルの選択**] ダイアログボックスで、適切なプロファイルを選択し、[ **OK]** をクリックします。 
    
5. [store table] リストビューで、[**メールボックス- _[ユーザー名]_ **をダブルクリックします。 
    
6. フォルダーツリービューで、ルートノードを展開します。 ルートノードに表示される名前は、選択されているプロファイルの種類によって異なります。 通常、このノードは**ルートメールボックス**として表示されます。
    
7. フォルダーツリービューで、インフォメーションストアが格納されているノードを展開します。 このノードに表示される名前は、選択されているプロファイルの種類によって異なります。 通常、このノードは**IPM_SUBTREE**または**インフォメーションストアのトップ**として表示されます。
    
8. 作成するアイテムの種類のフォルダーをダブルクリックします。 たとえば、予定を作成するには、[**予定**] フォルダーをクリックします。 
    
9. [ **Addins** ] メニューで、作成するアイテムに適したコマンドをクリックします。 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a>mfcmapi アプリケーションからコードをダウンロードして表示する

一部のトピックでは、mfcmapi アプリケーション自体のソースコードを参照しています。 次の手順では、mfcmapi ソースコードをダウンロードして Visual Studio で表示する方法について説明します。 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a>mfcmapi アプリケーションのソースコードをダウンロードして表示するには

1. 現在のバージョンの[mfcmapi](https://go.microsoft.com/fwlink/?LinkID=124154)アプリケーションのソースコードを、システム上のフォルダーにダウンロードします。 
    
2. mfcmapi-_変更セット_.zip 内のファイルを、ハードドライブ上の空のフォルダーに抽出します。
    
3. Visual Studio で mfcmapi プロジェクト (\ _foldername_/mfcmapi .vcproj) を開き、ソースコードを調べます。
    
## <a name="see-also"></a>関連項目

- [簡単なメールアイテムを作成する](how-to-create-a-simple-mail-item.md)
- [単純な定期的なタスクアイテムを作成する](how-to-create-a-simple-recurrent-task-item.md)
- [複雑な定期的な予定アイテムを作成する](how-to-create-a-complex-recurrent-appointment-item.md)
- [定期的なパターンの読み取りと解析](how-to-read-and-parse-a-recurrence-pattern.md)

