---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- xldefinebinaryname function [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798962"
---
# <a name="xldefinebinaryname"></a><span data-ttu-id="99766-104">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="99766-104">xlDefineBinaryName</span></span>

 <span data-ttu-id="99766-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="99766-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="99766-106">**XltypeBigData** **XLOPER**の永続的なストレージを割り当てるために使用/ **XLOPER12**。</span><span class="sxs-lookup"><span data-stu-id="99766-106">Used to allocate persistent storage for an **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="99766-107">定義されているバイナリの名前を使用してデータはブックと共に保存し、名前でいつでもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="99766-107">Data with a defined binary name is saved with the workbook, and can be accessed by name at any time.</span></span> <span data-ttu-id="99766-108">詳細については、「バイナリ名前スコープの制限」 [Excel XLL 開発で既知問題](known-issues-in-excel-xll-development.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99766-108">For more information, see "Binary Name Scope Limitation" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a><span data-ttu-id="99766-109">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="99766-109">Parameters</span></span>

 <span data-ttu-id="99766-110">_pxName_(**xltypeStr**)</span><span class="sxs-lookup"><span data-stu-id="99766-110">_pxName_ (**xltypeStr**)</span></span>
  
<span data-ttu-id="99766-p102">�f�[�^�̖��O��w�肷�镶����B������́A��\`���ꂽ���O�Ɠ��������̐����ɏ]���܂��B</span><span class="sxs-lookup"><span data-stu-id="99766-p102">A string specifying the name of the data. The string is subject to the same naming restrictions as defined names.</span></span>
  
 <span data-ttu-id="99766-113">_pxData_(**xltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="99766-113">_pxData_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="99766-p103">�i�[����f�[�^��w�肷�� Bigdata �\���́B���̊֐���Ăяo���ƁA **bigdata** �\���̂� **lpbData** �����o�[�͖��O����\`����Ă���f�[�^��|�C���g����K�v������܂��B�܂��A **cbData** �����o�[�ɂ́A�f�[�^�̒��� (�o�C�g�P��) ���܂܂�Ă���K�v������܂��B</span><span class="sxs-lookup"><span data-stu-id="99766-p103">Bigdata structure specifying the data to be stored. When you call this function, the **lpbData** member of the **bigdata** structure should point to the data for which the name is being defined, and the **cbData** member should contain the length of the data in bytes.</span></span> 
  
<span data-ttu-id="99766-116">_PxData_引数が指定された (**xltypeMissing**) でない場合は、 _pxName_で指定された名前付きの割り当てが削除されます。</span><span class="sxs-lookup"><span data-stu-id="99766-116">If the  _pxData_ argument is not specified (**xltypeMissing**), the named allocation specified by  _pxName_ is deleted.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99766-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="99766-117">See also</span></span>



[<span data-ttu-id="99766-118">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="99766-118">xlGetBinaryName</span></span>](xlgetbinaryname.md)


[<span data-ttu-id="99766-119">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="99766-119">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[<span data-ttu-id="99766-120">Excel �A�h�C�� (XLL) �J���ɂ�������m�̖��</span><span class="sxs-lookup"><span data-stu-id="99766-120">Known Issues in Excel XLL Development</span></span>](known-issues-in-excel-xll-development.md)

