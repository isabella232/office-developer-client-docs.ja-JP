---
title: マルチスレッド処理とメモリ管理
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798931"
---
# <a name="multithreading-and-memory-management"></a>マルチスレッド処理とメモリ管理

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
メモリの適切な処理は、Microsoft Excel の信頼性の高い XLL アドインの作成に不可欠です。適切なメモリ バッファーの割り当てや、不要になったバッファー メモリの解放を行わないと、パフォーマンスが低下し、リソース競合が発生し、Excel が不安定になります。
  
Microsoft Office Excel 2007 以降では、再計算時に最大 1,024 の同時実行スレッドを使用するよう Excel を構成できます。 場合によっては、特に複数のプロセッサが利用可能な場合や、クラスター化されたサーバーでユーザー定義関数を使用している場合には、マルチスレッドによってパフォーマンスが向上する可能性があります。
  
次のトピックでは、XLL でメモリやスレッドを管理する方法について説明します。
  
- [Excel のメモリ管理](memory-management-in-excel.md)
    
- [Excel におけるマルチスレッド処理とメモリ競合](multithreading-and-memory-contention-in-excel.md)
    
- [Excel でのマルチスレッド再計算](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a>関連項目



[Excel XLL の開発](developing-excel-xlls.md)

