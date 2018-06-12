---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm function [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798999"
---
# <a name="xlsheetnm"></a><span data-ttu-id="7e1c0-104">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="7e1c0-104">xlSheetNm</span></span>

<span data-ttu-id="7e1c0-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e1c0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7e1c0-106">�O���Q�ƂɊ܂܂�����V�[�g ID ����A���[�N�V�[�g�܂��̓}�N�� �V�[�g�̖��O (����Q�Ƃ��n����ꍇ�́A���݂̃V�[�g�̖��O) ��Ԃ��܂��B</span><span class="sxs-lookup"><span data-stu-id="7e1c0-106">Returns the name of a worksheet or macro sheet from its internal sheet ID contained within an external reference, or the name of the current sheet if passed an internal reference.</span></span>
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a><span data-ttu-id="7e1c0-107">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="7e1c0-107">Parameters</span></span>

<span data-ttu-id="7e1c0-108">_pxExtref_(**xltypeRef**または**xltypeSRef**)</span><span class="sxs-lookup"><span data-stu-id="7e1c0-108">_pxExtref_ (**xltypeRef** or **xltypeSRef**)</span></span>
  
<span data-ttu-id="7e1c0-109">���O��擾����V�[�g�ւ̎Q�ƁB</span><span class="sxs-lookup"><span data-stu-id="7e1c0-109">A reference to the sheet whose name you want.</span></span>
  
<span data-ttu-id="7e1c0-110">(**XltypeRef**) の外部参照を渡す場合のみを含める必要は、シートの ID です。</span><span class="sxs-lookup"><span data-stu-id="7e1c0-110">If you are passing an external reference (**xltypeRef**) it need only contain the ID of the sheet.</span></span> <span data-ttu-id="7e1c0-111">ワークシートのセルを表すデータ構造体は無視され、提供する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="7e1c0-111">The data structures that describe the cells on the worksheet are ignored and do not need to be provided.</span></span> <span data-ttu-id="7e1c0-112">ID は、0 に設定されている場合、 **xlSheetNm**は、現在のシートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="7e1c0-112">If the ID is set to zero, **xlSheetNm** returns the name of the current sheet.</span></span> 
  
<span data-ttu-id="7e1c0-113">(**XltypeSef**) の内部参照を渡す場合、 **xlSheetNm**は、現在のシートの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="7e1c0-113">If you are passing an internal reference (**xltypeSef**), **xlSheetNm** returns the name of the current sheet.</span></span> 
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7e1c0-114">プロパティ値/戻り値</span><span class="sxs-lookup"><span data-stu-id="7e1c0-114">Property value/Return value</span></span>

<span data-ttu-id="7e1c0-115">フォームのシート (**xltypeStr**) の名前を返します`[Book1]Sheet1`。</span><span class="sxs-lookup"><span data-stu-id="7e1c0-115">Returns the name of the sheet (**xltypeStr**) in the form  `[Book1]Sheet1`.</span></span>
  
## <a name="example"></a><span data-ttu-id="7e1c0-116">��</span><span class="sxs-lookup"><span data-stu-id="7e1c0-116">Example</span></span>

<span data-ttu-id="7e1c0-p102">���̗�́A�֐��̌Ăяo�����̃V�[�g�̖��O��\�����܂��B���̊֐��́AXLM �̃R�}���h �}�N���̎��s���Ƀ}�N�� �V�[�g����Ăяo���ꂽ�ꍇ�̂ݐ���ɓ��삵�܂��B����́A�R�}���h���������s�ł��� **xlcAlert** �̌Ăяo����s���Ă��邽�߂ł��B�܂��A **xlfCaller** ���Q�Ƃ�Ԃ��悤�ɂ���ɂ́A�_�C�A���O �{�b�N�X�A���j���[�܂��̓R�}���h �o�[����ł͂Ȃ��A�V�[�g����Ăяo����Ă���K�v�����邽�߂ł��B</span><span class="sxs-lookup"><span data-stu-id="7e1c0-p102">The following example displays the name of the sheet from which the function was called. The function works correctly only if called from a macro sheet while executing an XLM command macro. This is because it calls **xlcAlert**, which only commands can do, and it needs to be called from a sheet rather than a dialog box, menu, or command bar in order for **xlfCaller** to return a reference.</span></span> 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7e1c0-120">�֘A����</span><span class="sxs-lookup"><span data-stu-id="7e1c0-120">See also</span></span>

- [<span data-ttu-id="7e1c0-121">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="7e1c0-121">xlSheetId</span></span>](xlsheetid.md)
- [<span data-ttu-id="7e1c0-122">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="7e1c0-122">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

