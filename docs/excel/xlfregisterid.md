---
title: xlfRegisterId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegisterId
keywords:
- xlfregisterid function [excel 2007]
localization_priority: Normal
ms.assetid: d34cf20c-a5cd-45fb-9dcb-d49eac2d99dd
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: cd401393b7465442cef9342b942a27456871c68b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798986"
---
# <a name="xlfregisterid"></a>xlfRegisterId

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel ����Ăяo���ꂽ DLL �R�}���h����Ăяo�����Ƃ��ł��܂��B�֐������ɓo�^����Ă���ꍇ�́A���̊֐���ēo�^���Ȃ��ŁA�֐��̊����̓o�^ ID ��Ԃ��܂��B�֐����܂��o�^����Ă��Ȃ��ꍇ�́A���̊֐���o�^���āA�o�^ ID ��Ԃ��܂��B
  
```cs
Excel12(xlfRegisterId, LPXLOPER12 pxRes, 3,     LPXLOPER12 pxModuleText, LPXLOPER12 pxProcedure, LPXLOPER12 pxTypeText);
```

## <a name="parameters"></a>�p�����[�^�[

_pxModuleText_(**xltypeStr**)
  
�֐����܂܂�Ă��� DLL �̖��O�B
  
_pxProcedure_(**xltypeStr**または**xltypeNum**)
  
������̏ꍇ�́A�Ăяo���֐��̖��O�ł��B�����̏ꍇ�́A�Ăяo���֐��̃G�N�X�|�[�g�̏����ԍ��ł��B���m�Ō��S�ɂ��邽�߂ɁA��ɕ�����`����g�p���܂��B
  
_pxTypeText_(**xltypeStr**)
  
�֐��ւ̂��ׂĂ̈����̌^�Ɗ֐��̖߂�l�̌^��w�肷��A�ȗ��\�ȕ�����B�ڂ����́A�u���v�Z�N�V������Q�Ƃ��Ă��������B **xlAutoRegister** ���`����X�^���h�A���� DLL (XLL) �ł́A���̈�����ȗ��ł��܂��B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

**XlfUnregister**以降の呼び出しで使用できる関数 (**xltypeNum**) のレジスタ ID を返します。
  
## <a name="remarks"></a>����

�o�^ ID �͌�œo�^�������ۂɕK�v�ɂȂ邪�A�ێ��̂��߂ɋC��g�������Ȃ��A�Ƃ����ꍇ�ɁA���̊֐����𗧂��܂��B�܂��A���蓖�Ă�֐��� DLL �ɂ���ꍇ�́A���j���[�A�c�[���A����у{�^���ւ̊��蓖�Ăɂ�𗧂��܂��B
  
_xlfRegister_ �Ɏw�肳�ꂽ�L����  **pxFunctionText** ������g�p���� DLL �܂��� XLL �֐����o�^����Ă���ꍇ�́A�֐� _xlfEvaluate_ ��  **pxFunctionText** ��n�����ƂŁA���̓o�^ ID ��擾���邱�Ƃ�ł��܂��B
  
## <a name="see-also"></a>�֘A����

- [REGISTER](xlfregister-form-1.md)
- [UNREGISTER](xlfunregister-form-1.md)
- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

