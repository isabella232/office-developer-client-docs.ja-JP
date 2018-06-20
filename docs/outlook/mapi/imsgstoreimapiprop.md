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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 426333e6e2624adcd7cb6bc6dc4982b3d1ef1999
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801028"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore: IMAPIProp

  
  
**適用されます**: Outlook 
  
メッセージ情報を格納して、メッセージおよびフォルダーへのアクセスを提供します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |Mapidefs.h  <br/> |
|によって公開されます。  <br/> |メッセージ ストアのオブジェクト  <br/> |
|によって実装されます。  <br/> |メッセージ ストア プロバイダー  <br/> |
|によって呼び出されます。  <br/> |クライアント アプリケーションでは、MAPI スプーラーを無効、および MAPI  <br/> |
|インターフェイスの識別子。  <br/> |IID_IMsgStore  <br/> |
|ポインターの型。  <br/> |LPMDB  <br/> |
|トランザクション モデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>Vtable の順序

|||
|:-----|:-----|
|[アドバイス](imsgstore-advise.md) <br/> |メッセージ ・ ストアに影響を与える特定のイベントの通知を受け取ることを登録します。  <br/> |
|[アドバイズ中止します。](imsgstore-unadvise.md) <br/> |**IMsgStore::Advise**メソッドへの呼び出しは、設定済みの通知の送信をキャンセルします。  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |メッセージ ストアの同じエントリを参照しているかどうかを決定する 2 つのエントリ id を比較します。  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイス ポインターを返します。  <br/> |
|[SetReceiveFolder](imsgstore-setreceivefolder.md) <br/> |特定のメッセージ クラスの着信メッセージの送信先として、フォルダーを確立します。  <br/> |
|[GetReceiveFolder](imsgstore-getreceivefolder.md) <br/> |または、指定したメッセージ クラスの既定値として受信したメッセージの送信先には、メッセージ ストアのフォルダーが表示されるように設定されているフォルダーを取得します。  <br/> |
|[GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) <br/> |受信フォルダーのテーブル、テーブルのすべてのメッセージ ストアの受信フォルダーに関する情報へのアクセスを提供します。  <br/> |
|[StoreLogoff](imsgstore-storelogoff.md) <br/> |メッセージ ・ ストアの通常のログオフを有効にします。  <br/> |
|[AbortSubmit](imsgstore-abortsubmit.md) <br/> |発信キューからメッセージを削除しようとしています。  <br/> |
|[GetOutgoingQueue](imsgstore-getoutgoingqueue.md) <br/> |発信キュー テーブル、メッセージ ストアの送信キュー内のすべてのメッセージに関する情報が含まれているテーブルへのアクセスを提供します。  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |ロックまたはメッセージのロックを解除します。  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |メッセージ ストア プロバイダーは、送信されたメッセージの処理を実行できるようにします。  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |新しいメッセージが到着したメッセージ ・ ストアに通知します。  <br/> |
   
|**必要なプロパティ**|**アクセス レベル**|
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |値の取得および設定が可能です。  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_MDB_PROVIDER**([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
|**PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |値の取得のみ可能です。  <br/> |
   
次のプロパティは、メッセージ ストアの個人間メッセージ (IPM) のことです。
  
- **PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)

