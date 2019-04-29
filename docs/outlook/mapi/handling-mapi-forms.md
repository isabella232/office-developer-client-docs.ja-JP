---
title: MAPI フォームの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 91347f0c34b8d7b76e4e456397a1faa061f3b2c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423056"
---
# <a name="handling-mapi-forms"></a>MAPI フォームの処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI フォームは、特定のクラスのメッセージのビューアーです。 さまざまなメッセージクラスに属するメッセージをユーザーが操作できるようにするクライアントは、さまざまな MAPI フォームを処理するように記述する必要があります。 複数のフォームを処理するために、クライアントは、次の3つのオブジェクトを含むフォームビューアーというコンポーネントを実装します。
  
- [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インターフェイスをサポートするメッセージサイトオブジェクト。 
    
- [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インターフェイスをサポートするビューアドバイズシンク。 
    
- [imapiviewcontext: IUnknown](imapiviewcontextiunknown.md)インターフェイスをサポートするビューコンテキストオブジェクト。 
    
これらの各オブジェクトは、フォームサーバーと呼ばれるコンポーネントによって使用され、各フォームを実装し、そのストレージと、ビューを処理するクライアントによって生成される通知を処理します。 もう1つのコンポーネントであるフォームライブラリプロバイダーは、フォームマネージャーを実装します。 フォームマネージャーは、フォームサーバーの実行可能ファイルを格納するフォームライブラリを管理します。 この管理には、適切なフォームサーバーの読み込みと、サーバーとクライアントの間の初期通信の処理が含まれます。
  
次の図は、クライアントと MAPI フォームアーキテクチャの他の部分との関係を示しています。
  
## <a name="mapi-form-architecture"></a>MAPI フォームのアーキテクチャ
  
![MAPI フォームのアーキテクチャ](media/forms01.gif "MAPI フォームのアーキテクチャ")
  
クライアントが MAPI フォームの処理を計画している場合は、次の5つの基本的なタスクを実行するために、フォームマネージャーの[imapiformmgr: IUnknown](imapiformmgriunknown.md)インターフェイスを使用します。 
  
- メッセージが開かれたとき、または構成されたときに、適切な MAPI フォームサーバーを起動します。
    
- フォルダーのコンテンツテーブルにフォームサーバーのアイコンを表示します。
    
- フォーム通知を送受信します。 詳細については、「[フォーム通知の送信と受信](sending-and-receiving-form-notifications.md)」を参照してください。
    
- ユーザーがフォームライブラリからフォームサーバーをインストールまたは削除できるようにします。 詳細については、「[フォームライブラリを管理する](maintaining-a-form-library.md)」を参照してください。
    
- ユーザーがフォームサーバーを特定のフォルダーに関連付けることができるようにします。
    
フォームマネージャーにアクセスするには、 [MAPIOpenFormMgr](mapiopenformmgr.md)関数を初期化時に1回呼び出します。 
  
## <a name="in-this-section"></a>このセクションの内容

- [フォームビューアーの実装](implementing-a-form-viewer.md): view アドバイズシンク、メッセージサイト、ビューコンテキストを使用してフォームビューアーを実装する方法について説明します。
    
- [標準フォーム動詞の実装](implementing-standard-form-verbs.md): MAPI フォームのユーザーメニューまたはボタンクリックの動詞を実装する方法について説明します。
    
- [フォーム通知](sending-and-receiving-form-notifications.md)の送受信: フォーム通知を送受信する方法について説明します。
    
- [フォームライブラリの管理](maintaining-a-form-library.md): フォームに関するすべての重要な情報を保持するライブラリを管理する方法について説明します。
    
- [フォーム](loading-a-message-into-a-form.md)へのメッセージの読み込み: フォームにメッセージを読み込む方法について説明します。
    
- [フォームを使用した新しいメッセージの](composing-a-new-message-by-using-a-form.md)作成: フォームを使用してメッセージを作成する方法について説明します。
    
- [フォームアイコンの表示](displaying-form-icons.md): フォーム付きのアイコンを表示する手順について説明します。
    
## <a name="see-also"></a>関連項目

- [MAPI フォーム](mapi-forms.md)
- [MAPI フォームサーバーの開発](developing-mapi-form-servers.md)

