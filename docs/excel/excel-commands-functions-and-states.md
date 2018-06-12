---
title: Excel �̃R�}���h�A�֐��A����я��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- states [excel 2007],commands [Excel 2007],worksheet functions [Excel 2007],macro-sheet functions [Excel 2007],Excel states
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798802"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="f4601-104">Excel �̃R�}���h�A�֐��A����я��</span><span class="sxs-lookup"><span data-stu-id="f4601-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="f4601-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f4601-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f4601-106">Microsoft Excel �́A�R�}���h�Ɗ֐��Ƃ����A2 ��ނ̕ʁX�̒ǉ��@�\����ʂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="f4601-107">�R�}���h</span><span class="sxs-lookup"><span data-stu-id="f4601-107">Commands</span></span>

<span data-ttu-id="f4601-108">Excel �̃R�}���h�ɂ͎��̂悤�ȓ���������܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="f4601-109">���[�U�[���s���̂Ɠ������@�ŃA�N�V��������s����B</span><span class="sxs-lookup"><span data-stu-id="f4601-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="f4601-110">Excel �̐ݒ��ύX����A�h�L�������g��J���A����A�ҏW����A�Čv�Z��J�n����ȂǁA���[�U�[�����s�\�Ȃ����鑀�� (�g�p����C���^�[�t�F�C�X�̐����Ɉˑ����܂�) ����s�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="f4601-111">�g���b�v���ꂽ����̃C�x���g�����������Ƃ��ɁA�Ăяo�����悤�Z�b�g�A�b�v�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="f4601-112">�_�C�A���O �{�b�N�X��\���ł��A���[�U�[�ƑΘb�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="f4601-113">���N���b�N�ȂǁA�I�u�W�F�N�g��ŃA�N�V�������s����Ƃ��ɌĂяo�����悤�ɁA�I�u�W�F�N�g�̐���Ƀ����N�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="f4601-114">�Čv�Z���� Excel ���R�}���h��Ăяo�����Ƃ͂Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="f4601-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="f4601-115">�Čv�Z���Ɋ֐����R�}���h��Ăяo�����Ƃ͂ł��Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="f4601-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="f4601-116">�֐�</span><span class="sxs-lookup"><span data-stu-id="f4601-116">Functions</span></span>

<span data-ttu-id="f4601-117">Excel �̊֐��́A���̂��Ƃ���s���܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="f4601-118">�ʏ�A������󂯎��A��Ɍ��ʂ�Ԃ��B</span><span class="sxs-lookup"><span data-stu-id="f4601-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="f4601-119">Excel �̎��̕����Ƃ��āA1 �ȏ�̃Z���ɓ��͂ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="f4601-120">定義された名前定義で使用できる。</span><span class="sxs-lookup"><span data-stu-id="f4601-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="f4601-121">����t�������̐�������т������l�̎��Ŏg�p�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="f4601-122">�R�}���h�Ŋ֐���Ăяo����B</span><span class="sxs-lookup"><span data-stu-id="f4601-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="f4601-123">�֐����R�}���h��Ăяo�����Ƃ͂ł��Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="f4601-123">They cannot call commands.</span></span>
    
