---
title: MFCMAPI をコード サンプルとして
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: fc92cc8deb3d12c4bc8fca4c680fd4a675b4a578
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801638"
---
# <a name="mfcmapi-as-a-code-sample"></a>MFCMAPI をコード サンプルとして
 
**適用対象**: Outlook 
  
MFCMAPI サンプルでは、メッセージング API を使用して、グラフィカル ユーザー インターフェイスによって、MAPI ストアへのアクセスを提供します。 このサンプルをダウンロードした後は、MAPI インターフェイス、および参照の多くの例の使用状況を確認するのにはソース ファイルを使用できます。 詳細については、 [MAPI インターフェイス](mapi-interfaces.md)を参照してください。
  
|||
|:-----|:-----|
|プラットフォーム:  <br/> |Windows 7、Windows Vista、Windows Server 2008、Windows XP SP2、および Windows Server 2003 SP1 のプログラムをコンパイルするのには、Microsoft Visual Studio 2008  <br/> |
   
### <a name="to-download-mfcmapi"></a>MFCMAPI をダウンロードするには
  
1. [MFCMAPI](http://codeplex.com/MFCMAPI) ] ページで、[**ソース コード**] タブをクリックします。 
    
2. [**最近のチェックイン**では、最新のビルドでは、[**ダウンロード**] をクリックします。 
    
3. ライセンス契約を読み、[ **I Agree**] をクリックします。
    
4. **ファイルのダウンロード**] ダイアログ ボックスで [**保存**] をクリックします。 **名前を付けて保存**] ダイアログ ボックスで、ソース ファイルを保存するフォルダーを見つけてし、[**保存**] をクリックします。
    
5. **[ダウンロードの完了**] ダイアログ ボックスで**フォルダーを開く**をクリックします。 **を閉じる**] ダイアログ ボックスを閉じるしでそれらを保存したフォルダー内の圧縮されたソース ファイルを検索をクリックすることもできます。 
    
6. 右クリックし、 **MFCMAPI -\<バージョン番号\>.zip**ファイル、および、[**すべて展開**] をクリックします。 ダイアログ ボックスが表示されたら、表示されているフォルダーにファイルを抽出する**抽出**をクリックします。 **参照**を選択するか、別のフォルダーを作成するをクリックすることもできます。 
    
7. Visual Studio 2008 を管理者として実行します。
    
   > [!NOTE]
   > 場合は、コンピューターが Windows XP を実行して、必要がありますログインするは、管理者として。 お使いのコンピューターには、Windows Vista を実行して、管理者としてに記録される必要があり、Visual Studio 2008 のアイコンを右クリックし、[**管理者として実行**] をクリックする必要があります。 
  
8. Visual Studio 2008 で、[**ファイル**] をクリックを選択し、[**開く**] をポイントし、[**プロジェクト/ソリューション**] をクリックします。
    
9. サンプルを保存する場所を参照する**MFCMapi.vcproj**を選択し、[**開く**] をクリックします。
    
10. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
11. **ファイルに名前を付けて**保存] ダイアログ ボックスで [**保存**] をクリックします。
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>MFCMAPI をコード サンプルとして使用するには
  
**ソリューション エクスプ ローラー**では、 **MFCMapi**プロジェクトを展開し、プログラミング シナリオについては、**ヘッダー ファイル**、**リソース ファイル**、および**ソース ファイル**のノードでのファイルを確認します。 
  
[MAPI インターフェイス](mapi-interfaces.md)で多くのメソッドのトピックでは、プログラミングの例については、MFCMAPI ソース ファイルをポイントします。 たとえば、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)での指示がある関数を検索する`CMsgStoreDlg::OnDisplayReceiveFolderTable`MsgStoreDlg.cpp ファイルにします。 
  
## <a name="see-also"></a>関連項目

- [MAPI Samples](mapi-samples.md)

