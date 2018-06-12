---
title: C API �R�[���o�b�N�֐� Excel4�AExcel12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api callback
localization_priority: Normal
ms.assetid: 0f3ae86d-329a-4177-a65b-6288c248297e
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 221ea4c9c706d11acd31d3f2870d326a7189d299
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798757"
---
# <a name="c-api-callback-functions-excel4-excel12"></a><span data-ttu-id="4586b-104">C API �R�[���o�b�N�֐� Excel4�AExcel12</span><span class="sxs-lookup"><span data-stu-id="4586b-104">C API Callback Functions Excel4, Excel12</span></span>

<span data-ttu-id="4586b-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="4586b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="4586b-p101">DLL �� Microsoft Excel ���[�N�V�[�g�̓���֐��A�}�N�� �V�[�g�֐���R�}���h�AXLL �݂̂̓���֐���R�}���h��Ăяo����悤�ɁA **Excel4** �֐��� **Excel12** �֐����񋟂���܂��B���ׂĂ̍ŐV�o�[�W������ Excel �ł́A **Excel4** �֐���T�|�[�g���Ă��܂��BExcel 2007 �ȍ~�ł́A **Excel12** �֐����T�|�[�g����Ă��܂��B�����̊֐��� 2 �̃t�H�[���Œ񋟂���܂��B</span><span class="sxs-lookup"><span data-stu-id="4586b-p101">The **Excel4** and **Excel12** functions are provided to enable DLLs to call an internal Microsoft Excel worksheet function, macro sheet function or command, or XLL-only special function or command. All recent versions of Excel support the **Excel4** function. Starting in Excel 2007 the **Excel12** function is supported. Both functions are provided in two forms:</span></span> 
  
- <span data-ttu-id="4586b-110">可変長引数リストのフォーム (**Excel4/Excel12**)</span><span class="sxs-lookup"><span data-stu-id="4586b-110">A variable-length argument list form (**Excel4/Excel12**)</span></span>
    
- <span data-ttu-id="4586b-111">配列の引数の形式 (**Excel4v/Excel12v**)</span><span class="sxs-lookup"><span data-stu-id="4586b-111">An array-of-arguments form (**Excel4v/Excel12v**)</span></span>
    
<span data-ttu-id="4586b-112">これらのコールバックに渡される引数の方法を除いては、2 つのフォームが付きます。</span><span class="sxs-lookup"><span data-stu-id="4586b-112">Except for the way in which arguments are passed to these callbacks, the two forms are functionally equivalent.</span></span> <span data-ttu-id="4586b-113">両方のフォームの基本概念は、 [Excel4/Excel12](excel4-excel12.md)で詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="4586b-113">The basic concepts for both forms are fully described in [Excel4/Excel12](excel4-excel12.md).</span></span> <span data-ttu-id="4586b-114">[Excel4v/Excel12v](excel4v-excel12v.md)では、このフォームに関するその他の問題について説明します。</span><span class="sxs-lookup"><span data-stu-id="4586b-114">[Excel4v/Excel12v](excel4v-excel12v.md) covers other issues about this form.</span></span> 
  
## <a name="in-this-section"></a><span data-ttu-id="4586b-115">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="4586b-115">In this section</span></span>

[<span data-ttu-id="4586b-116">Excel4�AExcel12</span><span class="sxs-lookup"><span data-stu-id="4586b-116">Excel4/Excel12</span></span>](excel4-excel12.md)
  
[<span data-ttu-id="4586b-117">Excel4v/Excel12v</span><span class="sxs-lookup"><span data-stu-id="4586b-117">Excel4v/Excel12v</span></span>](excel4v-excel12v.md)
  

