---
title: MAPI でのエラー処理
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99e2c485-af84-46f4-84b4-fca2117b5a21
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 98ee0856411cce3a3e9012185be6c30503de7779
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287282"
---
# <a name="error-handling-in-mapi"></a>MAPI でのエラー処理

**適用対象**: Outlook 2013 | Outlook 2016 
  
成功、警告、およびエラーの値は、結果ハンドルまたは HRESULT と呼ばれる 32 ビットの数値を使用して返されます。 HRESULT は、実際には何も処理しません。単なる 32 ビットの値で、複数のフィールドが値にエンコードされています。 結果が 0 の場合は成功を示し、0 以外の結果は失敗を示します。
  
32 ビット プラットフォーム上の MAPI は、HRESULT 値でのみ動作します。
  
次の図は、32 ビット プラットフォームの HRESULT 形式を示しています。
  
**HRESULT の書式**
  
![HRESULT 形式](media/amapi_49.gif "HRESULT 形式")
  
HRESULT の高次ビットは、戻り値が成功または失敗を表すかどうかを示します。 ゼロに設定すると、値は成功を示します。 1 に設定すると、エラーが示されます。
  
R、C、N、および r のビットは HRESULT で予約されています。
  
両方のバージョンの機能フィールドは、エラーの責任領域を示します。 いくつかの機能がありますが、MAPI エラーの大部分は、インターフェイス エラーを表すFACILITY_ITFを使用します。 現在使用されている最も一般的な機能は、FACILITY_NULL、FACILITY_ITF、FACILITY_DISPATCH、FACILITY_RPC、FACILITY_STORAGE。 新しい施設が必要な場合は、一意である必要があるため、Microsoft が割り当てします。 次の表では、さまざまな機能フィールドについて説明します。
  
|Facility|説明|
|:-----|:-----|
|FACILITY_NULL  <br/> |広く適用可能な一般的な状態コード (たとえば、S_OKまたはE_OUTOF_MEMORY。値は 0 です。  <br/> |
|FACILITY_ITF  <br/> |インターフェイス メソッドから返されるほとんどの状態コードの場合。値はインターフェイスによって定義されます。 つまり、2 つの異なるインターフェイスから返される 32 ビット値がまったく同じ 2 つの HRESULT 値は、異なる意味を持つ場合があります。  <br/> |
|FACILITY_DISPATCH  <br/> |[IDispatch インターフェイスのエラーの](https://msdn.microsoft.com/library/ms221608.aspx)バインディングが遅い場合。  <br/> |
|FACILITY_RPC  <br/> |リモート プロシージャ呼び出しから返される状態コードの場合。  <br/> |
|FACILITY_STORAGE  <br/> |構造化ストレージに関連する [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) メソッドまたは [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) メソッド呼び出しから返される状態コードの場合。 Windows エラー コードの範囲 (つまり、256 未満) のコード (下位 16 ビット) の値を持つ状態コードは、対応する Windows エラーと同じ意味を持ちます。  <br/> |
   
コード フィールドは、エラーまたは警告を表す一意の番号です。
  

