---
title: RUNADDON 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
localization_priority: Normal
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Microsoft Visual Basic for Applications (VBA) プロジェクトでアドオンまたはマクロを実行します。
ms.openlocfilehash: 280f6eaf1e5db045d8c1d22965df00960d188112
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432010"
---
# <a name="runaddon-function"></a>RUNADDON 関数

Microsoft Visual Basic for Applications (VBA) プロジェクトでアドオンまたはマクロを実行します。 
  
## <a name="syntax"></a>構文

RUNADDON (" *string* ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |必須  <br/> |**String** <br/> | VBA プロジェクト内の **Addons** コレクションまたはマクロ内のアドオンの名前を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

RUNADDON 関数呼び出しを含むドキュメントのプロジェクト (または、参照されている場合は別のプロジェクト) に、 _string_という名前のマクロ (引数を持たないプロシージャ) が含まれていないと、Microsoft Visio は、_文字列_という名前のアドオンを実行します。 指定した名前のアドイン__ が見つからない場合、Visio は何もエラーを報告しません。 **TraceFlags** プロパティを使用すると、Visio が実行しようとするプロシージャとアドオンを監視することができます。 
  
標準モジュール内のプロシージャを呼び出すときは、複数のモジュールに同じ名前のプロシージャを含めることができるので、プロシージャを含むモジュール名 (たとえば、 *procName*) で文字列の先頭に指定することをお勧めします。 
  
RUNADDON 関数呼び出しを含む図面のプロジェクト以外のプロジェクトでプロシージャを呼び出すには、*から*を使用します (VBA プロジェクトの*projName*への参照を明示的に設定する必要があります)。 
  
> [!NOTE]
>  Visio 2002 以降、RUNADDON 関数は任意の VBA コードを含む文字列を実行できなくなりました。従来 RUNADDON 関数に渡されていたコードは、RUNADDON 関数から呼び出される図面の VBA プロジェクト内のプロシージャへ移動することができます。 
  
Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定とコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。 
  
以前のバージョンの Visio では、この関数は _RUNADDON に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example-1"></a>例 1

RUNADDON ("Calendar")
  
予定表 .exe というアドオンを起動します。
  
## <a name="example-2"></a>例 2

RUNADDON("Array Shapes")
  
Array Shapes という名の (VSL 実装) アドオンを起動します。
  
## <a name="example-3"></a>例 3

RUNADDON ("ThisDocument statistics")
  
この関数呼び出しを含む図面プロジェクト内の **ThisDocument** モジュール内で ReportStatistics マクロを呼び出します。 
  
> [!NOTE]
>  **ThisDocument** モジュール内でマクロを起動するには文字列の前に「ThisDocument」を付ける必要があります。 
  
## <a name="example-4"></a>例 4

RUNADDON (" *ModuleName* .reportstatistics ") 
  
この関数呼び出しを含むドキュメントプロジェクトの*ModuleName*内で reportstatistics マクロを呼び出します。 
  

