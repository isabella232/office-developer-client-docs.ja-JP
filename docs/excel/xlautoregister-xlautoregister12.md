---
title: xlAutoRegister/xlAutoRegister12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRegister
keywords:
- xlautoregister function [excel 2007]
localization_priority: Normal
ms.assetid: aa4673cf-8e97-4678-b8d4-6a74426334f9
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e6430a54b0c0ed3b6e08d3c9256cae7dcde926ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19798961"
---
# <a name="xlautoregisterxlautoregister12"></a>xlAutoRegister/xlAutoRegister12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�o�^�Ώۂ̊֐��̖߂�l�̌^�ƈ����̌^���Ȃ���ԂŁAXLM �֐� [REGISTER](xlautoregister-xlautoregister12.md)�A�܂��� C API �̓����� **xlfRegister** �֐��ɑ΂���Ăяo�������s�����ƁA��� Excel �� [xlAutoRegister](xlfregister-form-1.md) �֐���Ăяo���܂��B�����g�p����ƁA�G�N�X�|�[�g���ꂽ�֐��ƃR�}���h�̓�����X�g�� XLL �Ō����ł���悤�ɂȂ�A����̈����Ɩ߂�l�̌^����֐���o�^�ł��܂��B
  
Excel 2007 �ȍ~�ł́A **xlAutoRegister12** �֐��� XLL �ɂ���ăG�N�X�|�[�g�����ƁAExcel �� **xlAutoRegister** �֐��ɗD�悵�Ă��̊֐���Ăяo���܂��B 
  
Excel �ł́AXLL ������炢���ꂩ�̊֐���������ăG�N�X�|�[�g���邱�Ƃ͕s�v�ł��B
  
> [!NOTE]
> [!����] **xlAutoRegister**/  **xlAutoRegister12** �������̌^�Ɩ߂�l�̌^��w�肵�Ȃ��Ŋ֐���o�^���悤�Ƃ���ƁA�ŏI�I�ɃR�[�� �X�^�b�N���I�[�o�[�t���[���AExcel ���N���b�V�����錴���ƂȂ�ċA�Ăяo���̃��[�v���������܂��B 
  
```cs
LPXLOPER12 WINAPI xlAutoRegister12(LPXLOPER12 pxName);
LPXLOPER WINAPI xlAutoRegister(LPXLOPER pxName);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxName_(**xltypeStr**)
  
�o�^����� XLL �֐��̖��O�ł��B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

�֐��́A _xlfRegister_ �֐���g�p���āAXLL �֐�  **pxName** �̓o�^����s�������ʂ�Ԃ��K�v������܂��B�w�肵���֐��� XLL �t�@�C���̃G�N�X�|�[�g�� 1 �łȂ��ꍇ�A�֐��� **#VALUE!** �G���[��Ԃ����AExcel �� **#VALUE!** �Ɖ�߂��� **NULL** ��Ԃ��K�v������܂��B
  
## <a name="remarks"></a>����

**xlAutoRegister** �̎����ł́A�G�N�X�|�[�g���� XLL �t�@�C���̊֐��ƃR�}���h�̓�����X�g�ő啶�����������ʂ��錟������s���āA�n���ꂽ���O�Ƃ̈�v���������K�v������܂��B�֐��܂��̓R�}���h�����������ꍇ�A **xlAutoRegister** �� **xlfRegister** �֐���g�p���AExcel �Ɋ֐��̖߂�l�̌^�ƈ����̌^�A����ъ֐��Ɋւ��邻�̑��̕K�v����w�����镶�����w�肵�āA�o�^����s����K�v������܂��B����́A **xlfRegister** �ɑ΂���Ăяo�����Ԃ��ꂽ�ꍇ�ɂ�AExcel �ɕԂ��K�v������܂��B�֐�������ɓo�^���ꂽ�ꍇ�A **xlfRegister** �͊֐��̓o�^ ID ��܂� **xltypeNum** �l��Ԃ��܂��B 
  
### <a name="example"></a>��

���̊֐��̎�����ɂ��ẮA�t�@�C��  `SAMPLES\EXAMPLE\EXAMPLE.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[REGISTER](xlfregister-form-1.md)
  
[UNREGISTER](xlfunregister-form-1.md)

