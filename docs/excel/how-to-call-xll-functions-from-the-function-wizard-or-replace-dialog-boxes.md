---
title: 関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xll functions [excel 2007], calling from replace dialog box,Replace dialog box [Excel 2007], calling XLL functions,Function Wizard [Excel 2007], calling XLL functions,XLL functions [Excel 2007], calling from Function Wizard
localization_priority: Normal
ms.assetid: dc7e840e-6d1d-427b-97f9-7912e60ec954
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 7ebb33a5b98cebedfca7fb5923e62486bfd85696
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798894"
---
# <a name="call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes"></a><span data-ttu-id="22189-104">関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し</span><span class="sxs-lookup"><span data-stu-id="22189-104">Call XLL Functions from the Function Wizard or Replace Dialog Boxes</span></span>

 <span data-ttu-id="22189-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="22189-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="22189-p101">�����̏ꍇ�AMicrosoft Excel �̓u�b�N (�v�Z���}�N���̐��䉺�ɂ���ꍇ�̓u�b�N�̈ꕔ) �̒ʏ�̍Čv�Z���� XLL �֐���Ăяo���܂��B�֐��͖��O�t���͈͂����t�������ݒ莮�Ɋ܂܂�Ă��邱�Ƃ�����A�Z���̐����ɂ͑��݂��Ȃ����Ƃ�����_�ɒ��ӂ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="22189-p101">Microsoft Excel usually calls XLL functions during the normal recalculation of the workbook, or a part of it if the calculation is under the control of a macro. Remember that the function might not reside in a cell formula but might be part of a named range definition, or a conditional formatting expression.</span></span>
  
