---
title: コード サンプルとしての MFCMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f98eb842-fe76-4f60-b5e2-d2217d1a66ad
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: d72c224db8b3ae4bb6fee3d34f73d9949cda6b8d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356862"
---
# <a name="mfcmapi-as-a-code-sample"></a>コード サンプルとしての MFCMAPI
 
**適用対象**: Outlook 2013 | Outlook 2016 
  
mfcmapi サンプルでは、メッセージング API を使用して、グラフィカルユーザーインターフェイスを介して MAPI ストアへのアクセスを提供します。 このサンプルをダウンロードすると、ソースファイルを使用して、多くの MAPI インターフェイスおよび参照の使用状況の例を調べることができます。 詳細については、「 [MAPI のインターフェイス](mapi-interfaces.md)」を参照してください。
  
|||
|:-----|:-----|
|対象  <br/> |windows 7、windows Vista、windows server 2008、windows XP SP2、および windows server 2003 SP1 をコンパイルするための Microsoft Visual Studio 2008  <br/> |
   
### <a name="to-download-mfcmapi"></a>mfcmapi をダウンロードするには
  
1. [ [mfcmapi](https://codeplex.com/MFCMAPI) ] ページで、[**ソースコード**] タブをクリックします。 
    
2. [**最近のチェックイン**] で、最新のビルドに対して [**ダウンロード**] をクリックします。 
    
3. 使用許諾契約書の内容を確認し、[**同意**する] をクリックします。
    
4. **[ファイルのダウンロード]** ダイアログ ボックスで **[保存]** をクリックします。 [名前を付け**て保存**] ダイアログボックスで、ソースファイルを保存するフォルダーを見つけ、[**保存**] をクリックします。
    
5. [**ダウンロードの完了**] ダイアログボックスで、[**フォルダーを開く**] をクリックします。 また、[**閉じる**] をクリックしてダイアログボックスを閉じ、保存したフォルダーで zip 形式のソースファイルを特定することもできます。 
    
6. **mfcmapi\<-バージョン番号\>.zip**ファイルを右クリックし、[**すべて展開**] をクリックします。 表示されるダイアログボックスで、[**抽出**] をクリックして、表示されているフォルダーにファイルを抽出します。 [**参照**] をクリックして、別のフォルダーを選択または作成することもできます。 
    
7. 管理者として Visual Studio 2008 を実行します。
    
   > [!NOTE]
   > Windows XP を実行しているコンピューターでは、管理者としてログインする必要があります。 Windows Vista を実行しているコンピューターでは、管理者としてログインしていて、Visual Studio 2008 アイコンを右クリックし、[**管理者として実行**] をクリックする必要があります。 
  
8. Visual Studio 2008 で、[**ファイル**] をクリックし、[**開く**] をポイントして、[**プロジェクト/ソリューション**] をクリックします。
    
9. サンプルを保存した場所に移動し、[ **mfcmapi .vcproj**] を選択して、[**開く**] をクリックします。
    
10. [ **ビルド**] メニューで、[ **ソリューションのビルド**] をクリックします。
    
11. [名前を付け**てファイルを保存**] ダイアログボックスで、[**保存**] をクリックします。
    
### <a name="to-use-mfcmapi-as-a-code-sample"></a>コードサンプルとして mfcmapi を使用するには
  
**ソリューションエクスプローラー**で、[ **mfcmapi** ] プロジェクトを展開し、[**ヘッダーファイル**]、[**リソースファイル**]、[**ソースファイル**] の各ノード内のファイルを調べてプログラミングシナリオを確認します。 
  
「 [MAPI のインターフェイス](mapi-interfaces.md)」セクションにある多くのメソッドのトピックでは、プログラミング例のために mfcmapi ソースファイルをポイントしています。 たとえば、 [IMsgStore:: getreceivefoldertable](imsgstore-getreceivefoldertable.md)では、MsgStoreDlg ファイル内の関数`CMsgStoreDlg::OnDisplayReceiveFolderTable`を参照するように指示されます。 
  
## <a name="see-also"></a>関連項目

- [MAPI Samples](mapi-samples.md)

