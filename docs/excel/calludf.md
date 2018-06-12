---
title: CallUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6421c9a2-07f7-4deb-aa43-c50d82cb0002
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1d55f22de88b274d0403f81717d0fddefbea0219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798761"
---
# <a name="calludf"></a>CallUDF

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���p�t�H�[�}���X�̃R���s���[�e�B���O���Ń��[�U�[��`�֐���Ăяo���܂��B
  
```cpp
int CallUDF(int SessionId, WCHAR *XllName, WCHAR *UDFName, LPXLOPER12 pxAsyncHandle, int (*CallBackAddr)(), int ArgCount, LPXLOPER12 Parameter1, ...)
```

## <a name="parameters"></a>�p�����[�^�[

_セッション Id_
  
> �Ăяo����s���Z�b�V������ ID�B
    
_XLLName_
  
> ���[�U�[��`�֐����܂܂�� XLL �̖��O�B
    
_UDFName_
  
> ���[�U�[��`�֐��̖��O�B
    
_CallBackAddr_
  
> ���[�U�[��`�֐����I������Ƃ��ɃR�l�N�^���Ăяo���K�v������֐��B
    
_pxAsyncHandle_
  
> Excel �ƃR�l�N�^���A�ۗ����̃��[�U�[��`�֐��̌Ăяo����ǐՂ��邽�߂Ɏg�p����񓯊��n���h���B�R�l�N�^�ɂ���āA��قǁA�Ăяo�����I�������Ƃ� ( _CallBackAddr_ �����ɓn���ꂽ�֐��|�C���^�[��g�p���� Excel �ɃR�[���o�b�N����Ƃ�) �Ɏg�p����܂��B 
    
_について_
  
> ���[�U�[��`�֐��ɓn���������̐��B�ő�l�� 255 �ł��B
    
_パラメーター 1_
  
> ���[�U�[��`�֐��ɓn���l�B _ArgCount_ �Ŏ�����Ă���p�����[�^�[���Ƃɂ��̈����𔽕����܂��B
    
## <a name="return-value"></a>�߂�l

UDF �Ăяo��������ɊJ�n���ꂽ�ꍇ�ɂ� **xlHpcRetSuccess**�B **SessionId** �����������ȏꍇ�ɂ� _xlHpcRetInvalidSessionId_�B�^�C���A�E�g�ȂǑ��̃G���[���������ꍇ�ɂ� **xlHpcRetCallFailed**�B�Ăяo���ɂ���ăG���[ �R�[�h ( **xlHpcRetSuccess** �ȊO) ���Ԃ����ꍇ�AExcel �� UDF �Ăяo�������s�����ƌ��Ȃ��A  _pxAsyncHandle_ ��s�킸�ɁA�R�[���o�b�N�̔�����z�肵�܂���B
  
## <a name="remarks"></a>����

���̊֐��͔񓯊��Ŏ��s����܂��B
  
## <a name="see-also"></a>�֘A����

- [Excel �N���X�^�[ �R�l�N�^�֐�](excel-cluster-connector-functions.md)

