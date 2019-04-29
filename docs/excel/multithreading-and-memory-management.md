---
title: �}���`�X���b�h�����ƃ������Ǘ�
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414467"
---
# <a name="multithreading-and-memory-management"></a>マルチスレッド処理とメモリ管理

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
メモリの適切な処理は、Microsoft Excel の信頼性の高い XLL アドインの作成に不可欠です。適切なメモリ バッファーの割り当てや、不要になったバッファー メモリの解放を行わないと、パフォーマンスが低下し、リソース競合が発生し、Excel が不安定になります。
  
Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating. In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.
  
次のトピックでは、XLL でメモリやスレッドを管理する方法について説明します。
  
- [Excel のメモリ管理](memory-management-in-excel.md)
    
- [Excel におけるマルチスレッド処理とメモリ競合](multithreading-and-memory-contention-in-excel.md)
    
- [Excel でのマルチスレッド再計算](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>関連項目



[Excel XLL の開発](developing-excel-xlls.md)

