---
title: xlfSetName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfSetName
keywords:
- xlfsetname function [excel 2007]
localization_priority: Normal
ms.assetid: ea7fd713-7c1b-4648-a609-3334f595c61a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 48ce927f6bcb328a90779948a660cf9d0b460205
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798972"
---
# <a name="xlfsetname"></a>xlfSetName

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
DLL �Ɋ֘A�t�����Ă����`�ς݂̖��O��쐬����э폜���邽�߂Ɏg�p���܂��B
  
```cs
Excel12(xlfSetName, LPXLOPER12 pxRes, 2, LPXLOPER12 pxNameText, LPXLOPER12 pxNameDefinition);
```

## <a name="parameters"></a>�p�����[�^�[

_pxNameText_(**xltypeStr**)
  
���O�͈̔́B���̖��O�́A�L���Ȗ��O�Ɋւ��� Microsoft Excel �̒ʏ�̐����ɏ�������K�v������܂��B
  
_pxNameDefinition_(**xltypeStr**、 **xltypeNum**、 **xltypeBool**、 **xltypeErr**、 **xltypeMulti**、 **xltypeSRef**、 **xltypeRef**、または**xltypeInt**)
  
(省略可能)。 値、値、セル、またはセルの範囲のセットは、その_pxNameText_として定義されます。 省略すると、名前が削除されます。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

_pxRes_(**xltypeBool**または**xltypeErr**)
  
���삪���������ꍇ�� TRUE�A���O���쐬�܂��͍폜�ł��Ȃ��ꍇ�� FALSE�B1 �܂��͕����̈����������̏ꍇ�� #VALUE! ��Ԃ��܂��B
  
## <a name="remarks"></a>����

**xlfRegister** �ƗL����  _pxFunctionText_ ������g�p���Ċ֐��܂��̓R�}���h��o�^����ꍇ�AExcel ��DLL ���\�[�X�Ɋ֘A�t����ꂽ����쐬���܂��BDLL ���A�����[�h�����ƁA���̂悤�Ȗ��O�� [xlfSetName �֐�](xlfsetname.md)��g�p���č폜����K�v������܂��B�������A���̑���� Excel �̊��m�̖�肪�����Ŏ��s���܂��B�ڍׂɂ��ẮA�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v��Q�Ƃ��Ă��������B
  
### <a name="example"></a>��

**** �� `\SAMPLES\GENERIC\GENERIC.C` �֐��ɂ��ẮA�R�[�h��Q�Ƃ��Ă��������B
  
## <a name="see-also"></a>�֘A����

- [�d�v�Ŗ�ɗ��� C API XLM �֐�](essential-and-useful-c-api-xlm-functions.md)

