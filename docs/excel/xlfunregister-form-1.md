---
title: xlfUnregister (�`�� 1)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister
keywords:
- xlfunregister function [excel 2007]
localization_priority: Normal
ms.assetid: 850bf65f-a151-44d6-b49f-d53ae2c83760
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 6077027a27c054c5a5e65a751373c41a87cb3836
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798981"
---
# <a name="xlfunregister-form-1"></a>xlfUnregister (�`�� 1)

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel �ɂ���Ă��ꎩ�̂��Ăяo����� DLL �� XLL �R�}���h����Ăяo�����Ƃ��ł��܂��B����́A **UNREGISTER** �� Excel XLM �}�N�� �V�[�g����Ăяo���̂Ɠ����ł��B 
  
**xlfUnregister** �́A2 �̌`���ŌĂяo�����Ƃ��ł��܂��B 
  
- �`�� 1:�X�̃R�}���h��֐��̓o�^�������܂��B
    
- �`�� 2XLL �̃A�����[�h�Ɣ�A�N�e�B�u����s���܂��B
    
�`�� 1 �ŌĂяo�����ƁA���̊֐��́A **xlfRegister** �܂��� **REGISTER** ��g�p���Ċ��ɓo�^����Ă��� DLL �֐��܂��̓R�}���h�̎g�p�J�E���g����炵�܂��B���Ɏg�p�J�E���gDLL ��̂��ׂĂ̊֐��̎g�p�J�E���g�� 0 �ɂȂ�ƁADLL �̓���������A�����[�h����܂��B
  
**xlfRegister** (�__ ���܂��B�֐��̓o�^��������ꍇ�́A�֐��E�B�U�[�h�ɂ��̊֐��̖��O���\������Ȃ��Ȃ�悤�ɁA **xlfSetName** ��g�p���Ă��̖��O��폜����K�v������܂��B�ڂ����́u [Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��������������B
  
```cs
Excel4(xlfUnregister, LPXLOPER pxRes, 1, LPXLOPER pxRegisterId);
```

## <a name="parameters"></a>�p�����[�^�[

_pxRegisterId_(**xltypeNum**)
  
�o�^��������֐��̓o�^ ID�B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合を返します**TRUE** (**xltypeBool**)、それ以外の場合は FALSE を返します。
  
## <a name="remarks"></a>����

�֐��̓o�^ ID �́A�֐��̍ŏ��̓o�^���� **xlfRegister** �ɂ���ĕԂ���܂��B�܂��A [xlfRegisterId �֐�](xlfregisterid.md) �܂��� [xlfEvaluate �֐�](xlfevaluate.md)��Ăяo���Ď擾���邱�Ƃ�ł��܂��B�֐����܂��o�^����Ă��Ȃ��ꍇ�́AxlfRegisterId �͂��̊֐���o�^���悤�Ƃ��邱�Ƃɂ����ӂ��������B���̂��߁A�P�Ɋ֐��̓o�^��������ړI�� ID ��擾���悤�Ƃ��Ă���̂ł���΁A�o�^���ꂽ���O�� **xlfEvaluate** �ɓn���� ID ��擾���邱�Ƃ�����߂��܂��B�֐����o�^����Ă��Ȃ��ꍇ�A **xlfEvaluate** �� #NAME? �G���[�Ŏ��s���܂��B 
  
## <a name="example"></a>��

**** �� `\SAMPLES\GENERIC\GENERIC.C` �֐��̃R�[�h����Q�Ƃ��������B
  
```cs
int WINAPI fExit(void)
{
   XLOPER12  xDLL,    // The name of this DLL //
   xFunc,             // The name of the function //
   xRegId;            // The registration ID //
   int i;
//
// This code gets the DLL name. It then uses this along with information
// from g_rgFuncs[] to obtain a REGISTER.ID() for each function. The
// register ID is then used to unregister each function. Then the code
// frees the DLL name and calls xlAutoClose.
//
   // Make xFunc a string //
   xFunc.xltype = xltypeStr;
   Excel12f(xlGetName, &xDLL, 0);
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgWorksheetFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   for (i = 0; i < g_rgCommandFuncsRows; i++)
   {
      xFunc.val.str = (LPWSTR) (g_rgCommandFuncs[i][0]);
      Excel12f(xlfRegisterId,&xRegId,2,(LPXLOPER12)&xDLL,(LPXLOPER12)&xFunc);
      Excel12f(xlfUnregister, 0, 1, (LPXLOPER12) &xRegId);
   }
   Excel12f(xlFree, 0, 1,  (LPXLOPER12) &xDLL);
   return xlAutoClose();
}
```

## <a name="see-also"></a>�֘A����

- [xlfRegister (�`�� 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (�`�� 2)](xlfunregister-form-2.md)
- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

