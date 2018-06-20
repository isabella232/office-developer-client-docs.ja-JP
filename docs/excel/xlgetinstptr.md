---
title: xlGetInstPtr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a166f39c-f10b-4e56-8b5d-e6a54ee08c8f
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7cc07093e5db335d01fe85527746594d34d4d938
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798994"
---
# <a name="xlgetinstptr"></a>xlGetInstPtr

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
���� DLL ��Ăяo���Ă��� Microsoft Excel �C���X�^���X�̃C���X�^���X �n���h����Ԃ��܂��B
  
```cs
Excel4(xlGetInstPtr, LPXLOPER pxRes, 0);Excel12(xlGetInstPtr, LPXLOPER12 pxRes, 0);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��ɂ͈����͂���܂���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

インスタンス ハンドル (**xltypeBigData**) は、 **val.bigdata.h.hdata**フィールドになります。 
  
## <a name="remarks"></a>����

���̊֐���g�p����ƁADLL ��Ăяo���Ă��� Excel �̕����̎��s���C���X�^���X�����ł��܂��B
  
この関数は、32 ビットと 64 ビットの両方のバージョンの Excel で適切な値を返します。 導入 Excel 2010 の拡張機能として、 [xlGetInst](xlgetinst.md)関数を 32 ビット バージョンの Excel でのみ正常に動作します。 
  
**XLOPER**および**XLOPER12**の両方は、 **xltypeBigData**の値をサポートしているのと同じ構造を持つための API のコールバック関数、 [Excel4 と Excel12](excel4-excel12.md)の種類を使用して呼び出されたときにこの関数が正常に動作します。入力します。 
  
## <a name="example"></a>��

���̎g�p��ł́A�Ō�ɌĂяo���� Excel �R�s�[ �C���X�^���X��A���݌Ăяo���Ă��� Excel �R�s�[�Ɣ�r���܂��B�����ꍇ�ɂ� 1 ��Ԃ��A�قȂ�ꍇ�ɂ� 0 ��Ԃ��܂��B�֐������s����ƁA-1 ��Ԃ��܂��B���̎g�p��́A32 �r�b�g�� 64 �r�b�g�̗����̃o�[�W������ Excel �ō쓮���܂��B
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlGetInstPtrExample(void)
{
    XLOPER12 xRes;
    static HANDLE hOld = 0;
    short iRet;
    if (Excel12(xlGetInstPtr, &xRes, 0) != xlretSuccess)
    iRet = -1;
    else
    {
    HANDLE hNew;
    hNew =  xRes.val.bigdata.h.hdata;
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

- [xlGetHwnd](xlgethwnd.md)
- [xlGetInst](xlgetinst.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

