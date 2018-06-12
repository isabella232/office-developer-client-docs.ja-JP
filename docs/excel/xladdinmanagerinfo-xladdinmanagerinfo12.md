---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- xladdinmanagerinfo function [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798950"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a>xlAddInManagerInfo/xlAddInManagerInfo12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�A�h�C�� �}�l�[�W���[�� Excel �Z�b�V�����ŏ��߂ČĂяo���ꂽ�Ƃ��ɁAMicrosoft Excel �ɂ���ČĂяo����܂��B���̊֐��́A���g�p�̃A�h�C���ɂ��Ă̏���A�h�C�� �}�l�[�W���[�ɒ񋟂��邽�߂Ɏg�p����܂��B
  
Excel 2007 �ȍ~�̃o�[�W�����ł́AXLL �ɂ���ăG�N�X�|�[�g�����ꍇ�ɂ� **xlAddInManagerInfo** �ł͂Ȃ� **xlAddInManagerInfo12** ���Ăяo����܂��B **xlAddInManagerInfo12** �֐��́A **xlAddInManagerInfo** �Ɠ����悤�ɋ@�\���āAXLL �̓���ɂ�����o�[�W�����ŗL�̑���_�������K�v������܂��BExcel �ł́A **xlAddInManagerInfo12** �� **XLOPER12** �f�[�^�^��Ԃ��A **xlAddInManagerInfo** �� **XLOPER** �f�[�^�^��Ԃ��K�v������܂��B
  
**xlAddInManagerInfo12** �֐��� Excel 2007 ���O�� Excel �o�[�W�����ł͌Ăяo����܂���B **XLOPER12** ��T�|�[�g���Ă��Ȃ����߂ł��B
  
Excel �ł́AXLL ������炢���ꂩ�̊֐���������ăG�N�X�|�[�g���邱�Ƃ͕s�v�ł��B
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxAction:_ 数値**XLOPER または XLOPER12** (**xltypeInt**または**xltypeNum**) へのポインター。
  
Excel �ŗv���������ł��B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

_pxAction_ �����l 1 �̏ꍇ (1 �ɂȂ�悤�������邱�Ƃ�ł��܂�)�A���̊֐����������ƁA�A�h�C���ɂ��Ă̏�� (�ʏ�͖��O�B�o�[�W�����ԍ����܂܂�邱�Ƃ����܂�) ���܂܂�镶���񂪕Ԃ�܂��B����ȊO�̏ꍇ�A#VALUE ��Ԃ��܂��B 
  
�������Ԃ��Ȃ��ꍇ�AExcel ���߂�l�𕶎���ɕϊ����悤�Ƃ��܂��B
  
## <a name="remarks"></a>����

�Ԃ���镶���񂪁A���I�Ɋ��蓖�Ă�ꂽ�o�b�t�@�[��|�C���g���Ă���ꍇ�́A���̃o�b�t�@�[��ŏI�I�ɉ������K�v������܂��B������ Excel �ɂ���Ċ��蓖�Ă�ꂽ�ꍇ�A **xlbitXLFree** ��ݒ肵�ĉ�����܂��B������ DLL �ɂ���Ċ��蓖�Ă�ꂽ�ꍇ�ɂ́A **xlbitDLLFree** ��ݒ肵�ĉ�����܂��B����ɁA [xlAutoFree](xlautofree-xlautofree12.md) ( **XLOPER** ��Ԃ��ꍇ) �܂��� **xlAutoFree12** ( **XLOPER12** ��Ԃ��ꍇ) ��������Ȃ���΂Ȃ�܂���B
  
## <a name="example"></a>��

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a>関連項目



[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)

