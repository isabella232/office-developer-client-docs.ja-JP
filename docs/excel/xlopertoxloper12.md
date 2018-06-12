---
title: XLOperToXLOper12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- XLOperToXLOper12
keywords:
- xlopertoxloper12 function [excel 2007]
localization_priority: Normal
ms.assetid: b2d4581b-ebf6-4eba-aa95-69a5a9ee8028
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 76c78e5a2ad62b1a3d1aa23748b10e49e07f6543
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799008"
---
# <a name="xlopertoxloper12"></a>XLOperToXLOper12

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�Â� **XLOPER** ����V���� **XLOPER12** �ւ̕ϊ��Ɏg�p����ϊ����[�`���ł��B
  
```cs
BOOL XLOperToXLOper12(LPXLOPER pxloper, LPXLOPER12 pxloper12);
```

## <a name="parameters"></a>�p�����[�^�[

_pxloper_(**LPXLOPER**)
  
�ϊ��Ώۂ̃\�[�X **XLOPER** �ւ̃|�C���^�[�B 
  
_pxloper12_(**LPXLOPER12**)
  
�ϊ����ꂽ�l��i�[����^�[�Q�b�g **XLOPER12** �ւ̃|�C���^�[�B 
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

�ϊ������������ꍇ�� **TRUE**�B����ȊO�̏ꍇ�� **FALSE**�B 
  
## <a name="remarks"></a>����

**XLOPER** �̌^�ɉ����āA�ϊ������l�ɐV���������� �o�b�t�@�[����蓖�Ă܂��B�^�[�Q�b�g **XLOPER12** �́A���̃o�b�t�@�[��|�C���g���܂��B�ϊ��ɐ��������ꍇ�́A�R�s�[�Ɋ֘A�t����ꂽ��������Ăяo�����ŉ������K�v������܂��B **FreeXLOper12T** ��g�p���邱�Ƃ�A **free** ��g�p���Ē��ډ�����邱�Ƃ�ł��܂��B
  
�ϊ������s�����ꍇ�́A�Ăяo�����Ń�������������K�v�͂���܂���B
  
��ʂɁA�C�ӂ� **XLOPER** ���� **XLOPER12** �ւ̕ϊ����\�ł��B����ɑ΂��āA **XLOPER12** ���� **XLOPER** �ւ̕ϊ��́A **XLOPER** �Ɏ��܂肫��Ȃ��قǑ傫���z���Q�ƁA�܂��͒��������� **XLOPER12** �Ɋi�[����Ă���ƁA���s���邱�Ƃ�����܂� 
  
**XLOPER** �� ASCII �o�C�g������́A���P�[���Ɉˑ�������@�� **XLOPER12** �� Unicode ���C�h����������ɕϊ�����܂��B 
  
### <a name="example"></a>��

���̊֐��̃R�[�h�ɂ��ẮA�t�@�C��  `\SAMPLES\FRAMEWRK\FRAMEWRK.C` ��Q�Ƃ��Ă��������B 
  

