---
title: 名前付きプロパティのエラーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f56c56d8-db46-4c69-876f-2bbb4a5c1185
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6942690214af49274608a48490b8437bd59bff24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59551500"
---
# <a name="handling-named-property-errors"></a>名前付きプロパティのエラーの処理
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)�܂���[IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md)�傫�����鏈�����������悤�ɗv������ꍇ�A�G���[�l MAPI_E_TOO_BIG ���Ԃ���܂��B���M�҂ɉ�������K�v������܂��A�o�Ȉ˗��ɕ����A�������̈˗��A���[�v�œK�؂ȃ��\�b�h���܂��B 
  
�����I�Ȑ�������ƁA����̎��ʎq�ɑΉ��t���閼�O�͗v���ꍇ�ȂǁA1 �ȏ�̖��O�ŁA�Ăяo���̌��ʂ�������Ȃ��ꍇ�ɁA **GetNamesFromIDs**�� MAPI_W_ERRORS_RETURNED ��Ԃ��܂��B ���A�v���p�e�B�A�v���p�e�B�̃^�O�̔z��ŕs�����Ă���v���p�e�B�̃f�[�^�^�� PT_ERROR ��z�u���܂��B 
  
�N���C�A���g�� **GetNamesFromIDs**�̓v���p�e�B����̂悤�ȕԂ���錋�ʂɌĂяo����s�����Ƃ�����܂������O�t���̂��ׂẴv���p�e�B�́A�t���O�ɂ���ď��O�̎�ނ��A�w�肵���v���p�e�B��ݒ肷��ɂ̓v���p�e�B���܂܂�Ă��Ȃ��ꍇ�ɂ��܂��B�N���C�A���g���T�[�r�X �v���o�C�_�[����߂邱�Ƃ��ł��܂��B 
  
- S_OK ��Ԃ��܂��B
    
- �V���Ɋ��蓖�Ă�ꂽ�v���p�e�B �^�O�z��Ƀv���p�e�B �^�O�z��|�C���^�[�̓�e��ݒ肷��ɂ́A **cValues**�����o�[�� 0 �ɐݒ肵�܂��B 
    
- [MAPINAMEID](mapinameid.md)�\���̔z��̓�e�� NULL �ɐݒ肵�܂��B 
    
- 0 �� **MAPINAMEID**�\���̐��̓�e��ݒ肵�܂��B 
    
## <a name="see-also"></a>関連項目

- [MAPI ���O�t���v���p�e�B](mapi-named-properties.md)

