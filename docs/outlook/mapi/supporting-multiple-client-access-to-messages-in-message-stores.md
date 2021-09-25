---
title: ���[���̕ۑ��ꏊ�ŕ����N���C�A���g�̃��b�Z�[�W�ւ̃A�N�Z�X��T�|�[�g
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 31885c64-edb2-4a87-8730-09f163dedd40
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 907dd58dd06ed538a34c659bcd697bdacb16afbf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624105"
---
# <a name="supporting-multiple-client-access-to-messages-in-message-stores"></a>���[���̕ۑ��ꏊ�ŕ����N���C�A���g�̃��b�Z�[�W�ւ̃A�N�Z�X��T�|�[�g

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
It is possible for multiple client applications to open a given message simultaneously. Message store providers do not have to follow any particular rules for governing such access. However, if the client applications modify the message and save their changes, the store provider should comply with the following rules:
  
- ���b�Z�[�W��J���Ă���B��̃N���C�A���g�̏ꍇ�Ɠ��l�ɑ��s����[IMAPIProp::SaveChanges](imapiprop-savechanges.md)���\�b�h�̍ŏ��̌Ăяo��������܂��B 
    
- �㑱 **SaveChanges**�ʘb�𑼂̃N���C�A���g�ɂ���āA���b�Z�[�W �X�g�A �v���o�C�_�[���ύX�𖳎����AMAPI_E_OBJECT_CHANGED ��Ԃ��K�v������܂��B 
    
- FORCE_SAVE �t���O������x **SaveChanges**�Ăяo���ɂ��AMAPI_E_OBJECT_CHANGED ���^�[�� �R�[�h�ɑΉ�����A�v���P�[�V�����ɃN���C�A���g��g�p�ł��܂��B�N���C�A���g �A�v���P�[�V�����ł́A���b�Z�[�W �X�g�A �v���o�C�_�[�́A�V�����ňȑO�̕ύX��u�������Ă��������B 
    
�܂��́A���b�Z�[�W �X�g�A �v���o�C�_�[�́A��������o���A���[�U�[���A���̃��b�Z�[�W��ێ�����A�V�����ύX] �ŁA���̃��b�Z�[�W��㏑������A�܂��͕ʂ̏ꏊ�ɕύX��ۑ����邩�ǂ�����I��ł���C���^�[�t�F�C�X��s�����Ƃ��ł��܂��B
  
## <a name="see-also"></a>関連項目



[メッセージ ストアのメッセージの実装](implementing-messages-in-message-stores.md)

