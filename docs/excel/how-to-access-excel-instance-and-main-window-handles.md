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
# <a name="access-excel-instance-and-main-window-handles"></a><span data-ttu-id="c0b29-104">Excel のインスタンスをアクセスし、メイン ウィンドウのハンドル</span><span class="sxs-lookup"><span data-stu-id="c0b29-104">Access Excel Instance and Main Window Handles</span></span>

 <span data-ttu-id="c0b29-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c0b29-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c0b29-p101">Windows ���Ńv���O���~���O�����ꍇ�AMicrosoft Excel �̃C���X�^���X �n���h���܂��̓��C�� �E�B���h�E�̃n���h���̗�����K�v�ɂȂ邱�Ƃ�����܂��B���Ƃ��΁A�����̃n���h���́A�J�X�^���� Windows �_�C�A���O �{�b�N�X��쐬���A�\������̂ɖ𗧂��܂��B</span><span class="sxs-lookup"><span data-stu-id="c0b29-p101">To program in the Windows environment, sometimes you must know the Microsoft Excel instance handle or main window handle. For example, these handles are useful when you are creating and displaying custom Windows dialog boxes.</span></span>
  
<span data-ttu-id="c0b29-p102">�����̃n���h���ւ̃A�N�Z�X��񋟂��� 2 �� XLL ��p�� C API �֐�������܂��B���ꂼ��ɑΉ����� [xlGetInst](xlgetinst.md) �֐��� [xlGetHwnd](xlgethwnd.md) �֐��ł��BWin32 �ł́A���ׂẴn���h���� 32 �r�b�g�̐����ł��B�������A **XLOPER** ���݌v���ꂽ�Ƃ��AWindows �� 16 �r�b�g �V�X�e���ł����B���������āA�\���̂� 16 �r�b�g �n���h���̂݉\�ł��BWin32 �ł́A **Excel4** �܂��� **Excel4v** �ŌĂяo���ꂽ�Ƃ��ɁA **xlGetInst** �֐��� **xlGetHwnd** �֐��́A���S�� 32 �r�b�g �n���h���̉��ʕ����݂̂�Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="c0b29-p102">There are two XLL-only C API functions that provide access to these handles: the [xlGetInst](xlgetinst.md) function and the [xlGetHwnd](xlgethwnd.md) function respectively. In Win32, all handles are 32-bit integers. However, when the **XLOPER** was designed, Windows was a 16-bit system. Therefore, the structure only allowed for 16-bit handles. In Win32, when called with **Excel4** or **Excel4v**, the **xlGetInst** function and the **xlGetHwnd** function return only the low part of the full 32-bit handle.</span></span> 
  
<span data-ttu-id="c0b29-113">Excel 2007 �ȍ~�̃o�[�W�����ł́A[Excel12](excel4-excel12.md) �܂��� [Excel12v](excel4v-excel12v.md) �ł����̊֐����Ăяo�����ƁA�Ԃ���� **XLOPER12** �͊��S�� 32 �r�b�g �n���h�����琬���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="c0b29-113">In Excel 2007 and later versions, when these functions are called with [Excel12](excel4-excel12.md) or [Excel12v](excel4v-excel12v.md), the returned **XLOPER12** contains the full 32-bit handle.</span></span> 
  
<span data-ttu-id="c0b29-p103">���S�ȃC���X�^���X �n���h���̎擾�́A�ǂ̃o�[�W������ Excel �ł�e�Ղł��BDLL ���ǂݍ��܂��Ƃ��ɌĂяo����� Windows �R�[���o�b�N **DllMain** �ɁA���S�ȃC���X�^���X �n���h�����n����܂��B���̃C���X�^���X �n���h����O���[�o���ϐ��ɋL�^����ꍇ�A **xlGetInst** �֐���Ăяo���K�v�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="c0b29-p103">Obtaining the full instance handle is simple in any version of Excel, as it is passed to the Windows callback **DllMain**, which is called when the DLL is loaded. If you record this instance handle in a global variable, you never need to call the **xlGetInst** function.</span></span> 
  
## <a name="obtaining-the-main-excel-handle-in-excel-2003-and-earlier"></a><span data-ttu-id="c0b29-116">Excel 2003 �ȑO�̃o�[�W�����ł� ���C�� Excel �n���h���̎擾</span><span class="sxs-lookup"><span data-stu-id="c0b29-116">Obtaining the Main Excel Handle in Excel 2003 and Earlier</span></span>

<span data-ttu-id="c0b29-p104">Excel 2003 �ȑO�� 32 �r�b�g �o�[�W�����̃��C�� Excel �n���h����擾����ɂ́A�܂� **xlGetHwnd** �֐���Ăяo���A���ۂ̃n���h���̉��ʃ��[�h��擾���܂��B���ɁA�Ԃ��ꂽ���ʃ��[�h�ƈ�v�����̂�������邽�߂ɁA�g�b�v���x�� �E�B���h�E�̈ꗗ�𔽕���������K�v������܂��B���̃R�[�h�́A���̋Z�@������Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="c0b29-p104">To obtain the main Excel handle in Excel 2003 and earlier 32-bit versions, you must first call the **xlGetHwnd** function to obtain the low word of the actual handle. Then, you must iterate the list of top-level windows to search for a match with the returned low word. The following code illustrates the technique.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="c0b29-120">�֘A����</span><span class="sxs-lookup"><span data-stu-id="c0b29-120">See also</span></span>



[<span data-ttu-id="c0b29-121">DLL �܂��� XLL �t�@�C���̒�����_�C�A���O �{�b�N�X��\������</span><span class="sxs-lookup"><span data-stu-id="c0b29-121">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
[<span data-ttu-id="c0b29-122">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="c0b29-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="c0b29-123">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="c0b29-123">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

