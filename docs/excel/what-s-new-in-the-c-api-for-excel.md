---
title: Excel 用 C API の新機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c api [excel 2007],新機能
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 64e3933ec25f0771db5bd36bbf57f3f259cdc8a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439689"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Excel 用 C API の新機能

 **適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 と同時に、Microsoft Excel 2013 XLL ソフトウェア開発キット (SDK) にも次の機能のサポートが含まれています。
  
- **新機能**
    
    Microsoft Excel 2013 XLL SDK は、Excel 2013 のすべての新しいワークシート関数へのコール バックをサポートしています。 Excel 2013 関数の呼び出しの詳細については、「[DLL または XLL から Excel に呼び出す](calling-into-excel-from-the-dll-or-xll.md)」を参照してください。
    
- **非同期のユーザー定義関数**
    
    Excel 2013 ではユーザー定義関数 (UDF) の非同期の呼び出しをサポートしています。これは、さまざまな計算の同時実行を可能にすることで、パフォーマンスを向上します。 非同期 UDF の詳細については、「[非同期のユーザー定義関数](asynchronous-user-defined-functions.md)」を参照してください。
    
- **クラスター コネクタ**
    
    クラスター コネクタは、UDF を高パフォーマンスの計算クラスター上で実行できるようにします。 クラスター コネクタの作成の詳細については、「[Excel クラスター コネクタの開発](developing-excel-cluster-connectors.md)」を参照してください。
    
    > [!NOTE]
    > 計算クラスター上で実行する予定の XLL アドインは、クラスター セーフ関数のみを呼び出す必要があります。 使用可能な関数の詳細については、「[Excel XLL SDK API 関数リファレンス](excel-xll-sdk-api-function-reference.md)」および「[クラスター セーフ関数](cluster-safe-functions.md)」を参照してください。 
  
- **64 ビットのサポート**
    
    32 ビットと 64 ビットの XLL をコンパイルおよびリンクできるようになりました。詳細については、「[XLL を作成する](creating-xlls.md)」を参照してください。
    
## <a name="see-also"></a>関連項目



[Excel XLL の開発](developing-excel-xlls.md)
  
[Excel での C API を使用したプログラミング](programming-with-the-c-api-in-excel.md)
  
[Excel におけるマルチスレッド処理とメモリ競合](multithreading-and-memory-contention-in-excel.md)


[Excel XLL SDK の概要](getting-started-with-the-excel-xll-sdk.md)

