---
title: Excel XLL �̊J��
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- アドインが [excel 2007]、Xll の [Excel 2007] では、Xll の [Excel 2007] では、開発の開発
localization_priority: Normal
ms.assetid: dd27ae4d-ef97-47db-885c-ddd955816900
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: cb2483b9cd1b11bcfeee81bba02b6d593e8818fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798780"
---
# <a name="developing-excel-xlls"></a><span data-ttu-id="e61fd-104">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="e61fd-104">Developing Excel XLLs</span></span>

<span data-ttu-id="e61fd-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e61fd-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e61fd-106">Microsoft Excel の Xll の作成し、C API を使用する主な理由では、高性能なワークシート関数を作成します。</span><span class="sxs-lookup"><span data-stu-id="e61fd-106">The primary reason for writing Microsoft Excel XLLs and using the C API is to create high-performance worksheet functions.</span></span> <span data-ttu-id="e61fd-107">関数の高パフォーマンスのアプリケーション-Excel 2007 では、強力なサーバー リソースをマルチ スレッドのインターフェイスを記述する機能を起動し、-すれば、Excel の機能拡張の非常に重要な部分です。</span><span class="sxs-lookup"><span data-stu-id="e61fd-107">The applications of high-performance functions—and, starting in Excel 2007, the ability to write multithreaded interfaces to powerful server resources—make it a very important part of Excel extensibility.</span></span> <span data-ttu-id="e61fd-108">Xll のパフォーマンスがさらに新しいデータ型を追加して Excel 2007 で強化された、最も重要なをマルチ スレッド化します。</span><span class="sxs-lookup"><span data-stu-id="e61fd-108">The performance of XLLs was further enhanced in Excel 2007 by the addition of new data types and, most important, support for multithreading.</span></span>
  
<span data-ttu-id="e61fd-p102">C API �ɂ́AMicrosoft Visual Basic for Applications (VBA)�ACOM�A�܂��� Microsoft .NET Framework �̍��x�Őv���ȊJ���@�\�͂���܂���B�������Ǘ��͒჌�x���ōs����̂ŁA�J���҂ɂ��傫�ȐӔC�𕉂킹�邱�ƂɂȂ�܂��BCOM ��ʂ��Č��J����Ă��鑽���� Excel �@�\�́AVBA ��.NET Framework ��ʂ��ė��p�ł��܂����AC API �ɂ͌��J����Ă��܂���B</span><span class="sxs-lookup"><span data-stu-id="e61fd-p102">The C API has none of the higher-level rapid development features of Microsoft Visual Basic for Applications (VBA), COM, or the Microsoft .NET Framework. Memory management is low level, and therefore puts greater responsibility on the developer. Many Excel features that are exposed through COM, making them available through VBA and the .NET Framework, are not exposed to the C API.</span></span>


- [<span data-ttu-id="e61fd-112">Excel �v���O���~���O�̊T�O</span><span class="sxs-lookup"><span data-stu-id="e61fd-112">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
- [<span data-ttu-id="e61fd-113">DLL �̑���</span><span class="sxs-lookup"><span data-stu-id="e61fd-113">Working with DLLs</span></span>](working-with-dlls.md)
  
- <span data-ttu-id="e61fd-114">[Excel �� XLL �R�[�h�ɃA�N�Z�X����](accessing-xll-code-in-excel.md)</span><span class="sxs-lookup"><span data-stu-id="e61fd-114">[Accessing XLL Code in Excel](accessing-xll-code-in-excel.md)</span></span>
  
- <span data-ttu-id="e61fd-115">[関数ウィザードまたは [置換] ダイアログ ボックスから XLL 関数の呼び出し](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span><span class="sxs-lookup"><span data-stu-id="e61fd-115">[Call XLL Functions from the Function Wizard or Replace Dialog Boxes](how-to-call-xll-functions-from-the-function-wizard-or-replace-dialog-boxes.md)</span></span>
  
- [<span data-ttu-id="e61fd-116">DLL �܂��� XLL ���� Excel �ɌĂяo��</span><span class="sxs-lookup"><span data-stu-id="e61fd-116">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
  
- [<span data-ttu-id="e61fd-117">XLL ��쐬����</span><span class="sxs-lookup"><span data-stu-id="e61fd-117">Creating XLLs</span></span>](creating-xlls.md)
  
- <span data-ttu-id="e61fd-118">[���O�Ƒ��̃��[�N�V�[�g�̎���]������](evaluating-names-and-other-worksheet-formula-expressions.md)</span><span class="sxs-lookup"><span data-stu-id="e61fd-118">[Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md)</span></span>
  
- [<span data-ttu-id="e61fd-119">�}���\`�X���b�h�����ƃ������Ǘ�</span><span class="sxs-lookup"><span data-stu-id="e61fd-119">Multithreading and Memory Management</span></span>](multithreading-and-memory-management.md)
  
- <span data-ttu-id="e61fd-120">[�񓯊��̃��[�U�[��\`�֐�](asynchronous-user-defined-functions.md)</span><span class="sxs-lookup"><span data-stu-id="e61fd-120">[Asynchronous User-Defined Functions](asynchronous-user-defined-functions.md)</span></span>
  
- <span data-ttu-id="e61fd-121">[�N���X�^�[ �Z�[�t�֐�](cluster-safe-functions.md)</span><span class="sxs-lookup"><span data-stu-id="e61fd-121">[Cluster Safe Functions](cluster-safe-functions.md)</span></span>
  
- <span data-ttu-id="e61fd-122">[���Ԃ̂����鑀��Ń��[�U�[�ɂ�钆�f�������](permitting-user-breaks-in-lengthy-operations.md)</span><span class="sxs-lookup"><span data-stu-id="e61fd-122">[Permitting User Breaks in Lengthy Operations](permitting-user-breaks-in-lengthy-operations.md)</span></span>
  
- [<span data-ttu-id="e61fd-123">DLL �܂��� XLL �t�@�C���̒�����_�C�A���O �{�b�N�X��\������</span><span class="sxs-lookup"><span data-stu-id="e61fd-123">Displaying Dialog Boxes from Within a DLL or XLL</span></span>](displaying-dialog-boxes-from-within-a-dll-or-xll.md)
  
- [<span data-ttu-id="e61fd-124">Excel のインスタンスをアクセスし、メイン ウィンドウのハンドル</span><span class="sxs-lookup"><span data-stu-id="e61fd-124">Access Excel Instance and Main Window Handles</span></span>](how-to-access-excel-instance-and-main-window-handles.md)
  
- [<span data-ttu-id="e61fd-125">���ʌ݊���</span><span class="sxs-lookup"><span data-stu-id="e61fd-125">Backward Compatibility</span></span>](backward-compatibility.md)
  

