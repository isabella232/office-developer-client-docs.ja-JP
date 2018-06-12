---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12 function [excel 2007],TempInt function [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798952"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
������܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐��B 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>�p�����[�^�[

 _i_
  
�Ώۂ̐����l�B **XLOPER** �����́A�����t�� 16 �r�b�g���� (short int) �ł���̂ɑ΂��A **XLOPER12** �����́A�����t�� 32 �r�b�g���� ([long] int) �ł��邱�Ƃɂ����ӂ��������B 
  
## <a name="return-value"></a>�߂�l

�n���ꂽ�l��܂� **xltypeInt** ������Ԃ��܂��B 
  
## <a name="example"></a>��

���̗�ł́A **TempInt12** �֐���g�p���āA **xlfGetWorkspace** �Ɉ�����n���Ă��܂��B
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

