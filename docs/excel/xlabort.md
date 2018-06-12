---
title: xlAbort
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAbort
keywords:
- xlabort function [excel 2007]
localization_priority: Normal
ms.assetid: 0fe71454-6b00-464b-8abf-afb209d57754
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e90cbe496404b4cc602dee1ad21c91c8f5f91bfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798965"
---
# <a name="xlabort"></a>xlAbort

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
�V�X�e����̑��̃^�X�N�Ƀv���Z�b�T�𐶐����A���[�U�[�� **Esc** ������ă}�N��������������ǂ�����m�F���܂��B�u�b�N�̍Čv�Z���Ƀ��[�U�[�� **Esc** ���������ꍇ�́A���̊֐���Ăяo�����Ƃɂ���ă��[�N�V�[�g�֐���Ō��o���邱�Ƃ�ł��܂��B 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a>�p�����[�^�[

 _pxRetain_(**xltypeBool**)
  
(省略可能)。 **FALSE**、この関数にすると、ブレーク条件をチェックし、保留されている改行をクリアします。 ブレーク条件があっても続行するのにはこれを使用できます。 場合はこの引数を省略するか**は**、関数は、それをオフにすることがなくユーザーの中断をチェックします。
  
## <a name="property-valuereturn-value"></a>プロパティ値/戻り値

ユーザーが**esc キー**を押した場合は**TRUE** (**xltypeBool**) を返します。
  
## <a name="remarks"></a>����

### 

#### <a name="frequent-calls-may-be-needed"></a>�p�ɂȌĂяo�����K�v�ȏꍇ

���Ԃ̂�����֐���R�}���h�ł́A���̊֐���p�ɂɌĂяo���āA�v���Z�b�T��V�X�e����̑��̃^�X�N�ɐ�������K�v������܂��B
  
#### <a name="avoid-sensitive-language"></a>�����ȕ\��������

���[�U�[ �C���^�[�t�F�C�X�ł� "Abort" �Ƃ����p���g�p���Ȃ��悤�ɂ��܂��B����� "Cancel"�A"Halt"�A"Break"�A"Stop" �̎g�p��������Ă��������B
  
## <a name="example"></a>��

���̃R�[�h�́A1 �����o�߂���܂ŁA�܂��̓��[�U�[�� **Esc** ������܂ŁA�V�[�g��ŃA�N�e�B�u�ȃZ����J��Ԃ��ړ����܂��B�֐� **xlAbort** ��Ăяo�����Ƃ����܂��B����ɂ��v���Z�b�T����������A�����ł̃}���`�^�X�L���O���e�ՂɂȂ�܂��B 
  
 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
int WINAPI fDance(void)
{
   DWORD dtickStart;
   XLOPER12 xAbort, xConfirm;
   int boolSheet;
   int col=0;
   XCHAR rgch[32];
//
// Check what kind of sheet is active. If it is a worksheet or macro
// sheet, this function will move the selection in a loop to show
// activity. In any case, it will update the status bar with a countdown.
//
// Call xlSheetId; if that fails the current sheet is not a macro sheet or
// worksheet. Next, get the time at which to start. Then start a while
// loop that will run for one minute. During the while loop, check if the
// user has pressed ESC. If true, confirm the abort. If the abort is
// confirmed, clear the message bar and return; if the abort is not
// confirmed, clear the abort state and continue. After checking for an
// abort, move the active cell if on a worksheet or macro. Then
// update the status bar with the time remaining.
//
// This block uses TempActiveCell12(), which creates a temporary XLOPER12.
// The XLOPER12 contains a reference to a single cell on the active sheet.
// This function is part of the framework library.
//
   boolSheet = (Excel12f(xlSheetId, 0, 0) == xlretSuccess);
   dtickStart = GetTickCount();
   while (GetTickCount() < dtickStart + 60000L)
   {
      Excel12f(xlAbort, &xAbort, 0);
      if (xAbort.val.xbool)
      {
         Excel12f(xlcAlert, &xConfirm, 2,
           TempStr12(L"Are you sure you want to cancel this operation?"),
              TempNum12(1));
         if (xConfirm.val.xbool)
         {
            Excel12f(xlcMessage, 0, 1, TempBool12(0));
            return 1;
         }
         else
         {
            Excel12f(xlAbort, 0, 1, TempBool12(0));
         }
      }
      if (boolSheet)
      {
         Excel12f(xlcSelect, 0, 1,
            TempActiveCell12(0,(BYTE)col));
         col = (col + 1) & 3;
      }
      wsprintfW(rgch,L"0:%lu",
         (60000 + dtickStart - GetTickCount()) / 1000L);
      Excel12f(xlcMessage, 0, 2, TempBool12(1), TempStr12(rgch));
   }
   Excel12f(xlcMessage, 0, 1, TempBool12(0));
   return 1;
}
```

## <a name="see-also"></a>�֘A����



[DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

