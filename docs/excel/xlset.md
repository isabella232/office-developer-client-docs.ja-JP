---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- xlset function [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 63f50e441f5d851677f36754a17bcd6403705239
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799001"
---
# <a name="xlset"></a>xlSet

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�萔�l��Z����͈͂ɂ��΂₭�z�u���܂��B�ڂ����́A�u[Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��](known-issues-in-excel-xll-development.md)�v�́uxlSet �Ɣz�񐔎���܂ރu�b�N�v��������������B
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>�p�����[�^�[

_pxReference_(**xltypeRef**または**xltypeSRef**)
  
目的セルまたはセルを記述する四角形の参照です。 参照が、隣接するセルを記述する必要があります**xltypeRef**で`val.mref.lpmref->count`を 1 に設定する必要があります。 
  
_pxValue_
  
�Z���ɔz�u�����l�ł��B�ڂ����́A�u���v�Z�N�V������������������B
  
## <a name="remarks"></a>����

### <a name="pxvalue-argument"></a>pxValue 引数

_pxValue_は、値または配列の場合か。 値の場合は、全体の目的の範囲にその値が格納されます。 配列 (**xltypeMulti**) である場合、配列の要素は、四角形内の対応する場所に配置されます。
  
2 番目の引数の横方向の配列を使用する場合、重複していますダウン全体の四角形を塗りつぶす。 縦方向の配列を使用する場合は、四角形全体を入力するには、右、重複しています。 四角形の配列を使用すると、四角形の範囲内に配置するのには小さすぎますが、その範囲に **#N/A**s が埋め込まれます。
  
�Ώ۔͈͂��\�[�X�z�����������ꍇ�́A�Ώ۔͈͂̋��E�܂Œl���R�s�[����A�]���ȃf�[�^�͖�������܂��B
  
�w��̒����**** �S�̂��������ɂ́A2 �Ԗڂ̈�����ȗ����܂��B 
  
### <a name="restrictions"></a>����

**xlSet** ����ɖ߂����Ƃ͂ł��܂���B�܂��A�ȑO�͎g�p�\�������A���ɖ߂�����Ɋւ����񂪔j������܂��B 
  
**xlSet** �ł́A�Z���ɒ萔�݂̂�z�u�ł��A�����͔z�u�ł��܂���B 
  
**xlSet** �́A�N���X 3 �R�}���h�Ɠ����̊֐��Ƃ��ē��삵�܂��B�܂�ADLL ���I�u�W�F�N�g�A�}�N���A���j���[�A�c�[���o�[�A�V���[�g�J�b�g �L�[�A **[�}�N��]** �_�C�A���O �{�b�N�X�� **[���s]** �{�^�� (Excel 2007 �Ŏn�܂郊�{���� **[�\��]** �^�u�A����шȑO�̃o�[�W�����ł� **[�c�[��]** ���j���[����A�N�Z�X�ł��܂�) ����Ăяo���ꂽ�ꍇ�ɂ̂� DLL �Ŏg�p�ł��܂��B 
  
## <a name="example"></a>��

���̗�ł́A�}�N������n���ꂽ�l�� B205:B206 �ɓ��͂���܂��B���̃R�}���h�֐��̗�ɂ͈������K�v�ł���A **Application.Run** ���\�b�h��g�p���āAXLM �}�N�� �V�[�g�� VBA ���W���[������Ăяo�����ꍇ�ɂ̂ݓ��삵�܂��B 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a>�֘A����

- [xlCoerce](xlcoerce.md)
- [DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

