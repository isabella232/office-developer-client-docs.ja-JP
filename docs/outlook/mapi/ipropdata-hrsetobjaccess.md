---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348693"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>パラメーター

 _ulaccess_
  
> [����]�I�u�W�F�N�g�̃A�N�Z�X ���x����w�肷��t���O�̃r�b�g�}�b�v���܂��B�t���O����̂����ꂩ��ݒ肷�邱�Ƃ��ł��܂��B
    
IPROP_READONLY 
  
> �ǂݎ���p�ɃI�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B 
    
IPROP_READWRITE 
  
> �I�u�W�F�N�g�̓ǂݎ��/�������݃A�N�Z�X ���x����ݒ肵�܂��B
    
## <a name="return-value"></a>戻り値

S_OK 
  
> �I�u�W�F�N�g�̃A�N�Z�X ���x��������ɐݒ肵�܂��B
    
## <a name="remarks"></a>解説

**IPropData::HrSetObjAccess**���\�b�h�́A�X �̃v���p�e�B�ł͂Ȃ��A�I�u�W�F�N�g�S�̂̃A�N�Z�X ���x����ݒ肵�܂��B�I�u�W�F�N�g���쐬���ꂽ�Ƃ��Ɋm���A�N�Z�X ���x����ύX����̂ɂ́A **HrSetObjAccess**��g�p�ł��܂��B 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable. Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter. 
  
�N���C�A���g�ɓǂݎ���p�ɂȂ�v���p�e�B��g�p���ăI�u�W�F�N�g��쐬����ɂ́A[�ǂݎ��/�������݃I�u�W�F�N�g��쐬�A�K�v�ȃv���p�e�B��ǉ��A **HrSetObjAccess**�͓ǂݎ���p�̃A�N�Z�X��ύX����̂ɂ́A[�Ăяo������܂��B 
  
�N���C�A���g���V�����v���p�e�B��쐬���邱�Ƃ�h�~����̂� **HrSetObjAccess**��g�p���邱�Ƃ�ł��܂��B 
  
## <a name="see-also"></a>関連項目



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

