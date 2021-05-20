---
title: フォーム ビューアーの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435818"
---
# <a name="implementing-a-form-viewer"></a>フォーム ビューアーの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
フォーム ビューアーには、メッセージ サイト、ビューアアドバイス シンク、ビュー コンテキストの 3 つのオブジェクトが含まれます。 これらの各オブジェクトを使用すると、フォーム サーバーとそのフォームを操作できます。
  
メッセージ サイトは [、IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md) インターフェイスを実装し、メッセージの移動、保存、削除、新しいメッセージの作成、新しいフォーム サーバーの起動などのタスクをフォーム サーバーに支援するオブジェクトです。 メッセージ サイトは、さまざまなサービス プロバイダーに関するクライアントの状態に関する情報を取得するためにフォームによって使用されます。 たとえば、フォームはメッセージ サイトを使用して、現在のメッセージ ストア、メッセージ、またはフォルダーへのポインターを取得できます。 
  
IMAPIMessageSite インターフェイスには、次の **2 種類のメソッド** があります。 
  
- フォーム オブジェクトに情報を提供するメソッド。
    
- メッセージを操作するメソッド。
    
フォーム オブジェクトに情報を提供するメソッドは、簡単に実装できます。 [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md)を除くすべてのケースで、各メソッドで必要な情報が既に用意されている必要があります。
  
メッセージを操作するメソッドは、通常のユーザー インターフェイスを介してトリガーされた場合と同様に動作する必要があります。 たとえば、フォーム オブジェクトが [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) メソッドを呼び出す場合は、ユーザーが通常のユーザー インターフェイスで新しいカスタム メッセージを作成することを選択した場合と同じように動作します。 通常、この動作を生成するコマンドは、Compose、Open、Reply、Reply to All **Recipients、** および Forward です。    
  
ビュー コンテキストは [、IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) インターフェイスを実装し、フォーム サーバーに現在のメッセージのコンテキストを提供するオブジェクトであり、サーバーはフォルダー内の次または前のメッセージに簡単に切り替えます。 フォームは、情報を共有するためにビュー コンテキストを使用します。 ビュー コンテキスト オブジェクトを使用すると、フォームで次のコマンドを実行できます。 
  
- 通知のためにクライアントに登録します。
    
- フォルダー内の次または前のメッセージをアクティブ化します。
    
- 印刷情報を取得します。
    
- クライアントの状態を取得します。
    
- メッセージのテキスト バージョンを保存するために使用できるストリームを取得します。
    
[IMAPIMessageSite : IUnknown](imapimessagesiteiunknown.md)インターフェイスのメソッドと同様に **、IMAPIViewContext** のメソッドは、ビュー コンテキストに関連するユーザー アクションやクライアント機能と相関します。 たとえば、ビュー コンテキストは、次または前のメッセージをアクティブ化し、フォルダーの内容を並べ替え、フォルダーの内容をフィルター処理します。 
  
ユーザーがこれらの機能をアクティブ化するためのメカニズムは重要ではなく、これらの機能のセマンティクスが **IMAPIViewContext** インターフェイスのメソッドにうまくマップすることが重要です。 
  
ビューアアドバイス シンクは [、IMAPIViewAdviseSink : IUnknown](imapiviewadvisesinkiunknown.md) インターフェイスを実装し、ビューアーに影響を与えるフォーム サーバーからの通知を処理し、フォームとフォーム ビューアーが一緒に作業するのに役立つオブジェクトです。 詳細については、「フォーム通知の [送受信」を参照してください](sending-and-receiving-form-notifications.md)。 
  