<span data-ttu-id="22189-108">2 つ、[Excel] ダイアログ ボックスから関数を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="22189-108">There are two circumstances where a function can be called from an Excel dialog box.</span></span> <span data-ttu-id="22189-109">1 つは、**貼り付けの関数の引数**] ダイアログ ボックスは、ユーザーが同時に関数呼び出しの 1 つの引数を構築することです。</span><span class="sxs-lookup"><span data-stu-id="22189-109">One is the **Paste Function Arguments** dialog box, where users are able to construct a function call one argument at a time.</span></span> <span data-ttu-id="22189-110">数式がされているときは、もう一方を変更し、[**置換**] ダイアログ ボックスで Excel を使用して再入力します。</span><span class="sxs-lookup"><span data-stu-id="22189-110">The other is when formulas are being modified and reentered by Excel in the **Replace** dialog box.</span></span> <span data-ttu-id="22189-111">ダイアログ ボックスの [**貼り付けの関数の引数**は、正常に実行する関数をしないことも。</span><span class="sxs-lookup"><span data-stu-id="22189-111">For the **Paste Function Arguments** dialog box, you might not want your function to execute normally.</span></span> <span data-ttu-id="22189-112">実行に時間がかかるし、ダイアログ ボックスを使用して速度が低下しない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="22189-112">This may be because it takes a long time to execute and you do not want to slow down the use of the dialog box.</span></span> 
  
<span data-ttu-id="22189-113">**[関数貼り付け**] ダイアログ ボックスと、[**置換**] ダイアログ ボックスの両方がある Windows クラスの名前・ **bosa_sdm_XL**・ n、n は数値です。</span><span class="sxs-lookup"><span data-stu-id="22189-113">Both the **Paste Function** dialog box and the **Replace** dialog box have the Windows class name **bosa_sdm_XL**n, where n is a number.</span></span> <span data-ttu-id="22189-114">Windows には、 **GetClassName**Windows のハンドル、HWND 変数の型からこの名前を取得する API 関数が用意されています。</span><span class="sxs-lookup"><span data-stu-id="22189-114">Windows provides an API function, **GetClassName**, that obtains this name from a Windows handle, an HWND variable type.</span></span> <span data-ttu-id="22189-115">また、 **EnumWindows**、(DLL) 内で指定されたコールバック関数を呼び出す別の関数と現在開いているすべてのトップレベル ウィンドウの。</span><span class="sxs-lookup"><span data-stu-id="22189-115">It also provides another function, **EnumWindows**, that calls a supplied callback function (within your DLL) once for every top-level window that is currently open.</span></span>
  
<span data-ttu-id="22189-116">�R�[���o�b�N�֐��́A���̎菇�ł̂ݎ��s����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="22189-116">The callback function needs to perform only the following steps:</span></span>
  
1. <span data-ttu-id="22189-117">���̃E�B���h�E�̐e�� Excel �̌��݂̃C���X�^���X�ł��邱�Ƃ�m�F���܂� (���s���̃C���X�^���X����������ꍇ)�B</span><span class="sxs-lookup"><span data-stu-id="22189-117">Check if the parent of this window is the current instance of Excel (in case there are multiple instances running).</span></span>
    
2. <span data-ttu-id="22189-118">Windows �ɂ���ēn���ꂽ�n���h������N���X����擾���܂��B</span><span class="sxs-lookup"><span data-stu-id="22189-118">Get the class name from the handle passed in by Windows.</span></span>
    
3. <span data-ttu-id="22189-119">�N���X���� **bosa_sdm_XL**n �̌\`���ł��邱�Ƃ�m�F���܂��B</span><span class="sxs-lookup"><span data-stu-id="22189-119">Check if the class name is of the form **bosa_sdm_XL**n.</span></span>
    
4. <span data-ttu-id="22189-120">2 つのダイアログ ボックスの間の区別をする場合は、ダイアログ ボックスのタイトルに識別するテキストが含まれているかどうかを確認してください。</span><span class="sxs-lookup"><span data-stu-id="22189-120">If you need to distinguish between the two dialog boxes, check if the dialog box title contains some identifying text.</span></span> <span data-ttu-id="22189-121">**GetWindowText**Windows API 呼び出しを使用して、ウィンドウのタイトルを取得します。</span><span class="sxs-lookup"><span data-stu-id="22189-121">The window title is obtained using the Windows API call **GetWindowText**.</span></span>
    
<span data-ttu-id="22189-p105">���� C++ �R�[�h�́AWindows �ɓn�����N���X�ƃR�[���o�b�N������Ă��܂� (��L�̎菇����s���܂�)�B����́A�Y������_�C�A���O �{�b�N�X�̂ǂ��炩�ɐ�p�̃e�X�g��Ăяo���֐�����Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="22189-p105">The following C++ code shows a class and callback to be passed to Windows that performs these steps. This is called by the functions that call test specifically for either of the dialog boxes concerned.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="22189-p106">������ Excel �̃o�[�W�����̃E�B���h�E �^�C�g���͕ύX�����\��������A���̃R�[�h�������ɂȂ邱�Ƃ�����܂��B�܂��A **window_title_text** �� **NULL** �ɐݒ肷��ƁA�R�[���o�b�N�̌����ŃE�B���h�E �^�C�g���𖳎�����Ƃ������ʂ������܂��B</span><span class="sxs-lookup"><span data-stu-id="22189-p106">Window titles of future Excel versions might change and invalidate this code. Note also that setting **window_title_text** to **NULL** has the effect of ignoring window title in the callback search.</span></span> 
  
```cs
#define CLASS_NAME_BUFFSIZE  50
#define WINDOW_TEXT_BUFFSIZE  50
// Data structure used as input to xldlg_enum_proc(), called by
// called_from_paste_fn_dlg(), called_from_replace_dlg(), and
// called_from_Excel_dlg(). These functions tell the caller whether
// the current worksheet function was called from one or either of
// these dialog boxes.
typedef struct
{
  bool is_dlg;
  short low_hwnd;
  char *window_title_text; // set to NULL if don't care
}
  xldlg_enum_struct;
// The callback function called by Windows for every top-level window.
BOOL CALLBACK xldlg_enum_proc(HWND hwnd, xldlg_enum_struct *p_enum)
{
// Check if the parent window is Excel.
// Note: Because of the change from MDI (Excel 2010)
// to SDI (Excel 2013), comment out this step in Excel 2013.
  if(LOWORD((DWORD)GetParent(hwnd)) != p_enum->low_hwnd)
    return TRUE; // keep iterating
  char class_name[CLASS_NAME_BUFFSIZE + 1];
//  Ensure that class_name is always null terminated for safety.
  class_name[CLASS_NAME_BUFFSIZE] = 0;
  GetClassName(hwnd, class_name, CLASS_NAME_BUFFSIZE);
//  Do a case-insensitve comparison for the Excel dialog window
//  class name with the Excel version number truncated.
  size_t len; // The length of the window's title text
  if(_strnicmp(class_name, "bosa_sdm_xl", 11) == 0)
  {
// Check if a searching for a specific title string
    if(p_enum->window_title_text) 
    {
// Get the window's title and see if it matches the given text.
      char buffer[WINDOW_TEXT_BUFFSIZE + 1];
      buffer[WINDOW_TEXT_BUFFSIZE] = 0;
      len = GetWindowText(hwnd, buffer, WINDOW_TEXT_BUFFSIZE);
      if(len == 0) // No title
      {
        if(p_enum->window_title_text[0] != 0)
          return TRUE; // No match, so keep iterating
      }
// Window has a title so do a case-insensitive comparison of the
// title and the search text, if provided.
      else if(p_enum->window_title_text[0] != 0
      && _stricmp(buffer, p_enum->window_title_text) != 0)
        return TRUE; // Keep iterating
    }
    p_enum->is_dlg = true;
    return FALSE; // Tells Windows to stop iterating.
  }
  return TRUE; // Tells Windows to continue iterating.
}
```

<span data-ttu-id="22189-126">**[�֐��̓\��t��]** �_�C�A���O �{�b�N�X�ɂ̓^�C�g��������܂���B���̂��߁A���Ɏ����֐��ł́A�^�C�g���̂Ȃ��E�B���h�E�Ƃ�����v�����\�����߂ɁA�^�C�g�������̕�����ɋ�̕�����ł��� "" ��R�[���o�b�N�֐��ɓn���Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="22189-126">The **Paste Function** dialog box does not have a title, so the following function passes a search title string of "", that is, an empty string, to the callback to indicate that the match condition is that the window should not have a title.</span></span> 
  
```cs
bool called_from_paste_fn_dlg(void)
{
    XLOPER xHwnd;
// Calls Excel4, which only returns the low part of the Excel
// main window handle. This is OK for the search however.
    if(Excel4(xlGetHwnd, &xHwnd, 0))
        return false; // Couldn't get it, so assume not
// Search for bosa_sdm_xl* dialog box with no title string.
    xldlg_enum_struct es = {FALSE, xHwnd.val.w, ""};
    EnumWindows((WNDENUMPROC)xldlg_enum_proc, (LPARAM)&es);
    return es.is_dlg;
}
```

## <a name="see-also"></a><span data-ttu-id="22189-127">�֘A����</span><span class="sxs-lookup"><span data-stu-id="22189-127">See also</span></span>



<span data-ttu-id="22189-128">[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="22189-128">[Accessing XLL Code in Excel](accessing-xll-code-in-excel.md)</span></span>
  
[<span data-ttu-id="22189-129">DLL �܂��� XLL ���� Excel �ɌĂяo��</span><span class="sxs-lookup"><span data-stu-id="22189-129">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
[<span data-ttu-id="22189-130">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="22189-130">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

