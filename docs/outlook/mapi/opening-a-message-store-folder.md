---
title: メッセージ ストア フォルダーを開く
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d858e4fe-822e-4330-9ed3-4b7d22fa51dc
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: df7db013cb435484c721388abab51ab4ba43828f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331375"
---
# <a name="opening-a-message-store-folder"></a>メッセージ ストア フォルダーを開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
フォルダーを開く前に、そのエントリ識別子を使用できるようにする必要があります。 ほとんどのフォルダーについては、 **PR_ENTRYID**のプロパティを取得することを意味します。 一部の IPM サブツリーフォルダーやその他のルートフォルダーなどの特別なフォルダーの場合、MAPI は、メッセージストアの**imapiprop:: GetProps**メソッドを呼び出すことによってアクセスできる特殊なエントリ識別子プロパティを定義します。 これらのエントリ識別子は常に長期間で、次のように名前が付けられます。 
  
|**Folder**|**エントリ id プロパティ**|
|:-----|:-----|
|���M�g���C] �̃t�H���_�[  <br/> |**PR_IPM_OUTBOX_ENTRYID**([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))(IPM メッセージクラスのみ)  <br/> |
|削除済みアイテム フォルダー  <br/> |**PR_IPM_WASTEBASKET_ENTRYID**([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))  <br/> |
|���M�ς݃A�C�e��] �t�H���_�[  <br/> |**PR_IPM_SENTMAIL_ENTRYID**([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))  <br/> |
|IPM ���[�g �t�H���_�[  <br/> |**PR_IPM_SUBTREE_ENTRYID**([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))  <br/> |
|�������ʂ̃��[�g �t�H���_�[  <br/> |**PR_FINDER_ENTRYID**([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))  <br/> |
|共通ビューのルートフォルダー  <br/> |**PR_COMMON_VIEWS_ENTRYID**([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))  <br/> |
|個人用ビューのルートフォルダー  <br/> |**PR_VIEWS_ENTRYID**([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))  <br/> |
|連絡先のルートフォルダー  <br/> |**PR_IPM_CONTACT_ENTRYID**([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|下書きルートフォルダー  <br/> |**PR_IPM_DRAFTS_ENTRYID**([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
|ジャーナルルートフォルダー  <br/> |**PR_IPM_JOURNAL_ENTRYID**([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|予定表のルートフォルダー  <br/> |**PR_IPM_APPOINTMENT_ENTRYID**([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|メモルートフォルダー  <br/> |**PR_IPM_NOTE_ENTRYID**([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|タスクルートフォルダー  <br/> |**PR_IPM_TASK_ENTRYID**([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
   
これらの特殊なエントリ識別子のいずれかを取得しようとする前に、メッセージストアの**\_PR VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) プロパティを取得します。 **PR\_VALID_FOLDER_MASK**は、どの特別なエントリ識別子が存在するかを識別するビットマスクです。 特別なフォルダーには1ビットがあります。 ビットが設定されている場合は、対応するフォルダーがサポートされ、有効なエントリ識別子があることを示します。 たとえば、削除済みアイテムフォルダーが存在し、有効なエントリ識別子がある場合、\_フォルダー IPM_WASTEBASKET_VALID ビットが**PR_VALID_FOLDER_MASK**に設定されます。 
  
## <a name="open-the-folder-where-all-incoming-messages-of-a-particular-class-are-placed"></a>特定のクラスのすべての受信メッセージが配置されているフォルダーを開きます。
  
1. [IMsgStore:: getreceivefolder](imsgstore-getreceivefolder.md)を呼び出して、そのエントリ id を取得し、 _lpszmessageclass_パラメーターを設定して、メッセージクラスを識別する文字列を指すようにします。 たとえば、ipm サブツリーの受信トレイを開く場合は、[ipm _messageclass_ ] を [ipm] に指定します。 ipc メッセージの受信フォルダーを開く必要がある場合は、ipc をポイントするように設定します。 

   メッセージクラスの受信フォルダーが登録されていない場合、 **getreceivefolder**は、渡されたメッセージクラスの最長有効なプレフィックスに一致するメッセージクラスを持つ受信フォルダーを選択します。 詳細については、「 [MAPI 受信フォルダー](mapi-receive-folders.md)」を参照してください。 
   
   **PR_IPM_OUTBOX_ENTRYID**プロパティを使用して、IPM メッセージに対してのみ送信トレイフォルダーが開かれることに注意してください。 IPC メッセージの送信トレイを開いている場合は、代わりにその受信フォルダーのエントリ識別子を使用します。 受信および送信 IPC メッセージは両方とも、受信フォルダーに配置されます。 
    
2. 4つの**openentry**メソッドの1つを呼び出して、フォルダーを開き、それにアクセスするために使用できるインターフェイスポインターを返します。 フォルダーを開くには、次のいずれかのメソッドを呼び出すことができます。 
    
   - [IMAPISession::OpenEntry](imapisession-openentry.md)
    
   - [IMSLogon::OpenEntry](imslogon-openentry.md)
    
   - [IMsgStore::OpenEntry](imsgstore-openentry.md)
    
   - [IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
    
   選択する具体的な方法は、開かれるフォルダーと、その時点で使用可能なオブジェクトによって異なります。 **imapisession**メソッドは、現在のプロファイルにある任意のメッセージストアの任意のフォルダーを開くことができるので、開くフォルダーに関する情報がわからない場合にこの**openentry**を呼び出します。 フォルダーを所有しているメッセージストアと、メッセージストアへのポインターがあることがわかっている場合は、 **IMsgStore:: openentry**を呼び出します。 
    
   たとえば、受信フォルダーを開くには、 **IMsgStore**メソッドを使用します。 メッセージストアプロバイダーのログオンオブジェクトへのポインターがある場合は、 **IMSLogon:: openentry**を呼び出します。 これらの呼び出しは MAPI ではなくメッセージストアプロバイダーに直接移動するので、処理が速くなります。 開こうとしているフォルダーが既に開いているフォルダーのサブフォルダーである場合は、開いているフォルダーの**IMAPIContainer:: openentry**メソッドを呼び出します。 **IMAPIContainer**メソッドは、現在開かれているフォルダーのサブフォルダーのみを開き、短い用語のエントリ識別子に対応することを保証する唯一の方法です。 
    
3. 開くフォルダーを変更できるようにするには\_、 **openentry**呼び出しで mapi の BEST\_access または mapi\_の変更フラグを設定して、アクセスレベルを指定します。 これらのフラグは、フォルダーを開くときに、mapi での\_最高\_のアクセス許可、または読み取り/書き込みアクセス権\_の最高レベルのアクセスを付与するために、メッセージストアプロバイダーに推奨されています。 

   これらのフラグは候補に限定されるので、必要なアクセスレベルでフォルダーが開かれる場合と、開かない場合があります。 **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md)) プロパティを取得することにより、開いているフォルダーに対して実行できる操作の範囲を決定できます。 
    
   ただし、多くのメッセージストアプロバイダーは、フォルダープロパティとして、または階層テーブル内の列としてサポートするのではなく、必要に応じてこのプロパティの値を計算するので、取得に時間がかかることがあります。 別の方法として、実行する必要がある任意の操作を試行し、必要に応じてエラーを返すようにすることができます。
    
## <a name="see-also"></a>関連項目

- [PidTagEntryId 標準プロパティ](pidtagentryid-canonical-property.md) 
- [IMAPIProp::GetProps](imapiprop-getprops.md)

