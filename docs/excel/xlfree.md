---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- xlfree function [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798984"
---
# <a name="xlfree"></a>xlFree

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**Excel4**�A/ �A**Excel12**�A�܂��� [Excel12v](excel4-excel12.md) �̌Ăяo���Ŗ߂�l [XLOPER](excel4v-excel12v.md)[](excel4-excel12.md)[XLOPER12](excel4v-excel12v.md) ��쐬����Ƃ��ɁAMicrosoft Excel �����蓖�Ă������� ���\�[�X�������邽�߂Ɏg�p���܂��B **xlFree** �֐��͕⏕�������������A�|�C���^�[�� **NULL** �Ƀ��Z�b�g���܂����A **XLOPER**/ **XLOPER12**�̑��̕����͔j�����܂���B
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>�p�����[�^�[

 _px_1, ..., px_n_
  
1 �ȏ�� **XLOPER**/ **XLOPER12** �������܂��BExcel 2003 �܂ł̃o�[�W�����ł́A�n����|�C���^�[�̍ő吔�� 30 �ł��BExcel 2007 �ȍ~�́A255 �ɑ�������܂����B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

���̊֐��͒l��Ԃ��܂���B
  
## <a name="remarks"></a>����

**Excel4** �܂��� **Excel4v** ����߂�l�Ƃ��Ď擾���� **XLOPER**�A����� **Excel12** �܂��� **Excel12v** ����߂�l�Ƃ��Ď擾���� **XLOPER12** �́A�^�� **xltypeStr**�A **xltypeMulti**�A�܂��� **xltypeRef** �̂����ꂩ�̏ꍇ�͂��ׂĉ������K�v������܂��B���̌^�������Ă�A���ꂪ **Excel4** �܂��� **Excel12** ����擾������̂ł������A���Ƃ����ꂪ�⏕��������g�p���Ȃ��ꍇ�ł�A��肪�����邱�Ƃ͂���܂���B
  
����Ώۂ� Excel �����蓖�Ă���������܂� **XLOPER**/ **XLOPER12**�ւ̃|�C���^�[�� Excel �ɖ߂��ꍇ�A **xlbitXLFree** ��ݒ肵�� Excel �Ƀ�������m���ɉ�������܂��B 
  
## <a name="example"></a>��

���̗�ł� **GET.WORKSPACE(1)** ��Ăяo���AExcel ����s���̃v���b�g�t�H�[���𕶎���Ƃ��ĕԂ��܂��B�R�[�h�͕Ԃ��ꂽ��������Ŏg�p���邽�߂Ƀo�b�t�@�[�ɃR�s�[���܂��B�R�[�h�͂��̃o�b�t�@�[���� Excel �֐��Ŏg�p���邽�߂� **XLOPER12** �ɖ߂��܂��B�Ō�ɁA�R�[�h�͌x���{�b�N�X�ɕ������\�����܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>�֘A����

- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

