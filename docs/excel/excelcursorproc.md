---
title: ExcelCursorProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ExcelCursorProc
keywords:
- excelcursorproc function [excel 2007]
localization_priority: Normal
ms.assetid: 43759617-998d-4030-a17d-c4bbe35ffaf9
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 07be8da4a07b988d5e848048a088859b58ea3a14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798872"
---
# <a name="excelcursorproc"></a>ExcelCursorProc

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel のウィンドウをモーダル ダイアログ ボックスが表示されたら、カーソルは、Excel ウィンドウの上でビジー カーソルが。 この**WndProc**トラップ WM_SETCURSOR では、Windows メッセージと、カーソルが通常の矢印に戻す変更を入力します。 
  
```cs
LRESULT CALLBACK ExcelCursorProc(HWND hwnd, UINT wMsg, WPARAM wParam, LPARAM lParam);
```

## <a name="parameters"></a>�p�����[�^�[

 _hWndDlg_(**HWND**)
  
�_�C�A���O �{�b�N�X�� HWND Windows �n���h����܂�ł��܂��B
  
 _メッセージ_(**UINT**)
  
�������b�Z�[�W
  
 _wParam_(**WPARAM**)
  
 _lParam_(**LPARAM**)
  
Windows ���n��������
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

LRESULT:���b�Z�[�W���n���h�����ꂽ�ꍇ�� 0�A����ȊO�̏ꍇ�́A����� **WndProc** ����Ԃ���錋�ʁB
  
### <a name="example"></a>��

���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[�ėp DLL �̊֐�](functions-in-the-generic-dll.md)

