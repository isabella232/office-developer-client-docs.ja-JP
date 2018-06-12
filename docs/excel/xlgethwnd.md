---
title: xlGetHwnd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetHwnd
keywords:
- xlgethwnd function [excel 2007]
localization_priority: Normal
ms.assetid: be33b097-812b-4f5c-81be-4d9673e95b0b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a22365d6c945aaa5995e2c519c757a1a7515655a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798995"
---
# <a name="xlgethwnd"></a>xlGetHwnd

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel �E�B���h�E�̍ŏ�ʂ̃E�B���h�E �n���h����Ԃ��܂��B
  
```cs
Excel4(xlGetHwnd, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetHwnd, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��ɂ͈����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

[ **Val.w** ] フィールドには、ウィンドウ ハンドル (**xltypeInt**) が含まれています。 
  
## <a name="remarks"></a>����

���̊֐��́AWindows API �̃R�[�h��L�q���邽�߂ɖ𗧂��܂��B
  
[Excel4](excel4-excel12.md) �܂��� [Excel4v](excel4v-excel12v.md) ��g�p���āA���̊֐���Ăяo���ƁA�Ԃ���� XLOPER �����ϐ��́A16 �r�b�g�����t�� short int �ɂȂ�܂��B���̏ꍇ�ɓ���邱�Ƃ��ł���̂́A32 �r�b�g Windows �n���h���̉��� 16 �r�b�g�݂̂ł��B��ʕ������������ɂ́A���ׂĂ̊J�����E�B���h�E��ʂ��ăR�[�h��J��Ԃ��K�p���āA���ʕ����Ƃ̈�v���������K�v������܂��BExcel 2007 �ȍ~�A **XLOPER12** �̐����ϐ��� 32 �r�b�g int �ɂȂ������߁A�n���h���S�̂�܂߂邱�Ƃ��ł��A���ׂĂ̊J���Ă���E�B���h�E�𔽕���������K�v���Ȃ�Ȃ�܂����B 
  
### <a name="example"></a>��

[](fshowdialog.md) �� `SAMPLES\GENERIC\GENERIC.C` �ɂ��ẮA�R�[�h��Q�Ƃ��Ă��������B
  
## <a name="see-also"></a>�֘A����

- [xlGetInst](xlgetinst.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

