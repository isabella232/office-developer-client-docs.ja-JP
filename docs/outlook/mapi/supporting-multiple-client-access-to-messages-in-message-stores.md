---
title: ���[���̕ۑ��ꏊ�ŕ����N���C�A���g�̃��b�Z�[�W�ւ̃A�N�Z�X��T�|�[�g
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b13fbb9f2807c9814fed5ba3bcca8fe73aaa7b01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564221"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>���[���̕ۑ��ꏊ�ŕ����N���C�A���g�̃��b�Z�[�W�ւ̃A�N�Z�X��T�|�[�g

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
複数のクライアント アプリケーションが特定のメッセージを同時に開くことができます。 メッセージ ストア プロバイダーは、このようなアクセスを制御するための特定の規則に従う必要はありません。 ただし、クライアント アプリケーションは、メッセージを変更すると、それらの変更内容を保存、ストア プロバイダーは次の規則に従う必要があります。
  
- ���b�Z�[�W��J���Ă���B��̃N���C�A���g�̏ꍇ�Ɠ��l�ɑ��s����[IMAPIProp::SaveChanges](imapiprop-savechanges.md)���\�b�h�̍ŏ��̌Ăяo��������܂��B 
    
- �㑱 **SaveChanges**�ʘb�𑼂̃N���C�A���g�ɂ���āA���b�Z�[�W �X�g�A �v���o�C�_�[���ύX�𖳎����AMAPI_E_OBJECT_CHANGED ��Ԃ��K�v������܂��B 
    
- FORCE_SAVE �t���O������x **SaveChanges**�Ăяo���ɂ��AMAPI_E_OBJECT_CHANGED ���^�[�� �R�[�h�ɑΉ�����A�v���P�[�V�����ɃN���C�A���g��g�p�ł��܂��B�N���C�A���g �A�v���P�[�V�����ł́A���b�Z�[�W �X�g�A �v���o�C�_�[�́A�V�����ňȑO�̕ύX��u�������Ă��������B 
    
�܂��́A���b�Z�[�W �X�g�A �v���o�C�_�[�́A��������o���A���[�U�[���A���̃��b�Z�[�W��ێ�����A�V�����ύX] �ŁA���̃��b�Z�[�W��㏑������A�܂��͕ʂ̏ꏊ�ɕύX��ۑ����邩�ǂ�����I��ł���C���^�[�t�F�C�X��s�����Ƃ��ł��܂��B
  
## <a name="see-also"></a>�֘A����



[���[���̕ۑ��ꏊ�Ń��b�Z�[�W��������܂��B](implementing-messages-in-message-stores.md)

