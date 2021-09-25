---
title: MAPI �A�h���X��
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6703ba3f-54a5-4059-b10a-1d42a9e81be1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 562a3cadb6f36885e1870284e3c0d7f2aa7071aa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595904"
---
# <a name="mapi-address-book"></a>MAPI �A�h���X��

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
The integrated address book is an object that MAPI implements to provide access to an integrated collection of addressing information from all of the address book providers in the profile. With the address book, client applications and service providers do not have to differentiate between the unique addressing schemes of messaging systems. Instead, they can look up the addresses of any recipients in any messaging system, as long as the address book provider for the messaging system is installed.
  
The address book can be accessed programmatically, without user intervention, or interactively through the use of common dialog boxes. MAPI includes dialog boxes to display a summary list of the entries in the address book, detailed information about a particular recipient, a warning when a user creates a recipient that cannot be mapped to a unique address, and a set of template forms for creating new recipients.
  
MAPI �A�h���X���́A�K�w�\���ɂȂ��Ă��邱�ƂɃ��b�Z�[�W �X�g�A�\����Ɠ����ł��B�A�h���X���́A3 ��ނ̃A�h���X���v���o�C�_�[�ɂ���Ď����I�u�W�F�N�g�ւ̃A�N�Z�X��񋟂��܂��B
  
- �A�h���X���̃R���e�i�[ �I�u�W�F�N�g�ł��B
    
- �z�z���X�g �I�u�W�F�N�g�ł��B
    
- ���b�Z�[�W���O ���[�U�[ �I�u�W�F�N�g�ł��B
    
�A�h���X���v���o�C�_�[�ɂ���Ċ��蓖�Ă��Ă���A��ӂ̃G���g�����ʎq����ꂼ��̃I�u�W�F�N�g�̎�ނɃA�N�Z�X���܂��B 
  
���܂��܂Ȏ�ނ̃I�u�W�F�N�g��i�[���邱�ƂŁA�A�h���X���̃R���e�i�[�̓t�H���_�[�Ɏ��Ă��܂��B���̑��̃A�h���X���̃R���e�i�[�Ƃ��ă��b�Z�[�W���O ���[�U�[����єz�z���X�g�̃I�u�W�F�N�g��A�h���X���R���e�i�[��ێ��ł��܂��B�A�h���X���̃I�u�W�F�N�g��ۑ�����A�h���X���̃R���e�i�[��g�p���܂��B
  
To achieve the address book's integrated appearance, address book providers expose zero, one, or more of their top-level containers to MAPI which merges them and displays the results under a single top-level container. Address book providers can choose to expose one set of containers for one type of messaging session and a different set for another session. It is also possible for address book providers to have no top-level containers and expose only a list of templates that can be used to create recipients.
  
���b�Z�[�W�̃��[�U�[�Ɣz�z���X�g��̃I�u�W�F�N�g�́A���b�Z�[�W�̎�M�҂���������Ă��܂��B���b�Z�[�W�̃��[�U�[���X �̎�M�҂ł��B�z�z���X�g�́A��M�҂̃O���[�v�ł��B�e���b�Z�[�W�̃��[�U�[�́A����̃��b�Z�[�W���O �V�X�e���́A����̎�ނ̈�ӂ̃A�h���X������Ă��܂��B�z�z���X�g�́A��M�҂̖��O�t���̃R���N�V�����ł��B�z�z���X�g�ɂ́A���b�Z�[�W�̃��[�U�[ �I�u�W�F�N�g�Ƃ��̑��̔z�z���X�g��܂߂邱�Ƃ��ł��܂��B�N���C�A���g �A�v���P�[�V�����̃��[�U�[�́A�z�z���X�g�Ƀ��b�Z�[�W�𑗐M] ���b�Z�[�W�͊e���X�g�̃��b�Z�[�W�̃��[�U�[�̃����o�[�ɑ��M����邳��܂��B 
  
���b�Z�[�W�̃��[�U�[�Ɣz�z���X�g�̃x�[�X �A�h���X �v���p�e�B�ƌĂ΂�� 5 �̃v���p�e�B�̐ݒ肪����܂��B�����͕K�v�ȃv���p�e�B�ł���A���̂悤�ɊȒP�ɐ�����܂��B
  
|**��{ address �v���p�e�B**|**���**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |��M�҂̃A�h���X����͂��܂��B�e�A�h���X�̎�ނł́A����̌`���Ɉˑ����āA����̃��b�Z�[�W���O �V�X�e�����g���Ă��܂��B  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |��M�҂̖��O��\���\�Ȃł��B  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |��M�҂̃A�h���X�ł��B  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |�G���g�����ʎq����M�҂ɃA�N�Z�X���邽�߂Ɏg�p���܂��B  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |�o�C�i�������L�[����M�҂���ʂ��邽�߂Ɏg�p���܂��B  <br/> |
   
MAPI �ł́A�����̃O���[�v�̃x�[�X �A�h���X�̃v���p�e�B�̃o���G�[�V�����̃v���p�e�B���`���܂��B�����̑��̃O���[�v�́A���b�Z�[�W�̃��[�U�[�Ƃ��܂��܂ȏ󋵂ł̔z�z���X�g�ɂ��Đ�����܂��B���Ƃ��΁A�v���p�e�B�� 1 �̃O���[�v�ɂ́A���b�Z�[�W�⑼�̃O���[�v�̑㗝�l�̎�M�҂̑㗝�l�̑��M�҂��ɂ��Đ�����܂��B
  

