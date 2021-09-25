---
title: MAPI プロパティのエラーの処理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 23d68d8b-b0b6-4c32-8404-6acd23802db0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: a1c4877dae64ae1890557a40723edbc66e07552b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59580154"
---
# <a name="handling-mapi-property-errors"></a>MAPI プロパティのエラーの処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
�S�ʓI�Ɏ��s�����܂��͐��������ꍇ�́A����ɂ́A���� **IMAPIProp**���@�́A�����I�Ȑ�����񍐂��܂��B 
  
[GetProps](imapiprop-getprops.md)
  
[SetProps](imapiprop-setprops.md)
  
[DeleteProps](imapiprop-deleteprops.md)
  
[CopyTo](imapiprop-copyto.md)
  
[CopyProps](imapiprop-copyprops.md)
  
**GetProps** reports partial success when it can retrieve at least one of the requested properties for an object. **GetProps** indicates partial success by returning the warning MAPI_W_ERRORS_RETURNED and placing information about the unavailable properties in the property value array pointed to by the **lppPropArray** parameter. An unavailable property's entry in this array contains PT_ERROR for the property type in the **ulPropTag** member and MAPI_E_NOT_FOUND or another appropriate error value for the **Value** member. For example, if a client calls a folder's **GetProps** method to retrieve three properties and the third is unavailable, the message store provider places PT_ERROR in the third property type in the property value array and MAPI_E_NOT_FOUND in the third property value. 
  
**IMAPIProp**���̕��@�ł́A�قȂ镔���I�Ȑ�����񍐂��܂��B�����̕��@�ł́AS_OK ��Ԃ�[SPropProblemArray](spropproblemarray.md)�\����̃G���[����z�u���ĕ����I�Ȑ�����񍐂��܂��B���\�b�h�̐����܂��͎��s�������ǂ����Ɋ֌W�Ȃ��f�[�^���܂܂�� **GetProps**�̃v���p�e�B�l�̔z��Ƃ͈قȂ�A���M�҂ɂ́A�G���[�ɂ��Ċw�K���o�^����Ă���ꍇ�ɂ̂݁A�G���[������ꍇ�ɂ݂̂����̕��@�Ńv���p�e�B�̖��̔z�񂪑��݂��܂��B���M�҂ɂ́A�G���[����o�^����L���� **SPropProblemArray**�|�C���^�[��w�肷��K�v������܂��B 
  
**SetProps**�A **DeleteProps**�A **CopyTo**�A�܂��� **CopyProps**����Ԃ��ꂽ�ꍇ�A�G���[�l�A�����̕����ł͂Ȃ��G���[������Ă��܂��B�v���p�e�B���z��ŁA�g�p�\�ȏꍇ�͖����ł��B�N���C�A���g���������\���ɕێ�����Ă���f�[�^�ɃA�N�Z�X����ɂ��Ă�\�����̂������悤�K�v������܂��B�K�؂ȉ�����[IMAPIProp::GetLastError](imapiprop-getlasterror.md)���܂��B 
  
**GetLastError**�́AWindows SDK �ɓ������O�̊֐��Ɏ��Ă��܂��B�߂�l�Ŏg�p�ł���ł͂Ȃ����ڍׂȃG���[�Ɋւ�����̑o����񋟂��܂��B���҂́A�O�̃G���[�������������ƂɊւ������Ԃ��܂��B���́AWin32 **GetLastError**�֐��̌Ăяo�����̃X���b�h�ɂ���Đ������ꂽ�G���[ ���|�[�g **IMAPIProp::GetLastError**����݂̃I�u�W�F�N�g�ɂ���Đ������ꂽ�G���[�̕񍐂ł��B�܂�A�N���C�A���g�ł́A���b�Z�[�W�� MAPI_E_NO_ACCESS �� **DeleteProps**��Ăяo���ꍇ�́A���̃��b�Z�[�W�͓ǂݎ���p�A **GetLastError**���b�Z�[�W����񋟂��ꂽ�f�[�^��Ԃ����Ƃ�����Ԃ���܂��B 
  
## <a name="see-also"></a>関連項目

- [MAPI のプロパティの概要](mapi-property-overview.md)

