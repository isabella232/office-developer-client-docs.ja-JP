---
title: XLOper12ToXLOper
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOper12ToXLOper
keywords:
- xloper12toxloper function [excel 2007]
localization_priority: Normal
ms.assetid: b46f87c4-778b-4502-be57-c3725f73a644
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 2c06102699db8810da803ecc0ddfa30375fcc125
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798993"
---
# <a name="xloper12toxloper"></a>XLOper12ToXLOper

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�V���� **XLOPER12** ����Â� **XLOPER** �ւ̕ϊ��Ɏg�p����ϊ����[�`���ł��B
  
```cs
BOOL XLOper12ToXLOper(LPXLOPER12 pxloper12, LPXLOPER pxloper);
```

## <a name="parameters"></a>�p�����[�^�[

_pxloper12_(**LPXLOPER12**)
  
�ϊ��Ώۂ̃\�[�X **XLOPER12** �ւ̃|�C���^�[�B 
  
_pxloper_(**LPXLOPER**)
  
�ϊ����ꂽ�l��i�[����^�[�Q�b�g **XLOPER** �ւ̃|�C���^�[�B 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

�ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B 
  
## <a name="remarks"></a>����

**XLOPER12** �̌^�ɉ����āA�ϊ������l�ɐV���������� �o�b�t�@�[����蓖�Ă܂��B�^�[�Q�b�g **XLOPER** �́A���̃o�b�t�@�[��|�C���g���܂��B�ϊ��ɐ��������ꍇ�́A�R�s�[�Ɋ֘A�t����ꂽ��������Ăяo�����ŉ������K�v������܂��B **FreeXLOperT** ��g�p���邱�Ƃ�A **free** ��g�p���Ē��ډ�����邱�Ƃ�ł��܂��B
  
�ϊ������s�����ꍇ�́A�Ăяo�����Ń�������������K�v�͂���܂���B
  
**XLOPER12** ���� **XLOPER** �ւ̕ϊ��́A **XLOPER** �Ɏ��܂肫��Ȃ��قǑ傫���z���Q�ƁA�܂��͒��������� **XLOPER12** �Ɋi�[����Ă���ƁA���s���邱�Ƃ�����܂� 
  
**XLOPER12** �� Unicode ���C�h����������́A���P�[���Ɉˑ�������@�� **XLOPER** �� ASCII �o�C�g������ɕϊ�����܂��B 
  
**XLOPER12** **xltypeInt** �� 32 �r�b�g�����t�������ł��B **XLOPER** **xltypeInt** �� 16 �r�b�g�����t�������ł��B�w�肳�ꂽ **XLOPER12** ������ **XLOPER** �����̐����𒴂���ꍇ�́A���̐����� 8 �o�C�g�� double �ɕϊ�����A **xltypeNum** �^�� **XLOPER** �ŕԂ���܂��B���̏ꍇ�ɂ̂݁A���̊֐��͕ϊ����� **XLOPER** �̌^��ύX���܂��B
  
### <a name="example"></a>��

���̊֐��̃R�[�h�ɂ��ẮA�t�@�C��  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����

- [�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

