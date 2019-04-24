---
title: メッセージストアプロバイダーを使用したメッセージの受信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4763951e-ccfd-453e-b99c-5c7d5efb90c2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c93a4b56489c2bfb458e2e1cd872073e64d9998a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328449"
---
# <a name="receiving-messages-by-using-message-store-providers"></a>メッセージストアプロバイダーを使用したメッセージの受信

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージストアプロバイダーは、受信メッセージの送信をサポートする必要はありません (つまり、トランスポートプロバイダーと MAPI スプーラーがメッセージの配信ポイントとしてメッセージストアプロバイダーを使用することをサポートしています)。 ただし、メッセージストアプロバイダーが受信メッセージの送信をサポートしていない場合は、既定のメッセージストアとして使用することはできません。
  
受信メッセージの送信をサポートするために、メッセージストアプロバイダーは次のことを行う必要があります。
  
- クライアントアプリケーションが受信メッセージを検索できるように、 [IMsgStore:: getreceivefoldertable](imsgstore-getreceivefoldertable.md)および[IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)メソッドをサポートします。 
    
- [IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)メソッドをサポートします。これにより、MAPI スプーラーは、新しいメッセージが到着したことをメッセージストアプロバイダーに通知できるようになります。 
    
- 通知を実装して、クライアントが新しいメッセージ通知を登録できるようにします。 通知はオプションですが、プロバイダーで実装する必要があります。
    
受信メッセージがメッセージストアに配信されるときに実行されるメソッド呼び出しのシーケンスは次のとおりです。
  
1. MAPI スプーラーは、受信トレイ[EntryID](entryid.md)を持つ[IMsgStore:: openentry](imsgstore-openentry.md)を呼び出して、 [imapifolder](imapifolderimapicontainer.md)インターフェイスを取得します。 
    
2. MAPI スプーラーは、 [imapifolder:: CreateMessage](imapifolder-createmessage.md)を呼び出して、新しい message オブジェクトを取得します。 
    
3. MAPI スプーラーは、メッセージオブジェクトをトランスポートプロバイダーに渡します。
    
4. トランスポートプロバイダーは、メッセージのプロパティに、基になるメッセージングシステムのデータを格納し、message オブジェクトの[imapiprop:: SaveChanges](imapiprop-savechanges.md)メソッドを呼び出します。 
    
5. メッセージストアプロバイダーは、通知方法を使用して、登録されているクライアントに新しいメッセージが到着したことを通知します。
    
6. MAPI スプーラーは、メッセージストアの[IMsgStore:: NotifyNewMail](imsgstore-notifynewmail.md)メソッドを呼び出します。 
    
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

