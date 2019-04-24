---
title: アドレス帳を開く
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6d1a7e8e1d9debd7eb715bbe4958657c000f1e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326167"
---
# <a name="opening-the-address-book"></a>アドレス帳を開く

**適用対象**: Outlook 2013 | Outlook 2016 
  
���M��[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md)�𓝍����ꂽ�A�h���X����J���AMAPI [IAddrBook: IMAPIProp](iaddrbookimapiprop.md)�C���^�[�t�F�C�X�ւ̃|�C���^�[��擾���܂��B���ׂẴv���t�@�C���ŃA�h���X���̃v���o�C�_�[�̊e�R���e�i�[��̍��ڂɃA�N�Z�X���� **IAddrBook**�C���^�[�t�F�C�X�̃��\�b�h��g�p���邱�Ƃ��ł��܂��B 
  
**OpenAddressBook**�x���AMAPI_W_ERRORS_RETURNED�A�A�h���X���̃v���o�C�_�[�� 1 �ȏ�̖�肪�����������Ƃ������Ԃ����Ƃ�����܂��B�Θb�^�̃N���C�A���g�K�v������܂�[IMAPISession::GetLastError](imapisession-getlasterror.md)��Ăяo�� **OpenAddressBook**�Ԃ��ꂽ���A�ŏ��̎��Ԃ�\�����邻�̑��̃G���[����擾���A�x�����Ԃ���܂��B 
  
�Θb�^�̃N���C�A���g���x���𖳎����Ă̕��@�����������ꍇ�A�菇�ɐi�݂܂��B�Ԃ���� **IAddrBook**�C���^�[�t�F�C�X���L�����ǂ����Ɋ֌W�Ȃ����ׂāA�ꕔ�A�܂��̓A�h���X���v���o�C�_�[ �v���t�@�C����� [�Ȃ�] ����s���Ă��܂��B���̂��߁A�Z�b�V�������I�������Ƃ��ɁA **IAddrBook**�|�C���^�[��������Θb�^�ƑΘb�^�̗����̃N���C�A���g��o���Ă����Ă��������B 
  

