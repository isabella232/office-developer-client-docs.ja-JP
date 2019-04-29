---
title: IMsgStore imapiprop
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
  
メッセージストア情報およびメッセージとフォルダーへのアクセスを提供します。
  
|||
|:-----|:-----|
|ヘッダー ファイル:  <br/> |mapidefs.h  <br/> |
|公開者:  <br/> |メッセージストアオブジェクト  <br/> |
|実装元:  <br/> |メッセージストアプロバイダー  <br/> |
|呼び出し元:  <br/> |クライアントアプリケーション、mapi スプーラー、mapi  <br/> |
|インターフェイス識別子:  <br/> |IID_IMsgStore  <br/> |
|ポインターの種類:  <br/> |lpmdb  <br/> |
|トランザクションモデル:  <br/> |非トランザクション  <br/> |
   
## <a name="vtable-order"></a>v の順序

|||
|:-----|:-----|
|[助言](imsgstore-advise.md) <br/> |メッセージストアに影響を与える指定したイベントの通知を受信するように登録します。  <br/> |
|[アドバイズ](imsgstore-unadvise.md) <br/> |**IMsgStore:: Advise**メソッドへの呼び出しによって、以前に設定された通知の送信をキャンセルします。  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |2つのエントリ識別子を比較して、メッセージストア内の同じエントリを参照しているかどうかを判断します。  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |フォルダーまたはメッセージを開き、さらにアクセスするためのインターフェイスポインターを返します。  <br/> |
|[setreceivefolder](imsgstore-setreceivefolder.md) <br/> |特定のメッセージクラスの受信メッセージの送信先としてフォルダーを確立します。  <br/> |
|[getreceivefolder](imsgstore-getreceivefolder.md) <br/> |指定したメッセージクラスの受信メッセージの宛先として、またはメッセージストアの既定の受信フォルダーとして確立されたフォルダーを取得します。  <br/> |
|[getreceivefoldertable](imsgstore-getreceivefoldertable.md) <br/> |受信フォルダーテーブル (メッセージストアのすべての受信フォルダーに関する情報を含む表) へのアクセスを提供します。  <br/> |
|[storelogoff](imsgstore-storelogoff.md) <br/> |メッセージストアの正常なログオフを有効にします。  <br/> |
|[abortsubmit](imsgstore-abortsubmit.md) <br/> |送信キューからメッセージを削除しようとしています。  <br/> |
|[getoutgoingqueue](imsgstore-getoutgoingqueue.md) <br/> |送信キューテーブル (メッセージストアの送信キューにあるすべてのメッセージに関する情報を含むテーブル) へのアクセスを提供します。  <br/> |
|[SetLockState](imsgstore-setlockstate.md) <br/> |メッセージをロックまたはロック解除します。  <br/> |
|[FinishedMsg](imsgstore-finishedmsg.md) <br/> |メッセージストアプロバイダーが、送信されたメッセージに対して処理を実行できるようにします。  <br/> |
|[NotifyNewMail](imsgstore-notifynewmail.md) <br/> |新しいメッセージが到着したことをメッセージストアに通知します。  <br/> |
   
|**必須のプロパティ**|**アクセスレベル**|
|:-----|:-----|
|**PR_DISPLAY_NAME**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |読み取り/書き込み  <br/> |
|**PR_ENTRYID**([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_OBJECT_TYPE**([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_RECORD_KEY**([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_ENTRYID**([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_RECORD_KEY**([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_MDB_PROVIDER**([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |読み取り専用  <br/> |
|**PR_STORE_SUPPORT_MASK**([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |読み取り専用  <br/> |
   
次のプロパティは、個人間メッセージ (IPM) メッセージストアに対するものです。
  
- **PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **PR_MDB_PROVIDER**
    
- **PR_STORE_SUPPORT_MASK**
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)

