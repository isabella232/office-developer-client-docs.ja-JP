---
title: flushqueues メソッドの実装
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8719f8aa-a537-4253-b67d-c4d38c40472b
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1e5c78c71f7fddb04d3517aca0a34efa151ece08
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411779"
---
# <a name="implementing-the-flushqueues-method"></a>flushqueues メソッドの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI スプーラーは、 [IXPLogon:: flushqueues](ixplogon-flushqueues.md)メソッドを使用して、トランスポートプロバイダーとの間で保留中のメッセージをダウンロードしてアップロードします。 通常、MAPI スプーラーは、セッションにログオンしているすべてのトランスポートプロバイダーのキューをフラッシュします。これは、ユーザーのプロファイルの [transport order] セクションで設定されている最初のトランスポートプロバイダーから始まります。 キューのフラッシュは、ほとんどの場合、ユーザーによる直接要求の結果なので、キューがフラッシュされている間のメッセージの送信と受信は MAPI スプーラーに同期されます。 これらの呼び出しは同期的なので、トランスポートプロバイダーはできるだけ早く処理する必要があります。 
  
トランスポートプロバイダーは、次の一連の手順で説明されているように**flushqueues**呼び出しを処理して、適切なメッセージ処理を有効にし、他のトランスポートプロバイダーがモデムなどの外部リソースを MAPI スプーラーの一部として使用できるようにする必要があります。**flushqueues**操作。 
  
|**手順**|**コンポーネント**|**実装**|
|:-----|:-----|:-----|
|1.  <br/> |MAPI スプーラー  <br/> |ユーザーのプロファイルのトランスポート順にリストされている最初のトランスポートプロバイダーの**flushqueues**メソッドを呼び出し、要求されたフラグを_ulflags_パラメーターに渡します。 **flushqueues**は、アップロードおよびダウンロード操作全体に対してすべてのフラグが設定された状態で呼び出されます。  <br/> |
|2.  <br/> |トランスポートプロバイダー  <br/> |**flushqueues**呼び出しから戻る前に、いくつかの操作を行う必要があります。 以前に送信されたメッセージが延期されている場合は、NOTIFY_SENT_DEFERRED フラグセットを使用して[imapisupport:: SpoolerNotify](imapisupport-spoolernotify.md)メソッドを呼び出す必要があります。 MAPI スプーラーは、トランスポートプロバイダーがメッセージの処理を完了する機会になる前に、延期されたメッセージを取り消すことができることに注意してください。  <br/> トランスポートプロバイダーがモデムなどの外部リソースを使用している場合は、外部リソースへの接続を確立する必要があります。  <br/> トランスポートプロバイダーの状態行の**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) プロパティの STATUS_OUTBOUND_FLUSH ビットは、 [imapisupport:: modifystatusrow](imapisupport-modifystatusrow.md)メソッドを使用して設定する必要があります。  <br/> その後、トランスポートプロバイダーは、 **flushqueues**呼び出しの S_OK を返す必要があります。  <br/> |
|3.  <br/> |MAPI スプーラー  <br/> |STATUS_OUTBOUND_FLUSH ビットのトランスポートプロバイダーの状態の行を確認し、キュー内の最初のメッセージに対して[IXPLogon:: submitmessage](ixplogon-submitmessage.md)を呼び出します。  <br/> |
|4.  <br/> |トランスポートプロバイダー  <br/> |メッセージを処理し、 **submitmessage**呼び出しからを返します。  <br/> |
|5.  <br/> |MAPI スプーラー  <br/> |トランスポートプロバイダーが**submitmessage**から S_OK を返す場合、MAPI スプーラーは通常のメッセージ送信と同様に、メッセージに対して[IXPLogon:: endmessage](ixplogon-endmessage.md)を呼び出します。  <br/> トランスポートプロバイダーが**submitmessage**から S_OK 以外の値を返す場合、MAPI スプーラーは、 **endmessage**を呼び出す前、または**submitmessage**を再度呼び出す前に、値を適切に処理します。  <br/> |
|6.  <br/> |トランスポートプロバイダー  <br/> |_lなフラグ_パラメーターで、 **endmessage**からメッセージ処理の状態を返します。  <br/> |
|7.  <br/> |MAPI スプーラーとトランスポートプロバイダー  <br/> |**submitmessage**- **endmessage**ループは、キュー内のすべてのメッセージがダウンロードされるまで続きます。  <br/> |
|8.  <br/> |MAPI スプーラー  <br/> |NOTIFY_END_OUTBOUND_FLUSH フラグセットを使用して、トランスポートプロバイダーの[IXPLogon:: transportnotify](ixplogon-transportnotify.md)メソッドを呼び出して、メッセージのダウンロードが完了したことをトランスポートプロバイダーに通知します。  <br/> |
|9.  <br/> |トランスポートプロバイダー  <br/> |他のトランスポートプロバイダーが自分のキューをフラッシュするために使用できるように、送信メッセージの送信に使用される外部リソースを解放します。  <br/> トランスポートプロバイダーの状態行の**PR_STATUS_CODE**プロパティの STATUS_INBOUND_FLUSH ビットは、 **modifystatusrow**を使用して設定する必要があります。  <br/> |
|10.  <br/> |MAPI スプーラー  <br/> |STATUS_INBOUND_FLUSH ビットのトランスポートプロバイダーの状態の行をチェックし、 [IXPLogon:: startmessage](ixplogon-startmessage.md)が設定されている場合はそれを呼び出します。  <br/> |
|11.  <br/> |トランスポートプロバイダー  <br/> |メッセージを処理し、 **startmessage**から戻ります。 トランスポートプロバイダーが他のメッセージをアップロードする場合は、NOTIFY_NEWMAIL フラグセットを使用して**SpoolerNotify**を呼び出す必要があります。  <br/> トランスポートプロバイダーにアップロードするメッセージがない場合は、MAPI スプーラーが**startmessage**に渡されて戻るメッセージに、 [imapiprop:: SaveChanges](imapiprop-savechanges.md)を呼び出す必要があります。  <br/> |
|個.  <br/> |MAPI スプーラー  <br/> |メッセージで**SaveChanges**が呼び出されるまで、 **startmessage**の呼び出しを続行します。 トランスポートプロバイダーがアップロードを終了すると、MAPI スプーラーは NOTIFY_END_INBOUND_FLUSH フラグが設定された**transportnotify**を呼び出します。  <br/> |
|スリー.  <br/> |トランスポートプロバイダー  <br/> |**modifystatusrow**を使用して、ステータス行の**PR_STATUS_CODE**プロパティの STATUS_INBOUND_FLUSH ビットをクリアし、他のトランスポートプロバイダーが使用できるように、すべての外部リソースを解放します。  <br/> |
|第.  <br/> |MAPI スプーラー  <br/> |ユーザーのプロファイルのトランスポート順にリストされている次のトランスポートプロバイダーの**flushqueues**を呼び出します。  <br/> |
   
