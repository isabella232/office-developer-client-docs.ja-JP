---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm function [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798999"
---
# <a name="xlsheetnm"></a>xlSheetNm

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�O���Q�ƂɊ܂܂�����V�[�g ID ����A���[�N�V�[�g�܂��̓}�N�� �V�[�g�̖��O (����Q�Ƃ��n����ꍇ�́A���݂̃V�[�g�̖��O) ��Ԃ��܂��B
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>�p�����[�^�[

_pxExtref_(**xltypeRef**または**xltypeSRef**)
  
���O��擾����V�[�g�ւ̎Q�ƁB
  
(**XltypeRef**) の外部参照を渡す場合のみを含める必要は、シートの ID です。 ワークシートのセルを表すデータ構造体は無視され、提供する必要はありません。 ID は、0 に設定されている場合、 **xlSheetNm**は、現在のシートの名前を返します。 
  
(**XltypeSef**) の内部参照を渡す場合、 **xlSheetNm**は、現在のシートの名前を返します。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

フォームのシート (**xltypeStr**) の名前を返します`[Book1]Sheet1`。
  
## <a name="example"></a>��

���̗�́A�֐��̌Ăяo�����̃V�[�g�̖��O��\�����܂��B���̊֐��́AXLM �̃R�}���h �}�N���̎��s���Ƀ}�N�� �V�[�g����Ăяo���ꂽ�ꍇ�̂ݐ���ɓ��삵�܂��B����́A�R�}���h���������s�ł��� **xlcAlert** �̌Ăяo����s���Ă��邽�߂ł��B�܂��A **xlfCaller** ���Q�Ƃ�Ԃ��悤�ɂ���ɂ́A�_�C�A���O �{�b�N�X�A���j���[�܂��̓R�}���h �o�[����ł͂Ȃ��A�V�[�g����Ăяo����Ă���K�v�����邽�߂ł��B 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>�֘A����

- [xlSheetId](xlsheetid.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

