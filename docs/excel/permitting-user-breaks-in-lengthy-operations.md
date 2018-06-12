---
title: "���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f����\x82���"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- xlabort function [excel 2007],concurrent tasks [Excel 2007],user breaks [Excel 2007]
localization_priority: Normal
ms.assetid: 0e3df597-0aa6-497f-bc52-58c7dc064538
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: b13f9b9a8c0e5621b25df13537632bdbe5dfc29e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798935"
---
# <a name="permitting-user-breaks-in-lengthy-operations"></a><span data-ttu-id="0bcbd-104">���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������</span><span class="sxs-lookup"><span data-stu-id="0bcbd-104">Permitting User Breaks in Lengthy Operations</span></span>

 <span data-ttu-id="0bcbd-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="0bcbd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="0bcbd-106">Windows は、場所、機能やコマンドを実行するのには時間がかかることができます、プリエンプティブなマルチタス キングを使用している場合でもは、同時実行タスクのスケジュールを設定するために利用者からのオペレーティング システムにいくつかの時間を得ることをお勧めです。</span><span class="sxs-lookup"><span data-stu-id="0bcbd-106">Even though Windows uses preemptive multitasking, where your functions or commands can take a long time to execute, it is good practice to yield some time to the operating system now and again to help it schedule concurrent tasks.</span></span> <span data-ttu-id="0bcbd-107">Windows のネイティブの呼び出しを使用すると、これを行う、sleep 関数を使用しています。</span><span class="sxs-lookup"><span data-stu-id="0bcbd-107">Using native Windows calls, you can do this by using the sleep function.</span></span> <span data-ttu-id="0bcbd-108">C API を使用して、行うことができますそれを使用して、 [xlAbort 関数](xlabort.md)だけでなく、瞬時にプロセッサを生成、また、ユーザーが [キャンセル] キー、 **esc キー**を押したかどうかを参照してくださいを確認します。</span><span class="sxs-lookup"><span data-stu-id="0bcbd-108">Using the C API, you can do it by using the [xlAbort function](xlabort.md), which not only yields the processor for an instant, but also checks to see if the user has pressed the cancel key, **ESC**.</span></span>
  
<span data-ttu-id="0bcbd-p102">���̌��ʁA **xlAbort** �֐��ɂ��A���[�U�[���v���Z�X��I�����A�K�v�ȃN���[���A�b�v����s���āAExcel �ɃR���g���[����Ԃ����ǂ�����R�[�h�Ŋm�F�ł��܂��B�܂��A���f��Ԃ������邱�Ƃ��ł��܂��B����ɂ��A���[�U�[���R�}���h��I�����邩�ǂ�����m�F����_�C�A���O �{�b�N�X��R�}���h�ŕ\���ł��܂��B�R�}���h��I�����Ȃ��ꍇ�́A����  **FALSE**  �� *xlAbort* �֐���Ăяo���āA���f�����ł��܂��B(����̈�����  *TRUE*  �ł��B����͏�Ԃ�m�F���邾���ŉ�����܂���B)</span><span class="sxs-lookup"><span data-stu-id="0bcbd-p102">The **xlAbort** function therefore enables your code to check whether the user wants to end the process, do the necessary cleanup, and then return control to Excel. The function also enables you to clear the break condition. This enables your commands to display a dialog box to verify whether the user wants to end the command. If the user does not want to end the command, calling the **xlAbort** function with the argument  *FALSE*  clears the break. (The default argument is  *TRUE*  , which simply checks the condition but does not clear it.)</span></span> 
  
<span data-ttu-id="0bcbd-p103">���[�U�[��\`�֐� (UDF) �� XLL �R�}���h���� **xlAbort** �֐���Ăяo�����Ƃ��ł��܂��BUDF �ł́A���[�U�[�ɂ�钆�f�����o����āA **xlAbort** �֐��� **TRUE** ��Ԃ��ꍇ�A�ʏ�A�֐��̌v�Z�����f����A�v�Z���������Ȃ��������Ƃ��������̒l (�G���[�� 0) ���Ԃ���܂��B���Ԃ̂�����֐��̑��̃C���X�^���X (�����悤�ɂ��̏�Ԃ�m�F����) ����f�����悤�ɁA���̒��f��Ԃ������Ȃ��ł��������BExcel �́A�Čv�Z�̏I�����ɂ��̏�Ԃ�ÖٓI�ɉ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="0bcbd-p103">You can call the **xlAbort** function from a user-defined function (UDF) or from an XLL command. In a UDF, when the **xlAbort** function returns **TRUE**, having detected a user break, you would typically cut short the function calculation and return some value to indicate that the calculation was not completed, perhaps an error or zero. You would not clear the break condition so that other instances of lengthy functions that also check this condition also break. Excel implicitly clears this condition when a recalculation ends.</span></span>
  
<span data-ttu-id="0bcbd-118">Excel �̓R�}���h�̏I�����ɂ��̏�Ԃ�ÖٓI�ɉ�����܂����A�R�}���h�Œ��f��Ԃ����o���ꂽ�ꍇ�A�ʏ�͈��� **FALSE** �ɂ�� **xlAbort** �֐���Ăяo���ď�Ԃ������܂��B</span><span class="sxs-lookup"><span data-stu-id="0bcbd-118">When you detect a break condition in a command, you typically clear the condition by calling the **xlAbort** function again with the argument **FALSE**, although Excel implicitly clears this condition when a command ends.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0bcbd-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="0bcbd-119">See also</span></span>



[<span data-ttu-id="0bcbd-120">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="0bcbd-120">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="0bcbd-121">Excel �ł̃}���\`�X���b�h�Čv�Z</span><span class="sxs-lookup"><span data-stu-id="0bcbd-121">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="0bcbd-122">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="0bcbd-122">Developing Excel XLLs</span></span>](developing-excel-xlls.md)
  
[<span data-ttu-id="0bcbd-123">Excel のインスタンスをアクセスし、メイン ウィンドウのハンドル</span><span class="sxs-lookup"><span data-stu-id="0bcbd-123">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)

