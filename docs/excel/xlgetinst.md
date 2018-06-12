---
title: xlGetInst
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetInst
keywords:
- xlgetinst function [excel 2007]
localization_priority: Normal
ms.assetid: 631a8f4e-ea7c-4743-9ee1-b2233fd7d98d
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 9484f7bbc1f5e0fc5b0def17f2ce79ef226dcd17
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798982"
---
# <a name="xlgetinst"></a>xlGetInst

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���� DLL ��Ăяo���Ă��� Microsoft Excel �C���X�^���X�̃C���X�^���X �n���h����Ԃ��܂��B
  
```cs
Excel4(xlGetInst, LPXLOPER pxRes, 0); /* returns low part only */
Excel12(xlGetInst, LPXLOPER12 pxRes, 0); /* returns full handle */
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��ɂ͈����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

インスタンス ハンドル (**xltypeInt**) は、 **val.w**フィールドになります。 
  
## <a name="remarks"></a>����

���̊֐���g�p����ƁADLL ��Ăяo���Ă��� Excel �� �����̎��s���C���X�^���X�����ł��܂��B
  
[Excel4](excel4-excel12.md) �܂��� [Excel4v](excel4v-excel12v.md) ��g�p���Ă��̊֐���Ăяo���ƁA�Ԃ���� XLOPER �����ϐ��́A16 �r�b�g�����t�� short int �ɂȂ�܂��B���̏ꍇ�ɓ���邱�Ƃ��ł���̂́A32 �r�b�g Windows �n���h���̉��� 16 �r�b�g�݂̂ł��BExcel 2007 �ȍ~�A **XLOPER12** �̐����ϐ��� 32 �r�b�g�����t�� int �ɂȂ������߁A�n���h���S�̂�܂߂邱�Ƃ��ł��A���ׂĂ̊J���Ă���E�B���h�E�𔽕���������K�v���Ȃ�Ȃ�܂����B 
  
> [!IMPORTANT]
> [!�D�V] **xlGetInst** �֐��� 64 �r�b�g�ł� Microsoft Excel �Ŏg�p����ƁA���s���܂��B����́A **xltypeInt** �l�̌^�̑傫�����AExcel �ɂ���ĕԂ���� 64 �r�b�g���̃n���h����ێ��ł��Ȃ����߂ł��B���̂��߁AExcel 2010 �ł� [xlGetInstPtr](xlgetinstptr.md) �Ƃ������O�̐V�����֐�����������܂����B���̊֐��́A32 �r�b�g�� 64 �r�b�g�̂ǂ���̃o�[�W������ Excel �ł����ɓ��삵�܂��B 
  
## <a name="example"></a>��

���̎g�p��ł́A�Ō�ɌĂяo���� Excel �R�s�[ �C���X�^���X��A���݌Ăяo���Ă��� Excel �R�s�[�Ɣ�r���܂��B�����ꍇ�ɂ� 1 ��Ԃ��A�قȂ�ꍇ�ɂ� 0 ��Ԃ��܂��B�֐������s����ƁA-1 ��Ԃ��܂��B
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInst, &xRes, 0) != xlretSuccess)
        iRet = -1;
    else
    {
    HANDLE hNew;
    hNew = (HANDLE)xRes.val.w;
    if (hNew != hOld)
            iRet = 0;
    else
            iRet = 1;
    hOld = hNew;
    }
    return iRet;
}
```

## <a name="see-also"></a>�֘A����



[xlGetHwnd](xlgethwnd.md)
  
[xlGetInstPtr](xlgetinstptr.md)


[DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

