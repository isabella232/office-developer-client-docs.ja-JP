---
title: xlStack
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlStack
keywords:
- xlstack function [excel 2007]
localization_priority: Normal
ms.assetid: f9f030e8-1ec9-4cbf-92e1-360526260916
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: fcd073f7d2b97e84743d01c498435f186277e345
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798990"
---
# <a name="xlstack"></a>xlStack

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�X�^�b�N��̋󂫗̈��m�F���܂��B
  
```cs
Excel12(xlStack, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��Ɉ����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

スタックに残っているバイト数 (**xltypeInt**) の数を返します。
  
## <a name="remarks"></a>����

�ŋ߂̃o�[�W�����̎g�p�\�ȃX�^�b�N�̈�̗e�ʂ́A **XLOPER** �� 16 �r�b�g�̕����t�������Ɏ��܂�܂���B�܂�A **xlStack** �� **XLOPER** ����� **Excel4** �܂��� **Excel4v** ��g�p���ČĂяo�����Ƃ��� -32767 ���� 32768 �̊Ԃ̒l��Ԃ����Ƃ��ł���A�Ƃ������Ƃł��B���̏ꍇ�ɐ������l��擾����ɂ́A�߂�l�� unsigned short �^�ɃL���X�g���܂��B
  
Excel 2007 �ȍ~�ł́A **XLOPER12** ����� **Excel12** �܂��� **Excel12v** ��g�p���āA���̊֐���Ăяo���K�v������܂��B���̏ꍇ�A�߂�l�͎g�p�\�ȃX�^�b�N�̈�̗e�ʂ��A64 KB �̂����ꂩ���������ɂȂ�܂��B
  
Excel �ł́A�X�^�b�N��̋󂫗̈�ɐ���������܂��B���̗e�ʂ𒴂��Ȃ��悤�ɒ��ӂ���K�v������܂��B���ɑ傫�ȃf�[�^�\����z�u������A�\�Ȍ��葽���̃��[�J���ϐ���ÓI�ɂ��Ă͂����܂���B�֐���ċA�I�ɌĂяo���Ȃ��悤�ɂ��Ă��������B�����s���ƁA�X�^�b�N�������ɂ����ς��ɂȂ�܂��B
  
�X�^�b�N��I�[�o�[�������Ă���^��������ꍇ�́A���̊֐���p�ɂɌĂяo���āA�X�^�b�N�̈悪�ǂ̒��x�c���Ă��邩�m�F���܂��B
  
## <a name="example"></a>��

�ŏ��̗�ł́A�X�^�b�N�̋󂫗̈�̗e�ʂ������ꂽ�x�����b�Z�[�W���\������܂��B�����  `\SAMPLES\EXAMPLE\EXAMPLE.C` �Ɋi�[����Ă��܂��B2 �Ԗڂ̗�����������܂� ( **XLOPER** ��g�p)�B����� SDK �̃R�[�h��ɂ͊܂܂�Ă��܂���B
  
```cs
short WINAPI xlStackExample(void)
{
   XLOPER12 xRes;
   Excel12(xlStack, &xRes, 0);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
} 
short int WINAPI xlStackExample_XLOPER(void)
{
    XLOPER xRes;
    Excel4(xlStack, (LPXLOPER)&xRes, 0);
    xRes.xltype = xltypeNum; // Change the type to double
    // Cast to an unsigned short to get rid of the overflow problem
    xRes.val.num = (double)(unsigned short) xRes.val.w;
    Excel4(xlcAlert, 0, 1, (LPXLOPER)& xRes);
    return 1;
}
```

## <a name="see-also"></a>�֘A����

- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

