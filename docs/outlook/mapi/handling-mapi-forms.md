---
title: MAPI フォームの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b0e54f78257eb6890e8afbb7941dc625dc79be0c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800195"
---
# <a name="handling-mapi-forms"></a>MAPI フォームの処理

**適用されます**: Outlook 
  
MAPI フォームは、特定のクラスのメッセージ用のビューアーです。 さまざまなメッセージ クラスに属しているメッセージを処理するユーザーを許可するクライアントは、MAPI フォームのさまざまなを処理するために書き込む必要があります。 複数のフォームを処理するには、クライアントは、次の 3 つのオブジェクトが含まれているフォーム ビューアーと呼ばれるコンポーネントを実装します。
  
- サイト オブジェクトをサポートする、 [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md)インタ フェースです。 
    
- ビューをサポートするには、シンクをアドバイスする、 [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md)インタ フェースです。 
    
- サポートするビュー コンテキストのオブジェクトの[IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md)インタ フェースです。 
    
これらの各オブジェクトは、各フォームは、その記憶域およびビューを処理するクライアントによって生成された通知の処理を実装しているフォームのサーバーと呼ばれるコンポーネントによって使用されます。 他のコンポーネントの 1 つ、フォーム ライブラリのプロバイダーでは、フォーム マネージャーを実装します。 フォーム マネージャーは、フォーム サーバーの実行可能ファイルを保存するフォームのライブラリを管理します。 この管理には、フォームの適切なサーバーをロードし、サーバーとクライアント間の初期通信を処理が含まれています。
  
次の図は、クライアントと、MAPI フォームのアーキテクチャの他の部分間の関係を示しています。
  
## <a name="mapi-form-architecture"></a>MAPI フォームのアーキテクチャ
  
![MAPI フォームのアーキテクチャ](media/forms01.gif "MAPI フォームのアーキテクチャ")
  
フォーム マネージャーの使用する場合は、クライアントは、MAPI フォームを処理するために計画、 [IMAPIFormMgr: IUnknown](imapiformmgriunknown.md) 5 つの基本的なタスクを実行するためのインターフェイス。 
  
- メッセージを開くかで構成されるときは、適切な MAPI フォームのサーバーを起動します。
    
- フォルダーの内容のテーブルでは、フォーム サーバーのアイコンを表示します。
    
- フォームの通知を送受信します。 詳細については、[送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md)を参照してください。
    
- インストールまたはフォーム ライブラリからフォームのサーバーを削除できるようにします。 詳細については、[フォーム ライブラリの保守](maintaining-a-form-library.md)を参照してください。
    
- フォームのサーバーを特定のフォルダーに関連付けるようにします。
    
フォーム マネージャーにアクセスするには、初期化中に 1 回[MAPIOpenFormMgr](mapiopenformmgr.md)関数を呼び出します。 
  
## <a name="in-this-section"></a>このセクションの内容

- [フォーム ビューアーを実装する](implementing-a-form-viewer.md): ビューを使用して、フォームのビューアーを実装する方法について説明シンク、メッセージのサイト、およびビューのコンテキストを通知します。
    
- [標準フォームの動詞を実装する](implementing-standard-form-verbs.md): MAPI フォーム上のユーザーのメニューまたはボタンのクリック操作の動詞を実装する方法について説明します。
    
- [送信およびフォームの通知の受信](sending-and-receiving-form-notifications.md): フォームの通知を送受信する方法について説明します。
    
- [フォーム ライブラリを維持する](maintaining-a-form-library.md): フォームのすべての重要な情報を保持しているライブラリを管理する方法について説明します。
    
- [メッセージに、フォームの読み込み](loading-a-message-into-a-form.md): メッセージをフォームに読み込む方法について説明します。
    
- [フォームを使用して新しいメッセージを作成する](composing-a-new-message-by-using-a-form.md): フォームを使用してメッセージを作成する方法について説明します。
    
- [フォームのアイコンを表示する](displaying-form-icons.md): フォームを使用してアイコンを表示するための手順を説明します。
    
## <a name="see-also"></a>関連項目

- [MAPI フォーム](mapi-forms.md)
- [MAPI フォームのサーバーの開発](developing-mapi-form-servers.md)

