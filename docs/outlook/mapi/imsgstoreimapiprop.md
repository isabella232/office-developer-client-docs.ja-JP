---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422328"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ ストア情報とメッセージとフォルダーへのアクセスを提供します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|次のユーザーによって公開されます。  <br/> |メッセージ ストア オブジェクト  <br/> |
|実装元:  <br/> |メッセージ ストア プロバイダー  <br/> |
|呼び出し元:  <br/> |クライアント アプリケーション、MAPI スプーラー、MAPI  <br/> |
|インターフェイス識別子:  <br/> |IID_IMsgStore  <br/> |
|ポインターの種類:  <br/> |LPMDB  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[アドバイス](imsgstore-advise.md) <br/> |メッセージ ストアに影響を与える指定されたイベントの通知を受信するために登録します。  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |**IMsgStore::Advise** メソッドへの呼び出しで以前に設定された通知の送信をキャンセルします。  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |2 つのエントリ識別子を比較して、メッセージ ストア内の同じエントリを参照するかどうかを判断します。  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |フォルダーまたはメッセージを開き、さらにアクセスするインターフェイス ポインターを返します。  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |特定のメッセージ クラスの受信メッセージの宛先としてフォルダーを確立します。  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |指定したメッセージ クラスの受信メッセージの送信先として、またはメッセージ ストアの既定の受信フォルダーとして確立されたフォルダーを取得します。  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |メッセージ ストアのすべての受信フォルダーに関する情報を含む、受信フォルダー テーブルへのアクセスを提供します。  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |メッセージ ストアの順序付けされたログオフを有効にします。  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |送信キューからメッセージを削除します。  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |メッセージ ストアの送信キュー内のすべてのメッセージに関する情報を含む、送信キュー テーブルへのアクセスを提供します。  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |メッセージをロックまたはロック解除します。  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |メッセージ ストア プロバイダーが送信されたメッセージに対して処理を実行できます。  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |新しいメッセージが到着したとメッセージ ストアに通知します。  <br/> |
   
|**必須のプロパティ**|**アクセス レベル**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
次のプロパティは、対人間メッセージ (IPM) メッセージ ストア用です。
  
- **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)

