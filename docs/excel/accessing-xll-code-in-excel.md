---
title: Excel では XLL コードへのアクセス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- accessing xll code [excel 2007],XLLs [Excel 2007], accessing code,commands [Excel 2007], registration,functions [Excel 2007], registration,calling XLLs from Excel,registering commands [Excel 2007],registering functions [Excel 2007]
localization_priority: Normal
ms.assetid: 6e4bf1f3-8eca-4be5-9632-75355ac31d61
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 1523f9e8213cb955f1bfd995c42f921b001299fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798768"
---
# <a name="accessing-xll-code-in-excel"></a><span data-ttu-id="019c1-104">Excel では XLL コードへのアクセス</span><span class="sxs-lookup"><span data-stu-id="019c1-104">Accessing XLL code in Excel</span></span>

<span data-ttu-id="019c1-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="019c1-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="019c1-106">XLL �Ɋ܂܂��֐���R�}���h�� Microsoft Excel �ŃA�N�Z�X�ł���悤�ɂ���ɂ́A���̎������K�v�ƂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-106">To be accessible in Microsoft Excel, the functions and commands that an XLL contains:</span></span>
  
- <span data-ttu-id="019c1-107">XLL �ɂ���ăG�N�X�|�[�g����Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="019c1-107">Must be exported by the XLL.</span></span>
    
- <span data-ttu-id="019c1-108">Excel �ɓo�^����K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-108">Must be registered with Excel.</span></span>
    
## <a name="registering-functions-and-commands-with-excel"></a><span data-ttu-id="019c1-109">Excel の関数とコマンドを登録します。</span><span class="sxs-lookup"><span data-stu-id="019c1-109">Registering functions and commands with Excel</span></span>

<span data-ttu-id="019c1-110">�o�^���邱�Ƃɂ���āADLL �G���g�� �|�C���g�ɂ��Ď��̂��Ƃ� Excel �Ɏw�����܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-110">Registration tells Excel the following about a DLL entry point:</span></span>
  
- <span data-ttu-id="019c1-111">��\�����ǂ����B�܂��֐��̏ꍇ�ɂ́A�֐��E�B�U�[�h�ɕ\�����邩�ǂ����B</span><span class="sxs-lookup"><span data-stu-id="019c1-111">Whether it is hidden or, if a function, whether it is visible in the Function Wizard.</span></span>
    
- <span data-ttu-id="019c1-112">XLM �}�N���V�[�g����̂݌Ăяo���邩�A���邢�̓��[�N�V�[�g�����Ăяo���邩�B</span><span class="sxs-lookup"><span data-stu-id="019c1-112">Whether it is callable only from an XLM macro sheet, or also from a worksheet.</span></span>
    
- <span data-ttu-id="019c1-113">�R�}���h�̏ꍇ�A���[�N�V�[�g�֐����A�܂��̓}�N���V�[�g�����֐����ǂ����B</span><span class="sxs-lookup"><span data-stu-id="019c1-113">If a command, whether it is a worksheet function or a macro sheet equivalent function.</span></span>
    
- <span data-ttu-id="019c1-114">XLL/DLL �G�N�X�|�[�g���A����� Excel �Ŏg�p���閼�O�B</span><span class="sxs-lookup"><span data-stu-id="019c1-114">What its XLL/DLL export name is, and what name you want Excel to use.</span></span>
    
- <span data-ttu-id="019c1-115">�֐��̏ꍇ:</span><span class="sxs-lookup"><span data-stu-id="019c1-115">If it is a function:</span></span>
    
  - <span data-ttu-id="019c1-116">�Ԃ��f�[�^�^�A����ш����Ƃ��Ď��f�[�^�^�B</span><span class="sxs-lookup"><span data-stu-id="019c1-116">What data types it returns and takes as arguments.</span></span>
    
  - <span data-ttu-id="019c1-117">������C���v���[�X�ŕύX���Č��ʂ�Ԃ����ǂ����B</span><span class="sxs-lookup"><span data-stu-id="019c1-117">Whether it returns its result by modifying an argument in place.</span></span>
    
  - <span data-ttu-id="019c1-118">���������ǂ����B</span><span class="sxs-lookup"><span data-stu-id="019c1-118">Whether it is volatile.</span></span>
    
  - <span data-ttu-id="019c1-119">�X���b�h �Z�[�t�ł��邩�ǂ��� (Excel 2007 �ȍ~�ŃT�|�[�g����Ă��܂�)�B</span><span class="sxs-lookup"><span data-stu-id="019c1-119">Whether it is thread safe (supported starting in Excel 2007).</span></span>
    
  - <span data-ttu-id="019c1-120">�֐��\��t���E�B�U�[�h�ƃI�[�g�R���v���[�g �G�f�B�^�[�ɁA�֐��̌Ăяo����x�����邽�߂ɕ\������e�L�X�g�B</span><span class="sxs-lookup"><span data-stu-id="019c1-120">What text the Paste Function Wizard and AutoComplete editor should display to help with calling the function.</span></span>
    
  - <span data-ttu-id="019c1-121">���X�g�\���Ɏg�p����֐��J�e�S���B</span><span class="sxs-lookup"><span data-stu-id="019c1-121">Which function category it should be listed under.</span></span>
    
<span data-ttu-id="019c1-122">�O�q�̓_�́A���ׂ� C API �֐��� [xlfRegister](xlfregister-form-1.md) ��g�p���čs���܂��B���̊֐��� XLM �֐��� **REGISTER** �ɑ������܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-122">This is all achieved using the C API function [xlfRegister](xlfregister-form-1.md), equivalent to the XLM function **REGISTER**.</span></span>
  
## <a name="calling-xll-functions-directly-from-excel"></a><span data-ttu-id="019c1-123">Excel から直接 XLL 関数の呼び出し</span><span class="sxs-lookup"><span data-stu-id="019c1-123">Calling XLL functions directly from Excel</span></span>

<span data-ttu-id="019c1-124">XLL ���[�N�V�[�g�֐��ƃ}�N���V�[�g�֐���o�^����ƁA�g�ݍ��݊֐���Ăяo�����Ƃ��\�Ȏ��Ɏ������ׂĂ̏ꏊ���炻����Ăяo���܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-124">Once they are registered, XLL worksheet and macro sheet functions can be called from anywhere a built-in function can be called from:</span></span>
  
- <span data-ttu-id="019c1-125">���[�N�V�[�g�̒P��Z���܂��͔z�񐔎��B</span><span class="sxs-lookup"><span data-stu-id="019c1-125">A single-cell or array formula on a worksheet.</span></span>
    
- <span data-ttu-id="019c1-126">�}�N���V�[�g�̒P��Z���܂��͔z�񐔎��B</span><span class="sxs-lookup"><span data-stu-id="019c1-126">A single-cell or array formula on a macro sheet.</span></span>
    
- <span data-ttu-id="019c1-127">定義された名前の定義。</span><span class="sxs-lookup"><span data-stu-id="019c1-127">The definition of a defined name.</span></span>
    
- <span data-ttu-id="019c1-128">����t�������̃_�C�A���O �{�b�N�X�́A����Ɛ����̃t�B�[���h�B</span><span class="sxs-lookup"><span data-stu-id="019c1-128">The condition and limit fields in a conditional format dialog box.</span></span>
    
- <span data-ttu-id="019c1-129">C API �֐� [xlUDF](xludf.md) ���đ��̃A�h�C������B</span><span class="sxs-lookup"><span data-stu-id="019c1-129">From another add-in via the C API function [xlUDF](xludf.md).</span></span>
    
- <span data-ttu-id="019c1-130">**Application.Run** ���\�b�h���� Visual Basic for Applications (VBA) ����B</span><span class="sxs-lookup"><span data-stu-id="019c1-130">From Visual Basic for Applications (VBA) via the **Application.Run** method.</span></span> 
    
<span data-ttu-id="019c1-p101">C API �֐� **xlfCaller** ��g�p����ƁA�֐���̌Ăяo�����Z���ւ̎Q�Ƃ܂��̓Z���͈̔͂�擾�ł��܂��B�֐����Z���̏���t������������Ăяo���ꂽ�ꍇ�A�֘A���� 1 �܂��͕����̃Z���ւ̎Q�Ƃ�Ԃ��Ă���Ƃ��ɂ́A�Z���̐����� XLL �֐����܂܂�Ă���Ƃ͌���܂���B�֐��� VBA ���[�U�[��\`�֐� (UDF) ����Ăяo���ꂽ�ꍇ�A **xlfCaller** �� VBA �֐���Ăяo�����Z���̃A�h���X��ĂѕԂ��܂��B�ڂ����́A�u [xlfCaller](xlfcaller.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="019c1-p101">You can obtain a reference to the calling cell or range of cells within your function using the C API function **xlfCaller**. If the function was called from the cell's conditional format expression, you are still returned a reference to the associated cell or cells, so you cannot assume that the cell's formula contains the XLL function. If your function was called from a VBA user-defined function (UDF), **xlfCaller** again returns the address of the cells that called the VBA function. For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="019c1-135">Excel は、XLL 関数のコードを**貼り付け関数ウィザード**と**置換**] ダイアログ ボックスから呼び出しも行います。</span><span class="sxs-lookup"><span data-stu-id="019c1-135">Excel also calls XLL function code from the **Paste Function Wizard** and **Replace** dialog boxes.</span></span> <span data-ttu-id="019c1-136">場合は、関数が、実行に長い時間にかかることが特に、**貼り付けの関数の引数**] ダイアログ ボックスのコードの通常の実行を制限する必要があります。</span><span class="sxs-lookup"><span data-stu-id="019c1-136">You might need to restrict your code's normal running in the case of the **Paste Function Arguments** dialog box, especially where your function can take a long time to execute.</span></span> <span data-ttu-id="019c1-137">前面のウィンドウは、これらのダイアログ ボックスのいずれかと、その場合は、すべての開いているウィンドウを反復処理するプロジェクトのいくつかのコードを実装する必要がある場合が呼び出される関数がこれらのダイアログ ボックスのいずれかを検出するためにどちらかです。</span><span class="sxs-lookup"><span data-stu-id="019c1-137">To detect if your function is being called from either of these dialog boxes, you must implement some code in your project that iterates through all the open windows to determine if the front window is one of these dialog boxes, and, if so, which one.</span></span> 
  
## <a name="calling-xll-commands-directly-from-excel"></a><span data-ttu-id="019c1-138">XLL コマンドを Excel から直接呼び出すこと</span><span class="sxs-lookup"><span data-stu-id="019c1-138">Calling XLL commands directly from Excel</span></span>

<span data-ttu-id="019c1-139">XLL �R�}���h��o�^����ƁA���̃��[�U�[��\`�}�N����Ăяo�����Ƃ��ł��鎟�Ɏ�����������@�� XLL �R�}���h��Ăяo�����Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-139">Once they are registered, XLL commands can be called in all the ways that other user-defined macros can be called:</span></span>
  
- <span data-ttu-id="019c1-140">���[�N�V�[�g�ɖ��ߍ��܂�Ă���R���g���[�� �I�u�W�F�N�g�Ɋ֘A�t���邱�Ƃɂ���āB</span><span class="sxs-lookup"><span data-stu-id="019c1-140">By being associated with a control object embedded on a worksheet.</span></span>
    
- <span data-ttu-id="019c1-141">[�}�N���̎��s] �_�C�A���O �{�b�N�X����B</span><span class="sxs-lookup"><span data-stu-id="019c1-141">From the Run Macro dialog box.</span></span>
    
- <span data-ttu-id="019c1-142">**Application.Run** ���\�b�h��g�p���� VBA ���[�U�[��\`�}�N������B</span><span class="sxs-lookup"><span data-stu-id="019c1-142">From a VBA user-defined macro using the **Application.Run** method.</span></span> 
    
- <span data-ttu-id="019c1-143">�J�X�^�}�C�Y���ꂽ���j���[���ڂ܂��̓c�[���o�[����B</span><span class="sxs-lookup"><span data-stu-id="019c1-143">From a customized menu item or toolbar.</span></span>
    
- <span data-ttu-id="019c1-144">�R�}���h��o�^����Ƃ��ɃZ�b�g�A�b�v�����V���[�g�J�b�g �L�[�{�[�h�����g�p���āB</span><span class="sxs-lookup"><span data-stu-id="019c1-144">Using a shortcut keystroke set up when registering the command.</span></span>
    
- <span data-ttu-id="019c1-145">�w�肵���C�x���g���g���b�v�����Ƃ��Ɏ��s����R�}���h�Ƃ��āB</span><span class="sxs-lookup"><span data-stu-id="019c1-145">As the command to be run when a specified event is trapped.</span></span>
    
> [!NOTE]
> <span data-ttu-id="019c1-p103">XLL コマンドは非表示で、Excel のダイアログ ボックスで使用できるマクロの一覧に表示されません。ただし、[マクロ名] フィールドに手動で入力できます。Excel では、それらのダイアログ ボックスで、DLL エクスポート名ではなく登録されたとおりの名前であることが必要となります。</span><span class="sxs-lookup"><span data-stu-id="019c1-p103">XLL commands are hidden in that they do not appear on the list of available macros in Excel dialog boxes. But they can be entered manually into the macro name field. Excel expects the registered-as name in these dialog boxes, not the DLL export name.</span></span> 
  
<span data-ttu-id="019c1-149">Excel �ɓo�^����Ă��邷�ׂĂ� XLL �R�}���h�́A���̌\`���ł��邱�Ƃ� Excel �őz�肳��Ă��܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-149">All XLL commands registered with Excel are assumed by Excel to be of the following form:</span></span>
  
```cs
short WINAPI xll_cmd_name(void)
{
// Function code...
    return 1;
}

```

<span data-ttu-id="019c1-p104">Excel �ł́AXLM �}�N���V�[�g����Ăяo���ꂽ�ꍇ������߂�l����������܂��B�}�N���V�[�g����Ăяo���ꂽ�ꍇ�ɂ́A�߂�l�� **TRUE** �܂��� **FALSE** �ɕϊ�����܂��B���̂��߁A�R�}���h������Ɏ��s���ꂽ�ꍇ�ɂ� 1 ��A���s�������A���[�U�[�ɂ���ăL�����Z�����ꂽ�ꍇ�ɂ� 0 ��Ԃ��悤�ɂ��܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-p104">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span>
  
<span data-ttu-id="019c1-p105">C API �֐��� **xlfCaller** ��g�p����ƁA�R�}���h���Ăяo���ꂽ���@�ɂ��Ă̏���擾�ł��܂��B�ڂ����́A�u [xlfCaller](xlfcaller.md)�v��������������B</span><span class="sxs-lookup"><span data-stu-id="019c1-p105">You can obtain information about how your command was invoked using the C API function **xlfCaller**. For more information, see [xlfCaller](xlfcaller.md).</span></span>
  
<span data-ttu-id="019c1-p106">Excel 2007 �ȍ~�̃��[�U�[ �C���^�[�t�F�C�X�͈ȑO�̃o�[�W�����̂�̂Ƃ͑傫���قȂ�܂��B�قƂ�ǂ̏ꍇ�A�J�X�^�� ���j���[ �o�[�A���j���[�A�T�u���j���[�A���j���[���ځA���[�U�[�ݒ�c�[���o�[�A�c�[���o�[ �{�^���̒ǉ��ƍ폜��s���� C API �֐������������T�|�[�g����Ă��܂��B�������A�K������A���[�U�[������܂łɊ���Ă�����@�Œǉ����ڂ��g�p�\�ɂȂ�킯�ł͂���܂���B�ǉ��@�\�������������p�ł��邩�ǂ����𒍈ӂ��Ċm�F���A���p�ł��Ȃ��ꍇ�ɂ̓o�[�W�����ŗL�̃J�X�^�}�C�Y��������Ă��������BExcel 2007 �ȍ~�A���[�U�[ �C���^�[�t�F�C�X�̓}�l�[�W �R�[�h ���W���[����g�p���čœK�̕��@�ŃJ�X�^�}�C�Y����Ă��āAXLL �R�}���h�Ɩ��ɘA�������邱�Ƃ��ł��܂��B</span><span class="sxs-lookup"><span data-stu-id="019c1-p106">Starting in Excel 2007 user interface is very different from earlier versions. The C API functions that permit the addition and deletion of custom menu bars, menus, submenus, menu items, custom toolbars and toolbar buttons are still supported in most cases. However, they may not always make the added item available in a way that your users are familiar with. You should carefully check that any added functionality is still accessible, or implement a version-specific customization. Starting in Excel 2007 the user interface is best customized by using a managed code module that can then be tightly coupled to your XLL commands.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="019c1-159">�֘A����</span><span class="sxs-lookup"><span data-stu-id="019c1-159">See also</span></span>

- [<span data-ttu-id="019c1-160">XLL ��쐬����</span><span class="sxs-lookup"><span data-stu-id="019c1-160">Creating XLLs</span></span>](creating-xlls.md)
- <span data-ttu-id="019c1-161">[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span><span class="sxs-lookup"><span data-stu-id="019c1-161">[Call XLL Functions from the Function Wizard or Replace Dialog Boxes](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span></span>
- <span data-ttu-id="019c1-162">[�A�h�C�� �}�l�[�W���[�� XLL �C���^�[�t�F�C�X�֐�](add-in-manager-and-xll-interface-functions.md)</span><span class="sxs-lookup"><span data-stu-id="019c1-162">[Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)</span></span>
- [<span data-ttu-id="019c1-163">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="019c1-163">Developing Excel XLLs</span></span>](developing-excel-xlls.md)



