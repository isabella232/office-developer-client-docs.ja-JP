---
title: UnhookExcelWindow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- UnhookExcelWindow
keywords:
- unhookexcelwindow function
localization_priority: Normal
ms.assetid: 6508cb69-0c7c-4d8c-a466-dd79eb13e316
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7b70bf4ed0ff45921df407605baa692c7621bca4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798959"
---
# <a name="unhookexcelwindow"></a>UnhookExcelWindow

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
**HookExcelWindow** �ɂ���ĈȑO�ɃC���X�g�[�����ꂽ **ExcelCursorProc** ��폜���܂��B����́AMicrosoft Excel ���C�� **WndProc** �̑O�� **ExcelCursorProc** ���Ăяo�����Ƃ��Ɏ��s����܂��B
  
```cs
extern void FAR PASCAL UnhookExcelWindow(HANDLE hWndExcel);
```

## <a name="parameters"></a>�p�����[�^�[

 _hWndExcel_(**処理**)
  
Excel �̃��C�� �E�B���h�E �n���h���B
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

���̊֐��͒l��Ԃ��܂���B
  
## <a name="remarks"></a>����

���̊֐��́A **SetWindowLong()** ��g�p���� Excel ����� **WndProc** �𕜌����A **HookExcelWindow()** �ɂ���ĕۑ����ꂽ�A�h���X�𕜌����܂��B
  
### <a name="example"></a>��

���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[�ėp DLL �̊֐�](functions-in-the-generic-dll.md)

