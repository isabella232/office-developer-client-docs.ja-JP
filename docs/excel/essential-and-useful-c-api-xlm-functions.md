---
title: �d�v�Ŗ�ɗ��� C API XLM �֐�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- functions [excel 2007], c api xlm
localization_priority: Normal
ms.assetid: dc80cb3d-0d7e-4cb9-9870-3acc84eeca82
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 410a6009bf6bbb8146dcc1354e7f5688c28d96c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798793"
---
# <a name="essential-and-useful-c-api-xlm-functions"></a><span data-ttu-id="8e6d7-104">�d�v�Ŗ�ɗ��� C API XLM �֐�</span><span class="sxs-lookup"><span data-stu-id="8e6d7-104">Essential and Useful C API XLM Functions</span></span>

 <span data-ttu-id="8e6d7-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8e6d7-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8e6d7-p101">���̃Z�N�V�����Ő������֐��́ADLL �� XLL �J���҂ɓ��ɕ֗��� Microsoft Excel �̃R�[���o�b�N�֐��ł��B�����̊֐��̒��ŁA **xlfRegister** �֐��́AExcel ���璼�ڌĂяo�����߂Ɋ֐��ƃR�}���h��o�^���� XLL �� DLL �ɕs���ł��B�֐� **xlfUnregister** �� **xlfSetName** �́ADLL �� XLL �̊֐�����уR�}���h��o�^������邽�߂ɁA�g�ݍ��킹�Ďg�p����܂��B</span><span class="sxs-lookup"><span data-stu-id="8e6d7-p101">The functions described in this section are Microsoft Excel callback functions that are particularly useful to DLL and XLL developers. Of these, the **xlfRegister** function is essential for XLLs and DLLs that want to register their functions and commands so that they can be called directly from Excel. The functions **xlfUnregister** and **xlfSetName** are used in combination to unregister DLL and XLL functions and commands.</span></span> 
  
<span data-ttu-id="8e6d7-p102">�����̊֐��́AXLL �̊J�����̖𗧂� C API ��ʂ��āAExcel �ɂ���Č��J����܂��B������ Excel ���[�N�V�[�g�ɑΉ�����֐��ƁAXLM �}�N�� �V�[�g�Ŏg�p�ł���֐�����уR�}���h�ł��B</span><span class="sxs-lookup"><span data-stu-id="8e6d7-p102">Many more functions are exposed by Excel via the C API that are useful when you are developing XLLs. They correspond to the Excel worksheet functions and functions and commands that are available from XLM macro sheets.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="8e6d7-111">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="8e6d7-111">In this section</span></span>

[<span data-ttu-id="8e6d7-112">xlfCaller</span><span class="sxs-lookup"><span data-stu-id="8e6d7-112">xlfCaller</span></span>](xlfcaller.md)
  
[<span data-ttu-id="8e6d7-113">xlfEvaluate</span><span class="sxs-lookup"><span data-stu-id="8e6d7-113">xlfEvaluate</span></span>](xlfevaluate.md)
  
[<span data-ttu-id="8e6d7-114">xlfGetDef</span><span class="sxs-lookup"><span data-stu-id="8e6d7-114">xlfGetDef</span></span>](xlfgetdef.md)
  
[<span data-ttu-id="8e6d7-115">xlfGetName</span><span class="sxs-lookup"><span data-stu-id="8e6d7-115">xlfGetName</span></span>](xlfgetname.md)
  
[<span data-ttu-id="8e6d7-116">xlfRegister (�\`�� 1)</span><span class="sxs-lookup"><span data-stu-id="8e6d7-116">xlfRegister (Form 1)</span></span>](xlfregister-form-1.md)
  
[<span data-ttu-id="8e6d7-117">xlfRegister (�\`�� 2)</span><span class="sxs-lookup"><span data-stu-id="8e6d7-117">xlfRegister (Form 2)</span></span>](xlfregister-form-2.md)
  
[<span data-ttu-id="8e6d7-118">xlfRegisterId</span><span class="sxs-lookup"><span data-stu-id="8e6d7-118">xlfRegisterId</span></span>](xlfregisterid.md)
  
[<span data-ttu-id="8e6d7-119">xlfUnregister (�\`�� 1)</span><span class="sxs-lookup"><span data-stu-id="8e6d7-119">xlfUnregister (Form 1)</span></span>](xlfunregister-form-1.md)
  
[<span data-ttu-id="8e6d7-120">xlfUnregister (�\`�� 2)</span><span class="sxs-lookup"><span data-stu-id="8e6d7-120">xlfUnregister (Form 2)</span></span>](xlfunregister-form-2.md)
  
[<span data-ttu-id="8e6d7-121">xlfSetName</span><span class="sxs-lookup"><span data-stu-id="8e6d7-121">xlfSetName</span></span>](xlfsetname.md)
  

