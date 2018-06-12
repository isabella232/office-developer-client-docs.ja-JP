---
title: �t���[�����[�N ���C�u�����̊֐�
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- framework library functions [excel 2007],functions [Excel 2007], Framework library
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798893"
---
# <a name="functions-in-the-framework-library"></a>�t���[�����[�N ���C�u�����̊֐�

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
フレームワーク ライブラリは、Xll を簡単に記述するために作成されました。 **XLOPER**を管理するための単純な関数が含まれています/ 一時**XLOPER**を作成、**XLOPER12**メモリ/ **XLOPER12**、堅牢 (**Excel4**、 **Excel4v** Microsoft Excel の関数を呼び出す、* * Excel12 * *、* * Excel12v * *) と印刷は、接続されている端末上の文字列をデバッグします。
  
���̃��C�u�����Ɋ܂܂�Ă���֐��́A���̂悤�ȃR�[�h�̈ꕔ��ȗ�������̂ɖ𗧂��܂��B
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

�ȗ������ꂽ�R�[�h�͎��̗�̂悤�ɂȂ�܂��B
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

���̊֐����t���[�����[�N ���C�u�����Ɋ܂܂�Ă��܂��B
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**XLOPER �Ŏg�p����֐�**|**XLOPER12 �Ŏg�p����֐�**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[TempErr](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
�����̊֐���g�p����ƁADLL �܂��� XLL ��L�q���邽�߂ɕK�v�Ȏ��Ԃ�Z���ł��܂��B�܂��A�T���v�� �A�v���P�[�V���� GENERIC ����J����J�n���Ă�J�����Ԃ�Z�k�ł��܂��BGENERIC.C ��e���v���[�g�Ƃ��Ďg�p���āAXLL �̃t���[�����[�N��Z�b�g�A�b�v���Ă���A�����̃R�[�h��Ǝ��̃R�[�h�ɒu�������邱�Ƃ��ł��܂��B
  
�ꎞ�I�� **XLOPER**/ **XLOPER12** �֐��́A�t���[�����[�N ���C�u�����ɂ���ĊǗ�����郍�[�J�� �q�[�v�̃�������g�p���� **XLOPER**/ **XLOPER12** �l��쐬���܂��B **FreeAllTempMemory** �֐��A������� /  �֐��܂��� **Excel12f** �֐��̂����ꂩ��Ăяo���܂ŁA **XLOPER********XLOPER12** �̒l�͗L���Ȃ܂܈ێ�����܂��B( **Excel** �֐��� **Excel12f** �֐��́A���ʂ�Ԃ��O�ɂ��ׂĂ̈ꎞ�������������܂��B) 
  
�t���[�����[�N ���C�u�����̊֐���g�p����ɂ́AFRAMEWRK.H �t�@�C���� C �R�[�h�Ɋ܂߁AFRAMEWRK.C �t�@�C���܂��� FRMWRK32.LIB �t�@�C����R�[�h �v���W�F�N�g�ɒǉ�����K�v������܂��B
  
## <a name="see-also"></a>�֘A����

- [Excel XLL SDK API �֐����t�@�����X](excel-xll-sdk-api-function-reference.md)

