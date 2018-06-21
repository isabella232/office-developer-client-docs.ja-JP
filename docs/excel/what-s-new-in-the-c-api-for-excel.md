---
title: Excel 用 C API の新機能
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- c 言語の api [excel 2007]、新機能
localization_priority: Normal
ms.assetid: f11552e1-b8ea-4933-b6fc-c452b07eb59d
description: '�K�p�Ώ�: Excel 2013?| Office 2013?| Visual Studio'
ms.openlocfilehash: e80b667296af59f4d3f18238cd498830fcdc35a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19798948"
---
# <a name="whats-new-in-the-c-api-for-excel"></a>Excel 用 C API の新機能

 **適用されます**Excel 2013 |。Office 2013 |Visual Studio 
  
Microsoft Excel 2013 と協力して、Microsoft Excel 2013 XLL ソフトウェア開発キット (SDK) には、次の機能のサポートが含まれています。
  
- **新しい関数**
    
    Microsoft Excel 2013 XLL SDK には、Excel 2013 で、新しいワークシート関数のすべてのコールバックがサポートされています。 Excel 2013 関数を呼び出す方法の詳細については、 [DLL や xll ファイルから Excel への呼び出し](calling-into-excel-from-the-dll-or-xll.md)を参照してください。
    
- **非同期のユーザー定義関数**
    
    Excel 2013 は、同時に実行するいくつかの計算を有効にすると、パフォーマンスが向上する、ユーザー定義関数 (UDF) を非同期的に呼び出すことをサポートします。 非同期のユーザー定義関数の詳細については、 [Asynchronous User-Defined 関数](asynchronous-user-defined-functions.md)を参照してください。
    
- **クラスター コネクタ**
    
    クラスター コネクタは、ハイ パフォーマンス計算クラスター上で実行するには、ユーザー定義関数を有効にします。 クラスター コネクタを作成する方法の詳細については、 [Excel クラスター コネクタの開発](developing-excel-cluster-connectors.md)を参照してください。
    
    > [!NOTE]
    > 計算クラスター上で実行する XLL アドインでは、クラスター セーフな関数だけを呼び出す必要があります。 関数の詳細についてを使用して、 [Excel XLL SDK API 関数を参照](excel-xll-sdk-api-function-reference.md)し、[クラスターの安全な関数](cluster-safe-functions.md)を参照できます。 
  
- **64 ビットのサポート**
    
    コンパイルし、両方の 32 ビットおよび 64 ビットの Xll をリンクできます。 詳細については、 [Xll の作成](creating-xlls.md)を参照してください。
    
## <a name="see-also"></a>関連項目



[Excel XLL �̊J��](developing-excel-xlls.md)
  
[Excel �ł� C API ��g�p�����v���O���~���O](programming-with-the-c-api-in-excel.md)
  
[Excel 2007 �ɂ�����}���`�X���b�h�����ƃ���������](multithreading-and-memory-contention-in-excel.md)


[Excel XLL SDK �̊T�v](getting-started-with-the-excel-xll-sdk.md)

