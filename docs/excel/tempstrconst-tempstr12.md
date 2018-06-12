---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- tempstr12 function [excel 2007],TempStrConst function [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798958"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**xltypeStr** �������܂ވꎞ�I�� **XLOPER/XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B���͂Ƃ��� Null �ŏI������\�[�X�̕������󂯎��܂��B���̊֐��́A�V���������� �o�b�t�@�[����蓖�ĂāA���̃o�b�t�@�[�ɓn���ꂽ�������R�s�[���܂��B���͕�����͕ύX����Ȃ����߁A **const** �Ƃ��Đ錾����܂��B
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>�p�����[�^�[

 _str_
  
Null �ŏI������\�[�X�̕�����ւ̃|�C���^�[�B **XLOPER** �̏ꍇ�ATempStrConst �� 255 �o�C�g��蒷���������؂�̂Ă܂��B **XLOPER12** �̏ꍇ�ATempStr12Const �� 32,767 Unicode ������蒷���������؂�̂Ă܂��B
  
## <a name="return-value"></a>�߂�l

�n���ꂽ������o�b�t�@�[�̃R�s�[��i�[���Ă��� **xltypeStr** �������Ԃ��܂��B 
  
## <a name="remarks"></a>����

**XLOPER** ������̃t���[�����[�N�֐� **TempStr** �̓���͈قȂ�܂��B�w�肳�ꂽ������̍ŏ��̕�����㑱�̕�����̒����ŏ㏑�����悤�Ƃ��邽�߁A���ӂ��K�v�ł��B����͏�Ɉ��S�Ƃ����킯�ł͂���܂���B�ǂݎ���p�̕������n���ƁAMicrosoft Excel ���N���b�V������\��������܂��B���̕��@�ɂ��ꎞ�I�ȕ�����̍쐬�́A **TempStrConst** �� **TempStr12** �̗����œ��삷����@�Ƃ��Ă͐�������Ȃ��Ȃ�܂����B���������āA���͕�����̍ŏ��̕����́A������̐擪�Ƃ��� (�܂�A������\�������܂��͒�����\�������p�̃X�y�[�X�Ƃ��Ăł͂Ȃ�) ��������܂��B�e�����\���ł��Ȃ����߁A�J�n���ɃG���R�[�h���ꂽ������\�������̂��镶����͓n���Ȃ��ł��������B 
  
## <a name="example"></a>��

���̗�ł́A **TempStr12** �֐���g�p���ă��b�Z�[�W �{�b�N�X�̕������쐬���܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

