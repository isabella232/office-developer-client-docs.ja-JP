---
title: ���b�Z�[�W�̃X�g�A��̃t�H���_�[����J���܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d9309e47-2a92-4576-9921-c89cc48472c2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 0e7b479931b6b2b00dd3927133187fe058b4c6e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800019"
---
# <a name="exposing-folders-in-message-stores"></a>���b�Z�[�W�̃X�g�A��̃t�H���_�[����J���܂��B

  
  
**適用されます**: Outlook 
  
すべてのメッセージ ストア プロバイダーは、クライアント アプリケーションに最上位[IMAPIFolder](imapifolderimapicontainer.md)インターフェイスを提供する必要があります。 最上位のフォルダーは、全体のメッセージ ・ ストアに対応します。メッセージ ・ ストアのコンテンツとしてユーザーに表示されるフォルダーへのアクセスを提供します。 IPC メッセージおよびフォルダーと、フォルダーが表示される既定値としてさらに、最上位のフォルダーが使用多くの場合レポートが送信されるを参照するからです。 メッセージ ストア プロバイダーでは、IPM サブツリーが表示もする必要があります: IPM メッセージを格納するために使用するフォルダーのセット-クライアント アプリケーションにします。 
  
�N���C�A���g �A�v���P�[�V�����ł́A  [cbEntryId](imsgstore-openentry.md)�� _lpEntryId_�p�����[�^�[����ꂼ�� 0 �� NULL [IMsgStore::OpenEntry](imsgstore-openentry.md)���\�b�h��g�p���čŏ�ʂ̃t�H���_�[��J�����Ƃ��ł��܂��B�قƂ�ǂ̏ꍇ�A�������A�N���C�A���g �A�v���P�[�V������J���܂� IPM ���b�Z�[�W���܂܂�Ă���t�H���_�[�̐ݒ�B 
  
メッセージ ストアの IPM のフォルダー ツリー内のフォルダーの一覧を取得するには、次の手順に従います。
  
1. [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)���\�b�h��Ăяo���AMAPI �Z�b�V������g�p���܂��B 
    
2. **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) のプロパティの[IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出すには、結果のメッセージ データベースのポインターを使用します。
    
3. [IMAPIFolder](imsgstore-openentry.md)�|�C���^�[��擾�G���g�����ʎq�����**IMsgStore::OpenEntry**���\�b�h��Ăяo���܂��B 
    
4. �t�H���_�[�̓�e�̃e�[�u����擾����[IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md)���\�b�h��Ăяo���܂��B 
    
5. 最上位のフォルダー内のフォルダーを一覧表示する[IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出します。 
    
MAPI クライアントでは、他のフォルダーのオブジェクトとメッセージ ・ ストア内のメッセージ オブジェクトにアクセスするのにはこれらのフォルダーを使用します。 **IMAPIFolder**、およびその親インターフェイス[IMAPIContainer](imapicontainerimapiprop.md)には、メッセージ オブジェクトを含むフォルダーを作成し、メッセージを処理するクライアント要求に応答する、メッセージ ストア プロバイダーを実装する必要がありますメソッドが含まれています。
  
## <a name="see-also"></a>�֘A����



[���[���̕ۑ��ꏊ�Ńt�H���_�[��������܂��B](implementing-folders-in-message-stores.md)

