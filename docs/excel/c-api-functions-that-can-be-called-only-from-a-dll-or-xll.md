---
title: DLL または XLL からのみ呼び出し可能な C API 関数
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- 'functions [excel 2007], c api called from dll or xll ms.prod: office-online-server localization_priority: Normal ms.assetid: 87c9e75b-c364-4428-a169-010886313b85'
localization_priority: Normal
ms.assetid: 87c9e75b-c364-4428-a169-010886313b85
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7935d86d1c0a460bcbec85157429d99242a73620
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798774"
---
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a><span data-ttu-id="9da35-104">DLL または XLL からのみ呼び出し可能な C API 関数</span><span class="sxs-lookup"><span data-stu-id="9da35-104">C API Functions That Can Be Called Only from a DLL or XLL</span></span>

<span data-ttu-id="9da35-105">**適用対象**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9da35-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9da35-p101">C API に用意されている 15 個の Microsoft Excel コールバック関数は、**Excel4**、**Excel4v**、**Excel12**、または **Excel12v** 関数 (あるいは Framework 関数 **Excel** または **Excel12f** を間接的に使用する、これらの関数のいずれか) を使用しなければ呼び出すことができません。つまり、DLL または XLL からのみ呼び出しが可能です。</span><span class="sxs-lookup"><span data-stu-id="9da35-p101">The C API provides 15 Microsoft Excel callback functions that can only be called by using the **Excel4**, **Excel4v**, **Excel12**, or **Excel12v** functions (or by one of these functions indirectly using the Framework functions **Excel** or **Excel12f**). This means they can only be called from a DLL or XLL.</span></span>
  
## <a name="in-this-section"></a><span data-ttu-id="9da35-108">このセクションの内容</span><span class="sxs-lookup"><span data-stu-id="9da35-108">In this section</span></span>

[<span data-ttu-id="9da35-109">xlAbort</span><span class="sxs-lookup"><span data-stu-id="9da35-109">xlAbort</span></span>](xlabort.md)
  
[<span data-ttu-id="9da35-110">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="9da35-110">xlAsyncReturn</span></span>](xlasyncreturn.md)
  
[<span data-ttu-id="9da35-111">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="9da35-111">xlCoerce</span></span>](xlcoerce.md)
  
[<span data-ttu-id="9da35-112">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="9da35-112">xlDefineBinaryName</span></span>](xldefinebinaryname.md)
  
[<span data-ttu-id="9da35-113">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="9da35-113">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md)
  
[<span data-ttu-id="9da35-114">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="9da35-114">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md)
  
[<span data-ttu-id="9da35-115">xlEventRegister</span><span class="sxs-lookup"><span data-stu-id="9da35-115">xlEventRegister</span></span>](xleventregister.md)
  
[<span data-ttu-id="9da35-116">xlFree</span><span class="sxs-lookup"><span data-stu-id="9da35-116">xlFree</span></span>](xlfree.md)
  
[<span data-ttu-id="9da35-117">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="9da35-117">xlGetBinaryName</span></span>](xlgetbinaryname.md)
  
[<span data-ttu-id="9da35-118">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="9da35-118">xlGetHwnd</span></span>](xlgethwnd.md)
  
[<span data-ttu-id="9da35-119">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="9da35-119">xlGetInst</span></span>](xlgetinst.md)
  
[<span data-ttu-id="9da35-120">xlGetInstPtr</span><span class="sxs-lookup"><span data-stu-id="9da35-120">xlGetInstPtr</span></span>](xlgetinstptr.md)
  
[<span data-ttu-id="9da35-121">xlGetName</span><span class="sxs-lookup"><span data-stu-id="9da35-121">xlGetName</span></span>](xlgetname.md)
  
[<span data-ttu-id="9da35-122">xlRunningOnCluster</span><span class="sxs-lookup"><span data-stu-id="9da35-122">xlrunningoncluster</span></span>](xlrunningoncluster.md)
  
[<span data-ttu-id="9da35-123">xlSet</span><span class="sxs-lookup"><span data-stu-id="9da35-123">xlSet</span></span>](xlset.md)
  
[<span data-ttu-id="9da35-124">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="9da35-124">xlSheetId</span></span>](xlsheetid.md)
  
[<span data-ttu-id="9da35-125">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="9da35-125">xlSheetNm</span></span>](xlsheetnm.md)
  
[<span data-ttu-id="9da35-126">xlStack</span><span class="sxs-lookup"><span data-stu-id="9da35-126">xlStack</span></span>](xlstack.md)
  
[<span data-ttu-id="9da35-127">xlUDF</span><span class="sxs-lookup"><span data-stu-id="9da35-127">xlUDF</span></span>](xludf.md)
  
## <a name="see-also"></a><span data-ttu-id="9da35-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="9da35-128">See also</span></span>



[<span data-ttu-id="9da35-129">C API コールバック関数 Excel4、Excel12</span><span class="sxs-lookup"><span data-stu-id="9da35-129">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)

