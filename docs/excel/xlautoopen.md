---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlautoopen function [excel 2007]
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: bf64841cbd75e25443abe5cfc7d3d7419757e245
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798957"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���ׂĂ̗L���� XLL �ɂ���Ď�������уG�N�X�|�[�g�����K�v������R�[���o�b�N�֐��BXLL �֐��ƃR�}���h�̓o�^�A�f�[�^�\���̏������A���[�U�[ �C���^�[�t�F�C�X�̃J�X�^�}�C�Y�Ȃǂ�s���ꍇ�ɂ́A **xlAutoOpen** ��g�p���邱�Ƃ�����߂��܂��B 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��Ɉ����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数の実装では、1 (**int**) を返す必要があります。
  
## <a name="remarks"></a>����

XLL ���A�N�e�B�u�ɂȂ邽�тɁAMicrosoft Excel �� **xlAutoOpen** ��Ăяo���܂��B�ȉ��̏󋵂ŁAXLL �̓A�N�e�B�u�ɂȂ�܂��B 
  
- ����I�������O��� Excel �Z�b�V�����ŃA�N�e�B�u�ł������ꍇ�AExcel �Z�b�V�����̊J�n���B
    
- Excel �Z�b�V�������ɓǂݍ��܂ꂽ�ꍇ�B
    
- XLL �͈ȉ��̂������̕��@�œǂݍ��ނ��Ƃ��ł��܂��B
    
- **[�t�@�C��]** ���j���[�� **[�J��]** ��I����� (Excel �̃o�[�W������ XLL �ǂݍ��݂̂��̕��@��T�|�[�g���Ă���ꍇ)�B 
    
- �A�h�C�� �}�l�[�W���[��g�p����B
    
- ���� DLL �̖��O��B��̈����Ƃ��� [xlfRegister](xlfregister-form-1.md) ��Ăяo���ʂ� XLL ����B 
    
- ���� DLL �̖��O��B��̈����Ƃ��� [REGISTER](xlfregister-form-1.md) ��Ăяo�� XLM �}�N�� �V�[�g����B 
    
- �A�h�C�����AExcel �Z�b�V�������ɔ�A�N�e�B�u�ɂ���Ă���ēx�A�N�e�B�u�ɂ����ꍇ�A���̊֐��͍ăA�N�e�B�u���̂Ƃ��ɌĂяo����܂��B
    
### <a name="example"></a>��

���̊֐��̎�����ɂ��ẮA `SAMPLES\EXAMPLE\EXAMPLE.C` �t�@�C����  `SAMPLES\GENERIC\GENERIC.C` �t�@�C����������������B
  
## <a name="see-also"></a>�֘A����



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)

