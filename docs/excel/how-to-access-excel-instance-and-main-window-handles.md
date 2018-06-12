---
title: Excel のインスタンスをアクセスし、メイン ウィンドウのハンドル
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accessing excel handles,handles [Excel 2007], accessing,Excel instances, accessing,window handles [Excel 2007], accessing
localization_priority: Normal
ms.assetid: 21e1dbdc-06fa-4514-9437-c4cffc3b4621
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 035cd2a8423e3ab14f4b2ca4b73fbc39641e54d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798897"
---
# <a name="access-excel-instance-and-main-window-handles"></a>Excel のインスタンスをアクセスし、メイン ウィンドウのハンドル

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Windows ���Ńv���O���~���O�����ꍇ�AMicrosoft Excel �̃C���X�^���X �n���h���܂��̓��C�� �E�B���h�E�̃n���h���̗�����K�v�ɂȂ邱�Ƃ�����܂��B���Ƃ��΁A�����̃n���h���́A�J�X�^���� Windows �_�C�A���O �{�b�N�X��쐬���A�\������̂ɖ𗧂��܂��B
  
�����̃n���h���ւ̃A�N�Z�X��񋟂��� 2 �� XLL ��p�� C API �֐�������܂��B���ꂼ��ɑΉ����� [xlGetInst](xlgetinst.md) �֐��� [xlGetHwnd](xlgethwnd.md) �֐��ł��BWin32 �ł́A���ׂẴn���h���� 32 �r�b�g�̐����ł��B�������A **XLOPER** ���݌v���ꂽ�Ƃ��AWindows �� 16 �r�b�g �V�X�e���ł����B���������āA�\���̂� 16 �r�b�g �n���h���̂݉\�ł��BWin32 �ł́A **Excel4** �܂��� **Excel4v** �ŌĂяo���ꂽ�Ƃ��ɁA **xlGetInst** �֐��� **xlGetHwnd** �֐��́A���S�� 32 �r�b�g �n���h���̉��ʕ����݂̂�Ԃ��܂��B 
  
Excel 2007 �ȍ~�̃o�[�W�����ł́A[Excel12](excel4-excel12.md) �܂��� [Excel12v](excel4v-excel12v.md) �ł����̊֐����Ăяo�����ƁA�Ԃ���� **XLOPER12** �͊��S�� 32 �r�b�g �n���h�����琬���Ă��܂��B 
  
���S�ȃC���X�^���X �n���h���̎擾�́A�ǂ̃o�[�W������ Excel �ł�e�Ղł��BDLL ���ǂݍ��܂��Ƃ��ɌĂяo����� Windows �R�[���o�b�N **DllMain** �ɁA���S�ȃC���X�^���X �n���h�����n����܂��B���̃C���X�^���X �n���h����O���[�o���ϐ��ɋL�^����ꍇ�A **xlGetInst** �֐���Ăяo���K�v�͂���܂���B 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a>Excel 2003 �ȑO�̃o�[�W�����ł� ���C�� Excel �n���h���̎擾

Excel 2003 �ȑO�� 32 �r�b�g �o�[�W�����̃��C�� Excel �n���h����擾����ɂ́A�܂� **xlGetHwnd** �֐���Ăяo���A���ۂ̃n���h���̉��ʃ��[�h��擾���܂��B���ɁA�Ԃ��ꂽ���ʃ��[�h�ƈ�v�����̂�������邽�߂ɁA�g�b�v���x�� �E�B���h�E�̈ꗗ�𔽕���������K�v������܂��B���̃R�[�h�́A���̋Z�@������Ă��܂��B 
  
```cs
typedef struct _EnumStruct
{
  HWND hwnd;  // Return value for Excel main hWnd.
  unsigned short wLoword; //Contains LowWord of the Excel main hWnd
} EnumStruct;
#define CLASS_NAME_BUFFER  50
BOOL CALLBACK EnumProc(HWND hwnd, EnumStruct * pEnum)
{
  // First check the class of the window. Must be "XLMAIN".
  char rgsz[CLASS_NAME_BUFFER];
  GetClassName(hwnd, rgsz, CLASS_NAME_BUFFER);
  if (!lstrcmpi(rgsz, "XLMAIN"))
  {
    // If that hits, check the loword of the window handle.
    if (LOWORD((DWORD) hwnd) == pEnum->wLoword)
    {
      // We have a match, return Excel main hWnd.
      pEnum->hwnd = hwnd;
      return FALSE;
    }
  }
  // No match - continue the enumeration.
  return TRUE;
}
BOOL GetHwnd(HWND * pHwnd)
{
  XLOPER x;
  //
  // xlGetHwnd only returns the LoWord of Excel hWnd
  // so all the windows have to be enumerated to see
  // which match the LoWord retuned by xlGetHwnd.
  //
  if (Excel4(xlGetHwnd, &x, 0) == xlretSuccess)
  {
    EnumStruct enm;
    enm.hwnd = NULL;
    enm.wLoword = x.val.w;
    EnumWindows((WNDENUMPROC) EnumProc, (LPARAM) &enm);
    if (enm.hwnd != NULL)
    {
      *pHwnd = enm.hwnd;
      return TRUE;
    }
  }
  return FALSE;
}
```

## <a name="see-also"></a>�֘A����



[DLL �܂��� XLL �t�@�C���̒�����_�C�A���O �{�b�N�X��\������](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Excel XLL �̊J��](developing-excel-xlls.md)

