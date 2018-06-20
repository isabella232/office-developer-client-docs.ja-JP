---
title: メッセージ ストア プロバイダーの通知を提供します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c0e1cdba-ceb6-4a3f-8449-79d1a0ad1adf
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3abb4ba67ff5f0cf2284fa9286b6968698877b84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803710"
---
# <a name="providing-notifications-for-message-store-providers"></a>メッセージ ストア プロバイダーの通知を提供します。

  
  
**適用されます**: Outlook 
  
通知は省略可能ですが、適切なメッセージ ストア プロバイダーの非常に重要な含まにはれています。 クライアント アプリケーションと MAPI スプーラーは、メッセージ ストア プロバイダーからの通知メッセージを送信または受信側の受信メッセージを送信するときに、良好なパフォーマンスを取得するに依存します。 クライアントと、MAPI スプーラーは、メッセージ ストア プロバイダーから通知を受信する前に機能できますが、変更せずにメッセージ ・ ストア内のユーザーに通知することはできません。 通常、ユーザーが、クライアントは、メッセージ ストアを次に開くまで、新しいメッセージが到着したことを確認することことを意味では、フォルダーが表示されます。
  
クライアントは、 [IMsgStore::Advise](imsgstore-advise.md)メソッドを呼び出して、通知を登録します。 クライアントのパスで、 [IMAPIAdviseSink: IUnknown](imapiadvisesinkiunknown.md)インタ フェースは、クライアントが受け取るでは通知の種類を示すビットマスク、**アドバイズ**を格納、メッセージのどのオブジェクトを示す**エントリ Id**要求に適用されます。 オブジェクト (たとえば、メッセージ ・ ストア内の受信フォルダーに新しいメッセージが到着したときなど) に関連するイベントが発生すると、メッセージ ストア プロバイダーまたはオブジェクト自体はメソッドを呼び出す[IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) **のすべてのIMAPIAdviseSink**そのイベントの種類に対して登録されているオブジェクト。 
  
場合でも、メッセージの格納プロバイダー決して通知メッセージ ・ ストア内の変更の場合は、他の MAPI コンポーネント MAPI_E_NO_SUPPORT を取得する**IMsgStore::Advise**を実装する必要がありますが、します。 プロバイダーを格納、メッセージからの通知が他のコンポーネントに通知されます。 
  
## <a name="see-also"></a>関連項目



[���b�Z�[�W�̃X�g�A�̋@�[](message-store-features.md)(message-store-features.md)

