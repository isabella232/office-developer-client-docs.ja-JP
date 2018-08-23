---
title: メッセージ ストア プロバイダーを使用したメッセージ受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 94ea0fe7fba4e49c1f646d889f3727cf5ef4739d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803723"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>メッセージ ストア プロバイダーを使用したメッセージ受信

  
  
**適用対象**: Outlook 
  
メッセージ ストア プロバイダーは、受信メッセージの送信をサポートする必要はありません (メッセージを使用するには、トランスポート プロバイダーおよび MAPI スプーラーは、メッセージの配信場所としてプロバイダーを格納するは、機能をサポートする)。 ただし、メッセージ ストア プロバイダーが受信したメッセージの送信をサポートしていない場合、既定のメッセージ ストアとして使用できません。
  
受信メッセージの送信をサポートするために、メッセージ ストア プロバイダーは、次の。
  
- クライアント アプリケーションが受信メッセージを見つけることができますので、 [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md)メソッドと[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)メソッドをサポートします。 
    
- [IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)メソッドをサポートして、MAPI スプーラーが新しいメッセージが到着したメッセージ ストア プロバイダーに通知できるようにします。 
    
- 通知を実装するは、クライアントが新しいメッセージの通知を登録できるようにします。 通知はオプションですが、プロバイダーが実装する必要があります。
    
メッセージ ・ ストアに受信メッセージが配信されるときに発生する一連のメソッド呼び出しは次のとおりです。
  
1. MAPI スプーラーは、 [IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを取得するのには [受信トレイ] の[エントリ Id](entryid.md)を持つ[IMsgStore::OpenEntry](imsgstore-openentry.md)を呼び出します。 
    
2. MAPI スプーラーは、新しいメッセージ オブジェクトを取得する[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)を呼び出します。 
    
3. MAPI スプーラーは、トランスポート プロバイダーへのメッセージ オブジェクトを渡します。
    
4. トランスポート プロバイダーは、基になるメッセージング システムからのデータをメッセージのプロパティを格納し、メッセージ オブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
5. メッセージ ストア プロバイダーは、新しいメッセージが到着した登録済みのクライアントに通知するのには、通知方法を使用します。
    
6. MAPI スプーラーでは、メッセージ ストアの[IMsgStore::NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出します。 
    
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

