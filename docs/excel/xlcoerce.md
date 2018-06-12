---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- xlcoerce function [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798976"
---
# <a name="xlcoerce"></a>xlCoerce

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**XLOPER**/ **XLOPER12** �̌^��ʂ̌^�ɕϊ����邩�A�V�[�g�̃Z���̒l��������܂��B 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxSource_
  
�ϊ��Ώۂ̃\�[�X **XLOPER**/ **XLOPER12**�B 
  
 _pxDestType_(**xltypeInt**)
  
(省略可能)。 結果の型のビット マスクを受け入れるように喜んでいます。 複数の使用可能な型を指定するのには、ビットごとの**OR**演算子 (|) を使用してください。 この引数を省略すると、1 つのセルへの参照が値型の**xltypeStr**、 **xltypeNum**、 **xltypeBool**、 **xltypeErr**、 **xltypeNil** (参照先セルが空の場合)、およびブロックへの参照のいずれかに変換されます。セルは、 **xltypeMulti**に変換されます。 これにより、 **xlCoerce**はセルの値を検索する最も便利な方法です。 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

(**XltypeStr**、 **xltypeNum**、 **xltypeBool**、 **xltypeErr**、 **xltypeNil**、または**xltypeMulti**) は、強制変換された値を返します。
  
## <a name="remarks"></a>����

 **xlCoerce** �� **xltypeBigData** �܂��� **xltypeFlow** �ɕϊ��ł����A���̋t�̕ϊ���ł��܂���B **xltypeMissing** �܂��� **xltypeNil** �̌^��  _pxDestType_ �Ƃ��ēn�����Ƃ́A������ȗ����邱�Ƃɑ������܂��B�ꍇ�ɂ���ẮA�ϊ������s����ꍇ������܂��B���Ƃ��΁A������ɂ͐����ɕϊ��łȂ���̂�����܂��B 
  
�z��܂��͕����Z���̎Q�Ƃ�P��l�̌^�ɕϊ�����ƁA���ʂ͈�ԏ�̍��̃Z���܂��͔z��̗v�f�̒l�ɂȂ�܂��B
  
## <a name="example"></a>��

���̃R�[�h�́A `\SAMPLES\EXAMPLE\EXAMPLE.C` �ɂ���܂��B 
  
> [!NOTE]
> [!����] �����Ɏ�����鋭���菇���폜����A **xInt** ������ **xlcAlert** �ɓn�����悤�ɁA **xlcAlert** �֐��͈ÖٓI�Ɉ����𕶎���ɕϊ����悤�Ƃ��܂��B **xlcAlert** �̓R�}���h�̃}�N���ł��邽�߁A���̃R�[�h�̓}�N�� �V�[�g����Ăяo���ꂽ�Ƃ��̂ݐ������쓮���܂��B 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[xlSet](xlset.md)


[DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

