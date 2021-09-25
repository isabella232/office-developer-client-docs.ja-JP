---
title: メッセージ ストア フォルダーを開く
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cdd271a72166204a7c1a2f6c23b00c31f3489455
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555973"
---
# <a name="opening-a-message-store-folder"></a>メッセージ ストア フォルダーを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーを開く前に、そのエントリ識別子を使用できる必要があります。 ほとんどのフォルダーでは、このプロパティを **取得PR_ENTRYID意味** します。 IPM サブツリー フォルダーの一部や他のルート フォルダーなどの特別なフォルダーの場合、MAPI はメッセージ ストアの **IMAPIProp::GetProps** メソッドを呼び出すことによってアクセスできる特別なエントリ識別子プロパティを定義します。 これらのエントリ識別子は常に長期であり、次のように名前が付きます。 
  
|**Folder**|**エントリ識別子プロパティ**|
|:-----|:-----|
|���M�g���C] �̃t�H���_�[  <br/> |**PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md)) (IPM メッセージ クラスのみ)  <br/> |
|削除済みアイテム フォルダー  <br/> |**PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|���M�ς݃A�C�e��] �t�H���_�[  <br/> |**PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM ���[�g �t�H���_�[  <br/> |**PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|�������ʂ̃��[�g �t�H���_�[  <br/> |**PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|共通ビューのルート フォルダー  <br/> |**PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|個人用ビューのルート フォルダー  <br/> |**PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|連絡先のルート フォルダー  <br/> |**PR_IPM_CONTACT_ENTRYID** ([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|下書きルート フォルダー  <br/> |**PR_IPM_DRAFTS_ENTRYID** ([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|ジャーナル ルート フォルダー  <br/> |**PR_IPM_JOURNAL_ENTRYID** ([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|予定表のルート フォルダー  <br/> |**PR_IPM_APPOINTMENT_ENTRYID** ([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|Notes ルート フォルダー  <br/> |**PR_IPM_NOTE_ENTRYID** ([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|タスクのルート フォルダー  <br/> |**PR_IPM_TASK_ENTRYID** ([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
これらの特別なエントリ識別子のいずれかを取得する前に、メッセージ ストアの **\_ PR** VALID_FOLDER_MASK ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) プロパティを取得します。 **PR \_VALID_FOLDER_MASK** は、存在する特別なエントリ識別子を識別するビットマスクです。 特別なフォルダーごとに 1 ビットがあります。 ビットが設定されている場合は、対応するフォルダーがサポートされ、有効なエントリ識別子を持つかどうかを示します。 たとえば、[削除済みアイテム] フォルダーが存在し、有効なエントリ識別子を持つ場合、FOLDER IPM_WASTEBASKET_VALID ビットは 、 に \_ **設定PR_VALID_FOLDER_MASK。** 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>特定のクラスのすべての受信メッセージが配置されているフォルダーを開きます
  
1. [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md)を呼び出して、そのエントリ識別子を取得し _、lpszMessageClass_ パラメーターがメッセージ クラスを識別する文字列を指す設定を行います。 たとえば、IPM サブツリーの受信トレイを開く場合は  _、lpszMessageClass を_ IPM にポイントします。 IPC メッセージの受信フォルダーを開く場合は、IPC をポイントに設定します。 

   メッセージ クラスに登録済みの受信フォルダーがない場合 **、GetReceiveFolder** は、関連付けられたメッセージ クラスが渡されたメッセージ クラスの最長プレフィックスと一致する受信フォルダーを選択します。 詳細については [、「MAPI 受信フォルダー」を参照してください](mapi-receive-folders.md)。 
   
   **PR_IPM_OUTBOX_ENTRYIDプロパティは、IPM** メッセージの送信ボックス フォルダーを開くのに使用されます。 IPC メッセージの送信ボックスを開く場合は、受信フォルダーのエントリ識別子を代わりに使用します。 受信 IPC メッセージと送信 IPC メッセージの両方が受信フォルダーに配置されます。 
    
2. 4 つの **OpenEntry** メソッドのいずれかを呼び出してフォルダーを開き、アクセスに使用できるインターフェイス ポインターを返します。 次のいずれかのメソッドを呼び出して、フォルダーを開きます。 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   選択する特定の方法は、開くフォルダーと、その時点で使用可能なオブジェクトによって異なります。 **IMAPISession** メソッドは、現在のプロファイル内の任意のメッセージ ストアの任意のフォルダーを開くことができるので、開くフォルダーについて何も知らない場合は、**この OpenEntry** を呼び出します。 どのメッセージ ストアがフォルダーを所有し、メッセージ ストアへのポインターを持っている場合は **、IMsgStore::OpenEntry を呼び出します**。 
    
   たとえば **、IMsgStore メソッドを使用して** 受信フォルダーを開きます。 メッセージ ストア プロバイダーのログオン オブジェクトへのポインターがある場合は **、IMSLogon::OpenEntry を呼び出します**。 これらの呼び出しは、MAPI 経由ではなくメッセージ ストア プロバイダーに直接送信されるので、処理が高速になります。 開いているフォルダーが既に開いているフォルダーのサブフォルダーである場合は、開いているフォルダーの **IMAPIContainer::OpenEntry メソッドを呼び出** します。 **IMAPIContainer** メソッドは、現在開いているフォルダーのサブフォルダーのみを開き、短期的なエントリ識別子で動作する唯一のメソッドです。 
    
3. 開くフォルダーを変更できる場合は \_ \_ \_ **、OpenEntry** 呼び出しで MAPI BEST ACCESS フラグまたは MAPI MODIFY フラグを設定してアクセス レベルを指定します。 これらのフラグは、MAPI BEST ACCESS または読み取り/書き込みアクセスを MAPI MODIFY でフォルダーを開く際に、最高レベルのアクセスを許可するメッセージ ストア プロバイダーへの提案 \_ \_ \_ です。 

   これらのフラグは候補にしか含めないので、フォルダーは期待するアクセス レベルで開く場合と開かない場合があります。 プロパティ (  [PidTagAccess](pidtagaccess-canonical-property.md)) PR_ACCESSを取得することで、開いているフォルダーで実行できる操作の範囲を決定できます。 
    
   ただし、多くのメッセージ ストア プロバイダーは、フォルダー プロパティとして、または階層テーブル内の列としてサポートするのではなく、このプロパティの値をオンデマンドで計算しますので、取得には時間がかかる場合があります。 別の方法は、実行する必要がある操作を試み、必要に応じてエラーを返す方法です。
    
## <a name="see-also"></a>関連項目

- [PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

