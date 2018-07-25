---
title: Excel XLL SDK API 関数リファレンス
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: '適用対象: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798874"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Excel XLL SDK API 関数リファレンス

**適用対象**: Excel 2013 | Office 2013 | Visual Studio 
  
Microsoft Excel 2013 XLL SDK には、XLL の記述を高速化するために設計されたフレームワーク ライブラリのソース ファイルと 2 つのサンプル プロジェクト (Example と Generic) が含まれます。 
  
このセクションでは、次の関数リファレンスを提供します。
  
- XLL ファイルが呼び出すことのできる Excel コールバック。
    
- Microsoft Excel が検索する XLL コールバック。
    
- サンプルとフレームワークのプロジェクトの主要な機能。
    
## <a name="sample-projects"></a>サンプル プロジェクト

Excel 2013 XLL SDK には、次のサンプル プロジェクトのソース ファイルと Microsoft Visual Studio のプロジェクト ファイルが含まれます。
  
- **Framework** プロジェクト (`SAMPLES\FRAMEWRK\`) には、ライブラリ (FRAMEWRK.lib) にビルドできるプロジェクトが含まれており、他の XLL プロジェクトにリンクすることができます。 ライブラリには、XLL をより簡単に記述するための多くの関数とツールが含まれます。 このライブラリは、他の両方のプロジェクトで、ヘッダー ファイル FRAMEWRK.h と組み合わせて使われます。
    
- **Example** プロジェクト (`SAMPLES\EXAMPLE\`) には、XLL (EXAMPLE.xll) にビルドできるプロジェクトが含まれます。 XLL には、フレームワーク ライブラリを使う多くの例や、**xlAutoOpen** などの XLL アドイン インターフェイスの実装例が含まれます。
    
- **Generic** プロジェクト (`SAMPLES\GENERIC\`) には、XLL (GENERIC.xll) にビルドできるプロジェクトが含まれます。 XLL は、関数とコマンドのいくつかの例を示します。また、独自の XLL を記述するための土台とするのに適しています。
    
## <a name="in-this-section"></a>このセクションの内容

- [アドイン マネージャーと XLL インターフェイス関数](add-in-manager-and-xll-interface-functions.md)
  
- [C API コールバック関数 Excel4、Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [重要で役に立つ C API XLM 関数](essential-and-useful-c-api-xlm-functions.md)
  
- [DLL または XLL からのみ呼び出し可能な C API 関数](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [フレームワーク ライブラリの関数](functions-in-the-framework-library.md)
  
- [汎用 DLL の関数](functions-in-the-generic-dll.md)
  
- [Excel クラスター コネクタ関数](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>関連項目

- [Excel での C API を使用したプログラミング](programming-with-the-c-api-in-excel.md)
  
- [Excel XLL の開発](developing-excel-xlls.md)