<span data-ttu-id="f4601-p101">さらに Excel では、ユーザー定義ワークシート関数と、マクロ シート上で動作するよう設計されたユーザー定義関数とを区別しています。Excel では、ユーザー定義のマクロ シート関数がマクロ シートだけで使用されるように制限することはありません。これらの関数は、通常のワークシート関数を使用できる場所であればどこでも使用できます。</span><span class="sxs-lookup"><span data-stu-id="f4601-p101">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets. Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="f4601-126">���[�N�V�[�g�֐�</span><span class="sxs-lookup"><span data-stu-id="f4601-126">Worksheet Functions</span></span>

<span data-ttu-id="f4601-127">Excel ���[�N�V�[�g�֐��ɂ́A���̎��������Ă͂܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="f4601-128">�}�N�� �V�[�g���֐��ɂ̓A�N�Z�X�ł��Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="f4601-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="f4601-129">�v�Z����Ă��Ȃ��Z���̒l��擾�ł��Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="f4601-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="f4601-130">Excel 2007 �ȍ~�ł́A�X���b�h �Z�[�t�Ƃ��č쐬���A�o�^�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="f4601-131">�}�N���V�[�g�֐�</span><span class="sxs-lookup"><span data-stu-id="f4601-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="f4601-132">Excel �}�N���V�[�g�֐��ɂ́A���̎��������Ă͂܂�܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="f4601-133">�}�N�� �V�[�g���֐��ɃA�N�Z�X�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="f4601-134">�Ăяo�����̃Z���̒l��܂ލČv�Z���ꂽ�Z���̒l��擾�ł���B</span><span class="sxs-lookup"><span data-stu-id="f4601-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="f4601-135">Excel 2007 �ȍ~�ł́A�X���b�h �Z�[�t�Ƃ݂Ȃ���Ȃ��B</span><span class="sxs-lookup"><span data-stu-id="f4601-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="f4601-136">Excel でユーザー定義関数 (UDF) を処理する方法、関数には、許可、および方法を再計算関数は、関数を登録すると、すべて決定。</span><span class="sxs-lookup"><span data-stu-id="f4601-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="f4601-137">関数がワークシート関数として登録されているマクロ シート関数のみを実行できる処理を実行しようとする場合は、操作が失敗します。</span><span class="sxs-lookup"><span data-stu-id="f4601-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="f4601-138">スレッド セーフとして登録されているワークシート関数をマクロ シート関数を呼び出すしようとした場合は、Excel 2007 では、開始、もう一度、操作は失敗します。</span><span class="sxs-lookup"><span data-stu-id="f4601-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="f4601-139">Excel �́AMicrosoft Visual Basic for Applications (VBA) �� UDF ��}�N�� �V�[�g�����̊֐��Ƃ��Ĉ����܂��B������ UDF �̓��[�N�X�y�[�X���ƌv�Z����Ȃ��Z���̒l�ɃA�N�Z�X�ł��AExcel 2007 �ȍ~�A�X���b�h �Z�[�t�Ƃ͌��Ȃ���܂���B</span><span class="sxs-lookup"><span data-stu-id="f4601-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="f4601-140">Excel �̏��</span><span class="sxs-lookup"><span data-stu-id="f4601-140">Excel States</span></span>

<span data-ttu-id="f4601-141">���[�U�[�A�O���v���Z�X�A�}�N������s����g���b�v���ꂽ�C�x���g�A�܂��͎��Ԏw��� Excel �̃n�E�X�L�[�s���O �C�x���g ( **Autosave** �Ȃ�) �̃A�N�V�����ɂ���āAExcel �͂ǂ̎��_�ł�A�������Ԃ̂����̂ǂꂩ 1 �ɓ���܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="f4601-142">���[�U�[�́A���̂悤�ȏ�Ԃ�o�����܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="f4601-p103">**�����������:** ���s���̃R�}���h��}�N���͂���܂���B�\�����Ă���_�C�A���O �{�b�N�X�͂���܂���B�ҏW����Ă���Z���͂Ȃ��A���[�U�[�͐؂���A�R�s�[�A�\��t���̑���̓r���ł͂���܂���B�t�H�[�J�X���Ă��閄�ߍ��݃I�u�W�F�N�g�͂���܂���B</span><span class="sxs-lookup"><span data-stu-id="f4601-p103">**Ready state:** No commands or macros are being run. No dialog boxes are being displayed. No cells are being edited and the user is not in the middle of a cut/copy and paste operation. No embedded object has focus.</span></span> 
    
- <span data-ttu-id="f4601-147">**�ҏW���[�h:** ���[�U�[���A���b�N������ꂽ�Z���A�܂��͕ی삳��Ă��Ȃ��Z���ɁA�L���ȓ��͕�������͂��n�߂��ꍇ��A1 �ȏ�̃��b�N������ꂽ�Z���܂��͕ی삳��Ă��Ȃ��Z���� **F2** �L�[��������ꍇ�ł��B</span><span class="sxs-lookup"><span data-stu-id="f4601-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="f4601-148">**�؂���A�R�s�[�A�\��t�����[�h:** ���[�U�[���Z���܂��̓Z���͈͂�؂�������R�s�[�����肵�āA�����܂��\��t���Ă��Ȃ��ꍇ��A�����̓\��t�����삪�\�� [�\`����I����ē\��t��] �_�C�A���O �{�b�N�X��g�p���ē\��t�����ꍇ�ł��B</span><span class="sxs-lookup"><span data-stu-id="f4601-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="f4601-149">**�|�C���g ���[�h:** ���[�U�[�́A������ҏW���ŁA�ҏW���Ă��鐔���ɃA�h���X���ǉ������Z����I����Ă���Ƃ���ł��B</span><span class="sxs-lookup"><span data-stu-id="f4601-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="f4601-p104">���[�U�[�́A�ҏW�A�|�C���g�A�\��t���A�R�s�[ ���[�h�� **[ESC]** �L�[��������Ƃɂ���ĉ���ł��AExcel �͏���������Ԃɖ߂�܂��B���̃C�x���g�ł́A�����̏�Ԃ���̂悤�ɉ�����邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-p104">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state. Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="f4601-152">���[�U�[���r���g�C�� �_�C�A���O �{�b�N�X��J���B</span><span class="sxs-lookup"><span data-stu-id="f4601-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="f4601-153">���[�U�[���Čv�Z��J�n����B</span><span class="sxs-lookup"><span data-stu-id="f4601-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="f4601-154">���[�U�[���R�}���h����s����B</span><span class="sxs-lookup"><span data-stu-id="f4601-154">The user runs a command.</span></span>
    
- <span data-ttu-id="f4601-155">Excel �� **Autosave** �������s����B</span><span class="sxs-lookup"><span data-stu-id="f4601-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="f4601-156">�^�C�}�[ �C�x���g���g���b�v�����B</span><span class="sxs-lookup"><span data-stu-id="f4601-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="f4601-p105">�Ō�̗�́A�A�h�C���J���҂ɂƂ��ďd�v�ł��B�^�C�}�[ �C�x���g �g���b�v���p�ɂɐݒ肳����s����邱�Ƃ��AExcel �̒ʏ�̎g���₷���ɋy�ڂ��e�����������K�v������܂��B���̓_���A�h�C���̋@�\���ɂƂ��ďd�v�ȕ����ł���ꍇ�A���[�U�[���K�v�ɉ����Đ؂���A�R�s�[�A�\��t���̑���𐳏�ɍs����悤�ɁA�A�h�C���̎��s��ꎞ�I�ɒ��f���镪����₷�����@����[�U�[�ɒ񋟂���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="f4601-p105">The last example is of importance to add-in developers. You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed. When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f4601-160">�֘A����</span><span class="sxs-lookup"><span data-stu-id="f4601-160">See also</span></span>



[<span data-ttu-id="f4601-161">Excel �v���O���~���O�̊T�O</span><span class="sxs-lookup"><span data-stu-id="f4601-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
<span data-ttu-id="f4601-162">[���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������](permitting-user-breaks-in-lengthy-operations.md)</span><span class="sxs-lookup"><span data-stu-id="f4601-162">[Permitting User Breaks in Lengthy Operations](permitting-user-breaks-in-lengthy-operations.md)</span></span>

