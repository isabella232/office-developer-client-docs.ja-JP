---
title: MAPI ���ʂȃt�H���_�[
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2aa2376-b293-4d05-9104-218cc1fe1758
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 396a6c01d0b9cd867706a7dd4997bd6ddd7fd147
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578291"
---
# <a name="mapi-special-folders"></a>MAPI ���ʂȃt�H���_�[

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI では、特定のメッセージの種類の既定のフォルダーとして定義済みのロールを提供するために特別ないくつかのフォルダーを定義します。 これらの特別なフォルダー通常は削除できませんし、特別なエントリの識別子のプロパティがあります。
  
いくつかに含まれる個人間メッセージ (IPM) サブツリーの 8 つの特別なフォルダーがあります。 MAPI は、クライアントが、その後クライアントできる場合があります、フォルダーを削除するのには必要な場合は、メッセージ ・ ストアへのアクセスを受信する前に、これらのフォルダーを作成します。 メッセージ ストアのプロバイダーによっては、そうでないときに、削除を使用できます。 次の表では、これらのフォルダーについて説明します。
  
**MAPI �t�H���_�[**

|**�t�H���_�[**|**���**|
|:-----|:-----|
|���M�g���C] �̃t�H���_�[  <br/> |IPM �̑��M���b�Z�[�W���\������܂��B  <br/> |
|�폜�ς݃A�C�e�� �t�H���_�[  <br/> |�폜�ƃ}�[�N����Ă��� IPM ���b�Z�[�W���\������܂��B  <br/> |
|���M�ς݃A�C�e��] �t�H���_�[  <br/> |���M���ꂽ IPM ���b�Z�[�W���\������܂��B  <br/> |
|IPM ���[�g �t�H���_�[  <br/> |IPM ���b�Z�[�W��Ǘ����邽�߂̃t�H���_�[���܂܂�Ă��܂��B  <br/> |
|�t�H���_�[���\������܂��B  <br/> |����̃��b�Z�[�W�̃N���X�̎�M���b�Z�[�W���\������܂��B  <br/> |
|�������ʂ̃��[�g �t�H���_�[  <br/> |�������ʂ�Ǘ����邽�߂̃t�H���_�[���܂܂�Ă��܂��B  <br/> |
|��ʓI�ȃr���[�̃��[�g �t�H���_�[  <br/> |���b�Z�[�W �X�g�A�̃r���[��Ǘ����邽�߂̃t�H���_�[���܂܂�Ă��܂��B  <br/> |
|�l�p�r���[�̃��[�g �t�H���_�[  <br/> |����̃��[�U�[ �r���[��Ǘ����邽�߂̃t�H���_�[���܂܂�Ă��܂��B  <br/> |
   
最初の 4 つのフォルダーは、IPM サブツリー、MAPI がメッセージ ・ ストアが初期化されるときに作成するフォルダーのツリーに関連します。 対話型のメッセージング クライアントの既定のメッセージ ストアには、それらのフォルダーの階層で、IPM フォルダー サブツリーとその他の特別なフォルダーが常に含まれます。 非既定のメッセージ ストアが検索結果のルート フォルダー、IPM サブツリーのルート フォルダー、削除済みアイテム フォルダー、および受信フォルダーをサポートするためにのみ必要です。 IPM サブツリー フォルダーが存在しを有効なことを確認して、クライアントは、 [HrValidateIPMSubtree](hrvalidateipmsubtree.md)関数を呼び出すことができます。 **HrValidateIPMSubtree**は、フォルダーをチェックし、問題がある場合にそれらを再作成します。 
  
検索結果、共通のビューと個人用ビューのルート フォルダーは、IPM サブツリーです。これらのフォルダーは、メッセージ ・ ストアのルート フォルダーに作成されます。 検索結果のルート フォルダーには、一連の検索条件を満たすメッセージの内容のテーブルをサポートしているフォルダーが含まれています。 ほとんどのクライアントがすべての検索の結果の親である単一のルート フォルダーを指定するが、検索結果フォルダーの任意のフォルダー内に作成できるは、クライアント、セッション中に作成したフォルダーです。 
  
共通ビューと個人用ビューのルート フォルダーには、ビュー、またはメッセージおよびフォルダーのデータを表示する優先の方法を説明するメッセージが含まれています。 共通ビューのルート フォルダーには、クライアントがメッセージ ・ ストア内の任意のフォルダーで使用できるビューが含まれています。[個人用ビュー] フォルダーには、特定のフォルダーまたはフォルダーの特定のユーザーが定義されているビューが含まれています。
  
IPM メッセージを処理するクライアントでは、すべてのフォルダーとメッセージ ・ ストアのルート フォルダーではなく、IPM サブツリーのルート フォルダーの下のメッセージを作成します。 IPM 以外のクライアントは、この-コンピューター間または人間とコンピューター間で交換されるメッセージを処理するクライアント、IPM のクライアントからのメッセージを非表示にする簡単な方法です。 
  
MAPI では、特殊なエントリに、これらの特別なフォルダーの識別子のプロパティが割り当てられます。 特別なフォルダーのエントリ id のリストは、[メッセージ ストアのフォルダーを開く](opening-a-message-store-folder.md)を参照してください。
  
### <a name="outlook-special-folders"></a>Outlook �̓��ʂȃt�H���_�[

Outlook の特別なフォルダーは、そのエントリの受信トレイ フォルダーとメッセージ ・ ストアのルート フォルダーに格納されている Id によって識別されます。
  
|**�t�H���_�[**|**�v���p�e�B��ݒ肷��ɂ�**|
|:-----|:-----|
|�\��\  <br/> |**PR_IPM_APPOINTMENT_ENTRYID**([PidTagIpmAppointmentEntryId](pidtagipmappointmententryid-canonical-property.md))  <br/> |
|連絡先  <br/> |**PR_IPM_CONTACT_ENTRYID**([PidTagIpmContactEntryId](pidtagipmcontactentryid-canonical-property.md))  <br/> |
|ジャーナル  <br/> |**PR_IPM_JOURNAL_ENTRYID**([PidTagIpmJournalEntryId](pidtagipmjournalentryid-canonical-property.md))  <br/> |
|メモ  <br/> |**PR_IPM_NOTE_ENTRYID**([PidTagIpmNoteEntryId](pidtagipmnoteentryid-canonical-property.md))  <br/> |
|タスク  <br/> |**PR_IPM_TASK_ENTRYID**([PidTagIpmTaskEntryId](pidtagipmtaskentryid-canonical-property.md))  <br/> |
|下書き  <br/> |**PR_IPM_DRAFTS_ENTRYID**([PidTagIpmDraftsEntryId](pidtagipmdraftsentryid-canonical-property.md))  <br/> |
   
## <a name="see-also"></a>関連項目



[MAPI �t�H���_�[](mapi-folders.md)

