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
description: アドオンまたはマクロで、Microsoft Visual Basic for Applications (VBA) プロジェクトを実行します。
ms.openlocfilehash: 31ac32c742827311d8aaee4547024ad97d2c48e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806343"
---
# <a name="runaddon-function"></a>RUNADDON 関数

アドオンまたはマクロで、Microsoft Visual Basic for Applications (VBA) プロジェクトを実行します。 
  
## <a name="syntax"></a>構文

RUNADDON (以下"*文字列*") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | VBA プロジェクト内の **Addons** コレクションまたはマクロ内のアドオンの名前を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

RUNADDON 関数呼び出しを含む図面のプロジェクト (または別のプロジェクトが参照されている場合) は_文字列_をという名前のマクロ (引数を持たないプロシージャ) を持たない場合、Microsoft Visio は、 _string_という名前のアドオンを実行します。 _String_という名前のアドオンが見つからない場合、Visio は何もし、エラーは報告されません。 ( **TraceFlags**プロパティはプロシージャを実行しようとしている Visio のアドオンを監視するのに使用ことができます)。 
  
標準モジュールでプロシージャを呼び出す、ときに、複数のモジュールが同じ名前のプロシージャを持つことができますので、プロシージャ (たとえば、 *moduleName.procName*) を含むモジュールの名前を持つ文字列を付けることをお勧めします。 
  
プロジェクト内のプロシージャを呼び出す以外の RUNADDON 関数呼び出しを含む図面のプロジェクトを使用して、構文*projName.modName.procName* (する必要がありますが明示的に設定する*projName*への参照、VBA プロジェクトに)。 
  
> [!NOTE]
>  Visio 2002 以降、RUNADDON 関数は任意の VBA コードを含む文字列を実行できなくなりました。従来 RUNADDON 関数に渡されていたコードは、RUNADDON 関数から呼び出される図面の VBA プロジェクト内のプロシージャへ移動することができます。 
  
Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定とコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。 
  
以前のバージョンの Visio では、この関数は _RUNADDON に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example-1"></a>例 1

RUNADDON("Calendar.exe")
  
Calendar.exe と呼ばれるアドオンを起動します。
  
## <a name="example-2"></a>例 2

RUNADDON("Array Shapes")
  
Array Shapes という名の (VSL 実装) アドオンを起動します。
  
## <a name="example-3"></a>例 3

RUNADDON("ThisDocument.ReportStatistics")
  
この関数呼び出しを含む図面プロジェクト内の **ThisDocument** モジュール内で ReportStatistics マクロを呼び出します。 
  
> [!NOTE]
>  **ThisDocument** モジュール内でマクロを起動するには文字列の前に「ThisDocument」を付ける必要があります。 
  
## <a name="example-4"></a>例 4

RUNADDON ("*します*。ReportStatistics」) 
  
ドキュメントを含むプロジェクトをこの関数の呼び出しで、*モジュール名*で ReportStatistics マクロを呼び出します。 
  

