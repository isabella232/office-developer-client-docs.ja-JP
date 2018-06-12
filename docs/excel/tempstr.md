---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- tempstr function [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798955"
---
# <a name="tempstr"></a>TempStr

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**xltypeStr** �o�C�g�������i�[���Ă���ꎞ�I�� **XLOPER** ��쐬����A�񐄏��̃t���[�����[�N ���C�u�����֐��ł��B���͂Ƃ��āANULL �ŏI������\�[�X�������󂯎��܂��B�󂯎����������̍ŏ��̕�����㑱�̕�����̒����ŏ㏑�����悤�Ƃ��܂��B���̓���͈��S�łȂ����Ƃ�����A�ǂݎ���p�̕������n���ƁAMicrosoft Excel ���N���b�V������\��������܂��B 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>�p�����[�^�[

 _str_
  
NULL �ŏI������\�[�X������ւ̃|�C���^�[�B **TempStr** �� 255 �o�C�g��������������؂�l�߂܂��B 
  
## <a name="return-value"></a>�߂�l

�n���ꂽ������o�b�t�@�[�ւ̃|�C���^�[��i�[���Ă��� **xltypeStr** �������Ԃ��܂��B 
  
## <a name="remarks"></a>����

���̕��@�ɂ��ꎞ�I�ȕ�����̍쐬�́A[TempStrConst �� TempStr12](tempstrconst-tempstr12.md) �̗����œ��삷����@�Ƃ��Ă͐�������Ȃ��Ȃ�܂����B�����̊֐��́A�V���������� �o�b�t�@�[����蓖�ĂāA���̃o�b�t�@�[�ɓn���ꂽ�������R�s�[���܂��B **TempStrConst** �� **TempStr12** �̓��͕�����͕ύX����Ȃ����߁A **const** �Ƃ��Đ錾����܂��B����ɑ΂��āA **TempStr** �ւ̓��͕�����͕ύX����邽�߁A **const** �Ƃ��Đ錾�ł��܂���B���͕�����̍ŏ��̕����́A���������̃X�y�[�X�Ƃ��Ĉ����A���̊֐��ɂ���ď㏑������܂��B
  
## <a name="see-also"></a>�֘A����



[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)

