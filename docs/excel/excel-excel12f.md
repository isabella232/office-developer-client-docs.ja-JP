---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- excel function [excel 2007],Excel12f function [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798809"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
フレームワーク ライブラリの機能です。 **Excel**は、 [Excel4](excel4-excel12.md)関数のラッパーです。 **Excel12f**は、 [Excel12](excel4-excel12.md)関数のラッパーです。 それぞれは、どの引数が 0 で、一時**XLOPER**または**XLOPER12**の作成が失敗したことを示すであることを確認するを確認します。 エラーが発生する場合は、各デバッグ メッセージを出力します。 完了したら、各一時**XLOPER**と**XLOPER12**の作成されている可能性があるすべての一時的なメモリを解放します。
  
 **Excel12f** �́AExcel 2007 C API ���C�u�����ȍ~�� DLL ����̂݌Ăяo�����Ƃ��ł��܂��B����ɁAExcel 2007 �ȍ~�ŋN�������Ƃ��̂ݓ��삵�A����ȊO�� **xlretFailed** �Ŏ��s���܂��B 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>�p�����[�^�[

 _iFunction_(**int**)
  
�Ăяo���R�}���h�܂��͊֐���������l�B�ڍׂɂ��ẮA[Excel4�AExcel12](excel4-excel12.md) ��Q�Ƃ��Ă��������B
  
 _pxRes_
  
�]�����ꂽ�֐��̌��ʂ̃|�C���^�B���ʂɎ�����郁�����͂��ׂāAExcel �ɂ���Ċ��蓖�Ă��A�s�v�ɂȂ����� [xlFree](xlfree.md) ��Ăяo���ĉ�����邩�A�܂��� Excel �ɖ߂��ꍇ�� **xlbitXLFree** ��ݒ肵�ĉ�����܂��B 
  
 _iCount_(**int**)
  
�֐��ɓn���������̐��BExcel 2007 �ȍ~�A������ 255 �ɐ�������Ă��܂��B����ȑO�̃o�[�W�����̐����l�� 30 �ł��B
  
 _argument1, ..._
  
�ȗ��\�ȁA�֐��̈����B���ׂĂ̈����́A **Excel** �̏ꍇ�� **XLOPER** �ւ̃|�C���^�[�A **Excel12f** �̏ꍇ�� **XLOPER12** �ւ̃|�C���^�[�ɂ���K�v������܂��B
  
## <a name="return-value"></a>�߂�l

どちらの関数は、同じエラーが発生し、 **Excel4**、 **Excel4v**、 **Excel12**、および**Excel12v**としての成功コードを返します。 これらのコードの詳細については、 [Excel4/Excel12](excel4-excel12.md)を参照してください。 さらに、これらのフレームワークの機能は、パラメーターに NULL ポインターの場合は、C API を呼び出さずに**xlretFailed**が検出されたを返します。 
  
## <a name="example"></a>��

���̗�ł́A�s���Ȉ����� **Excel12f** �֐��ɓn���āA�f�o�b�K�[�Ƀ��b�Z�[�W�𑗐M���Ă��܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>�֘A����



[Excel4�AExcel12](excel4-excel12.md)


[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

