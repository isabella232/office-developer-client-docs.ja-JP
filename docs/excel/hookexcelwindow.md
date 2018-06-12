---
title: HookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- HookExcelWindow
keywords:
- hookexcelwindow function [excel 2007]
localization_priority: Normal
ms.assetid: 13f0ae5e-9951-4e89-a245-7cf68c6f6724
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 8965cc6b1e3d24001c42744f2ee7d447aa4c79b5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798891"
---
# <a name="hookexcelwindow"></a>HookExcelWindow

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**ExcelCursorProc** ��C���X�g�[�����āAMicrosoft Excel �̃��C�� **WndProc** �̑O�ɌĂяo�����悤�ɂ��܂��B
  
```cs
extern void FAR PASCAL HookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>�p�����[�^�[

 _hWndExcel_(**処理**)
  
Excel �̃��C�� �E�B���h�E �n���h���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

���̊֐��͒l��Ԃ��܂���B
  
## <a name="remarks"></a>����

���̊֐��́A **GetWindowLong()** ��g�p���� Excel **WndProc** �̃A�h���X��擾���܂��B����� **WndProc** ��Ăяo���A�������邽�߂Ɏg�p�ł��邱�̒l��O���[�o���Ɋi�[���܂��B�Ō�ɁA **SetWindowLong()** ��g�p���āA���̃A�h���X�� **ExcelCursorProc** �̃A�h���X�ɒu�������܂��B
  
### <a name="example"></a>��

���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[�ėp DLL �̊֐�](functions-in-the-generic-dll.md)

