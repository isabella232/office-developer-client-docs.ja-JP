---
title: メッセージ ストア プロバイダーを使用したメッセージの受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418730"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>メッセージ ストア プロバイダーを使用したメッセージの受信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア プロバイダーは、受信メッセージの送信をサポートする必要があります (つまり、トランスポート プロバイダーと MAPI スプーラーがメッセージの配信ポイントとしてメッセージ ストア プロバイダーを使用する機能をサポートします)。 ただし、メッセージ ストア プロバイダーが受信メッセージの送信をサポートしていない場合は、既定のメッセージ ストアとして使用できません。
  
受信メッセージの送信をサポートするには、メッセージ ストア プロバイダーが次の操作を行う必要があります。
  
- クライアント アプリケーションが受信メッセージを検索できるよう [、IMsgStore:::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) メソッドと [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) メソッドをサポートします。 
    
- MAPI スプーラーが新しいメッセージが到着したとメッセージ ストア プロバイダーに通知できるよう [、IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md) メソッドをサポートします。 
    
- クライアントが新しいメッセージ通知に登録できるよう、通知を実装します。 通知はオプションですが、プロバイダーはそれらを実装する必要があります。
    
受信メッセージがメッセージ ストアに配信される場合に発生するメソッド呼び出しのシーケンスは次のとおりです。
  
1. MAPI スプーラーは、IMAPIFolder インターフェイスを取得するために受信トレイ[エントリ ID](entryid.md)を使用して[IMsgStore::OpenEntry](imsgstore-openentry.md) [を呼び出](imapifolderimapicontainer.md)します。 
    
2. MAPI スプーラーは [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) を呼び出して、新しいメッセージ オブジェクトを取得します。 
    
3. MAPI スプーラーは、メッセージ オブジェクトをトランスポート プロバイダーに渡します。
    
4. トランスポート プロバイダーは、基になるメッセージング システムからのデータをメッセージのプロパティに入力し、メッセージ オブジェクトの [IMAPIProp::SaveChanges メソッドを呼び出](imapiprop-savechanges.md) します。 
    
5. メッセージ ストア プロバイダーは、通知メソッドを使用して、新しいメッセージが到着したと登録済みのクライアントに通知します。
    
6. MAPI スプーラーは、メッセージ ストアの [IMsgStore::NotifyNewMail メソッドを呼び出](imsgstore-notifynewmail.md) します。 
    
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

