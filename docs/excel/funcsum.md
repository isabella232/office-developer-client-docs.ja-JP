---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum function [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798886"
---
# <a name="funcsum"></a>FuncSum

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
1 ���� 29 �̈��������āA���̍��v��v�Z���郆�[�U�[��`���[�N�V�[�g�֐��̗�B�e�����Ɏw��ł���̂́A1 �̐����A�͈́A�܂��͔z��ł��BGENERIC.xll ���ǂݍ��܂��ƁAGENERIC.xll �ɂ���Ă��̊֐����o�^����āA���[�N�V�[�g����Ăяo�����Ƃ��ł���悤�ɂȂ�܂��B 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>�p�����[�^�[

 _px1 px29_(**LPXLOPER12**)
  
**XLOPER12** �����ւ̃|�C���^�[�B�֐��́A�C�ӂ̓��͂̌^��󂯓���܂����A�����A�����̃��e�����z��A����ѐ����܂��͋󔒃Z���݂̂��܂܂�Ă���͈͂�Ώۂɍ쓮����悤�R�[�f�B���O����Ă��܂��B29 �����̈��������������ƁA�c��̈����� **xltypeMissing** �Ƃ��ċ�������܂��B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

**LPXLOPER12 xltypeNum** ( **xltypeErr**)
  
�������ꂽ�������X�g�A�͈͓�̃Z���A�z���̗v�f�ɁA�����ȊO�̕��������݂���ꍇ�́A�����̍��v�A���邢�� #VALUE!�B
  
### <a name="example"></a>��

���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[�ėp DLL �̊֐�](functions-in-the-generic-dll.md)

