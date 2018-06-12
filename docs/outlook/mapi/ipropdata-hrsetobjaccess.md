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
ms.openlocfilehash: 06cad6e80a2def1c1c3d692a80efeebe0e654a92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801135"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**適用されます**: Outlook 
  
�I�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>�p�����[�^�[

 _ulAccess_
  
> [����]�I�u�W�F�N�g�̃A�N�Z�X ���x����w�肷��t���O�̃r�b�g�}�b�v���܂��B�t���O����̂����ꂩ��ݒ肷�邱�Ƃ��ł��܂��B
    
IPROP_READONLY 
  
> �ǂݎ���p�ɃI�u�W�F�N�g�̃A�N�Z�X ���x����ݒ肵�܂��B 
    
IPROP_READWRITE 
  
> �I�u�W�F�N�g�̓ǂݎ��/�������݃A�N�Z�X ���x����ݒ肵�܂��B
    
## <a name="return-value"></a>�߂�l

S_OK 
  
> �I�u�W�F�N�g�̃A�N�Z�X ���x��������ɐݒ肵�܂��B
    
## <a name="remarks"></a>����

**IPropData::HrSetObjAccess**���\�b�h�́A�X �̃v���p�e�B�ł͂Ȃ��A�I�u�W�F�N�g�S�̂̃A�N�Z�X ���x����ݒ肵�܂��B�I�u�W�F�N�g���쐬���ꂽ�Ƃ��Ɋm���A�N�Z�X ���x����ύX����̂ɂ́A **HrSetObjAccess**��g�p�ł��܂��B 
  
## <a name="notes-to-callers"></a>呼び出し側への注意

プロパティのアクセス レベルを設定するのには最初の呼び出し**HrSetObjAccess**で、IPROP_READWRITE フラグを変更可能なオブジェクトを作成するのには、 _ulAccess_パラメーターに設定します。 ターゲット プロパティを指定する_lpPropTagArray_パラメーターが指す配列に、 [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)のメソッドを呼び出します。 
  
�N���C�A���g�ɓǂݎ���p�ɂȂ�v���p�e�B��g�p���ăI�u�W�F�N�g��쐬����ɂ́A[�ǂݎ��/�������݃I�u�W�F�N�g��쐬�A�K�v�ȃv���p�e�B��ǉ��A **HrSetObjAccess**�͓ǂݎ���p�̃A�N�Z�X��ύX����̂ɂ́A[�Ăяo������܂��B 
  
�N���C�A���g���V�����v���p�e�B��쐬���邱�Ƃ�h�~����̂� **HrSetObjAccess**��g�p���邱�Ƃ�ł��܂��B 
  
## <a name="see-also"></a>�֘A����



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

