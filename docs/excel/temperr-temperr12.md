---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- temperr function [excel 2007],TempErr12 function [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798943"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel ���[�N�V�[�g�̃G���[��܂ވꎞ **XLOPER**/ **XLOPER12**��쐬����t���[�����[�N ���C�u�����֐��B 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>�p�����[�^�[

 _err_
  
�ړI�̃G���[ �R�[�h�܂��̓��e�������l�Ɠ����̐��l����̕\�Ɏ����܂��B
  
|**�G���[**|**XLCALL.H �Œ�`���ꂽ�G���[ �R�[�h**|**������ 10 �i��**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7  <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15  <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>�߂�l

�n���ꂽ�G���[ �R�[�h��܂� **xltypeBool** ��Ԃ��܂��B 
  
## <a name="example"></a>��

���̗�ł́A **TempErr12** �֐���g�p���� #VALUE! �G���[�� Excel �ɕԂ��܂��B 
  
> [!NOTE]
> [!����] �t���[�����[�N ���C�u�����֐� **TempErr12** �́A����o�b�t�@�[���烁��������蓖�Ă܂��B���̃������́A�ʏ�A�t���[�����[�N�֐� **Excel12f** ���Ăяo�����Ɖ������܂��B���̗�̊֐����A **Excel12f** ��Ăяo�����ɌJ��Ԃ��Ăяo�����ƁA������ ���[�N���������܂��B 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

