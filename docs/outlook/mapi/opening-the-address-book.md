---
title: アドレス帳を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 62a4e6a09570cc3d71b0797ed7fff162d05ee416
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583688"
---
# <a name="opening-the-address-book"></a>アドレス帳を開く

**適用されます**: Outlook 2013 |Outlook 2016 
  
���M��[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)�𓝍����ꂽ�A�h���X����J���AMAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)�C���^�[�t�F�C�X�ւ̃|�C���^�[��擾���܂��B���ׂẴv���t�@�C���ŃA�h���X���̃v���o�C�_�[�̊e�R���e�i�[��̍��ڂɃA�N�Z�X���� **IAddrBook**�C���^�[�t�F�C�X�̃��\�b�h��g�p���邱�Ƃ��ł��܂��B 
  
**OpenAddressBook**�x���AMAPI_W_ERRORS_RETURNED�A�A�h���X���̃v���o�C�_�[�� 1 �ȏ�̖�肪�����������Ƃ������Ԃ����Ƃ�����܂��B�Θb�^�̃N���C�A���g�K�v������܂�[IMAPISession::GetLastError](imapisession-getlasterror.md)��Ăяo�� **OpenAddressBook**�Ԃ��ꂽ���A�ŏ��̎��Ԃ�\�����邻�̑��̃G���[����擾���A�x�����Ԃ���܂��B 
  
�Θb�^�̃N���C�A���g���x���𖳎����Ă̕��@�����������ꍇ�A�菇�ɐi�݂܂��B�Ԃ���� **IAddrBook**�C���^�[�t�F�C�X���L�����ǂ����Ɋ֌W�Ȃ����ׂāA�ꕔ�A�܂��̓A�h���X���v���o�C�_�[ �v���t�@�C����� [�Ȃ�] ����s���Ă��܂��B���̂��߁A�Z�b�V�������I�������Ƃ��ɁA **IAddrBook**�|�C���^�[��������Θb�^�ƑΘb�^�̗����̃N���C�A���g��o���Ă����Ă��������B 
  

