---
title: MAPI ��M��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 88a4360d-6ab8-466e-8ebd-af80227ee00a
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ebdaf47b4f20763574ffac73bddeb3eb4eeb95df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328218"
---
# <a name="mapi-recipients"></a>MAPI ��M��

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
���ׂẴ��b�Z�[�W�𑗐M����̂ɂ́A1 �܂��͕����̈���A�܂��͈�A�̃��b�Z�[�W�̔z�M���\���v���p�e�B�����܂��B��M�҂����b�Z�[�W�̃R���e�L�X�g�ł̂ݎg�p���邽�� MAPI �̌ʂ̃I�u�W�F�N�g�̑���Ƀ��b�Z�[�W�̃I�u�W�F�N�g�ƌ��Ȃ���܂��B�N���C�A���g�ƃv���o�C�_�[ **IMessage** �C���^�[�t�F�C�X��g�p���Ď�M�҂�g�p���܂��B�ڍׂɂ��ẮA [IMessage: IMAPIProp](imessageimapiprop.md)��Q�Ƃ��Ă��������B
  
�N���C�A���g�ł́A���̎�M�҂̃e�[�u������A���b�Z�[�W�̎�M�҂��A�N�Z�X���܂��B���ׂẴ��b�Z�[�W�ɂ́A��M�҂��M�҂̂��ꂼ��ɂ��Ă̊T�v����܂ރe�[�u��������܂��B�e�[�u���Ɋ܂܂�Ă����́A���b�Z�[�W�̏�Ԃɂ���ĈقȂ�܂��B���b�Z�[�W�́A[�\�����A���̎�M�҂́A�\��� 3 ��݂̂�����܂��B
  
- 表示名、または**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- 受信者の種類、または**PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- 行識別子、または**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
メッセージが名前解決プロセスに切り替えられた後、各受信者には、エントリ識別子または**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) 列もあります。 And when the message has been submitted, the rows in the recipient table will add two more columns:
  
- アドレスの種類、または**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- トランスポート責任、または**PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Clients can retrieve a message's recipient table by calling its **IMessage::GetRecipientTable** method or its **IMAPIProp::OpenProperty** method. For more information, see [IMessage::GetRecipientTable](imessage-getrecipienttable.md) and [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Message store providers are expected to support both of these approaches. The **OpenProperty** approach requires that the client specify IID_IMAPITable as the interface identifier and **PR_MESSAGE_RECIPIENTS** as the property tag. **PR_MESSAGE_RECIPIENTS**([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) は、メッセージの受信者テーブルを表す table オブジェクトプロパティです。 Message store providers are required to set **PR_MESSAGE_RECIPIENTS** for each message and include it in the array of property tags returned from the **IMAPIProp::GetPropList** method. For more information, see [IMAPIProp::GetPropList](imapiprop-getproplist.md).
  
��M�҂̃e�[�u���𑀍삷����@�̏ڍׂɂ��ẮA [��M�҂̃e�[�u��](recipient-tables.md)��Q�Ƃ��Ă��������B
  
��M�҂̃e�[�u���ɃA�N�Z�X���邽�߂Ɏg�p����Ă���A�ɉ����� **PR_MESSAGE_RECIPIENTS**��g�p�ł��܂��B 
  
- **IMAPIProp::CopyTo** �܂��͏��O����A�܂��̓R�s�[����Ƃ��ɁA��M�҂�܂߂�ɂ́A **IMAPIProp::CopyProps** ���܂��B���̑��̏���Q�Ƃ��Ă��������A [IMAPIProp::CopyTo](imapiprop-copyto.md)�����[IMAPIProp::CopyProps](imapiprop-copyprops.md)���܂��B
    
- �q�̐�������M�҂ɓK�p���邩��������ʐ������܂��B
    
Clients can add recipients to a message by copying entries from the MAPI address book or by creating new entries. These new entries, called one-offs, can exist temporarily or be saved permanently in a modifiable container. Whereas recipients that are taken from the address book have entry identifiers associated with their address book provider, one-off recipients have entry identifiers that are formatted by MAPI. Transport providers and clients associate one-off entry identifiers with various types of addresses. 
  
�g�����X�|�[�g �v���o�C�_�[�ʘb **IMAPISupport::CreateOneOff** ���M�̃A�h���X�� 1 �����̃G���g�����ʎq��쐬���郁�b�Z�[�W�̏ꍇ�B 
  
- �A�h���X�������Ă���Q�[�g�E�F�C���܂��B
    
- ���݂̃v���t�@�C���ŃA�h���X���v���o�C�_�[�ɂ���ẮA�A�h���X��������邱�Ƃ͂ł��܂���B
    
�ڍׂɂ��ẮA [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)��Q�Ƃ��Ă��������B
  
�N���C�A���g����M�Z���ꎞ�G���g�����ʎq��쐬����̂ɂ́A **IAddrBook::CreateOneOff** ��Ăяo�����b�Z�[�W�̏ꍇ�B 
  
- �A�h���X�́A1 �����̃A�h���X�Ƃ��Đݒ肳��܂��B
    
- �A�h���X�́A�C���^�[�l�b�g �A�h���X�Ƃ��Đݒ肳��܂��B
    
�ڍׂɂ��ẮA [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)��Q�Ƃ��Ă��������B
  
�ڍׂɂ��ẮA1 �����̃G���g�����ʎq�ƃA�h���X�A [1 �����̃G���g�����ʎq](one-off-entry-identifiers.md)��[1 �����̃A�h���X](one-off-addresses.md)��Q�Ƃ��Ă��������B
  
��M�҂̃v���p�e�B�́A�A�h���X���̃v���p�e�B�ƈ���̈���ɌŗL�̃v���p�e�B�̑g�ݍ��킹�ł��B���ׂĂ̎�M�҂ɂ́A�A�h���X���v���o�C�_�[�ɂ���Ċ��蓖�Ă��Ă���A�x�[�X �A�h���X �v���p�e�B������܂��B�G���g���́A���M���b�Z�[�W�̎�M�҂Ƃ��Ďg�p�����̃x�[�X �A�h���X �v���p�e�B�́A���ׂẴ��b�Z�[�W�̎�M�҂̃v���p�e�B��ێ����� **ADRLIST** �\���ɃR�s�[����܂��B 
  
��M�җp�ɐݒ肳��Ă��� 2 �̃v���p�e�B�́A **PR_RECIPIENT_TYPE** **PR_RESPONSIBILITY**�ł��B **PR_RECIPIENT_TYPE**�́A��M�҂��v���C�}���Acarbon copy �̗��A�u���C���h �J�[�{�� �R�s�[�A�܂��͍đ��M�����M�҂��ǂ���������܂��B�ŏ��� 3 �̎�ނ́A�ŏ��ɑ��M����郁�b�Z�[�W�̎�M�҂Ɋ��蓖�Ă��܂��B 
  
��M�҂Ƀ��b�Z�[�W���\������Ȃ��ꍇ�́A�����đ��M���悤�Ƃ��܂������A��M�҂��R�s�[����܂�����̎�ސݒ肪 MAPI_P1 ��đ��M���鈶���w�肵�܂��B�ꕔ�̎�M�҂ɂ́A���b�Z�[�W���\�������A�����̏ꍇ�A���� **PR_RECIPIENT_TYPE**�v���p�e�B�́A���b�Z�[�W��đ������Ƃ� MAPI_SUBMITTED �t���O�̓�e�ƃ}�[�N����܂��B�N���C�A���g�̓v���C�}���̎�M�҂�������邽�߂ɕK�v�Ȃ܂��́A **PR_RECIPIENT_TYPE**�����M�҂� MAPI_TO �ɐݒ肵�܂��B���̑��̂��ׂĂ̎�ނ̓I�v�V�����ł��B 
  
 **PR_RESPONSIBILITY** is set to indicate to the transport provider whether or not it should handle sending to the recipient. When an outgoing message is first sent, all of the recipients set **PR_RESPONSIBILITY** to FALSE. As a transport provider claims responsibility for sending to one or more of the recipients, their **PR_RESPONSIBILITY** properties are set to TRUE. 
  

