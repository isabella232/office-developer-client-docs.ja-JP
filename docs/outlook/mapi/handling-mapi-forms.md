---
title: MAPI フォームの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 05a1f1b61a8958bc2a32eb31988318cf43a8541b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580168"
---
# <a name="handling-mapi-forms"></a>MAPI フォームの処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI フォームは、特定のクラスのメッセージのビューアーです。 さまざまなメッセージ クラスに属するメッセージをユーザーが操作できるクライアントは、さまざまな MAPI フォームを処理するために記述する必要があります。 複数のフォームを処理するために、クライアントは次の 3 つのオブジェクトを含むフォーム ビューアーと呼ばれるコンポーネントを実装します。
  
- [IMAPIMessageSite : IUnknown インターフェイス](imapimessagesiteiunknown.md)をサポートするメッセージ サイト オブジェクト。 
    
- [IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md)インターフェイスをサポートするビューアズ シンク。 
    
- [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md)インターフェイスをサポートするビュー コンテキスト オブジェクト。 
    
これらの各オブジェクトは、各フォームを実装するフォーム サーバーと呼ばれるコンポーネントによって使用され、そのストレージとビューを処理するクライアントによって生成された通知を処理します。 もう 1 つのコンポーネントであるフォーム ライブラリ プロバイダーは、フォーム マネージャーを実装します。 フォーム マネージャーは、フォーム サーバーの実行可能ファイルを格納するフォーム ライブラリを管理します。 この管理には、適切なフォーム サーバーの読み込みと、サーバーとクライアント間の初期通信の処理が含まれます。
  
次の図は、クライアントと MAPI フォーム アーキテクチャの他の部分との関係を示しています。
  
## <a name="mapi-form-architecture"></a>MAPI フォームのアーキテクチャ
  
![MAPI フォームのアーキテクチャ](media/forms01.gif "MAPI フォームのアーキテクチャ")
  
クライアントが MAPI フォームの処理を計画している場合は、フォーム マネージャーの [IMAPIFormMgr : IUnknown](imapiformmgriunknown.md) インターフェイスを使用して、次の 5 つの基本的なタスクを実行します。 
  
- メッセージが開かまたは構成されている場合は、適切な MAPI フォーム サーバーを起動します。
    
- フォルダーのコンテンツ テーブルにフォーム サーバーのアイコンを表示します。
    
- フォーム通知の送受信。 詳細については、「フォーム通知の [送受信」を参照してください](sending-and-receiving-form-notifications.md)。
    
- ユーザーがフォーム ライブラリからフォーム サーバーをインストールまたは削除できます。 詳細については、「フォーム ライブラリ [の保守」を参照してください](maintaining-a-form-library.md)。
    
- ユーザーがフォーム サーバーを特定のフォルダーに関連付け許可します。
    
フォーム マネージャーにアクセスするには、初期化中に [MAPIOpenFormMgr](mapiopenformmgr.md) 関数を 1 回呼び出します。 
  
## <a name="in-this-section"></a>このセクションの内容

- [フォーム ビューアーの実装](implementing-a-form-viewer.md): ビューアアドバイス シンク、メッセージ サイト、およびビュー コンテキストを使用してフォーム ビューアーを実装する方法について説明します。
    
- [標準フォーム動詞の実装](implementing-standard-form-verbs.md): MAPI フォームのユーザー メニューまたはボタンクリックの動詞を実装する方法について説明します。
    
- [フォーム通知の送受信](sending-and-receiving-form-notifications.md): フォーム通知の送受信方法について説明します。
    
- [フォーム ライブラリの管理](maintaining-a-form-library.md): フォームに関する重要な情報を保持するライブラリを管理する方法について説明します。
    
- [メッセージをフォームに読み込む](loading-a-message-into-a-form.md): フォームにメッセージを読み込む方法について説明します。
    
- [フォームを使用して新しいメッセージを](composing-a-new-message-by-using-a-form.md)作成する : フォームを使用してメッセージを作成する方法について説明します。
    
- [フォーム アイコンの表示](displaying-form-icons.md): フォームでアイコンを表示する手順について説明します。
    
## <a name="see-also"></a>関連項目

- [MAPI フォーム](mapi-forms.md)
- [MAPI フォーム サーバーの開発](developing-mapi-form-servers.md)

