---
title: コード サンプルとしての MFCMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356862"
---
# <a name="mfcmapi-as-a-code-sample"></a>コード サンプルとしての MFCMAPI
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
MFCMAPI サンプルでは、メッセージング API を使用して、グラフィカル ユーザー インターフェイスを介して MAPI ストアへのアクセスを提供します。 このサンプルをダウンロードした後、ソース ファイルを使用して、多くの MAPI インターフェイスと参照の使用例を確認できます。 詳細については [、「MAPI インターフェイス」を参照してください](mapi-interfaces.md)。
  
|||
|:-----|:-----|
|プラットフォーム:  <br/> |Microsoft Visual Studio 2008 Windows 7、Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 用にコンパイルする  <br/> |
   
### <a name="to-download-mfcmapi"></a>MFCMAPI をダウンロードするには
  
1. [[MFCMAPI] ページで](https://codeplex.com/MFCMAPI)、[ソース コード]**タブをクリック** します。 
    
2. [ **最近のチェックイン] で、[** 最新の **ビルドのダウンロード** ] をクリックします。 
    
3. 使用許諾契約書を読み、[同意する] **をクリックします**。
    
4. **[ファイルのダウンロード]** ダイアログ ボックスで **[保存]** をクリックします。 [名前 **を付けて保存** ] ダイアログ ボックスで、ソース ファイルを保存するフォルダーを探し、[保存] を **クリックします**。
    
5. [ダウンロードの **完了] ダイアログ ボックス** で、[フォルダーを開く] **をクリックします**。 [閉じる] **をクリック** してダイアログ ボックスを閉じ、保存したフォルダー内の圧縮されたソース ファイルを検索することもできます。 
    
6. MFCMAPI- バージョン番号ファイルを右クリック.zip、[すべて展開]**をクリックします**。 **\< \>** 表示されるダイアログ ボックスで、[抽出] **を** クリックして、表示されるフォルダーにファイルを抽出します。 [参照] をクリック **して** 別のフォルダーを選択または作成することもできます。 
    
7. 管理者Visual Studio 2008 を実行します。
    
   > [!NOTE]
   > XP でコンピューターがWindowsしている場合は、管理者としてログインしている必要があります。 コンピューターが Windows Vista を実行している場合は、管理者としてログインし、Visual Studio 2008 アイコンを右クリックし、[管理者として実行] をクリックする必要 **があります**。 
  
8. [Visual Studio 2008 で、[ファイル] をクリックし、[開く] をポイントして **、[Project/ソリューション] をクリックします**。
    
9. サンプルを保存した場所を参照し **、[MFCMapi.vcproj]** を選択し、[開く] を **クリックします**。
    
10. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
11. [ファイルに **名前を付けて保存]** ダイアログ ボックスで、[保存] を **クリックします**。
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>MFCMAPI をコード サンプルとして使用するには
  
ソリューション **エクスプローラーで****、MFCMapi** プロジェクトを展開し、プログラミング シナリオ用のヘッダー ファイル、リソース ファイル、およびソース ファイル ノードのファイルを調べてください。 
  
[MAPI インターフェイス] セクションの [多くのメソッド トピック](mapi-interfaces.md) は、プログラミングの例を示す MFCMAPI ソース ファイルを指しています。 たとえば [、IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) では  `CMsgStoreDlg::OnDisplayReceiveFolderTable` 、MsgStoreDlg.cpp ファイル内の関数を確認するように指示されます。 
  
## <a name="see-also"></a>関連項目

- [MAPI Samples](mapi-samples.md)

