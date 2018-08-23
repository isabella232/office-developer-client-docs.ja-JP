---
title: メッセージ ストアのフォルダーを開く
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 63b8224ad56e2b9985c9d733e2a3c27c67eb2f7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801686"
---
# <a name="opening-a-message-store-folder"></a>メッセージ ストアのフォルダーを開く

**適用対象**: Outlook 
  
任意のフォルダーを開くには、そのエントリの識別子が利用できなければなりません。 ほとんどのフォルダーの**PR_ENTRYID**プロパティの取得を意味します。 IPM サブツリー フォルダーおよびその他のルート フォルダーの一部などの特別なフォルダーには、MAPI は、メッセージ ストアの**IMAPIProp::GetProps**メソッドを呼び出すことによってアクセス可能な特別なエントリの識別子のプロパティを定義します。 これらのエントリの識別子は常に長期的なありです。 
  
|**Folder**|**エントリの識別子のプロパティ**|
|:-----|:-----|
|���M�g���C] �̃t�H���_�[  <br/> |**PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))(IPM メッセージ クラスのみ)  <br/> |
|�폜�ς݃A�C�e�� �t�H���_�[  <br/> |**PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|���M�ς݃A�C�e��] �t�H���_�[  <br/> |**PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM ���[�g �t�H���_�[  <br/> |**PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|�������ʂ̃��[�g �t�H���_�[  <br/> |**PR_FINDER_ENTRYID**([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|共通ビューのルート フォルダー  <br/> |**PR_COMMON_VIEWS_ENTRYID**([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|個人用ビューのルート フォルダー  <br/> |**PR_VIEWS_ENTRYID**([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|ルート フォルダーの連絡先  <br/> |**PR_IPM_CONTACT_ENTRYID**([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|[下書き] フォルダーをルートします。  <br/> |**PR_IPM_DRAFTS_ENTRYID**([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|仕訳帳のルート フォルダー  <br/> |**PR_IPM_JOURNAL_ENTRYID**([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|ルート フォルダーの予定表  <br/> |**PR_IPM_APPOINTMENT_ENTRYID**([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|メモ ルート フォルダー  <br/> |**PR_IPM_NOTE_ENTRYID**([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|タスクのルート フォルダー  <br/> |**PR_IPM_TASK_ENTRYID**([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
これらの特別なエントリ id のいずれかを取得しようとすると、前に取得、 **PR\_VALID_FOLDER_MASK**メッセージ ストアのプロパティを ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md))。 **PR\_VALID_FOLDER_MASK**は、特別なエントリの識別子が存在するを識別するビットマスクです。 それぞれの特別なフォルダーの 1 つのビットがあります。 ビットが設定されている場合の対応するフォルダーがサポートされて、エントリの有効な識別子が含まれていることを示します。 たとえば、削除済みアイテム フォルダーが存在し、有効なエントリの識別子では、フォルダーには\_ **PR_VALID_FOLDER_MASK**で IPM_WASTEBASKET_VALID ビットが設定されます。 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>特定のクラスのすべての受信メッセージが配置されているフォルダーを開きます
  
1. そのエントリ id、メッセージ クラスを識別する文字列を指すように_lpszMessageClass_パラメーターの設定を取得するために[IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出します。 など、IPM サブツリーの受信トレイを開く場合は、IPM に_lpszMessageClass_をポイントします。 IPC メッセージの受信フォルダーを開く場合は、IPC を指すように設定します。 

   メッセージ クラスに登録されている受信フォルダーがない場合、 **GetReceiveFolder**は、渡された関連するメッセージ クラスがメッセージ クラスの使用可能な最長のプレフィックスに一致する受信フォルダーを選択します。 詳細については、 [MAPI が表示されるフォルダー](mapi-receive-folders.md)を参照してください。 
   
   **PR_IPM_OUTBOX_ENTRYID**プロパティを使用すると、IPM メッセージに対してのみ、[送信トレイ] フォルダーを開くことに注意してください。 IPC メッセージを送信トレイを開く場合のエントリの識別子を使用代わりにそのフォルダーが表示されます。 IPC メッセージの受信と送信の両方は、受信フォルダーに配置されます。 
    
2. フォルダーを開き、それにアクセスするために使用できるインターフェイス ポインターを返すに 4 つの**OpenEntry**メソッドのいずれかを呼び出します。 フォルダーを開くには、次の方法のいずれかを呼び出すことができます。 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   選択した特定のメソッドは、フォルダーを開くことができませんし、時に使用可能なオブジェクトによって異なります。 **IMAPISession**メソッドは、現在のプロファイルで任意のメッセージ ストアの任意のフォルダーを開くことができます、ため、フォルダーを開くことについては何もわからないとき、この**OpenEntry**を呼び出します。 メッセージ ・ ストアは、フォルダーを所有していることがわかって、メッセージ ・ ストアへのポインターがある場合は、 **IMsgStore::OpenEntry**を呼び出します。 
    
   などの**IMsgStore**メソッドを使用して、受信フォルダーを開きます。 メッセージ ストア プロバイダーのログオン オブジェクトへのポインターを使っている場合は、 **IMSLogon::OpenEntry**を呼び出します。 これらの呼び出しは、MAPI 経由ではなく、メッセージ ストア プロバイダーに直接移動、ため処理が速くなります。 フォルダーを開いている場合は、既にあることを開き、開いているフォルダーの**IMAPIContainer::OpenEntry**メソッドを呼び出して、フォルダーのサブフォルダーです。 **IMAPIContainer**メソッドでは、現在開いているフォルダーのサブフォルダーのみが開き、短期的なエントリの識別子を使用する唯一の方法が保証します。 
    
3. 開かれるフォルダーに変更を加えることができる場合は、アクセス レベルを指定するには、いずれかの MAPI\_ベスト\_アクセスまたは MAPI\_の**OpenEntry**呼び出しのフラグを変更します。 これらのフラグは、MAPI の最上位のレベルのアクセスを許可するメッセージ ストア プロバイダーへのご提案\_ベスト\_へのアクセスまたは読み取り/書き込みアクセスは、MAPI の\_を変更するフォルダーを開くとき。 

   これらのフラグは提案のみであるため、フォルダー可能性がありますか、期待どおりのアクセス レベルで開くことができません可能性があります。 **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティを取得するには、開いているフォルダーで実行できる操作の範囲を指定できます。 
    
   ただし、メッセージ ストア プロバイダーの多くは、フォルダーのプロパティ、または、階層テーブル内の列としてサポートしているのではなく、要求時にこのプロパティの値を計算するための取得は、時間がかかる。 別の方法では、どのような操作を実行し、必要な場合にエラーを返す必要があります。
    
## <a name="see-also"></a>関連項目

- [PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

