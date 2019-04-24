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
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6d2d3c824c482e3726cdaefa869393002a80f44
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301653"
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

