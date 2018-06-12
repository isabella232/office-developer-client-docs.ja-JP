---
title: �ėp DLL �̊֐�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- generic dll [excel 2007], functions,functions [Excel 2007], Generic DLL
localization_priority: Normal
ms.assetid: 80ce2247-d69d-45b0-b5e2-4ff0d7078a2c
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e78f276e58ca1c98786e28ed5167762cf0bfdf7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798898"
---
# <a name="functions-in-the-generic-dll"></a><span data-ttu-id="dbfdb-104">�ėp DLL �̊֐�</span><span class="sxs-lookup"><span data-stu-id="dbfdb-104">Functions in the Generic DLL</span></span>

 <span data-ttu-id="dbfdb-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="dbfdb-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="dbfdb-p101">�t�H���_�[  `\EXAMPLES\GENERIC\` �ɂ́A�T���v���� DLL GENERIC.xll ��R���p�C�����邽�߂ɕK�v�� Microsoft Visual Studio �̃v���W�F�N�g �t�@�C���ƃ\�[�X �R�[�h �t�@�C�����܂܂�Ă��܂��B���̃v���W�F�N�g��e���v���[�g�Ƃ��Ďg�p���ēƎ��� Microsoft Excel XLL ��쐬�ł��܂��B���̃v���W�F�N�g�̃\�[�X �R�[�h�ɂ́AExcel C API �̑����̋@�\��������Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="dbfdb-p101">The folder  `\EXAMPLES\GENERIC\` contains Microsoft Visual Studio project files and source code files that are needed to compile the example DLL GENERIC.xll. You can use this project as a template for writing your own Microsoft Excel XLLs. The source code in this project demonstrates many of the features of the Excel C API.</span></span> 
  
<span data-ttu-id="dbfdb-109">GENERIC.xll ��ǂݍ��ނƁA���� 4 �̃R�}���h������ **[Generic]** ���j���[���쐬����܂��B</span><span class="sxs-lookup"><span data-stu-id="dbfdb-109">When you load GENERIC.xll, it creates a new **Generic** menu with four commands:</span></span> 
  
- <span data-ttu-id="dbfdb-110">**Dialog** - [Microsoft Excel] �_�C�A���O �{�b�N�X��\�����܂��B</span><span class="sxs-lookup"><span data-stu-id="dbfdb-110">**Dialog** - Displays a Microsoft Excel dialog box.</span></span> 
    
- <span data-ttu-id="dbfdb-111">**ダンス**- は、 **ESC**キーを押すまで選択範囲を移動します。</span><span class="sxs-lookup"><span data-stu-id="dbfdb-111">**Dance** - Moves the selection around until you press the **ESC** key.</span></span> 
    
- <span data-ttu-id="dbfdb-112">**Native Dialog** - [Windows] �_�C�A���O �{�b�N�X��\�����܂��B</span><span class="sxs-lookup"><span data-stu-id="dbfdb-112">**Native Dialog** - Displays a Windows dialog box.</span></span> 
    
- <span data-ttu-id="dbfdb-113">**Exit** - GENERIC.xll ��A�����[�h���A **[Generic]** ���j���[��폜���܂��B</span><span class="sxs-lookup"><span data-stu-id="dbfdb-113">**Exit** - Unloads GENERIC.xll and removes the **Generic** menu.</span></span> 
    
<span data-ttu-id="dbfdb-p102">GENERIC.xll �͂܂��A���[�N�V�[�g�֐� Func1�AFuncSum�A����� FuncFib ��񋟂��܂��B�����͂��ł� GENERIC.xll ���ǂݍ��܂�Ă���Ƃ��Ɏg�p�ł��܂��BGENERIC.xll �́A�A�h�C�� �}�l�[�W���[��g�p���ēǂݍ��ނ��Ƃ��ł��܂��B�Ō�� Excel �Z�b�V����������ɏI���������_�ŃA�N�e�B�u�ɂȂ��Ă����ꍇ�́A���̎��̃Z�b�V�����ł�ǂݍ��܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="dbfdb-p102">GENERIC.xll also provides three worksheet functions, Func1, FuncSum, and FuncFib, which can be used whenever GENERIC.xll is loaded. GENERIC.xll can be loaded using the Add-in Manager, or it is loaded if it was active at the normal end of the last Excel session.</span></span>
  
<span data-ttu-id="dbfdb-116">���̃v���W�F�N�g�ł́A�t���[�����[�N ���C�u���� (FRMWRK32.lib) ��g�p���܂��B</span><span class="sxs-lookup"><span data-stu-id="dbfdb-116">This project uses the framework library (FRMWRK32.lib).</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="dbfdb-117">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="dbfdb-117">In this section</span></span>

[<span data-ttu-id="dbfdb-118">DIALOGMsgProc</span><span class="sxs-lookup"><span data-stu-id="dbfdb-118">DIALOGMsgProc</span></span>](dialogmsgproc.md)
  
[<span data-ttu-id="dbfdb-119">ExcelCursorProc</span><span class="sxs-lookup"><span data-stu-id="dbfdb-119">ExcelCursorProc</span></span>](excelcursorproc.md)
  
[<span data-ttu-id="dbfdb-120">HookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="dbfdb-120">HookExcelWindow</span></span>](hookexcelwindow.md)
  
[<span data-ttu-id="dbfdb-121">UnhookExcelWindow</span><span class="sxs-lookup"><span data-stu-id="dbfdb-121">UnhookExcelWindow</span></span>](unhookexcelwindow.md)
  
[<span data-ttu-id="dbfdb-122">fShowDialog</span><span class="sxs-lookup"><span data-stu-id="dbfdb-122">fShowDialog</span></span>](fshowdialog.md)
  
[<span data-ttu-id="dbfdb-123">fDance</span><span class="sxs-lookup"><span data-stu-id="dbfdb-123">fDance</span></span>](fdance.md)
  
[<span data-ttu-id="dbfdb-124">fDialog/fDialog12</span><span class="sxs-lookup"><span data-stu-id="dbfdb-124">fDialog/fDialog12</span></span>](fdialog-fdialog12.md)
  
[<span data-ttu-id="dbfdb-125">fExit</span><span class="sxs-lookup"><span data-stu-id="dbfdb-125">fExit</span></span>](fexit.md)
  
[<span data-ttu-id="dbfdb-126">Func1</span><span class="sxs-lookup"><span data-stu-id="dbfdb-126">Func1</span></span>](func1.md)
  
[<span data-ttu-id="dbfdb-127">FuncSum</span><span class="sxs-lookup"><span data-stu-id="dbfdb-127">FuncSum</span></span>](funcsum.md)
  
[<span data-ttu-id="dbfdb-128">FuncFib</span><span class="sxs-lookup"><span data-stu-id="dbfdb-128">FuncFib</span></span>](funcfib.md)
  
## <a name="see-also"></a><span data-ttu-id="dbfdb-129">�֘A����</span><span class="sxs-lookup"><span data-stu-id="dbfdb-129">See also</span></span>



<span data-ttu-id="dbfdb-130">[�t���[�����[�N ���C�u�����̊֐�](functions-in-the-framework-library.md)</span><span class="sxs-lookup"><span data-stu-id="dbfdb-130">[Functions in the Framework Library](functions-in-the-framework-library.md)</span></span>

