---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- xlfcaller function [excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 92d2d1877d7b315d178ef1fa36b47bd5f9f8e661
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798969"
---
# <a name="xlfcaller"></a>xlfCaller

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���ݎ��s���� DLL �R�}���h�܂��͊֐���Ăяo�����Z���A�Z���͈̔́A���j���[�̃R�}���h�A�c�[���o�[�̃c�[���A�܂��̓I�u�W�F�N�g�Ɋւ������Ԃ��܂��B
  
|**�Ăяo�����̃R�[�h**|**�߂�l**|
|:-----|:-----|
|DLL  <br/> |�o�^ ID�B  <br/> |
|�P��̃Z��  <br/> |�P��Z���̎Q�ƁB  <br/> |
|�����Z���̔z�񐔎�  <br/> |�����Z���̎Q�ƁB  <br/> |
|����t�������ݒ莮  <br/> |�����ݒ�̏�����K�p����Ă���Z���ւ̎Q�ƁB  <br/> |
|���j���[  <br/> | 4 �̗v�f�̒P��s�z��  <br/>  �o�[�� ID�B  <br/>  ���j���[�̈ʒu�B  <br/>  �T�u���j���[�̈ʒu�B  <br/>  �R�}���h�̈ʒu�B  <br/> |
|�c�[���o�[  <br/> | 2 �̗v�f�̒P��s�z��  <br/>  �g�ݍ��݃c�[���o�[�̏ꍇ�̓c�[���o�[�ԍ��A�J�X�^�� �c�[���o�[�̏ꍇ�̓c�[���o�[���B  <br/>  �c�[���o�[��̈ʒu�B  <br/> |
|�O���t�B�b�N �I�u�W�F�N�g  <br/> |�I�u�W�F�N�g�̎��ʎq (�I�u�W�F�N�g��)�B  <br/> |
|xlcOnEnter�AON.ENTER�A�C�x���g �g���b�v�Ɋ֘A�t����ꂽ�R�}���h  <br/> |���͂���� 1 �܂��͕����̃Z���ւ̎Q�ƁB  <br/> |
|xlcOnDoubleclick�AON.DOUBLECLICK�A�C�x���g �g���b�v�Ɋ֘A�t����ꂽ�R�}���h  <br/> |�_�u���N���b�N���ꂽ�Z�� (�K������A�N�e�B�u�ȃZ���ł͂���܂���)�B  <br/> |
|Auto_Open�AAutoClose�AAuto_Activate �܂��� Auto_Deactivate �}�N��  <br/> |�Ăяo�����V�[�g�̖��O�B  <br/> |
|���̈ꗗ�ɂȂ����̃��\�b�h  <br/> |#REF!�G���[�B  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

�߂�l�� **XLOPER**/ **XLOPER12** �f�[�^�^�� **xltypeRef**�A **xltypeSRef**�A **xltypeNum**�A **xltypeStr**�A **xltypeErr**�A�܂��� **xltypeMulti** �̂����ꂩ�ł��B�����̌^�̂��� 3 �͊��蓖�Ă�ꂽ��������|�C���g���Ă��邽�߁A�s�v�ɂȂ��� **xlfCaller** �̖߂�l�͕K�� [xlFree �֐�](xlfree.md)�ւ̌Ăяo���ŉ������K�v������܂��B 
  
**XLOPERs**/ **XLOPER12s** �̏ڍׂɂ��ẮA�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v��Q�Ƃ��Ă��������B
  
## <a name="remarks"></a>����

���̊֐��́ADLL/XLL ���[�N�V�[�g�֐�����Ăяo���\�ȗB��̔񃏁[�N�V�[�g�֐��ł��B���̑��� XLM ���֐��́A�R�}���h�܂��̓}�N�� �V�[�g�����̊֐�����̂݌Ăяo���ł��܂��B
  
## <a name="example"></a>��

 `\SAMPLES\EXAMPLE\EXAMPLE.C`�B���̊֐��̓R�}���h �}�N�� (xlcSelect) ��Ăяo���A�}�N�� �V�[�g����Ăяo���ꂽ�ꍇ�ɂ̂ݐ��������삵�܂��B
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

