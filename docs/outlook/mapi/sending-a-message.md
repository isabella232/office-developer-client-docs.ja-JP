---
title: メッセージを送信する
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 291d1b5595c8f0779b5d5644397a1ebfd2576a0f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629586"
---
# <a name="sending-a-message"></a>メッセージを送信する

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージを送信する準備ができたら、 [その IMessage::SubmitMessage メソッドを呼び出](imessage-submitmessage.md) します。 **SubmitMessage** は、メッセージを送信キューに入れ、メッセージの MSGFLAG_SUBMIT **(** [PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) プロパティに PR_MESSAGE_FLAGS フラグを設定します。
  
メッセージ ストア プロバイダーは、トランスポート プロバイダーと緊密に結合されている場合、メッセージをメッセージング システムに配信するトランスポートに直接送信します。 密に結合されていない場合、メッセージ ストア プロバイダーは、送信キューが変更されたと MAPI スプーラーに通知し、MAPI スプーラーはメッセージを適切なトランスポート プロバイダーに転送します。
  
ユーザーが送信操作をキャンセルできる場合は [、IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) を呼び出してこの機能を実装します。 **AbortSubmit** は、送信キューからメッセージを削除します。 メッセージが基になるメッセージング システムに与えられるまで、ユーザーは送信を停止できます。 
  
**SubmitMessage が** データを返MAPI_E_CORRUPT_DATA、送信されるデータが失われたと仮定します。 2 回目の送信を試みる前に [、IMAPIProp::SetProps](imapiprop-setprops.md) と [IMAPIProp::SaveChanges](imapiprop-savechanges.md)を呼び出してメッセージを書き戻します。 これらの **IMAPIProp** 呼び出しが失敗した場合、または SubmitMessage が **2** 度目に失敗した場合は、ユーザーにエラーを表示します。 
  
SubmitMessage の呼び **出しが成功** した後、受信者リストに割り当てられたメモリを解放し、メッセージとその添付ファイルを解放します。 メッセージが送信された後、MAPI は、これらのオブジェクトのポインターに対するそれ以上の操作を許可しません。 1 つの例外は **、IUnknown::Release を呼び出しています**。 多くのメッセージ ストア プロバイダーが送信されたメッセージのエントリ識別子を無効にしたため、他の呼び出しは許可されません。
  

