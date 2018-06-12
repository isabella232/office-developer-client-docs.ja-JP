---
title: xlfRegister (�`�� 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister function [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798973"
---
# <a name="xlfregister-form-2"></a>xlfRegister (�`�� 2)

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel ���璼�ڌĂяo���悤�ɁA DLL �R�}���h�� XLL �R�}���h��g���ČĂяo�����Ƃ��ł��܂��B����́A **REGISTER** �� Excel XLM �}�N�� �V�[�g����Ăяo���̂Ɠ����ł��B 
  
���� **xlfRegister** �֐��́A����2 �̌`���ŌĂяo�����Ƃ��ł��܂��B 
  
- [xlfRegister (�`�� 1)](xlfregister-form-1.md):�R�}���h��֐���X�ɓo�^���܂��B
    
- xlfRegister (�`�� 2):XLL ��ǂݍ���ŃA�N�e�B�u�����܂��B
    
���̊֐���`�� 2 �ŌĂяo�����ꍇ�́A[xlAutoOpen](xlautoopen.md) �v���V�[�W����܂� XLL �̓ǂݍ��݂ƃA�N�e�B�u���̂ݍs���܂��B 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxModuleText_(**xltypeStr**)
  
�ǂݍ��݂ƃA�N�e�B�u����s�� DLL ���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合、この DLL (**xltypeStr**) の名前を返します。 それ以外の場合、#VALUE を返します。 エラーです。
  
## <a name="see-also"></a>�֘A����



[�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

