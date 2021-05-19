---
title: メッセージ ストア プロバイダーへの通知の提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419934"
---
# <a name="providing-notifications-for-message-store-providers"></a>メッセージ ストア プロバイダーへの通知の提供

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知はオプションですが、優れたメッセージ ストア プロバイダーの非常に重要な部分です。 クライアント アプリケーションと MAPI スプーラーは、メッセージ ストア プロバイダーからの通知に依存して、送信メッセージの送信時や受信メッセージの受信時に優れたパフォーマンスを得る。 クライアントと MAPI スプーラーは、メッセージ ストア プロバイダーからの通知を受信せずに機能できますが、メッセージ ストア内の変更をユーザーに通知する必要はありません。 通常、これは、クライアントが次にメッセージ ストアの受信フォルダーを開くまで、新しいメッセージが届いたのをユーザーが確認できないという意味です。
  
クライアントは [、IMsgStore::Advise](imsgstore-advise.md) メソッドを呼び出して通知に登録します。 クライアントは [、IMAPIAdviseSink : IUnknown](imapiadvisesinkiunknown.md)インターフェイス、クライアントが受信に関心を持つ通知の種類を示すビットマスク、およびメッセージ ストア内の Advise 要求が適用されるオブジェクトを示す **EntryID** を渡します。 関連するイベントがオブジェクトで発生した場合 (たとえば、メッセージ ストアの受信フォルダーに新しいメッセージが到着した場合)、メッセージ ストア プロバイダーまたはオブジェクト自体は、そのイベントの種類に登録されている[IMAPIAdviseSink オブジェクトのすべてについて IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md)メソッドを呼び出す必要があります。  
  
メッセージ ストア プロバイダーがメッセージ ストア内の変更を他の MAPI コンポーネントに通知しない場合でも **、IMsgStore::Advise** を実装してメッセージ ストアを返す必要MAPI_E_NO_SUPPORT。 これにより、メッセージ ストア プロバイダーからの通知を期待しない他のコンポーネントに通知されます。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