クライアントアプリケーションがトランスポートプロバイダーの status オブジェクトで[imapistatus:: flushqueues](imapistatus-flushqueues.md)を呼び出す場合、トランスポートプロバイダーは状態行の適切なビットを**modifystatusrow**に設定する必要があります。 その後、mapi スプーラーは、mapi スプーラーの利便性でトランスポートプロバイダーの**IXPLogon:: flushqueues**メソッドを呼び出します。 クライアントアプリケーションの**imapistatus:: flushqueues**呼び出しの結果として、トランスポートプロバイダーの**IXPLogon:: flushqueues**メソッドが呼び出されると、この操作はクライアントアプリケーションに非同期で行われます。 それ以外の場合、 **IXPLogon:: flushqueues**は MAPI スプーラーと同期して動作します。 
  
パフォーマンス上の理由から、MAPI スプーラーは、トランスポートプロバイダーの状態行に STATUS_INBOUND_FLUSH および STATUS_OUTBOUND_FLUSH フラグが設定されている場合にのみ、トランスポートプロバイダーの**flushqueues**メソッドを呼び出します。 そのため、トランスポートプロバイダーは、ステータス行の STATUS_OUTBOUND_FLUSH および STATUS_INBOUND_FLUSH フラグをクリアすることによって、いつでも**flushqueues**操作を停止することができます。 MAPI スプーラーがシャットダウンされ、 **flushqueues**操作を終了する必要がある場合は、NOTIFY_END_INBOUND_FLUSH と NOTIFY_END_OUTBOUND_FLUSH の両方のフラグが設定された**transportnotify**を呼び出します。 トランスポートプロバイダーは、すべての外部リソースを解放し、を返します。 
  

