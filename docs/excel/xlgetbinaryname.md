---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- xlgetbinaryname function [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798978"
---
# <a name="xlgetbinaryname"></a><span data-ttu-id="78eb0-104">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="78eb0-104">xlGetBinaryName</span></span>

<span data-ttu-id="78eb0-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="78eb0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="78eb0-106">[XlDefineBinaryName 関数](xldefinebinaryname.md)によって保存されたデータへのハンドルを返すために使用します。</span><span class="sxs-lookup"><span data-stu-id="78eb0-106">Used to return a handle for data saved by the [xlDefineBinaryName function](xldefinebinaryname.md).</span></span> <span data-ttu-id="78eb0-107">定義されているバイナリの名前を使用してデータはブックと共に保存され、名前でいつでもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="78eb0-107">Data with a defined binary name is saved with the workbook and can be accessed by name at any time.</span></span> <span data-ttu-id="78eb0-108">詳細については、 [Excel の XLL の開発での既知の問題](known-issues-in-excel-xll-development.md)で「バイナリの名前スコープの制限」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="78eb0-108">For more information, see "Binary name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a><span data-ttu-id="78eb0-109">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="78eb0-109">Parameters</span></span>

<span data-ttu-id="78eb0-110">_pxRes_(**xltypeBigData**または**xltypeErr**)</span><span class="sxs-lookup"><span data-stu-id="78eb0-110">_pxRes_ (**xltypeBigData** or **xltypeErr**)</span></span>
  
<span data-ttu-id="78eb0-p102">�擾���ꂽ�f�[�^�܂��̓G���[��w�肷�� Bigdata �\���̂́A�擾�ł��Ȃ������f�[�^�܂��͒�\`����Ă��Ȃ����O�ɂȂ�܂��B�֐����Ԃ����ƁA \*\*XLOPER\*\*\*\*\*\*/  �� **hdata** �����o�[�ɂ́A���O�t���f�[�^�̃n���h�����܂܂�܂��B  _pxRes_ ���s�v�ɂȂ�ꍇ�A **xlFree** �ւ̌Ăяo���ŉ�����Ȃ���΂Ȃ�܂���B</span><span class="sxs-lookup"><span data-stu-id="78eb0-p102">Bigdata structure specifying the retrieved data or an error is the data could not be retrieved or the name is not defined. When the function returns, the **hdata** member of the **XLOPER**/ **XLOPER12** contains a handle for the named data.  _pxRes_ should be freed in a call to **xlFree** when no longer required.</span></span> 
  
<span data-ttu-id="78eb0-114">_pxName_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="78eb0-114">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="78eb0-115">�f�[�^�̖��O��w�肷�镶����B</span><span class="sxs-lookup"><span data-stu-id="78eb0-115">A string specifying the name of the data.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78eb0-116">����</span><span class="sxs-lookup"><span data-stu-id="78eb0-116">Remarks</span></span>

<span data-ttu-id="78eb0-p103">Microsoft Excel �ɂ́A **hdata** �ŕԂ���郁���� �n���h��������܂��BWindows �ł́A�n���h���̓O���[�o�� ������ �n���h���ł� ( **GlobalAlloc** �֐��Ŋ��蓖�Ă��܂�)�B</span><span class="sxs-lookup"><span data-stu-id="78eb0-p103">Microsoft Excel owns the memory handle returned in **hdata**. In Windows, the handle is a global memory handle (allocated by the **GlobalAlloc** function).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="78eb0-119">�֘A����</span><span class="sxs-lookup"><span data-stu-id="78eb0-119">See also</span></span>

- [<span data-ttu-id="78eb0-120">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="78eb0-120">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
- [<span data-ttu-id="78eb0-121">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="78eb0-121">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

