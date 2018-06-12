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
# <a name="xlabort"></a><span data-ttu-id="3f50f-104">xlAbort</span><span class="sxs-lookup"><span data-stu-id="3f50f-104">xlAbort</span></span>

 <span data-ttu-id="3f50f-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f50f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3f50f-p101">�V�X�e����̑��̃^�X�N�Ƀv���Z�b�T�𐶐����A���[�U�[�� **Esc** ������ă}�N��������������ǂ�����m�F���܂��B�u�b�N�̍Čv�Z���Ƀ��[�U�[�� **Esc** ���������ꍇ�́A���̊֐���Ăяo�����Ƃɂ���ă��[�N�V�[�g�֐���Ō��o���邱�Ƃ�ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="3f50f-p101">Yields the processor to other tasks in the system and checks whether the user has pressed **ESC** to cancel a macro. If the user has pressed **ESC** during a workbook recalculation, it can also be detected from within a worksheet function by calling this function.</span></span> 
  
```cs
Excel12(xlAbort, LPXLOPER12 pxRes, 1, LPXLOPER12 pxRetain);
```

## <a name="parameters"></a><span data-ttu-id="3f50f-108">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3f50f-108">Parameters</span></span>

 <span data-ttu-id="3f50f-109">_pxRetain_(**xltypeBool**)</span><span class="sxs-lookup"><span data-stu-id="3f50f-109">_pxRetain_ (**xltypeBool**)</span></span>
  
<span data-ttu-id="3f50f-110">(省略可能)。</span><span class="sxs-lookup"><span data-stu-id="3f50f-110">(Optional).</span></span> <span data-ttu-id="3f50f-111">**FALSE**、この関数にすると、ブレーク条件をチェックし、保留されている改行をクリアします。</span><span class="sxs-lookup"><span data-stu-id="3f50f-111">If **FALSE**, this function checks for the break condition and clears any pending break.</span></span> <span data-ttu-id="3f50f-112">ブレーク条件があっても続行するのにはこれを使用できます。</span><span class="sxs-lookup"><span data-stu-id="3f50f-112">This enables the user to continue despite the break condition.</span></span> <span data-ttu-id="3f50f-113">場合はこの引数を省略するか**は**、関数は、それをオフにすることがなくユーザーの中断をチェックします。</span><span class="sxs-lookup"><span data-stu-id="3f50f-113">If this argument is omitted or is **TRUE**, the function checks for a user abort without clearing it.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="3f50f-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="3f50f-114">Property value/Return value</span></span>

<span data-ttu-id="3f50f-115">ユーザーが**esc キー**を押した場合は**TRUE** (**xltypeBool**) を返します。</span><span class="sxs-lookup"><span data-stu-id="3f50f-115">Returns **TRUE** (**xltypeBool**) if the user has pressed **ESC**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f50f-116">����</span><span class="sxs-lookup"><span data-stu-id="3f50f-116">Remarks</span></span>

### 

#### <a name="frequent-calls-may-be-needed"></a><span data-ttu-id="3f50f-117">�p�ɂȌĂяo�����K�v�ȏꍇ</span><span class="sxs-lookup"><span data-stu-id="3f50f-117">Frequent Calls May Be Needed</span></span>

<span data-ttu-id="3f50f-118">���Ԃ̂�����֐���R�}���h�ł́A���̊֐���p�ɂɌĂяo���āA�v���Z�b�T��V�X�e����̑��̃^�X�N�ɐ�������K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="3f50f-118">Functions and commands that could take a long time should call this function frequently to yield the processor to other tasks in the system.</span></span>
  
#### <a name="avoid-sensitive-language"></a><span data-ttu-id="3f50f-119">�����ȕ\��������</span><span class="sxs-lookup"><span data-stu-id="3f50f-119">Avoid Sensitive Language</span></span>

<span data-ttu-id="3f50f-p103">���[�U�[ �C���^�[�t�F�C�X�ł� "Abort" �Ƃ����p���g�p���Ȃ��悤�ɂ��܂��B����� "Cancel"�A"Halt"�A"Break"�A"Stop" �̎g�p��������Ă��������B</span><span class="sxs-lookup"><span data-stu-id="3f50f-p103">Avoid using the term "Abort" in your user interface. Consider using "Cancel," "Halt," "Break," or "Stop" instead.</span></span>
  
## <a name="example"></a><span data-ttu-id="3f50f-122">��</span><span class="sxs-lookup"><span data-stu-id="3f50f-122">Example</span></span>

<span data-ttu-id="3f50f-p104">���̃R�[�h�́A1 �����o�߂���܂ŁA�܂��̓��[�U�[�� **Esc** ������܂ŁA�V�[�g��ŃA�N�e�B�u�ȃZ����J��Ԃ��ړ����܂��B�֐� **xlAbort** ��Ăяo�����Ƃ����܂��B����ɂ��v���Z�b�T����������A�����ł̃}���\`�^�X�L���O���e�ՂɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="3f50f-p104">The following code repeatedly moves the active cell on a sheet until one minute has elapsed or until the user presses **ESC**. It calls the function **xlAbort** occasionally. This yields the processor, easing cooperative multitasking.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="3f50f-126">�֘A����</span><span class="sxs-lookup"><span data-stu-id="3f50f-126">See also</span></span>



[<span data-ttu-id="3f50f-127">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="3f50f-127">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

