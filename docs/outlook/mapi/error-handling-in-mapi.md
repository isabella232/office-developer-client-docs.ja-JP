---
title: MAPI でのエラー処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287282"
---
# <a name="error-handling-in-mapi"></a>MAPI でのエラー処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
成功、警告、およびエラー値は、result handle と呼ばれる32ビットの数値、または HRESULT を使用して返されます。 HRESULT は、実際には何もハンドルではありません。値でエンコードされた複数のフィールドを持つ32ビットの値にすぎません。 結果が0の場合は成功を示し、0以外の結果は失敗を示します。
  
32ビットプラットフォームでの MAPI は、HRESULT 値に対してのみ機能します。
  
次の図は、32ビットプラットフォームの HRESULT 形式を示しています。
  
**HRESULT の書式**
  
![HRESULT 形式](media/amapi_49.gif "HRESULT 形式")
  
HRESULT の上位ビットは、戻り値が成功または失敗を表しているかどうかを示します。 0に設定すると、値は success を示します。 1に設定されている場合は、エラーを示します。
  
r、C、N、および r のビットは、HRESULT で予約されています。
  
両方のバージョンのファシリティフィールドは、エラーが発生する責任の領域を示します。 いくつかの機能がありますが、大部分の MAPI エラーは FACILITY_ITF を使用してインターフェイスエラーを表します。 現在使用されている最も一般的なファシリティは、FACILITY_NULL、FACILITY_ITF、FACILITY_DISPATCH、FACILITY_RPC、および FACILITY_STORAGE です。 新しい機能が必要な場合は、一意である必要があるため、Microsoft はそれらを割り当てます。 次の表では、さまざまな機能フィールドについて説明します。
  
|Facility|説明|
|:-----|:-----|
|FACILITY_NULL  <br/> |S_OK や E_OUTOF_MEMORY などの広範に適用される一般的な状態コードの場合は、値は0です。  <br/> |
|FACILITY_ITF  <br/> |インターフェイスメソッドから返されるほとんどの状態コードについては、値はインターフェイスによって定義されます。 つまり、2つの異なるインターフェイスから返される32ビット値がまったく同じで2つの HRESULT 値は、意味が異なる場合があります。  <br/> |
|FACILITY_DISPATCH  <br/> |遅延バインディングの[IDispatch](https://msdn.microsoft.com/library/ms221608.aspx)インターフェイスエラーの場合。  <br/> |
|FACILITY_RPC  <br/> |リモートプロシージャコールから返された状態コードの場合。  <br/> |
|FACILITY_STORAGE  <br/> |構造化ストレージに関連する[IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx)または[IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)メソッドの呼び出しから返された状態コードの場合。 windows エラーコードの範囲内のコードを含む状態コード (下位16ビット) の値 (つまり、256未満) は、対応する windows エラーと同じ意味を持ちます。  <br/> |
   
[コード] フィールドは、エラーまたは警告を表すために割り当てられた一意の番号です。
  

