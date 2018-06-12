---
title: xlSheetId
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetId
keywords:
- xlsheetid function [excel 2007]
localization_priority: Normal
ms.assetid: cb32059c-b899-49cf-8028-ff828998ab75
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e4e184d4e456ffe26292fe31b1b41463834216f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798989"
---
# <a name="xlsheetid"></a>xlSheetId

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�O���Q�Ƃ�쐬���邽�߂ɁA���O�t���̃V�[�g�̃V�[�g ID ��������܂��B
  
```cs
Excel12(xlSheetId, LPXLOPER12 pxRes, 1, LPXLOPER12 pxSheetName);
```

## <a name="parameters"></a>�p�����[�^�[

_pxSheetName_(**xltypeStr**)
  
(省略可能)。 詳細を確認するブックとシートの名前です。 省略した場合、 **xlSheetId**関数は、(前面) のアクティブ シートのシート ID を返します。 
  
## <a name="return-value"></a>�߂�l

_pxRes-\>val.mref.idSheet_ �̃V�[�g ID ��Ԃ��܂��B 
  
> [!NOTE]
> [!����]  _pxRes-\>val.mref.lpmref_ �z��|�C���^�[�́A���̌Ăяo���̌�� NULL �ɐݒ肳��邽�߁A **xlFree** ��Ăяo���āA���̃^�C�v�ɒʏ�܂܂�Ă��郁������������K�v�͂���܂��� (����͊��S�Ɉ��S�ł����K�v����܂���)�B 
  
## <a name="remarks"></a>����

�w�肳�ꂽ�V�[�g��܂ރu�b�N�́A���̊֐���g�p���邽�߂ɊJ���Ă���K�v������܂��BDLL ����J���Ă��Ȃ��u�b�N�ւ̎Q�Ƃ�쐬������@�͂���܂���B **xlSheetId** ��g�p�����Q�Ƃ̍쐬�̏ڍׂɂ��ẮA�u [Excel �̃������Ǘ�](memory-management-in-excel.md)�v�� **xltypeRef** �쐬�̗��Q�Ƃ��Ă��������B 
  
## <a name="example"></a>��

 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetIdExample(void)
{       
   XLOPER12 xSheetName, xRes;
   xSheetName.xltype = xltypeStr;
   xSheetName.val.str = L"\022[BOOK1.XLSX]Sheet1";
   Excel12(xlSheetId, &xRes, 1, (LPXLOPER12)&xSheetName);
   Excel12f(xlcAlert, 0, 1, TempNum12(xRes.val.mref.idSheet));
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>関連項目

- [xlSheetNm](xlsheetnm.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

