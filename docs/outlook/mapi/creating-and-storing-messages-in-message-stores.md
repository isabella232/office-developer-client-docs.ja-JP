---
title: �쐬�ƃ��b�Z�[�W �X�g�A�Ń��b�Z�[�W��ۑ����܂��B
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589176"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>�쐬�ƃ��b�Z�[�W �X�g�A�Ń��b�Z�[�W��ۑ����܂��B

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
���b�Z�[�W �X�g�A �v���o�C�_�[��쐬���ċ@�\�L����Ƀ��b�Z�[�W��i�[������@�A��ɂȂ�L���惁�J�j�Y�����̂ɑ傫���ˑ����܂��B��ʂɁA���b�Z�[�W�Ƃ��̒l�̃v���p�e�B��ێ����邽�߂̃R�[�h��L�q�݂̂ɂ���K�v������܂��B
  
���b�Z�[�W�̕ۑ����v���o�C�[�[�́A�V�������b�Z�[�W��쐬�A�v���o�C�](imapifolderimapicontainer.md)�[�́A���b�Z�[�W�̕K�v�ȃv���p�e�B���A���b�Z�[�W��쐬����K�v������܂��B�����̃v���p�e�B�̈ꗗ�̃h�L�������g�ɋL�ڂ���āA [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md)�C���^�[�t�F�C�X�ł��B���̌�A�N���C�A���g �A�v���P�[�V������[IMAPIProp](imapipropiunknown.md)���@�ŁA�ǉ��̃v���p�e�B��ǉ����܂��B 
  
メッセージは、プロバイダーの保存、基になるストレージ機構にメッセージを保存、するとプロバイダーは、メッセージのプロパティを反復処理し、完全に復元できる場合は、メッセージを開いた後で、基になるストレージ機構に保存する必要があります。
  
MAPI が必要です[IMessage](imessageimapiprop.md)インターフェイスのプロパティは、トランザクション処理されている、ことそれらを変更しないになることは永続的なメッセージ オブジェクトの[IMAPIProp::SaveChanges](imapiprop-savechanges.md)メソッドが呼び出されるまでを意味します。 メッセージ ストア プロバイダーは、この動作を実装します。 通常これは困難です。単にそれらを修正しているときに、メモリ内のプロパティを保持していると、**たいていは SaveChanges**が呼び出されたときに基になるストレージ機構に組み込むにも同じことを意味します。 
  
���b�Z�[�W�̃I�u�W�F�N�g�̈ꕔ�̃v���p�e�B�ł́A���̂悤�ɁA **SaveChanges**���\�b�h�Ɋ֘A����N���C�A���g �A�v���P�[�V�����ɓ��ʂȈӖ�������܂��B 
  
- **SaveChanges**が呼び出される前に、読み取り専用ですが、後で、いくつかのプロパティは読み取り/書き込みをする必要があります。 メッセージを作成し、読み取り/書き込み) をクライアント アプリケーションが**PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) を最初に設定は、たとえば、 **savechanges メソッド**の最初の呼び出し後に変更することはできませんが。
    
- �ꕔ�̃v���p�e�B�ł́A **IMAPIFolder**���@�ɂ́A[�t�H���_�[�̃v���p�e�B�ɓ��ʂ̊֌W������܂��B���Ƃ��΁A **PR_MESSAGE_FLAGS**�v���p�e�B��[IMAPIFolder::CreateMessage](imapifolder-createmessage.md)�ʘb�Ɏg�p����t���O�Ɋ֘A���Ă��܂��B 
    
- 最初に**SaveChanges**が呼び出されるまで、いくつかプロパティを使用できません可能性があります。 たとえば、 **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) はできない場合があります**SaveChanges**が呼び出されるまでです。 
    
- いくつかのプロパティは、メッセージ オブジェクトの他のプロパティに特別な関係を持つことができます。 たとえば、([PidTagBody](pidtagbody-canonical-property.md)) である**PR_BODY**プロパティは通常、リッチ テキスト形式のメッセージをサポートしているメッセージ ストア プロバイダーに、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) のプロパティから派生します。
    
- いくつかのプロパティは、メッセージ ・ ストアに関連する複数のオブジェクトの種類によって使用されます。 たとえば、フォルダーおよびオブジェクトとメッセージ オブジェクトを格納するメッセージの**PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) のプロパティが必要です。
    
���̂悤�ȃv���p�e�B�̐������Z�}���e�B�N�X��������郁�b�Z�[�W �X�g�A �v���o�C�_�[�̐ӔC���邱�Ƃ�����߂��܂��B
  
## <a name="see-also"></a>�֘A����



[���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B](implementing-messages-in-message-stores.md)

