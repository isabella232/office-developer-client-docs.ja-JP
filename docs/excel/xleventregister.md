---
title: xlEventRegister
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b98637d4-02e3-4dbd-8be5-6b46d32980c6
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: d837d87c479f70f0184a7cf1612dea5ab8c99e6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798975"
---
# <a name="xleventregister"></a>xlEventRegister

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�C�x���g �n���h���[�̓o�^�Ɏg�p���܂��BExcel 2010 �ɓ�������܂����B
  
```vb
Excel12(xlEventRegister, LPXLOPER12 pxRes, 2, LPXLOPER12 pxProcedure, LPXLOPER12 pxEvent);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxProcedure_(**xltypeStr**)
  
DLL �R�[�h�Ŏ�����Ă���A�C�x���g �n���h���[�֐��̖��O�B
  
 _pxEvent_(**xltypeInt**)
  
_pxProcedure_ �p�����[�^�[�Ŏw�肵���֐��ŏ��������C�x���g�B 
  
Excel 2010 �ȍ~�� Excel �ł́A���̃C�x���g��T�|�[�g���Ă��܂��B
  
|**�C�x���g**|**���**|
|:-----|:-----|
|**xleventCalculationEnded** <br/> |Excel ���v�Z����������Ƃ��ɔ������܂��B�v�Z���Ɋ��蓖�Ă����\�[�X�́A���̃C�x���g�̌�ŉ���ł��܂��B  <br/> |
|**xleventCalculationCanceled** <br/> |���[�U�[���v�Z�𒆒f�����Ƃ��ɔ������܂��BXLL �́A������񓯊��̃A�N�e�B�r�e�B���~���܂��B���̃C�x���g�̒���ɁACalculationEnded �C�x���g���������܂��B  <br/> |
   
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

成功した場合は、 **TRUE** (**xltypeBool**) を返します。 失敗した場合は、 **FALSE**が返されます。
  
## <a name="see-also"></a>�֘A����



[�񓯊��̃��[�U�[��`�֐�](asynchronous-user-defined-functions.md)

