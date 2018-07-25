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
# <a name="c-api-functions-that-can-be-called-only-from-a-dll-or-xll"></a>DLL または XLL からのみ呼び出し可能な C API 関数

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
C API に用意されている 15 個の Microsoft Excel コールバック関数は、**Excel4**、**Excel4v**、**Excel12**、または **Excel12v** 関数 (あるいは Framework 関数 **Excel** または **Excel12f** を間接的に使用する、これらの関数のいずれか) を使用しなければ呼び出すことができません。つまり、DLL または XLL からのみ呼び出しが可能です。
  
## <a name="in-this-section"></a>このセクションの内容

[xlAbort](xlabort.md)
  
[xlAsyncReturn](xlasyncreturn.md)
  
[xlCoerce](xlcoerce.md)
  
[xlDefineBinaryName](xldefinebinaryname.md)
  
[xlDisableXLMsgs](xldisablexlmsgs.md)
  
[xlEnableXLMsgs](xlenablexlmsgs.md)
  
[xlEventRegister](xleventregister.md)
  
[xlFree](xlfree.md)
  
[xlGetBinaryName](xlgetbinaryname.md)
  
[xlGetHwnd](xlgethwnd.md)
  
[xlGetInst](xlgetinst.md)
  
[xlGetInstPtr](xlgetinstptr.md)
  
[xlGetName](xlgetname.md)
  
[xlRunningOnCluster](xlrunningoncluster.md)
  
[xlSet](xlset.md)
  
[xlSheetId](xlsheetid.md)
  
[xlSheetNm](xlsheetnm.md)
  
[xlStack](xlstack.md)
  
[xlUDF](xludf.md)
  
## <a name="see-also"></a>関連項目



[C API コールバック関数 Excel4、Excel12](c-api-callback-functions-excel4-excel12.md)

