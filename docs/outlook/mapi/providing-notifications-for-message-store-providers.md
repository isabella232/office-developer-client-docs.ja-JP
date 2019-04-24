---
title: メッセージストアプロバイダー用の通知の提供
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a28e6e6f008517a6b1c2c82dfa391b478963880f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328470"
---
# <a name="providing-notifications-for-message-store-providers"></a>メッセージストアプロバイダー用の通知の提供

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
通知はオプションですが、適切なメッセージストアプロバイダーの非常に重要な部分です。 クライアントアプリケーションと MAPI スプーラーは、メッセージストアプロバイダーからの通知に依存して、送信メッセージの送信または受信メッセージの受信時のパフォーマンスを向上させます。 クライアントと MAPI スプーラーは、メッセージストアプロバイダーから通知を受信せずに機能しますが、メッセージストアの変更をユーザーに通知することはできません。 通常、これは、クライアントが次にメッセージストアの受信フォルダーを開くまで、新しいメッセージが到着するのをユーザーが確認できないことを意味します。
  
[IMsgStore:: Advise](imsgstore-advise.md)メソッドを呼び出すことにより、クライアントは通知を登録します。 クライアントは[IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インターフェイスを渡します。これは、クライアントが受け取る通知の種類を示すビットマスクと、メッセージストア内のどのオブジェクトが**アドバイス**を示すかを示す**EntryID**です。要求はに適用されます。 オブジェクトで関連するイベントが発生した場合 (たとえば、メッセージストア内の受信フォルダーに新しいメッセージが到着したときなど)、メッセージストアプロバイダーまたはオブジェクト自体[](imapiadvisesink-onnotify.md)が、**すべてのに対して IMAPIAdviseSink:: onnotify メソッドを呼び出す必要があります。** そのイベントの種類に対して登録されている IMAPIAdviseSink オブジェクト。 
  
メッセージストアプロバイダーがメッセージストア内の変更の他の MAPI コンポーネントに通知しない場合でも、MAPI_E_NO_SUPPORT を返すには**IMsgStore:: アドバイズ**を実装する必要があります。 これは、メッセージストアプロバイダーからの通知を必要としない他のコンポーネントに通知します。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

