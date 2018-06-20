---
title: DIALOGMsgProc
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- DIALOGMsgProc
keywords:
- dialogmsgproc function [excel 2007]
localization_priority: Normal
ms.assetid: 9a538e83-ba34-4806-bb8c-7cda3beb6b66
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 3a69d192babbcf0419850e203f51d8cfd81cdef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798773"
---
# <a name="dialogmsgproc"></a>DIALOGMsgProc

**適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
この手順が関連付けられているネイティブの Windows のダイアログ ボックスでその[fShowDialog](fshowdialog.md)が表示されます。 ダイアログ ボックスのボタン、入力フィールド、またはコントロールのいずれかの操作時に発生するイベント (メッセージ) の windows と呼ばれるサービス ルーチンが用意されています。 
  
```cs
BOOL CALLBACK DIALOGMsgProc(HWND hWndDlg, UINT message, WPARAM wParam, LPARAM lParam);
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

 ���b�Z�[�W����������Ă���ꍇ�� **TRUE**�A�������̏ꍇ�� **FALSE**�B 
  
### <a name="example"></a>��

���̊֐��̃\�[�X �R�[�h�ɂ��ẮA `\SAMPLES\GENERIC\GENERIC.C` ��Q�Ƃ��Ă��������B 
  
## <a name="see-also"></a>�֘A����



[�ėp DLL �̊֐�](functions-in-the-generic-dll.md)

