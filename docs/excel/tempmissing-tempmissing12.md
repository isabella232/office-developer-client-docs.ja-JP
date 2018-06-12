---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- tempmissing function [excel 2007],TempMissing12 function [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798953"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�^�C�v **xltypeMissing** �̈ꎞ / ******XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>�p�����[�^�[

���̊֐��Ƀp�����[�^�[�͂���܂���B
  
## <a name="return-value"></a>�߂�l

**xltypeMissing** **XLOPER**/ **XLOPER12** �Ƀ|�C���^�[��Ԃ��܂��B
  
## <a name="example"></a>��

���̗�ł� **TempMissing12** ��g�p���� 3 �̕s������������ **xlcWorkspace** �Ɏw�肵�A���̌�� **Boolean** **FALSE** ��w�肵�āA���[�N�V�[�g�̃X�N���[�� �o�[�̕\�����\���ɂ��܂��B�ŏ��� 3 �̈����́A�e����󂯂Ȃ����̃��[�N�X�y�[�X�ݒ�ɑΉ����܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

