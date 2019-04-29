---
title: メッセージを送信する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423623"
---
# <a name="sending-a-message"></a>メッセージを送信する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを送信する準備ができたら、 [IMessage:: submitmessage](imessage-submitmessage.md)メソッドを呼び出します。 **submitmessage**は、メッセージを送信キューに配置し、メッセージの**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに MSGFLAG_SUBMIT フラグを設定します。
  
メッセージストアプロバイダーは、トランスポートプロバイダーと密に結び付けられている場合、メッセージをメッセージングシステムに配信するトランスポートに直接付与します。 密結合されていない場合、メッセージストアプロバイダーは、送信キューが変更されたことを mapi スプーラーに通知し、mapi スプーラーは適切なトランスポートプロバイダーにメッセージを転送します。
  
ユーザーが送信操作を取り消すことができるようにする場合は、 [IMsgStore:: abortsubmit](imsgstore-abortsubmit.md)を呼び出してこの機能を実装します。 **abortsubmit**は、発信キューからメッセージを削除します。 ユーザーは、メッセージが基になるメッセージングシステムに渡されるまで、送信を停止することを許可できます。 
  
**submitmessage**が MAPI_E_CORRUPT_DATA を返す場合は、送信されるデータが失われたと仮定します。 2回目の送信を試行する前に、 [imapiprop:: setprops](imapiprop-setprops.md)と[imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出して、メッセージを再度書き込みます。 これらの**imapiprop**の呼び出しが失敗するか、または**submitmessage**が2回目に失敗した場合は、ユーザーにエラーを表示します。 
  
**submitmessage**を正常に呼び出した後、受信者リストに割り当てられているメモリを解放し、メッセージとその添付ファイルを解放します。 メッセージが送信されると、MAPI では、これらのオブジェクトのポインターに対して他の操作は許可されません。 1つの例外は、 **IUnknown:: Release**を呼び出すことです。 多くのメッセージストアプロバイダーは、送信されたメッセージのエントリ id を無効にするため、他の通話は許可されません。
  

