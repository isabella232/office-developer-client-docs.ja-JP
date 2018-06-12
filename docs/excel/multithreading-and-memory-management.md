---
title: �}���`�X���b�h�����ƃ������Ǘ�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798931"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="5abe0-103">�}���\`�X���b�h�����ƃ������Ǘ�</span><span class="sxs-lookup"><span data-stu-id="5abe0-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="5abe0-104">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="5abe0-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="5abe0-p101">�������̓K�؂ȏ����́AMicrosoft Excel �̐M�����̍��� XLL �A�h�C���̍쐬�ɕs���ł��B�K�؂ȃ����� �o�b�t�@�[�̊��蓖�Ă�A�s�v�ɂȂ����o�b�t�@�[ �������̉����s��Ȃ��ƁA�p�t�H�[�}���X���ቺ���A���\�[�X�������������AExcel ���s����ɂȂ�܂��B</span><span class="sxs-lookup"><span data-stu-id="5abe0-p101">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel. Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="5abe0-107">Microsoft Office Excel 2007 以降では、最大 1,024 の同時実行スレッドを使用して、再計算時に Excel を構成できます。</span><span class="sxs-lookup"><span data-stu-id="5abe0-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="5abe0-108">場合によっては、複数のプロセッサが利用可能な場合に特にまたはユーザー定義関数はクラスター化されたサーバーは、マルチ スレッドで実行されているパフォーマンス向上できます。</span><span class="sxs-lookup"><span data-stu-id="5abe0-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="5abe0-109">���̃g�s�b�N�ł́AXLL �Ń�������X���b�h��Ǘ�������@�ɂ��Đ�����܂��B</span><span class="sxs-lookup"><span data-stu-id="5abe0-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="5abe0-110">Excel �̃������Ǘ�</span><span class="sxs-lookup"><span data-stu-id="5abe0-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="5abe0-111">Excel 2007 �ɂ�����}���\`�X���b�h�����ƃ���������</span><span class="sxs-lookup"><span data-stu-id="5abe0-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="5abe0-112">Excel �ł̃}���\`�X���b�h�Čv�Z</span><span class="sxs-lookup"><span data-stu-id="5abe0-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="5abe0-113">�֘A����</span><span class="sxs-lookup"><span data-stu-id="5abe0-113">See also</span></span>



[<span data-ttu-id="5abe0-114">Excel XLL �̊J��</span><span class="sxs-lookup"><span data-stu-id="5abe0-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

