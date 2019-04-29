---
title: ipropdatahrgetpropaccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5e36cf12b7a5b1643f5a0ec97223030718195a7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433438"
---
# <a name="ipropdatahrgetpropaccess"></a>IPropData::HrGetPropAccess

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
�A�N�Z�X ���x���� 1 �܂��͕����̃I�u�W�F�N�g�̃v���p�e�B�̏�Ԃ�擾���܂��B
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>パラメーター

 _lppPropTagArray_
  
> [�`�F�b�N �A�E�g]�A�N�Z�X ���x���ƃX�e�[�^�X��擾���邽�߂̃v���p�e�B������v���p�e�B �^�O�̔z��̓��͂���ȊO�̏ꍇ�A�|�C���^�[�� NULL ���� **HrGetPropAccess**�ɂ́A�A�N�Z�X ���x���Ƃ��ׂẴv���p�e�B�̏�Ԃ�擾����K�v������܂��B �o�͂ł́A�ǂ̃A�N�Z�X�ƃX�e�[�^�X�̃t���O�̃v���p�e�B�̃^�O�̔z�񂪎擾����܂����B�t���O�� _lprgulAccess_�p�����[�^�[��w���z��Ɋi�[����܂��B 
    
 _lprgulAccess_
  
> [�o��]�t���O �r�b�g�}�X�N�̔z��ւ̃|�C���^�[�B�e�r�b�g�́A�A�N�Z�X ���x�����]�A�܂��͂��̗����� _lpPropTagArray_�p�����[�^�[��w���A�z���̓���̃v���p�e�B���\������܂��B2 �̔z��A�ʒu _lprgulAccess_�|�C���g��̍ŏ��̃v���p�e�B�Ő������ŏ��̃r�b�g���� _lpPropTagArray_�|�C���g�Ȃǂł��B �v���p�e�B�̃^�O���ƂɁA���̃t���O��ݒ�ł��܂��B 
    
|**�A�N�Z�X ���x���̃t���O**|**�t���O�̏��**|
|:-----|:-----|
|IPROP_READONLY �v���p�e�B��ύX�ł��Ȃ����Ƃ�����܂��B  <br/> |IPROP_CLEAN �v���p�e�B���ύX����Ă��Ȃ����Ƃ�����܂��B  <br/> |
|IPROP_READWRITE �v���p�e�B��ύX�ł��邱�Ƃ�����܂��B  <br/> |IPROP_DIRTY �v���p�e�B���ύX����Ă��邱�Ƃ�����܂��B  <br/> |
   
## <a name="return-value"></a>戻り値

S_OK 
  
> �v���p�e�B�̃A�N�Z�X ���x���Ə�ԃt���O������ɕԂ���܂���B
    
## <a name="remarks"></a>注釈

**IPropData::HrGetPropAccess**���\�b�h�́A�A�N�Z�X ���x���� 1 �ȏ�̃v���p�e�B�̏�Ԃ�����t���O�̐ݒ��擾���܂��B 
  
## <a name="notes-to-callers"></a>呼び出し元に関するメモ:

**HrGetPropAccess**��́A���̖ړI�Ŏg�p�ł��܂��B 
  
- �N���C�A���g���ύX���ꂽ�܂��͏������݉\�ȃv���p�e�B��폜���邩�ǂ�����m�F���܂��B
    
- �N���C�A���g��ύX����[IMAPIProp](imapipropiunknown.md)���\�b�h��g�p���ăv���p�e�B��폜�ł��Ȃ��悤�ɂ��܂��B 
    
_lppPropTagArray_��w���v���p�e�B �^�O�z���̃v���p�e�B�̂����ꂩ���폜����Ă���ꍇ�́A **HrGetPropAccess**�́A�o�͂� 0 �ɔz��̃G���g����ݒ肵�܂��B _lppPropTagArray_�� NULL �ɐݒ肵�āA�I�u�W�F�N�g�̃v���p�e�B�̂����ꂩ���폜����Ă���A�z��ŁA�폜�����v���p�e�B���Ԃ���܂��B 
  
�v���p�e�B���ύX����Ă���ꍇ�A���� IPROP_DIRTY �Ƀt���O���ݒ�z��̑Ή�����G���g���� _lprgulAccess_�|�C���g���܂��BIPROP_READONLY �� IPROP_READWRITE �ɐݒ肳��܂��B 
  
�v���p�e�B�͂��Ȃ��ύX�܂��͍폜�AIPROP_READONLY �܂��� IPROP_READWRITE �̃t���O���ݒ肳��܂��B 
  
## <a name="see-also"></a>関連項目



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

