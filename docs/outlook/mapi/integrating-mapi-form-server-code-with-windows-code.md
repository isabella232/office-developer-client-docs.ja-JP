---
title: MAPI フォーム サーバー コードとサーバー コードWindowsする
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 53213ca6fb5bd22f4d952c317869e707c7034736
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59620612"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>MAPI フォーム サーバー コードとサーバー コードWindowsする

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム サーバーが Win32 アプリケーションである点を思い出してください。 そのため、フォーム サーバーのメモリへの読み込みとクリーンな終了に関連するタスクがあります。 すべてのアプリケーションWindows同様に、フォーム サーバーのエントリ ポイントは **WinMain 関数** です。 この関数は、次のタスクを実行するための適切な場所です。 
  
- フォーム サーバーが他の OLE コンポーネントと対話できるよう、ウィンドウ クラスを作成および登録します。
    
- フォーム オブジェクトのユーザー インターフェイス用のウィンドウ クラスまたはクラスの作成と登録。
    
- [MAPIInitialize 関数を呼び出](mapiinitialize.md)します。 **MAPIInitialize は** 、必要な OLE 初期化も処理します。 これは、フォーム サーバーのインスタンスごとに 1 回実行する必要があります。 
    
- フォーム サーバーのクラス識別子 (CLSID) の文字列表現を使用してグローバルアトムを登録する。 この atom は、フォーム サーバーの有効期間内に存在する必要があります。
    
- OLE 関数 [CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx) を呼び出して、フォーム サーバーのクラス ファクトリを OLE に登録します。 
    
- メッセージを受信するためのメイン ウィンドウの作成。 このウィンドウは、ユーザーが個々のフォーム オブジェクトに関連付けられている特定のウィンドウを操作する場合なので、表示する必要はない可能性があります。 ただし、開発中にメイン ウィンドウは、フォーム サーバーの出力または制御をデバッグする際に便利な場所になります。
    
- フォーム サーバーの有効期間中に実行されるメッセージ ループを作成し、Windows メッセージをアクティブなフォーム オブジェクトに変換してディスパッチします。
    
フォーム サーバーが終了すると、次のタスクが実行されます。
  
- OLE 関数 [CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx) を呼び出して、メッセージ クラスの OLE 登録を取り消します。 
    
- **MAPIUninitialize を呼び** 出して、MAPI へのフォーム サーバーの接続を適切に閉じます。 
    
- クラス識別子の文字列表現を含むグローバルアトムを削除します。
    
## <a name="see-also"></a>関連項目



[フォーム サーバー コードの作成](writing-form-server-code.md)

