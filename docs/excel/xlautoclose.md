---
title: xlAutoClose
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoClose
keywords:
- xlautoclose function [excel 2007]
localization_priority: Normal
ms.assetid: 147e46cd-d4d7-49eb-acdc-5a2ebc2fb6c2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3cbe1cd879fb5a91d14b38f8a659a7f77d943fe7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798977"
---
# <a name="xlautoclose"></a>xlAutoClose

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
XLL �t�@�C������A�N�e�B�u�ɂȂ邽�тɁAMicrosoft Excel �ɌĂяo����܂��BExcel �Z�b�V����������ɏI������ƁA�A�h�C���͔�A�N�e�B�u�ɂȂ�܂��B�A�h�C���́AExcel �Z�b�V�������Ƀ��[�U�[�ɂ���Ĕ�A�N�e�B�u�������ꍇ������܂��B���̊֐��͂��̏ꍇ�ɌĂяo����܂��B
  
�֐��ƃR�}���h�̓o�^����A���\�[�X�̉���A�J�X�^�}�C�Y����ɖ߂����ƂȂǂ� XLL �����s�ł���悤���邽�߂ɓK�؂Ȃ��Ƃł͂���܂����AExcel �͂��̊֐���������G�N�X�|�[�g����̂ɁAXLL ��K�v�Ƃ��܂���B�֐��ƃR�}���h�� XLL �������I�ɓo�^������Ȃ��ꍇ�A **xlAutoClose** �֐���Ăяo������AExcel �͂������s���܂��B 
  
```cs
int WINAPI xlAutoClose(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��Ɉ����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

この関数の実装では、1 (**int**) を返す必要があります。
  
## <a name="remarks"></a>����

XLL ����A�N�e�B�u�ɂȂ�A�܂胁��������A�����[�h����邽�тɁAExcel �� **xlAutoClose** �֐���Ăяo���܂��B�ȉ��̏󋵂ŁAXLL �͔�A�N�e�B�u�ɂȂ�܂��B 
  
- �Z�b�V�������ɃA�N�e�B�u�ȏꍇ�ɁAExcel �Z�b�V����������ɏI���������_�B
    
- Excel �Z�b�V�������ɖ����I�ɃA�����[�h���ꂽ�ꍇ�B
    
- XLL �͈ȉ��̂������̕��@�ŃA�����[�h�����\��������܂��B
    
- �A�h�C�� �}�l�[�W���[��g�p����B
    
- ���� DLL �̖��O��B��̈����Ƃ��� [xlfUnregister](xlfunregister-form-1.md) ��Ăяo���ʂ� XLL ����B 
    
- ���� DLL �̖��O��B��̈����Ƃ��� [UNREGISTER](xlfunregister-form-1.md) ��Ăяo�� XLM �}�N�� �V�[�g����B 
    
���̊֐��́A�ȉ�����s���܂��B
  
- XLL ���ǉ������C�ӂ̃��j���[�܂��̓��j���[���ڂ�폜����B
    
- �C�ӂ̕K�v�ȃO���[�o�� �N���[���A�b�v����s����B
    
- �쐬���ꂽ�C�ӂ̖��O�A���ɃG�N�X�|�[�g���ꂽ�֐��̖��O��폜����B **REGISTER** �ւ� 4 �Ԗڂ̈��������݂���ꍇ�A�֐��̓o�^���������̖��O��쐬���錴���ɂȂ�ꍇ�����邱�Ƃɂ����ӂ��������B 
    
## <a name="example"></a>��

���̊֐��̎���������  `SAMPLES\EXAMPLE\EXAMPLE.C` �t�@�C����  `SAMPLES\GENERIC\GENERIC.C` �t�@�C����Q�Ƃ��Ă��������B���̃R�[�h�́A  `SAMPLES\GENERIC\GENERIC.C` �ɂ���܂��B
  
```cs
int WINAPI xlAutoClose(void)
{
   int i;
   XLOPER12 xRes;
//
// This block first deletes all names added by xlAutoOpen or
// xlAutoRegister12. Next, it checks if the drop-down menu Generic still
// exists. If it does, it is deleted using xlfDeleteMenu. It then checks
// if the Test toolbar still exists. If it is, xlfDeleteToolbar is
// used to delete it.
//
// The following code to delete the defined names
// does not work in the current version of Excel. 
// You cannot delete these names once they are Registered.
// The code is left here in case the functionality becomes 
// available in a future version.
//
   for (i = 0; i < g_rgWorksheetFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgWorksheetFuncs[i][2]));
   for (i = 0; i < g_rgCommandFuncsRows; i++)
      Excel12f(xlfSetName, 0, 1, TempStr12(g_rgCommandFuncs[i][2]));
//
// Everything else works as documented.
//
   Excel12f(xlfGetBar, &amp;xRes, 3, TempInt12(10), TempStr12(L"Generic"), TempInt12(0));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteMenu, 0, 2, TempNum12(10), TempStr12(L"Generic"));
      // Free the XLOPER12 returned by xlfGetBar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   Excel12f(xlfGetToolbar, &amp;xRes, 2, TempInt12(7), TempStr12(L"Test"));
   if (xRes.xltype != xltypeErr)
   {
      Excel12f(xlfDeleteToolbar, 0, 1, TempStr12(L"Test"));
      // Free the XLOPER12 returned by xlfGetToolbar //
      Excel12f(xlFree, 0, 1, (LPXLOPER12) &amp;xRes);
   }
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[xlAutoOpen](xlautoopen.md)


[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)

