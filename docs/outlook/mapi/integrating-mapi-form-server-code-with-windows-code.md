---
title: MAPI フォーム サーバー コードと Windows コードの統合
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b37ae47e40906342aeecf179848311556a7d4ba4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573993"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>MAPI フォーム サーバー コードと Windows コードの統合

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
フォーム サーバーが Win32 アプリケーションであることに注意します。 などは、フォームのサーバーをメモリに読み込むと、正常に終了に関連するいくつかのタスクがあります。 すべての Windows アプリケーションと同様に、フォームのサーバーのエントリ ポイントが**WinMain**関数です。 この関数は、次のタスクを実行する適切な場所です。 
  
- 作成して、フォームのサーバーがほかの OLE コンポーネントを使用して対話できるように、ウィンドウ クラスを登録します。
    
- 作成して、ウィンドウ クラスまたはフォームのオブジェクトのユーザー インターフェイスのクラスを登録します。
    
- [生じます](mapiinitialize.md)関数を呼び出しています。 **生じます**が、必要な OLE の初期化には、同様に処理されます。 これは、フォーム サーバーのインスタンスごと 1 回だけ実行してください。 
    
- フォーム サーバーのクラス識別子 (CLSID) の文字列表現でグローバル アトムを登録しています。 フォーム サーバーの有効期間のこのアトムが存在します。
    
- フォーム サーバーのクラス ファクトリを OLE に登録して[います](http://msdn.microsoft.com/en-us/library/ms693407.aspx)OLE 関数を呼び出します。 
    
- メッセージを受信するのにはメイン ウィンドウを作成しています。 このウィンドウはおそらく、ユーザーが個々 のフォーム オブジェクトに関連付けられている特定の windows と対話するために、表示する必要はありません。 ただし、開発時にメイン ・ ウィンドウは、出力またはフォーム サーバーのコントロールをデバッグするための便利な場所。
    
- フォーム サーバーの有効期間を実行するためのメッセージ ループを作成して、翻訳作業中のフォーム オブジェクトへの windows メッセージのディスパッチします。
    
フォーム サーバーが終了するは、次のタスクを実行する必要があります。
  
- OLE 関数、メッセージ クラスの OLE の登録を取り消すには[CoRevokeClassObject](http://msdn.microsoft.com/en-us/library/ms688650%28VS.85%29.aspx)を呼び出します。 
    
- Mapi フォーム サーバーの接続を正しく閉じるには、 **MAPIUninitialize**を呼び出します。 
    
- クラス識別子の文字列表現が含まれているグローバル アトムを削除します。
    
## <a name="see-also"></a>関連項目



[フォーム サーバー コードの記述](writing-form-server-code.md)

