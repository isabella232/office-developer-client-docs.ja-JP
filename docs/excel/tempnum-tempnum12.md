---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- tempnum12 function [excel 2007],TempNum function [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798949"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel ���[�N�V�[�g�̔ԍ���܂ވꎞ **XLOPER**/ **XLOPER12** ��쐬����t���[�����[�N ���C�u�����֐� (IEEE 8 �o�C�g�̔{���x���������_�^)�B 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>�p�����[�^�[

 _d_ (**ダブル**)
  
�z��l�BIEEE �K�i�̔񐳋K���͌��݃T�|�[�g����Ă��Ȃ����߁A�[���Ɋۂ߂��܂��B���̖�����ɑΉ����Ă��܂��B
  
## <a name="return-value"></a>�߂�l

�n�����l��܂ސ��l **xltypeNum**�B�܂��́A�񐳋K�����l�ɓn���ꂽ�ꍇ�̓[����Ԃ��܂��B 
  
## <a name="example"></a>��

���̗�ł́A **TempNum12** �֐���g�p���āA **xlfGetWorkspace** �Ɉ�����n���Ă��܂��B
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

