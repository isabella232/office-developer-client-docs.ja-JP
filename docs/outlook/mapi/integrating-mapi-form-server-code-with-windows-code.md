---
title: MAPI フォームサーバーコードと Windows コードの統合
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 47ec3e97-ad2b-43ea-842a-b2a0675eef48
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 33b205c0ac5caf5fc049a0732cd219aa2c321326
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332180"
---
# <a name="integrating-mapi-form-server-code-with-windows-code"></a>MAPI フォームサーバーコードと Windows コードの統合

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォームサーバーが Win32 アプリケーションであることを思い出してください。 そのため、フォームサーバーをメモリに読み込み、クリーンに終了することに関連するタスクがいくつかあります。 すべての Windows アプリケーションと同様に、フォームサーバーのエントリポイントは**WinMain**関数です。 この関数は、次のタスクを実行するための適切な場所です。 
  
- フォームサーバーが他の OLE コンポーネントと対話できるように、ウィンドウクラスを作成して登録します。
    
- form オブジェクトのユーザーインターフェイス用のウィンドウクラスまたはクラスを作成して登録します。
    
- [MAPIInitialize](mapiinitialize.md)関数を呼び出します。 **MAPIInitialize**では、必要な OLE 初期化も同様に処理されます。 これは、フォームサーバーのインスタンスごとに1回実行する必要があります。 
    
- フォームサーバーのクラス識別子 (CLSID) の文字列表記を使用して、グローバルアトムを登録します。 この atom は、フォームサーバーの有効期間中は存在する必要があります。
    
- ole 関数[CoRegisterClassObject](https://msdn.microsoft.com/library/ms693407.aspx)を呼び出して、ole を使用してフォームサーバーのクラスファクトリを登録します。 
    
- メッセージを受信するためのメインウィンドウを作成します。 このウィンドウは、ユーザーが個々の form オブジェクトに関連付けられている特定のウィンドウと対話するため、表示されている必要はありません。 ただし、開発時に、メインウィンドウは、フォームサーバーの出力やコントロールをデバッグするための便利な場所になることがあります。
    
- フォームサーバーの有効期間中に実行されるメッセージループを作成し、windows メッセージをアクティブな form オブジェクトに変換してディスパッチします。
    
フォームサーバーが終了すると、次のタスクが実行されます。
  
- ole 関数[CoRevokeClassObject](https://msdn.microsoft.com/library/ms688650%28VS.85%29.aspx)を呼び出して、メッセージクラスの ole 登録を取り消します。 
    
- **MAPIUninitialize**を呼び出して、フォームサーバーの MAPI への接続を適切に閉じます。 
    
- クラス識別子の文字列表現を含むグローバルアトムを削除します。
    
## <a name="see-also"></a>関連項目



[フォームサーバーコードの記述](writing-form-server-code.md)

