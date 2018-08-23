---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: d0054e54d56fbe1cc6d6d783ffcd6330d8ab2e6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564662"
---
# <a name="ipropdatahrsetpropaccess"></a>IPropData::HrSetPropAccess

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
�A�N�Z�X ���x���܂��̓I�u�W�F�N�g�̃v���p�e�B�� 1 �ȏ�̏�Ԃ�ݒ肵�܂��B
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a>�p�����[�^�[

 _lpPropTagArray_
  
> [����]�v���p�e�B��ύX�ł��邱�Ƃ�����v���p�e�B �^�O�̔z��ւ̃|�C���^�[�B 
    
 _rgulAccess_
  
> [����]�t���O �r�b�g�}�X�N�̔z�񂵂܂��B�e�r�b�g�́A�A�N�Z�X ���x���̏��]�A�܂��͂��̗����� _lpPropTagArray_�p�����[�^�[���Q�ƁA�z���̓���̃v���p�e�B�̊e���\������܂��B2 �̔z��A�ʒu _rgulAccess_�ōŏ��̃r�b�g�ɂ��Đ���ŏ��̃v���p�e�B�� _lpPropTagArray_�|�C���g�ɁA���̂ł��B �v���p�e�B�̃^�O���ƂɁA1 �̃A�N�Z�X ���x���̃t���O�� 1 �̃t���O��ݒ�ł��܂��B���̕\�́A�\�ȃt���O������܂��B 
    
|**�A�N�Z�X ���x���̃t���O**|**�t���O�̏��**|
|:-----|:-----|
|�v���p�e�B��ύX�ł��Ȃ����Ƃ�����AIPROP_READONLY  <br/> |IPROP_CLEAN �v���p�e�B���ύX����Ă��Ȃ����Ƃ�����܂��B  <br/> |
|IPROP_READWRITE �v���p�e�B��ύX�ł��邱�Ƃ�����܂��B  <br/> |IPROP_DIRTY �v���p�e�B���ύX����Ă��邱�Ƃ�����܂��B  <br/> |
   
## <a name="return-value"></a>�߂�l

S_OK 
  
> �A�N�Z�X ���x���Ə�Ԃ̃t���O������ɐݒ肳��Ă��܂��B
    
MAPI_E_NO_ACCESS 
  
> �ǂݎ���p�I�u�W�F�N�g�܂��͔��M�҂��\���ȃA�N�Z�X��������Ă���I�u�W�F�N�g�̃v���p�e�B��ݒ肵�܂����B
    
MAPI_E_INVALID_PARAMETER 
  
> _rgulAccess_�p�����[�^�[�ɂ́A�t���O�AIPROP_READONLY IPROP_READWRITE �Ȃǂ̖����ȑg�ݍ��킹���܂܂�Ă��܂��B 
    
## <a name="remarks"></a>����

**IPropData::HrSetPropAccess**���\�b�h�́A�A�N�Z�X ���x������� [lpPropTagArray](sproptagarray.md)�p�����[�^�[��w��_SPropTagArray_�\���̃v���p�e�B �^�O�Ŏ��ʂ����v���p�e�B�̏�Ԃ�ύX���܂��B�e�v���p�e�B�ɂ� _rgulAccess_�z��őΉ�����G���g��������܂��B1 �̃t���O������v���p�e�B�̃A�N�Z�X ���x���ʂɁA�Y������G���g����ݒ�ł��܂���Ԃ�����t���O��ݒ肵�܂��B 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

����̃v���p�e�B] �̒l���ύX���ꂽ�Ƃ��Ɍ��肵����A�I�u�W�F�N�g�̃v���p�e�B�� 1 �ȏ�̃A�N�Z�X ���x����ύX����̂ɂ́A **HrSetPropAccess**��g�p���܂��B 
  
## <a name="see-also"></a>�֘A����



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

