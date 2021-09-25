---
title: RUNADDON 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251492
ms.localizationpriority: medium
ms.assetid: 122c1d30-3cb9-7e7d-b4cc-e93ab8e4da4f
description: Microsoft Visual Basic for Applications (VBA) プロジェクトでアドオンまたはマクロを実行します。
ms.openlocfilehash: 9f861cc5b118f7146f9d778226720e45fa5aba73
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573419"
---
# <a name="runaddon-function"></a>RUNADDON 関数

Microsoft Visual Basic for Applications (VBA) プロジェクトでアドオンまたはマクロを実行します。 
  
## <a name="syntax"></a>構文

RUNADDON() *文字列*  ") 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _string_ <br/> |必須  <br/> |**String** <br/> | VBA プロジェクト内の **Addons** コレクションまたはマクロ内のアドオンの名前を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

RUNADDON 関数呼び出しを含むドキュメントのプロジェクト (または参照されている場合は別のプロジェクト) に、string という名前のマクロ (引数を持つプロシージャ) がない場合、Microsoft Visio はアドオンの名前付き文字列 _を実行します_。 名前付き文字列が見つからない場合、Visioは何も実行し、エラーは報告しません。 **TraceFlags** プロパティを使用すると、Visio が実行しようとするプロシージャとアドオンを監視することができます。 
  
標準モジュールでプロシージャを呼び出す場合は、複数のモジュールが同じ名前のプロシージャを持つ可能性があるため、プロシージャを含むモジュール名  *(moduleName.procName* など) を文字列の先頭に付けます。 
  
RUNADDON 関数呼び出しを含むドキュメントのプロジェクト以外のプロジェクトでプロシージャを呼び出す場合は、  *構文 projName.modName.procName*  を使用します (VBA プロジェクトで  *projName*  への参照を明示的に設定している必要があります)。 
  
> [!NOTE]
>  Visio 2002 以降、RUNADDON 関数は任意の VBA コードを含む文字列を実行できなくなりました。従来 RUNADDON 関数に渡されていたコードは、RUNADDON 関数から呼び出される図面の VBA プロジェクト内のプロシージャへ移動することができます。 
  
Visio でのコードの実行に関する詳細については、この『シェイプシート リファレンス』の「[Visio のセキュリティ設定とコードの実行について](about-security-settings-and-running-code-in-visio-shapesheet.md)」を参照してください。 
  
以前のバージョンの Visio では、この関数は _RUNADDON に相当します。Visio 4.0 以降のバージョンでは、どちらのスタイルも使用できます。 
  
## <a name="example-1"></a>例 1

RUNADDON("Calendar.exe")
  
アドインと呼ばれるアドオンを起動Calendar.exe。
  
## <a name="example-2"></a>例 2

RUNADDON("Array Shapes")
  
Array Shapes という名の (VSL 実装) アドオンを起動します。
  
## <a name="example-3"></a>例 3

RUNADDON("ThisDocument.ReportStatistics")
  
この関数呼び出しを含む図面プロジェクト内の **ThisDocument** モジュール内で ReportStatistics マクロを呼び出します。 
  
> [!NOTE]
>  **ThisDocument** モジュール内でマクロを起動するには文字列の前に「ThisDocument」を付ける必要があります。 
  
## <a name="example-4"></a>例 4

RUNADDON(" *ModuleName*  .ReportStatistics") 
  
この関数呼び出しを含むドキュメント プロジェクト  *の ModuleName*  の ReportStatistics マクロを呼び出します。 
  

