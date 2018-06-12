---
title: "title: \"DLL �܂��� XLL ����̂݌Ăяo���\x94\\�� C API �֐�\" ms.author: mroberts author: mroberts manager: soliver ms.date: 11/16/2014 ms.audience: Developer ms.topic: overview keywords:"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- 'functions [excel 2007], c api called from dll or xll ms.prod: office-online-server localization_priority: Normal ms.assetid: 87c9e75b-c364-4428-a169-010886313b85'
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: 'description: "�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio"'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798774"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="90e05-104">DLL �܂��� XLL ����̂݌Ăяo���\�� C API �֐�</span><span class="sxs-lookup"><span data-stu-id="90e05-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="90e05-105">**適用されます**Excel 2013 |。Office 2013 |Visual Studio</span><span class="sxs-lookup"><span data-stu-id="90e05-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="90e05-p101">C API �ɂ́A **Excel4**�A **Excel4v**�A **Excel12** �܂��� **Excel12v** �֐���g�p���� (�܂��͂̃t���[�����[�N�֐� **Excel** �܂��� **Excel12f** ��ԐړI�Ɏg�p���邱���̂����ꂩ�̊֐��ɂ����) �̂݌Ăяo�����\�� 15 �� Microsoft Excel �R�[���o�b�N�֐�������܂��B�܂�ADLL �܂��� XLL ����̂݌Ăяo�����\�ł��B</span><span class="sxs-lookup"><span data-stu-id="90e05-p101">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**). This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="90e05-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="90e05-108">In this section</span></span>

[<span data-ttu-id="90e05-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="90e05-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="90e05-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="90e05-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="90e05-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="90e05-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="90e05-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="90e05-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="90e05-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="90e05-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="90e05-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="90e05-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="90e05-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="90e05-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="90e05-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="90e05-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="90e05-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="90e05-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="90e05-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="90e05-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="90e05-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="90e05-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="90e05-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="90e05-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="90e05-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="90e05-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="90e05-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="90e05-122">xlRunningOnCluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="90e05-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="90e05-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="90e05-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="90e05-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="90e05-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="90e05-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="90e05-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="90e05-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="90e05-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="90e05-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="90e05-128">�֘A����</span><span class="sxs-lookup"><span data-stu-id="90e05-128">See also</span></span>



<span data-ttu-id="90e05-129">[C API �R�[���o�b�N�֐� Excel4�AExcel12](c-api-callback-functions-excel4-excel12.md)</span><span class="sxs-lookup"><span data-stu-id="90e05-129">[C API Callback Functions Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)</span></span>

